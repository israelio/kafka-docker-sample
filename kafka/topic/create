#!/bin/sh
if [[ -z "$1" ]]; then
    echo 'Missing topic name'
    exit 0
fi

docker exec -it kafka \
kafka-topics --create --zookeeper zookeeper:2181 --replication-factor 1 --partitions 1 --if-not-exists --topic $1
