# Overview
A step-by-step guide on how to do DevOps CI/CD using AWS, Jenkins and Docker.

# Create AWS Account
**AWS Free Tier Promotion**
![AWS Free Tier Promotion](screenshots/aws/1-aws-free-tier-promotion.png)

**Create AWS Account**
![Create AWS Account](screenshots/aws/2-create-aws-account.png)

**Select Account Type**
![Select Account Type](screenshots/aws/3-setup-account-type.png)

**Optional - Personalize Experience**

This gives AWS an opportunity to provide tutorial suggestions and tailor the user experience to your specific role.
![Personalize Experience](screenshots/aws/4-personalize-aws-experience.png)

**Login to AWS Console**
![Login to AWS Console](screenshots/aws/5-login-to-aws-console.png)

**Select CloudFormation Service**
![Select CloudFormation Service](screenshots/aws/6-select-cloud-formation-service.png)

**Click Create Stack**
![Click Create Stack](screenshots/aws/7-create-aws-stack.png)

**Select Create Template Designer**
![Select Create Template Designer](screenshots/aws/8-create-aws-template-designer.png)

**Click Create Template In Designer**
![Click Create Template In Designer](screenshots/aws/9-create-template-in-designer.png)

**Select YAML Radio Button**
![Select YAML Radio Button](screenshots/aws/10-select-yaml.png)

**Select Template Tab**
![Select Template Tab](screenshots/aws/11-select-template-tab.png)

**Clear Template Section**
![Clear Template Section](screenshots/aws/12-clear-everything-in-template-section.png)

**Copy/Paste EC2 Template**
![Copy/Paste EC2 Template](screenshots/aws/13-paste-ec2-instance-template.png)
Copy Template From
```
https://raw.githubusercontent.com/subsari/snippets/master/aws/ec2-centos7-instance.yml
```

**Click Refresh Icon**
![Click Refresh Icon](screenshots/aws/14-click-refresh-icon.png)

**Click Valid Icon**

This will validate the template and prompt you if there are any syntax errors.
![Click Valid Icon Checkmark](screenshots/aws/15-click-validate-icon.png)

**Click Create Stack Icon**
![Click Create Stack Icon](screenshots/aws/16-click-create-stack-icon.png)

**Click Next On Create Stack**
![Click Next On Create Stack](screenshots/aws/17-click-next-on-create-stack.png)

**Specify Stack Name**
![Specify Stack Name](screenshots/aws/18-specify-stack-name.png)

**Specify PUBLIC SSH Key**

[HowToGenerateSSHKey.MD](HowToGenerateSSHKey.MD)

![Specify Public SSH Key](screenshots/aws/19-specify-ssh-key-security-group-subnet-vpc.png)

![Specify Default Security Group, Any Subnet and Default VPC](screenshots/aws/19-specify-ssh-key-security-group-subnet-vpc.png)

**Specify Stack Options**
![Specify Stack Options](screenshots/aws/20-stack-options-leave-blank.png)

**Click Next On Stack Options**
![Click Next On Stack Options](screenshots/aws/21-click-next-on-stack-options.png)

**Review Stack Options**
![Review Stack Options](screenshots/aws/22-review-stack-options.png)

**Click Next On Review Stack Options**
![Click Next On Review Stack Options](screenshots/aws/23-click-next-on-review-stack-options.png)

**Stack Creation In Progress**
![Stack Creation In Progress](screenshots/aws/24-stack-creation-inprogress.png)

**Stack Creation Done**
![Stack Creation Done](screenshots/aws/25-stack-creation-done.png)

**View Stack Resources**

Click the Refresh Icon on the right-hand side.
![Click Stack Resources](screenshots/aws/26-stack-creation-resources.png)

**Navigate To Stack Resource**
![Click Stack Resource](screenshots/aws/27-click-stack-resource-link.png)

**Copy EC2 Public IP**
![Copy EC2 Public IP](screenshots/aws/28-copy-ec2-instance-ip.png)

**Check Inbound Range IP**
![Check IP Inbound Range](screenshots/aws/29-click-default-security-group.png)

<strong>Do you know/recognize the 'Source' value?</strong>
If not, then follow the link below before continuing.

[HowToOpenSecurityGroup.MD](HowToOpenSecurityGroup.MD)

**Connect to EC2 Instance Using SSH & Private Key**
![SSH to EC2 Instance Using SSH & Private Key](screenshots/aws/30-ssh-to-instance-specify-private-key.png)

**Install Java, Install & Configure Jenkins**
1. [HowToInstallJava](HowToInstallJava.MD)
2. [HowToInstallJenkins](HowToInstallJenkins.MD)
3. [HowToConfigureJenkins](HowToConfigureJenkins.MD)

**Install cURL**
```
sudo yum install curl -y
```

**Install GIT**
1. Connect to Instance
2. Execute Yum Command
```
sudo yum install git -y
```
![Install Git](screenshots/git/1-install-git.png)

**Install Docker**
1. Connect to Instance
2. Execute Docker Install Command
```
sudo yum install docker -y
```
![Install Docker](screenshots/docker/1-install-docker-command.png)

**Enable Docker**
```
sudo systemctl enable docker
```

**Start Docker**
```
sudo systemctl start docker
```

# Jenkins #
**Create New Jenkins Job**
![Create New Jenkins Job](screenshots/jenkins/9-create-new-job.png)

**Create New Jenkins Pipeline**
![Create New Jenkins Pipeline](screenshots/jenkins/10-create-new-pipeline.png)

**Specify Pipeline Details**

1. Check Prevent Concurrent Builds
2. Specify To Build Every 5 Minutes
![Specify Pipeline Details](screenshots/jenkins/11-specify-pipeline-details.png)
3. Copy/Paste Pipeline Script From: https://raw.githubusercontent.com/subsari/snippets/master/jenkins/pipeline-example.yml

![Specify Pipeline Script](screenshots/jenkins/12-specify-pipeline-script.png)

**Click 'Build Now' to Build Pipeline**
![Build Pipeline](screenshots/jenkins/13-build-pipeline.png)

**Wait For Pipeline To Build**
![Wait For Pipeline To Build](screenshots/jenkins/14-wait-for-build.png)

**Navigate To Build**
![Navigate To Build](screenshots/jenkins/15-navigate-to-build.png)

**View Build Log**
![View Build Log](screenshots/jenkins/16-view-build-log.png)

**View Builds Overview**
![View Builds](screenshots/jenkins/17-view-builds-overview.png)

# Setup Continuous Integration & Continuous Deployment
1. [HowToInstallJenkinsGithubPlugin.MD](HowToInstallJenkinsGithubPlugin.MD)
2. [HowToBuildJenkinsOnGitPush.MD](HowToBuildJenkinsOnGitPush.MD)

# Final Result Video
**Process Overview**

1. Code pushed to repository
2. Webhook project triggered from code pushed
3. Webhook project builds
4. MyProjectPipeline builds (triggered after successful build of Webhook project)

**MyProjectPipeline Builds**
1. Repository cloned to workspace
2. Docker image is built
3. Docker instance runs
4. Unit & Integration tests run on Docker instance
5. Environment is cleaned up (ie. remove Docker instance & workspace)
6. Code promoted and deployed on successful testing
 

![DevOps CI/CD AWS, Jenkins & Docker](screenshots/devops/devops-ci-cd-aws-jenkins-docker.gif)