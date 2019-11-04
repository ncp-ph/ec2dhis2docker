# ec2dhis2docker
## Nutrition Center of the Philippines (jsolon@ncp.org.ph)
#### AWS EC2 t2.small instance with Ubuntu18.04 64bit ###
**Maintained by:** Dexter N. (dhec.naag@gmail.com)<br>
**Disclaimer:** This is for testing purposes only, the Maintainer, NCP (the owner) or its affiliations is free from liabilities of any kind.

This does not cover AWS signup, EC2 launches and other configurations. A basic knowledge of Linux commands and Docker might be required though the procedure below is straighforward.<br>
It was tested and guaranteed to work on a Virtualbox instance with Ubuntu 18.04 and 19.04 for personal use (OS installation is not covered). Feel free to import your own sample data and configure it to your needs.<br>

NCP's aim is to run DHIS2 on EC2 instance as well as on other OS platforms the fastest way and with basic technical knowledge.

**Procedures:**<br>
1. Launch a t2.small (or better) EC2 with Ubuntu 18.04 OS 64bit
2. Login to the instance using your SSH Client
3. Then: `sudo apt update && sudo apt upgrade -y`
4. Then: `sudo apt install docker docker-compose -y` 
5. Clone this repository: `sudo git clone https://github.com/ncp-ph/ec2dhis2docker.git`
6. Go to the directory: `cd ec2dhis2docker`
7. Then execute: `sudo docker-compose up -d` (for dhis-web version: `sudo docker-compose -f dhis2-web.yml up -d`)
8. Wait until containers are up (takes less about 5 minutes, if you want to see what's going on the background, you can use the following command: `docker logs -f dhis2`) 
9. Go to http://ec2-endpoint_or_ip_address_here and login with these credentials: admin/district

**Important Notes:**<br> 
a. Any changes on the site is saved on **'datadb'** folder which is on the same directory as this repository<br>
b. By default, the dhis2-core is configured on the docker-compose.yml file<br>
c. If you want to use the web version (now unsupported, according to DHIS2 team) you can use a free-tier t2.micro EC2 instance.<br>
d. This was also tested to run on AWS Linux, CentOS but it will require more configurations that is not written here<br>
e. This was not tested nor work on any WindowsOS and MacOS yet(work-in-progress)
