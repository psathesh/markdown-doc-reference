# Kafka

For full documentation visit 

[kafka.apache.org](https://kafka.apache.org/){:target="_blank"}


## Installation

Download and unpack the Kibana official distribution.

Run the below on Mac.

`./bin/kibana`

Open the below url on the browser.

`http://localhost:5601/`


## Starting the server

#### Starting Zookeeper

	$ cd /Users/upurusa/tools/servers/kafka_2.12-2.5.0
	
	$ ./bin/zookeeper-server-start.sh config/zookeeper.properties

#### Starting our brokers

	$ cd /Users/upurusa/tools/servers/kafka_2.12-2.5.0

	$ ./bin/kafka-server-start.sh config/server.properties
	



[BACK to TOC](../../README.md)

----------