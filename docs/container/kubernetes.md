# kubernetes

For full documentation visit [kubernetes.io](https://kubernetes.io/){:target="_blank"}.

## Installation

    $ brew tap mongodb/brew
    

## Commands

Brew commands for start stop mongoDB

	-- Start MongoDB --
	$ brew services start mongodb-community@4.2
	



## Configuration changes

MongoDB configuration file location

	$ cd /Users/upurusa/tools/servers/mongodb

Change location of the MongoDB configuration files

	$ ls -lart /usr/local/etc/mongod.conf
	
	$ rm -rf /usr/local/etc/mongod.conf
	$ ln -s /Users/upurusa/tools/servers/mongodb/mongod.conf /usr/local/etc/mongod.conf



	