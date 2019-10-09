# ec2dhis2docker
AWS EC2 t2.micro instance on Ubuntu18.04 64bit and DHIS2+PostgreSQL 

1. Launch a t2.micro (or better) EC2 with Ubuntu 18.04 OS 64bit
2. Login to the instance and do: sudo apt update
3. Then: sudo apt upgrade
4. Then last: sudo apt install docker docker-compose	 
5. Pull this repository upon logging in on SSH (Default is /home/ubuntu/) and execute: sudo docker-compose up -d
6. Wait until containers are up
