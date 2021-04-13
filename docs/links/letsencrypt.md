# LetsEncrypt - CertBot

For full documentation visit 

[letsencrypt.org](https://letsencrypt.org/)

[CertBot](https://certbot.eff.org/)

[LetsEncrypt CertBot & AWS](https://itnext.io/using-letsencrypt-ssl-certificates-in-aws-certificate-manager-c2bc3c6ae10)


## Installation

    $ brew install letsencrypt

## Commands
    
	$ mkdir ~/letsencrypt
	
	$ cd ~/letsencrypt
	
	$ certbot certonly \
    	--manual \
    	--preferred-challenges=dns \
    	--email sathesh.purushothaman@savvas.com \
    	--agree-tos \
    	--config-dir ./config \
    	--logs-dir ./logs \
    	--work-dir ./workdir \
    	-d '*.savvasdev.com'

	$ certbot certonly \
		--manual \
		--preferred-challenges=dns \
		--email p.sathesh@gmail.com \
		--agree-tos \
		--config-dir ./config \
		--logs-dir ./logs \
		--work-dir ./workdir \
		-d '*.bagi-inc.com'
		


[BACK to TOC](./../README.md)

----------