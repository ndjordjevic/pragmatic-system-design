## Queues
1. Two roles: producer and consumer, totally decoupled
2. Pros: Buffering, message durability. Cons: Increase system complexity and latency

## Messages
1. Two types: Messages queue (sync notify only one consumer, arrive out of order) and Pub/Sub (notify multiple consumers, always in order)
2. RabbitMQ, Kafka
