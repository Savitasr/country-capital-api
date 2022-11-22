# DevOps_CI_CD_Assignment7 
###1.Login and configure Jenkins server on your system. Configure Docker for Jenkins pipeline. 
###2.Architect a simple calculator application that supports addition, subtraction and product of two positive integers. 
###3.Develop the application package with simple unit test cases in Python 3.x 
###4.Automate the infrastructure creation with AWS CloudFormation templates. (use SAM templates for AWS Lambda functions) 
###5.Add web hooks to trigger a Jenkins build every time changes are pushed to a Git branch on GitHub. 
###6.Trigger the Jenkins pipeline job that uses Docker agent to: 
 ####a. CI: Run the unit test cases and build the package 
 ####b. CD: Deploy the code package to AWS cloud. 
 
 
 Creating AWS account 
 Create key pair 
o Open Amazon EC2 console and sign in 
o Under network and security select key pairs 
o Click on create key pair 
o Save private key name (.pem format) 
 Create security group 
o Decide whom to access your instance 
o Sign in to AWS management console 
o Open Amazon EC2 console by selecting EC2 under compute 
o Select security groups, create security group and enter webserver5G 
o Select VPC from list 
o On inbound tab add rules 
 Select add rule and select SSH 
 Under source select custom and enter ip address in textbox 
 Select add rule and select HTTP from typelist 
 Select add rule and select Custom TCP rule 
 Under port range enter 8080 
 Select Create 
 Launch an Amazon EC2 instance 
o Sign in to AWS management console 
o Open Amazon EC2 console by selecting EC2 under compute 
o From Amazon EC2 dashboard, select Launch Instance. 
o Choose an Amazon Machine Image (AMI) 
o Creating a key pair section 
 Select an existing security group 
 Select webserver 5G 
 Select launch instances 
o Choose instances. 
 Installing and configuring Jenkins 
o Select instance and locate Public DNS 
o From start menu, select All programs>PuTTY>PuTTY 
o In category pane expand connection, expand SSH, select Auth then select .ppk 
file(generated from key pair) 
o Select open to start PuTTY session. 
o Use SSH command to connect instance 
o Enter Yes 
o Downloading and installing Jenkins 
 Ensure software packages are up to date on your instance 
sudo yum update- 
 Add Jenkins repo using following command 
 Import a key file from Jenkins CI to enable the installation from package 
 Install java 
 Install Jenkins 
 Enable Jenkins 
 Start Jenkins as a service 
o Configuring Jenkins 
 Connect to server (http://35.173.133.139:8080) 
 Click install suggested plugins 
 After installation create Admin user, save and continue. 
 Select manage Jenkins and manage manage Plugins 
 Enter and Select Amazon EC2 plugin 
 Select Back to Dashboard 
 Select configure a cloud 
 Select manage Jenkins 
 Add new cloud, select Amazon EC2 
 Click add under EC2 credentials 
 Enter IAM user with permissions to launch EC2 instances and 
select add 
 Select add for EC2 key pairs private key 
 From Jenkins credentials provider Select SSH username with 
private key and set username to EC2 user 
 Select enter under private key then select add 
 Open private key which is created 
 Test connection and ensure it status “Success”, select save. 

