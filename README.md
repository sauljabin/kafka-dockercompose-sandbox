# Kafka Docker Compose Sandbox

## Get Started

Run the cluster:

```sh
docker compose up -d
```

Stop the container and remove volume:

```sh
docker compose down -v
```

## Kafka commands

Create a topic:

```shell
kafka-topics --create --bootstrap-server localhost:19093 \
    --replication-factor 3 \
    --partitions 3 \
    --topic test
```

Delete a topic:

```shell
kafka-topics --delete --bootstrap-server localhost:19093 \
    --topic test
```

List topics:

```shell
kafka-topics --bootstrap-server localhost:19093 --list
```

List Groups:

```shell
kafka-consumer-groups --bootstrap-server localhost:19093 --list
```

Delete group:

```shell
kafka-consumer-groups --bootstrap-server localhost:19093 --delete --group test
```