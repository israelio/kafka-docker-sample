#!/bin/sh
#
# The number of partitions for a topic can only be increased.
# If partitions are increased for a topic that has a key,
# the partition logic or ordering of the messages will be affected.
#
#!/bin/sh
if [[ -z "$1" ]]; then
    echo 'Missing topic name'
    exit 0
fi

#!/bin/sh
if [[ -z "$1" ]]; then
    echo 'Missing new partition size'
    exit 0
fi

docker exec -it kafka \
kafka-topics --zookeeper zookeeper:2181 --alter --topic $1 --partitions $2
