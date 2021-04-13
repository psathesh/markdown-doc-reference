# Nginx

For full documentation visit [nginx.com](https://www.nginx.com/){:target="_blank"}.

## Installation

    $ brew install nginx

## Commands

#### Brew commands

`$ sudo brew services start nginx`

`$ sudo brew services stop nginx`

`$ sudo brew services restart nginx`

#### Nginx commands

`$ nginx -h`

`$ sudo nginx`

`$ sudo nginx -s stop`

`$ sudo nginx -s reload`

`$ sudo nginx -t`

`$ sudo nginx -c /Users/upurusa/tools/servers/nginx/sample-config/config1.conf`

## Configuration changes

Location of the nginx local files
    
	$ cd /Users/upurusa/tools/servers/nginx

Location of the nginx pid file    

	/usr/local/var/run/nginx.pid

Change location of the nginx default configuration files
    
	$ ls -lart /usr/local/etc/nginx
	
	$ rm -rf /usr/local/etc/nginx
	$ ln -s /Users/upurusa/tools/servers/nginx/conf /usr/local/etc/nginx

Change location of the nginx log files

	$ ls -lart /usr/local/var/log/nginx
   
	$ rm -rf /usr/local/var/log/nginx
	$ ln -s /Users/upurusa/tools/servers/nginx/log /usr/local/var/log/nginx
    

	

[BACK to TOC](../../README.md)

----------