# ec2dhis2docker
AWS EC2 t2.micro instance on Ubuntu18.04 64bit and DHIS2+PostgreSQL<br> 
Tested on: Virtualbox, AWS Linux and CentOS with Docker

1. Launch a t2.micro (or better) EC2 with Ubuntu 18.04 OS 64bit
2. Login to the instance using your SSH Client
3. Then: sudo apt update && sudo apt upgrade -y
4. Then: sudo apt install docker docker-compose -y 
5. Clone this repository: sudo git clone https://github.com/dhec/ec2dhis2docker.git
6. Go to the directory: cd ec2dhis2docker
7. Then execute: sudo docker-compose up -d ( sudo docker-compose -f dhis2-core.yml for dhis2-core version )
8. Wait until containers are up (takes < 5 minutes for dhis-web and ~10 minues for dhis-core) 
9. Go to http://<public_ip_address> and login with these credentials: admin/district

Important Notes:<br> 
a. any changes on the site is saved on 'datadb' folder which is on the same directory as this repository<br>
b. by default, the dhis2-web or lightweight version is configured on the docker-compose.yml file, if you want to use the core version make sure that your EC2 instance is at least t2.small or higher
