# ansible_challenge

This repo primarily conists of one ansible playbook,templates and files which are required to perform the below 6 tasks, and the ansible playbook already has been 
tested successfully on Ubuntu 16.04. 

1 Write an Ansible Playbook to perform the following including install the following software for development on EC2 "ec2_devops" created in Problem #1 above.
2 Apache webserver; Configure it to start at server boot, and listening on all interfaces on port 80
3 Tomcat application server;Configure it to start at server boot, and listening on all interfaces on port 8080
4 MySQL database server;Configure it to start at server boot, and listening on all interfaces on port 3306
5 Install below packages
  Telnet
  Curl
  Nslookup
  Oracle JDK
6 Disable firewalls on "ec2_devops" or allow ports 80, 8080, 3306 from anywhere to access the 3 services configured above. 

How to run the playbook 

#######################
                 Download all files attached in this repo, I have placed those files  /home/ubuntu on the ansible server.  If you you would like to copy these files under different location, then  please update ansible_main.yaml file as well.
                 Below ansible variables have been updated in /etc/ansible/hosts file. 

[ec2_devops]
10.7.7.1 #Here you have to mention the IP address where you will be installing and configuring apache httpd, apache tomcat and mysql
[ec2_devops:vars]
http_port= 8080
https_port= 8443
admin_username= admin
admin_password= adminsecret
mysql_root_password = my_Sq1kk
root@ip-172-17-17-222:~#

                 
                 Run the below command to execute the playbook
                 #ansible-playbook ansible_main.yaml
                 
                 
