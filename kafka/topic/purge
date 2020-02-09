#!/bin/sh
if [[ -z "$1" ]]; then
    echo 'Missing topic name'
    exit 0
fi

docker exec -it kafka \
kafka-configs --zookeeper zookeeper:2181 --alter --entity-type topics --entity-name $1 --add-config retention.ms=1000

sleep 2m

docker exec -it kafka \
kafka-configs --zookeeper zookeeper:2181 --alter --entity-type topics --entity-name $1 --delete-config retention.ms
