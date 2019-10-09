# ec2dhis2docker
AWS EC2 t2.micro instance on Ubuntu18.04 64bit and DHIS2+PostgreSQL 

1. Launch a t2.micro (or better) EC2 with Ubuntu 18.04 OS 64bit
2. Login to the instance and do:
	2.1 sudo apt update
	2.2 sudo apt upgrade
	2.3 sudo apt install docker docker-compose
	2.4 sudo reboot now 
3. Pull this repository upon logging in on SSH (Default is /home/ubuntu/) and execute: docker-compose up -d
4. Wait until containers are up.
