# Overview
A step-by-step guide on how to do configure Jenkins to build a project upon a github commit push event.

This enables you to perform Continuous Integration & Continuous Deployment for your DevOps initiatives.

# Install Github Integration Jenkins Plugin
[HowToInstallJenkinsGithubPlugin.MD](HowToInstallJenkinsGithubPlugin.MD)

# Configure Jenkins 
**Click New Item**
![Click New Item](screenshots/jenkins/build-project-on-git-push/1-click-new-item.png)
**Specify Description**
![Specify Description](screenshots/jenkins/build-project-on-git-push/2-specify-description.png)
**Select Git Radio Button**
![Select Git Radio Button](screenshots/jenkins/build-project-on-git-push/3-click-git-under-source-code-management.png)
**Specify Project URL**
![Specify Project URL](screenshots/jenkins/build-project-on-git-push/4-specify-project-url.png)
**Specify Branch**
![Specify Branch](screenshots/jenkins/build-project-on-git-push/5-specify-branch.png)
**Click Add Credentials**
![Click Add Credentials](screenshots/jenkins/build-project-on-git-push/6-click-add-credentials.png)
**Specify Username & Password**
![Specify Username & Password](screenshots/jenkins/build-project-on-git-push/7-specify-username-password.png)
**Select Credentials**
![Select Credentials](screenshots/jenkins/build-project-on-git-push/8-select-credentials.png)
**Check Github Hook Trigger**
![Check Github Hook Trigger](screenshots/jenkins/build-project-on-git-push/9-check-github-hook-trigger.png)
**Click Save**
![Click Save](screenshots/jenkins/build-project-on-git-push/10-click-save.png)

# Configure Github Project
**Open Git Repository**
![Open Git Repository](screenshots/git/configure-webhook/1-open-git-repository.png)

**Click Settings Tab**
![Click Settings Tab](screenshots/git/configure-webhook/2-click-settings-tab.png)

**Click Webhooks**
![Click Webhooks](screenshots/git/configure-webhook/3-click-webhooks-section.png)

**Click Add Webhook**
![Click Add Webhook](screenshots/git/configure-webhook/4-click-add-webhook.png)

**Specify Project URL**
![Specify Project URL](screenshots/git/configure-webhook/5-specify-project-url.png)

**Specify Individual Events**
![Specify Individual Events](screenshots/git/configure-webhook/6-check-select-individual-select-pushes-active-click-add-webhook.png)

# Build After Webhook Project Builds
**Go To Jenkins Dashboard**
![Go To Jenkins Dashboard](screenshots/jenkins/build-project-on-git-push/cd-1-jenkins-dashboard.png)
**Click Configure**
![Click Configure](screenshots/jenkins/build-project-on-git-push/cd-2-open-project-click-configure.png)
**Select Build After**
![Select Build After](screenshots/jenkins/build-project-on-git-push/cd-3-select-build-after.png)
**Specify Project Name With Webhook**
![Specify Project With Webhook](screenshots/jenkins/build-project-on-git-push/cd-4-specify-project-with-webhook.png)
**Save Webhook Build**
![Save Webhook Build](screenshots/jenkins/build-project-on-git-push/cd-5-save-webhook-build.png)

# Final Result Video
![DevOps CI/CD AWS, Jenkins & Docker](screenshots/devops/devops-ci-cd-aws-jenkins-docker.gif)