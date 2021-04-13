# MongoDB

For full documentation visit [mongodb](https://www.mongodb.com/){:target="_blank"}.

## Installation

    $ brew tap mongodb/brew
    
    $ brew install mongodb-community@4.2


## Commands

Brew commands for start stop mongoDB

	-- Start MongoDB --
	$ brew services start mongodb-community@4.2
	
	-- Stop MongoDB	--
	$ brew services stop mongodb-community@4.2

	-- To verify that MongoDB is running --
	$ ps aux | grep -v grep | grep mongod

	## Start MongoDB with configuration file
	$ mongod --config /Users/upurusa/tools/servers/mongodb/mongod.conf


## Configuration changes

MongoDB configuration file location

	$ cd /Users/upurusa/tools/servers/mongodb

Change location of the MongoDB configuration files

	$ ls -lart /usr/local/etc/mongod.conf
	
	$ rm -rf /usr/local/etc/mongod.conf
	$ ln -s /Users/upurusa/tools/servers/mongodb/mongod.conf /usr/local/etc/mongod.conf


Change location of MongoDB log files

	$ ls -lart /usr/local/var/log/mongodb
   
	$ rm -rf /usr/local/var/log/mongodb
	$ ln -s /Users/upurusa/tools/servers/mongodb/logs /usr/local/var/log/mongodb


Change location of MongoDB database file path

	$ ls -lart /usr/local/var/mongodb
   
	$ rm -rf /usr/local/var/mongodb
	$ ln -s /Users/upurusa/tools/servers/mongodb/dbpath /usr/local/var/mongodb

	

[BACK to TOC](./../README.md)

----------