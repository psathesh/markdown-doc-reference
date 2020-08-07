# Network

All network related commands and setup


## IP loopback set up on MacOs

[Article: MacOS Adding a loopback alias](https://aaron.blog/2011/02/04/mac-os-x-adding-a-loopback-alias){:target="_blank"}

[Article: MacOS permanently create an ifconfig loopback alias](https://medium.com/@david.limkys/permanently-create-an-ifconfig-loopback-alias-macos-b7c93a8b0db){:target="_blank"}

[Article: MacOS Persistent loopback interfaces](https://blog.felipe-alfaro.com/2017/03/22/persistent-loopback-interfaces-in-mac-os-x){:target="_blank"}


Check the ping and create a IP loopback alias

	$ ifconfig
	$ ping 127.0.0.2
	$ sudo ifconfig lo0 alias 127.0.0.2

Check the ping and remove a IP loopback alias

	$ ifconfig
	$ ping 127.0.0.2	
	$ sudo ifconfig lo0 -alias 127.0.0.2

Steps to create the ip loopback and persist them through launch daemons

	$ sudo nano /Library/LaunchDaemons/org.sathesh.loopback.ip2.plist

Sample launch daemon file

	<?xml version="1.0" encoding="UTF-8"?>
	<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
	<plist version="1.0">
	<dict>
		<key>Disabled</key>
		<false/>
		<key>Label</key>
		<string>org.sathesh.loopback.ip2</string>
		<key>ProgramArguments</key>
		<array>
			<string>/sbin/ifconfig</string>
			<string>lo0</string>
			<string>alias</string>
			<string>127.0.0.2</string>
		</array>
		<key>RunAtLoad</key>
		<true/>
	</dict>
	</plist>

Start the service and verify the launch daemon configuration

	$ sudo launchctl load /Library/LaunchDaemons/grep org.sathesh.loopback.ip2.plist

	$ sudo launchctl list | grep org.sathesh.loopback.ip2
	
	-	0	org.sathesh.loopback.ip2
	
	
	$ ifconfig lo0
	
	lo0: flags=8049<UP,LOOPBACK,RUNNING,MULTICAST> mtu 16384
		options=1203<RXCSUM,TXCSUM,TXSTATUS,SW_TIMESTAMP>
		inet 127.0.0.1 netmask 0xff000000 
		inet6 ::1 prefixlen 128 
		inet6 fe80::1%lo0 prefixlen 64 scopeid 0x1 
		inet 127.0.0.2 netmask 0xff000000 
		inet 127.0.0.3 netmask 0xff000000 
		nd6 options=201<PERFORMNUD,DAD>




[BACK to TOC](../../README.md)

----------