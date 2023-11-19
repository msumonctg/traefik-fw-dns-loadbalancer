<h4>Tested on: <b>Ubuntu 20.04 LTS</b> And <b>Zorin OS 16.3</b></h4>

Place these 2 files (<i>docker-compose.yml, traefik_dynamic.yml</i>) on same directory. And edit the file: <b>docker-compose.yml</b> on line number 20, replace the <i>'/home/sumon'</i> with your current directory path.
<br><br>
Pull the Traefik image on local docker registry.
<br>
-> <code>docker pull traefik:v2.10</code>

To allow docker to listen on port 53 run these commands:
<br>
-> <code>systemctl disable systemd-resolved</code>
<br>
-> <code>systemctl stop systemd-resolved</code>

Finally execute this command to deploy the load balancer:
<br>
-> <code>docker-compose up -d</code>

Browse this URL: <b>http://YOUR_IP:8080/</b>, here you will get service status.
