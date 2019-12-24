### rabbitmq amqlib in nodejs with typescript


[twawszczak/amqplib-as-promised](https://github.com/twawszczak/amqplib-as-promised)


 

```ts
import { Connection } from 'amqplib-as-promised'
const connection = new Connection(AMQP_URL)
await connection.init()
const channel = await connection.createChannel() // or createConfirmChannel
await channel.assertQueue(queueName)
await channel.sendToQueue(queueName, Buffer.from(testMessage))
await channel.close()
await connection.close()
```
