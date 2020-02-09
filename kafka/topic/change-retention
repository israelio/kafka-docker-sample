#!/bin/sh
if [[ -z "$1" ]]; then
    echo 'Missing topic name'
    exit 0
fi

if [[ -z "$2" ]]; then
    echo 'Missing retention time in msec'
    exit 0
fi

docker exec -it kafka \
kafka-configs --zookeeper zookeeper:2181 --alter --entity-type topics --entity-name $1 --add-config retention.ms=$2
