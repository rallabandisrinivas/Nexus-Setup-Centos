# Nexus-Setup-Centos

In recent work, we need to build a Nexus private server to save some related jar packages of the docker image and maven. First, put the official download address of the Nexus3 installation package. Here we choose Unix to download and install.

Step-1 --> Install nexus 
$yum install wget -y

Then we execute the following command to put the nexus installation package under our /usr/local
$ cd /home 
$ wget https://sonatype-download.global.ssl.fastly.net/repository/downloads-prod-group/3/nexus-3.28.0-01-unix.tar.gz 
$ tar -zxvf nexus-3.28.0-01-unix.tar.gz
$ mv nexus-3.16.1-02-unix ./nexus

Step-2 --> Modify the user used to run nexus 
$ cd /home/nexus/bin 
$ vim nexus.rc 
run_as_user="root"

Step-3 --> Modify nexus startup port 
$ vim /home/nexus/etc/nexus-default.properties

Step-4 --> Install Java 
$sudo yum install java-1.8.0-openjdk

Step-5 --> Start Nexus 
$ ./nexus start 
$ ./nexus restart 
$ ./nexus stop 
$ ./nexus run & 
$ ./nexus status

Step-6 --> Launch Nexus by using your Public_IP and port number8081 
 http://Public_ip:8081/

Step-7 -->To get admin password go to the following location 
$cd /home/sonatype-work/nexus3/ cat admin.password

Step-8 -->Paste the password in the browser and Login into the Browser


 
