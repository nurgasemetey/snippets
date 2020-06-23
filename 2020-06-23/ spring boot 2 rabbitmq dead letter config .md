###  spring boot 2 rabbitmq dead letter config 


[tutorials/HelloWorldMessageApp.java at master · eugenp/tutorials](https://github.com/eugenp/tutorials/blob/master/spring-amqp/src/main/java/com/baeldung/springamqp/simple/HelloWorldMessageApp.java "tutorials/HelloWorldMessageApp.java at master · eugenp/tutorials")



[tutorials/SimpleDLQAmqpConfiguration.java at master · eugenp/tutorials](https://github.com/eugenp/tutorials/blob/master/spring-amqp/src/main/java/com/baeldung/springamqp/errorhandling/configuration/SimpleDLQAmqpConfiguration.java "tutorials/SimpleDLQAmqpConfiguration.java at master · eugenp/tutorials")



[Error Handling with Spring AMQP | Baeldung](https://www.baeldung.com/spring-amqp-error-handling "Error Handling with Spring AMQP | Baeldung")


 

```java
@Configuration
public class RabbitConfig {

    public static final String INVESTMENT_NOTIFIER_QUEUE_RABBITMQ = "feasibility-new-project-event";
    public static final String INVESTMENT_NOTIFIER_QUEUE_RABBITMQ_DEADLETTER = "feasibility-new-project-event-deadletter";

//    public static final String FEASIBILITY_INVESTMENT_QUEUE = QUEUE_MESSAGES + ".dlq";

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

    @Bean
    Queue feasibilityInvestmentQueue() {
        return QueueBuilder.durable(INVESTMENT_NOTIFIER_QUEUE_RABBITMQ)
                .withArgument("x-dead-letter-exchange", INVESTMENT_NOTIFIER_QUEUE_RABBITMQ_DEADLETTER)
                .build();
    }
}

----
    @RabbitListener(queues = INVESTMENT_NOTIFIER_QUEUE_RABBITMQ)
    public void listen(byte[] message) throws Exception {
        Map<String, Object> parsedMessage = (Map<String,Object>)objectMapper.readValue(message, Object.class);
        NewProject newProject = NewProject.builder().name((String) parsedMessage.get("name")).feasibilityId((String) parsedMessage.get("_id")).build();
        newProjectService.save(newProject);
    }
```
