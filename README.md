# apache-kafka-producer-demo
This application helps to understand how to send JSON objects using Kafka in realtime
1) Download and install the Kafka on Windows, name the folder as kafka under c:\.
2) Configure the zookeeper.properties file under folder c:\kafka\config, 
   dataDir=c:/kafka/zookeeper-data
3) Configure the server.properties file under folder c:\kafka\config,
   listeners=PLAINTEXT://127.0.0.1:9092
   log.dirs=c:/kafka/kafka-logs
4) Run the zookeeper in a new command terminal using the command from path c:\kafka,
   .\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties
5) Run the kafka server in a new command terminal using the command from path c:\kafka,
   .\bin\windows\kafka-server-start.bat .\config\server.properties
6) Run the topic creation in a new command terminal from path c:\kafka,
   .\bin\windows\kafka-topics.bat --create --topic TestTopic --bootstrap-server localhost:9092 --replication-factor 1 --partitions 1
7) Run the producer in a new command terminal to create the messages in topic TestTopic from path c:\kafka,
   .\bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic TestTopic
   >Welcome to the world of Kafka Messaging
   >Happy Learning
8) Run the consumer in a new command terminal to consume the messages from topic TestTopic on path c:\kafka,
   .\bin\windows\kafka-console-producer.bat --broker-list localhost:9092 --topic TestTopic
