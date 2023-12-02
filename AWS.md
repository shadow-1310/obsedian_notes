### Steps

1. Make the account in Amazon Console
3. Go to EC2 and 
	1. click launch instances
	2. choose AMI - Amazon Machine Image - Ubuntu
	3. Choose instance typre
		1. t2.micro ( 1GB memory)
		2. t2.nano
		3. t2.large
	4. Configure instance
	5. Add storage
		1. 8 GB SSD
4. Select or create key-pair
	1. download key-pair in .pem format
5. Check running instances if it is running - 
	1. it will show running 
6. Connect to instance
	1. windows
		1. use putty and putty generator
			1. convert .pem file to .ppk file (public -private key)
			2. find public ipv4 address of running instance
			3. also find username (default is ubuntu)
			4. use it for connecting
			5. give .ppk file for ssh authentication
	2. Linux
		```bash
			ssh -i <pem-file> hostname@address
		```
7. Setup python and pip in the machine 
- change app.run args
	- host = 0.0.0.0
	- port = 8080
8. run the app (flask or streamlit)
9. check Public DNS (in SSH client section)
	1. use DNS/8080 for http
	2. use DNS/433 for https
#### Security Group
- name and description
- inbound rule
	- all traffic
	- ssh
	- udp
	- tcp
	- https
- source
	- anywhere - 0.0.0.0
	- my ip
- change security group of the instance 
- Terminate instance if not using


## CI-CD
- build docket image of source code
- push docker image to ECR
- Launch EC2
- pull image from ECR to EC2
- launch docker image in EC2

1. Create IAM user
	1. attach policy
		1. EC2 registry full access
		2. EC2 full access
2. Create access key for CLI
	1. access key
	2. secret key
3. Create ECR repo
	1. save the URI
4. Create EC2 machine
	1. Name the machine
	2. Select the machine
	3. create the key pair
5. Open Ec2 machine and install docker
6. Configure EC2 as self hosted runner
	1. setting in github page
	2. run some commands in machine
7. Setup github secrets