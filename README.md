## Description

This project includes a sample docker compose yml file which can be used to setup a local kafka env.

The project includes zookeeper and a single kafka node.

Clone this repo and run the following:

## Setup environment
```
$ chmod +x make-commands-executable.sh

$ ./make-commands-executable.sh
```
## start / stop environments

You can then use the following commands:

#### Start up the docker compose - bring up zookeeper and kafka
* Kafka will start at port 9092
* Zookeeper will start at port 2181

```
$ ./start
```

#### Stop the docker compose
```
$ ./stop
```


## Kafka commands

### <U>Operational related commands</U>

#### List available brokers
```
$ ./kafka/list-brokers
```
#### Show kafka logs
```
$ ./kafka/logs
```
#### Show kafka version
```
$ ./kafka/version
```
#### Get a bash shell on the kafka docker instance
```
$ ./kafka/shell
```
#### Run a command on inside the kafka docker instance
```
$ ./kafka/run-within-docker <the_command_that_you_would_like_to_run>
```
### <U>Topic related commands</U>

#### List current topics
```
$ ./kafka/topic/list
```
#### Create a new kafka topic
* created with replication-factor 1 and partitions 1
```
$ ./kafka/topic/create <topic_name>

sample:
./kafka/topic/create tone
```
#### Pick a look at the details of a topic
```
$ ./kafka/topic/details <topic_name>

sample:
./kafka/topic/details tone
```
#### Delete a topic
```
$ ./kafka/topic/delete <topic_name>

sample:
./kafka/topic/delete tone
```
#### Purge topic content
```
$ ./kafka/topic/purge
```
#### Change topic retention
```
$ ./kafka/topic/change-retention <topic_name> <retention_time_in_msec>
```
#### Increase topic partitions
```
$ ./kafka/topic/increase-partition <topic_name> <new_partition_size>
```
### <U>Message related commands</U>
#### Produce a new message
* Each line is a new message, hit ctrl-c to end.
```
$ ./kafka/message/produce <topic_name>

sample:
./kafka/message/produce tone
```
#### Consume new messages from last time
```
$ ./kafka/message/consume <topic_name>

sample:
./kafka/message/consume tone
```
#### Consume new messages from the beginning
```
$ ./kafka/message/consume-from-beginning <topic_name>

sample:
./kafka/message/consume-from-beginning tone
```


## ZooKeeper commands

#### Show ZooKeeper logs
```
$ ./zookeeper/logs
```
#### Get a bash shell on the zookeeper docker instance
```
$ ./zookeeper/shell
```

# kafka-docker-sample
