# Jenkins
# Jenkins Installation for Redhat: https://www.jenkins.io/doc/book/installing/linux/#red-hat-centos 

#script

#!/bin/bash 
sudo wget -O /etc/yum.repos.d/jenkins.repo \
    https://pkg.jenkins.io/redhat/jenkins.repo
sudo rpm --import https://pkg.jenkins.io/redhat/jenkins.io-2023.key
sudo yum upgrade
# Add required dependencies for the jenkins package
sudo yum install java-17-openjdk
sudo yum install jenkins
#Start the Jenkins service with the command:
sudo systemctl start jenkins
#Check the status of the Jenkins service using the command:
sudo systemctl status jenkins
