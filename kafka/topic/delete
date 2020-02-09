#!/bin/sh
if [[ -z "$1" ]]; then
    echo 'Missing topic name'
    exit 0
fi

docker exec -it kafka \
kafka-topics --zookeeper zookeeper:2181 --delete --topic $1
