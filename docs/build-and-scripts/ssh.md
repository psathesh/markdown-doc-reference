# SSH

SSH Commands

[openssh](https://www.openssh.com/manual.html)


## Commands

	$ ssh -L 127.0.0.1:13310:dbs-b3-1001:1521 upurusa@bridge.pearsoncmg.com

## SSH Pass commands

	$ brew install https://raw.githubusercontent.com/kadwanev/bigboybrew/master/Library/Formula/sshpass.rb

	$ sshpass -p 'Micr0sc0p3' ssh -o StrictHostKeyChecking=no psview@icduppsnxweb01.pearsontc.com 'ls -lrt'

	$ sshpass -p 'Micr0sc0p3' ssh psview@icduppsnxweb01.pearsontc.com "ls -lrt;"

	$ sshpass -p 'Micr0sc0p3' ssh -t psview@icduppsnxweb01.pearsontc.com "tail -1000f /opt/customer/logs/apache/psn-prod-SSL.http.access.log.2017-11-10-04_00; bash;"

	$ sshpass -p 'Micr0sc0p3' ssh -t psview@icduppsnxweb01.pearsontc.com "bash; ls -lrt;"

	
	

[BACK to TOC](./../README.md)

----------