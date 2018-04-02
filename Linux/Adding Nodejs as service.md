# Adding nodejs as a service

## Install Uptime 
* $sudo apt install uptime
* $sudo apt-get install upstart-sysv
* $sudo update-initramfs -u
* $sudo reboot

## create the service
* $cd /etc/init
* $vi app.conf
* Add the following script
		
		description "node.js server"
		author      "Foo Bar"
		
		# used to be: start on startup
		# until we found some mounts weren't ready yet while booting
		
		start on started mountall
		stop on shutdown
		
		# automatically respawn
		
		respawn
		respawn limit 99 5
		
		script
			
			export HOME="/root"
			exec /usr//bin/nodejs /var/lib/jenkins/workspace/nodejs-project/app.js >> /var/log/node.log 2>&1
		
		end script
