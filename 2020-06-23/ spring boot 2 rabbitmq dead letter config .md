###  spring boot 2 rabbitmq dead letter config retry


[tutorials/HelloWorldMessageApp.java at master · eugenp/tutorials](https://github.com/eugenp/tutorials/blob/master/spring-amqp/src/main/java/com/baeldung/springamqp/simple/HelloWorldMessageApp.java "tutorials/HelloWorldMessageApp.java at master · eugenp/tutorials")


[tutorials/SimpleDLQAmqpConfiguration.java at master · eugenp/tutorials](https://github.com/eugenp/tutorials/blob/master/spring-amqp/src/main/java/com/baeldung/springamqp/errorhandling/configuration/SimpleDLQAmqpConfiguration.java "tutorials/SimpleDLQAmqpConfiguration.java at master · eugenp/tutorials")



[Error Handling with Spring AMQP | Baeldung](https://www.baeldung.com/spring-amqp-error-handling "Error Handling with Spring AMQP | Baeldung")

[amqp.node/api_args.js at d98449b453a00ac4c968dd76a72c5f55652488e2 · squaremo/amqp.node](https://github.com/squaremo/amqp.node/blob/d98449b453a00ac4c968dd76a72c5f55652488e2/lib/api_args.js "amqp.node/api_args.js at d98449b453a00ac4c968dd76a72c5f55652488e2 · squaremo/amqp.node")


https://dzone.com/storage/temp/13106079-1583492711447.png


[Spring Boot + RabbitMQ Tutorial — Retry and Error Handling Example - DZone Integration](https://dzone.com/articles/spring-boot-rabbitmq-tutorial-retry-and-error-hand "Spring Boot + RabbitMQ Tutorial — Retry and Error Handling Example - DZone Integration")

### Description

Overall 
sender must initialize its own queue
also initialize deadletter queue

for example
            let queues: [string, string][] = [[INVESTMENT_NOTIFIER_RABBITMQ_QUEUE, INVESTMENT_NOTIFIER_RABBITMQ_DEADLETTER_QUEUE]]
            for (const queue of queues) {
                const channel = await connection.createConfirmChannel();
                await channel.assertQueue(queue[0], {deadLetterExchange:"", deadLetterRoutingKey:queue[1]});
                await channel.assertQueue(queue[1], );

                this.channelMap[queue[0]] = channel;
            }
means that queue will be initialized with "" as deadletter exchange(default exchange) and INVESTMENT_NOTIFIER_RABBITMQ_DEADLETTER_QUEUE as deadletter routing key(which means that there must be queue INVESTMENT_NOTIFIER_RABBITMQ_DEADLETTER_QUEUE) to where our data will go to INVESTMENT_NOTIFIER_RABBITMQ_DEADLETTER_QUEUE
also deadletter queue is initialized as you can see

```java

//RECEIVER not needed if you just receiving
@Configuration
public class RabbitConfig {

    public static final String INVESTMENT_NOTIFIER_QUEUE_RABBITMQ = "feasibility-new-project-event";

    @Autowired
    GeneralProperties generalProperties;

    @Bean
    public ConnectionFactory connectionFactory() {
        CachingConnectionFactory connectionFactory = new CachingConnectionFactory();
        connectionFactory.setAddresses(generalProperties.getRabbitaddress());
        connectionFactory.setPort(generalProperties.getRabbitport());
        connectionFactory.setUsername(generalProperties.getRabbitusername());
        connectionFactory.setPassword(generalProperties.getRabbitpassword());
        return connectionFactory;
    }

    @Bean
    public AmqpAdmin amqpAdmin() {
        return new RabbitAdmin(connectionFactory());
    }

}


----
    @RabbitListener(queues = INVESTMENT_NOTIFIER_QUEUE_RABBITMQ)
    public void listen(byte[] message) throws Exception {
        Map<String, Object> parsedMessage = (Map<String,Object>)objectMapper.readValue(message, Object.class);
        NewProject newProject = NewProject.builder().name((String) parsedMessage.get("name")).feasibilityId((String) parsedMessage.get("_id")).build();
        newProjectService.save(newProject);
        throw exception()
    }
//RECEIVER spring boot config
spring:
  rabbitmq:
    listener:
      simple:
        retry:
          enabled: true
          initial-interval: 3s
          max-attempts: 6
          max-interval: 10s
          multiplier: 2
---

//SENDER
---

            let queues: [string, string][] = [[INVESTMENT_NOTIFIER_RABBITMQ_QUEUE, INVESTMENT_NOTIFIER_RABBITMQ_DEADLETTER_QUEUE]]
            for (const queue of queues) {
                const channel = await connection.createConfirmChannel();
                await channel.assertQueue(queue[0], {deadLetterExchange:"", deadLetterRoutingKey:queue[1]});
                await channel.assertQueue(queue[1], );

                this.channelMap[queue[0]] = channel;
            }

//SENDER spring boot

@Configuration
public class RabbitConfig {

    public static final String NEW_PROJECT_FEASIBILITY_EVENT = "new-project-feasibility-event";
    public static final String NEW_PROJECT_FEASIBILITY_EVENT_DLQ = "new-project-feasibility-event"+".dlq";

    @Bean
    Queue messagesQueue() {
        return QueueBuilder.durable(NEW_PROJECT_FEASIBILITY_EVENT)
                .withArgument("x-dead-letter-exchange", "")
                .withArgument("x-dead-letter-routing-key", NEW_PROJECT_FEASIBILITY_EVENT_DLQ)
                .build();
    }

    @Bean
    Queue deadLetterQueue() {
        return QueueBuilder.durable(NEW_PROJECT_FEASIBILITY_EVENT_DLQ).build();
    }
}

---
RECEIVER


try {
                let newProject = JSON.parse(message.content.toString());
                this.newProjectListener.process(newProject);
                channel.ack(message);
            } catch(err) {
                //requeue is set false to send to deadletter
                channel.nack(message, false, false);
            }




```

