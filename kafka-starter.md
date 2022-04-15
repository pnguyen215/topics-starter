## Kafka

### Kafka & Zookeeper Configuration

- Download Apache Kafka from its [Official Site](https://kafka.apache.org/downloads "Kafka download").

- Extract tgz via cmd or from the available tool to a location of your choice
- Create Data folder for Zookeeper and Apache Kafka
  
> Create “data” folder and Kafka / Zookeeper directories inside data folder

  ![Kafka & Zookeeper Configuration!](/assets/kafka_001.png "Kafka & Zookeeper Configuration")

- Change the default configuration value

> Update zookeeper data directory path in “config/zookeeper.Properties” configuration file.

  ![Kafka & Zookeeper Configuration!](/assets/kafka_002.png "Kafka & Zookeeper Configuration")

> Update Apache Kafka log file path in “config/server.properties” configuration file.

  ![Kafka & Zookeeper Configuration!](/assets/kafka_003.png "Kafka & Zookeeper Configuration")

### Start Zookeeper

```
.\bin\windows>zookeeper-server-start.bat ../../config/zookeeper.properties
```

> And make sure zookeeper started successfully

  ![Kafka & Zookeeper Configuration!](/assets/kafka_004.png "Kafka & Zookeeper Configuration")

### Start Apache Kafka

> Run on: localhost:9092

```
.\bin\windows>kafka-server-start.bat ../../config/server.properties
```

### Create a Kafka Topic

> partitions: from 1 to 16

```
.\bin\windows>kafka-topics.bat --create --topic quick-start-events --bootstrap-server localhost:9092 --replication-factor 1 --partitions 16
```

### List Kafka Topics

```
.\bin\windows>kafka-topics.bat --list --bootstrap-server localhost:9092
```

### Creating Kafka Producer

```
.\bin\windows>kafka-console-producer.bat --broker-list localhost:9092 --topic quick-start-events
```

### Creating Kafka Consumer

```
.\bin\windows>kafka-console-consumer.bat --bootstrap-server localhost:9092 --topic quick-start-events --from-beginning
```