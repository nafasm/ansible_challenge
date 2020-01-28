# ansible_challenge

  This repo primarily conists of one ansible playbook,templates and files which are required to perform the below 5 tasks, and the ansible playbook already has been tested successfully on Ubuntu 16.04. 

  This Ansible Playbook install and configure the following applications, For example: Here  I have installed all these on a aws EC2  instance named "ec2_devops".  You may refer https://github.com/nafasm/terraform_challenge for more information. 

2 Apache webserver; Configure it to start at server boot, and listening on all interfaces on port 80

2 Tomcat application server;Configure it to start at server boot, and listening on all interfaces on port 8080

3 MySQL database server;Configure it to start at server boot, and listening on all interfaces on port 3306

4 Install below packages

  Telnet
  Curl
  Nslookup
  Oracle JDK
  
5 Disable firewalls on "ec2_devops" or allow ports 80, 8080, 3306 from anywhere to access the 3 services configured above. 

How to run the playbook 

#######################

                1.  Download all files attached in this repo, I have placed those files  /home/ubuntu on the ansible server.  If you you would like to copy these files under different location, then  please update ansible_main.yaml file as well.
                2. Update varialbes and host information in /etc/ansible/hosts file.  For exmaple, I have updated my /etc/ansible/hosts as below 

[ec2_devops]
10.7.7.1 #Here you have to mention the IP address where you will be installing and configuring apache httpd, apache tomcat and mysql
[ec2_devops:vars]
http_port= 8080
https_port= 8443
admin_username= admin
admin_password= adminsecret
mysql_root_password = my_Sq1kk
root@ip-172-17-17-222:~#

            3.  Run the below command to execute the playbook
            
                 #ansible-playbook ansible_main.yaml
                 
                 
