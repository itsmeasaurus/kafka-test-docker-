# Kafka Quick Start with Docker

This repository provides a Docker Compose setup for running Apache Kafka and ZooKeeper. It includes a basic configuration to demonstrate Kafka's publish-subscribe messaging system using the topic `chat-messages`.

## Prerequisites

Before you begin, ensure you have Docker and Docker Compose installed on your system.

- [Install Docker](https://docs.docker.com/get-docker/)
- [Install Docker Compose](https://docs.docker.com/compose/install/)

## Getting Started

### 1. Clone the Repository

Start by cloning this repository to your local machine. Use the following command to clone using Git:

```bash
git clone https://github.com/itsmeasaurus/kafka-test-docker-.git
cd kafka-test-docker
```


### 2. Run the container

```bash
docker-compose up -d
```


### 3. Access the Kafka container

```bash
docker exec -it [container-id] /bin/sh
```


### 4. Run Kafka producer

```bash
kafka-console-producer.sh --topic chat-messages --bootstrap-server localhost:9092
```
Type texts for test and you will see that from the consumer side. The following step is to see at consumer.


### 5. Run Kafka consumer

Open a new terminal or tab, access the kafka container, run kafka consumer

```bash
docker exec -it kafka /bin/sh
kafka-console-consumer.sh --topic chat-messages --from-beginning --bootstrap-server localhost:9092
```



