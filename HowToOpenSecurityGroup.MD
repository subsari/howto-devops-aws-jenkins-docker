# Overview
A step-by-step guide on how to do open the security group to allow connections from any IP address.

# How to Open AWS Security Group To All IPs
1. Open AWS Services Link
![Open AWS Services Dropdown](screenshots/security-group/1-navigate-to-ec2-service.png)
2. Click Security Groups
![Click Security Groups](screenshots/security-group/2-click-security-groups.png)
3. Click Inbound Tab
![Click Inbound Tab](screenshots/security-group/3-click-inbound-tab.png)
4. Click Edit Button
![Click Edit Button](screenshots/security-group/4-click-edit-button.png)
5. Specify IP Range
![Specify IP Range](screenshots/security-group/5-specify-ip-range.png)
6. Save Inbound Rules
![Save Inbound Rules](screenshots/security-group/6-save-inbound-rules.png)

Never leave the security group open to all IP addresses. For security measures you want to eventually come back and specify a limited set of IP addresses. It's the simplest way to secure your cloud instances.