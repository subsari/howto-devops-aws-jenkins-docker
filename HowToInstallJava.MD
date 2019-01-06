# Overview
A step-by-step guide on how to install Java on AWS CentOS 7.

# How to Generate An SSH Key
1. Connect to EC2 Instance
2. Execute Install Command
![Execute Install Command](screenshots/java/1-execute-install-command.png)
3. View Installed Version
![View Installed Version](screenshots/java/2-view-version-installed.png)
4. Set Environment Variables
![Set Environment Variables](screenshots/java/3-set-global-variables.png)

Set Java Home
```
echo 'export JAVA_HOME=/usr/lib/jvm/jre-1.8.0-openjdk' | sudo tee -a /etc/profile
```

Set JRE Home
```
echo 'export JRE_HOME=/usr/lib/jvm/jre' | sudo tee -a /etc/profile
```

Execute Source Command To Read From File
```
source /etc/profile
```