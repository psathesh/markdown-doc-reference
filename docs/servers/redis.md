# Redis

For full documentation visit [redis.io](https://redis.io/){:target="_blank"}.

## Installation

    $ brew install redis

## Commands

#### commands

`$ redis-server`

`$ cd /Users/upurusa/tools/servers/redis`

`$ redis-server ./redis.conf`

`$ sudo brew services restart nginx`

`$ redis-server /Users/upurusa/tools/servers/redis/redis.conf`


## Configuration changes

Location of Redis local files
    
	$ cd /Users/upurusa/tools/servers/redis

Change location of the Redis configuration files
    
	$ ls -lart /usr/local/etc/redis.conf
	$ rm -rf /usr/local/etc/redis.conf
	$ ln -s /Users/upurusa/tools/servers/redis/conf/redis.conf /usr/local/etc/redis.conf

Change location of the Redis sentinel configuration files
    
	$ ls -lart /usr/local/etc/redis-sentinel.conf
	$ rm -rf /usr/local/etc/redis-sentinel.conf
	$ ln -s /Users/upurusa/tools/servers/redis/conf/redis-sentinel.conf /usr/local/etc/redis-sentinel.conf

Change location of the Redis db file path

	$ ls -lart /usr/local/var/db/redis
	$ rm -rf /usr/local/var/db/redis
	$ ln -s /Users/upurusa/tools/servers/redis/db/redis /usr/local/var/db/redis

Change location of the Redis log file

	$ ls -lart /usr/local/var/log/redis.log
	$ rm -rf /usr/local/var/log/redis.log
	$ ln -s /Users/upurusa/tools/servers/redis/logs/redis.log /usr/local/var/log/redis.log


[BACK to TOC](./../README.md)

----------