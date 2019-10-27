# ec2dhis2docker
AWS EC2 t2.micro instance with Ubuntu18.04 64bit<br> 
Tested on: EC2 instances and Virtualbox<br>
Maintained by: Dexter N. (dhec.naag@gmail.com)<br>
For: Nutrition Center of the Philippines (jsolon@ncp.org.ph)<br>
Disclaimer: This is for testing purposes only, the Maitainer, NCP(the owner) or its affiliations is free from liabilities of any kind. 

Procedures:<br>
1. Launch a t2.micro (or better) EC2 with Ubuntu 18.04 OS 64bit
2. Login to the instance using your SSH Client
3. Then: sudo apt update && sudo apt upgrade -y
4. Then: sudo apt install docker docker-compose -y 
5. Clone this repository: sudo git clone https://github.com/ncp-ph/ec2dhis2docker.git
6. Go to the directory: cd ec2dhis2docker
7. Then execute: sudo docker-compose up -d (for dhis-core version: sudo docker-compose -f dhis2-core.yml up -d)
8. Wait until containers are up (takes < 5 minutes for dhis-web and >10 minutes for dhis-core) 
9. Go to http://ec2-endpoint_or_ip_address_here and login with these credentials: admin/district

Important Notes:<br> 
a. Any changes on the site is saved on 'datadb' folder which is on the same directory as this repository<br>
b. By default, the dhis2-web or lightweight version is configured on the docker-compose.yml file<br>
c. If you want to use the core version make sure that your EC2 instance is at least t2.small or higher<br>
c. This was also tested to run on AWS Linux, CentOS but will require more configurations that is not written here<br>
d. This will not work nor tested on any WindowsOS and MacOS
