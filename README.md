Tested on: Ubuntu 20.04 LTS And Zorin OS 16.3

Place these 2 files (docker-compose.yml, traefik_dynamic.yml) on same directory. And edit the file- docker-compose.yml on line number 20, replace the '/home/sumon' with your current directory path.

Pull the Traefik image on local docker registry.
-> docker pull traefik:v2.10

To allow docker to listen on port 53 run these commands:
-> systemctl disable systemd-resolved
-> systemctl stop systemd-resolved

Finally execute this command to deploy the load balancer:
-> docker-compose up -d

Browse this URL: http://YOUR_IP:8080/, here you will get service status.
