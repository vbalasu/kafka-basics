# kafka-basics

Simple scripts in Python and Bash to work with Kafka

#### Bash scripts

**start.sh**
```
nohup bin/zookeeper-server-start.sh config/zookeeper.properties &
nohup bin/kafka-server-start.sh config/server.properties &
```

**create_topic.sh**
```
bin/kafka-topics.sh --create --topic quickstart-events --bootstrap-server localhost:9092
```

**list_topics.sh**
```
bin/kafka-topics.sh --list --bootstrap-server localhost:9092
```

**consume.sh**
```
bin/kafka-console-consumer.sh --topic quickstart-events --from-beginning --bootstrap-server localhost:9092
```

**delete_topc.sh**
```
bin/kafka-topics.sh --bootstrap-server localhost:9092 --delete --topic quickstart-events
```

#### Python programs (Jupyter Notebooks)

[producer.ipynb](producer.ipynb)

[consumer.ipynb](consumer.ipynb)

[Kafka.ipynb](Kafka.ipynb) - Databricks