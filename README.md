## Instruction with Kafka

```
Start zookeeper
$bin/zookeeper-server-start.sh config/zookeeper.properties

Start kafka server/broker
$bin/kafka-server-start.sh config/server.properties

Create topic = demo03
$bin/kafka-topics.sh --bootstrap-server localhost:9092 --create --replication-factor 1 --partitions 3 --topic demo03

List of topics
$bin/kafka-topics.sh --bootstrap-server localhost:9092 --list 

Send message to Topic = demo03
$bin/kafka-console-producer.sh --broker-list localhost:9092 --topic demo03

Read message from Topic = demo03
$bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic demo03 --from-beginning
```