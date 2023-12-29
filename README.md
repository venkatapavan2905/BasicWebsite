# BasicWebsite
This is a basic Website which runs with five services on five individual Virtual Machines.

Infrastructure:

   Five VMs are spun up by using a Vagrantfile which has boxes of 4 CentOS VMs and 1 Ubuntu VM. Vagrant host manager plugin was used to make entries of all other VMs in /etc/hosts ineach VM.

Services:

 1. Mariadb Service on db01 VM.
 2. Memcached service on mc01 VM.
 3. RabbitMQ service on rmq01 VM.
 4. Tomcat service on app01 VM.
 5. Ngnix service on web01 VM.

All the services are connected by configuring application.properties (/src/main/resources/application.properties) file in project directory of Tomcat server. 

All the services are configured to provision the need to run a basic website.

** This git repo is cloned in db01 VM to copy schema of Database
** This git repo is cloned in app01 VM to perform build opration (maven install) to deploy the artifact(.war) file to /usr/local/tomcat/webapps/ .

 


