#!/bin/sh
if [[ -z "$1" ]]; then
    echo 'Missing topic name'
    exit 0
fi

docker exec -it kafka \
kafka-console-consumer --bootstrap-server localhost:9092 --topic $1
