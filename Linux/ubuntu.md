|Command|Descritpion|
|------|------|
|sudo netstat -tulpn \| grep :80|verify which process is attached to port 80|
|sudo ssh username@IP -i|to connect to the machine with a key|
|sudo rm -r mydir|To Delete the entire Directeory|
|cd /etc/systemd/system/|Location of the services in linux|
|sudo systemctl daemon-reload|Reload service|
|sudo systemctl stop service-name|Stop a service|
|sudo systemctl start service-name|start a service|
|cp -R source destination/|copy the Directory in a recursive way|
|ssh-keygen|To Generate a public key and a private key|
|ssh ubuntu@IP_of_machine -i ~/.ssh/id_rsa -o ProxyCommand='ssh -W %h:%p -q ubuntu@ProxyIP'|To connect to a machine through a proxy|


