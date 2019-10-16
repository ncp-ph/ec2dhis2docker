# ec2dhis2docker
AWS EC2 t2.micro instance on Ubuntu18.04 64bit and DHIS2+PostgreSQL 
(Tested on Virtualbox and other OS with Docker)

1. Launch a t2.micro (or better) EC2 with Ubuntu 18.04 OS 64bit
2. Login to the instance using your SSH Client
3. Then: sudo apt update
4. Then: sudo apt upgrade
5. Then lastly: sudo apt install docker docker-compose	 
6. Pull this repository upon logging in on SSH (Default is /home/ubuntu/) and execute: sudo docker-compose up -d
7. Wait until containers are up (takes < 5 minutes) 
8. Go to http://<public_ip> or http://<endpoint> and login with these credentials: admin/district

Note: any changes on the site is saved on 'datadb' folder which is on the same directory as this repository
