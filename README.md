Spring Boot with Kafka Producer Example \n
This Project covers how to use Spring Boot with Spring Kafka to Publish JSON/String message to a Kafka topic

Start Zookeeper
bin/zookeeper-server-start.sh config/zookeeper.properties
Start Kafka Server
bin/kafka-server-start.sh config/server.properties
Create Kafka Topic
bin/kafka-topics.sh --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic Kafka_Example
Consume from the Kafka Topic via Console
bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic Kafka_Example --from-beginning
Publish message via WebService
http://localhost:8081/kafka/publish/Sai
http://localhost:8081/kafka/publish/sam

kafka commands for windows
zookeeper-server-start.bat ../../config/zookeeper.properties
kafka-server-start.bat ../../config/server.properties
kafka-topics.bat --create --zookeeper localhost:2181 --replication-factor 1 --partitions 1 --topic Kafka_Example
kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic Kafka_Example --from-beginning
