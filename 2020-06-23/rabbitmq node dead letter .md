### rabbitmq node dead letter 


[Dead Letter Exchanges — RabbitMQ](https://www.rabbitmq.com/dlx.html "Dead Letter Exchanges — RabbitMQ")


 

```ts
let queues: [string, string][] = [["feasibility-new-project-event", "feasibility-new-project-event-deadletter"]]
            for (const queue of queues) {
                const channel = await connection.createConfirmChannel();
                await channel.assertQueue(queue[0], {deadLetterExchange:queue[1]});
                await channel.assertExchange(queue[1], "direct");
                this.channelMap[queue[0]] = channel;
            }
```
