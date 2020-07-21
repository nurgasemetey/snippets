### rabbitmq node dead letter 


[Dead Letter Exchanges — RabbitMQ](https://www.rabbitmq.com/dlx.html "Dead Letter Exchanges — RabbitMQ")
[Back-off and retry with RabbitMQ](https://dev.venntro.com/2014/07/back-off-and-retry-with-rabbitmq/ "Back-off and retry with RabbitMQ")
[node-amqp: Setting up a dead letter exchange](http://mediaingenuity.github.io/2013/09/06/node-amqp-dead-letter-exchange.html "node-amqp: Setting up a dead letter exchange")
 

```ts
let queues: [string, string][] = [["feasibility-new-project-event", "feasibility-new-project-event-deadletter"]]
            for (const queue of queues) {
                const channel = await connection.createConfirmChannel();
                await channel.assertQueue(queue[0], {deadLetterExchange:queue[1]});
                await channel.assertExchange(queue[1], "direct");
                this.channelMap[queue[0]] = channel;
            }
```
