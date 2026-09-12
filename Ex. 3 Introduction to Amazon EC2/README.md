# Lab 3 – Introduction to Amazon Elastic Compute Cloud (EC2)

## Author

* **Name**: Sugeshan S
* **Register Number**:212224040337
* **Date of Submission**: 21.08.2026

---

## Objective

The objective of this experiment is to understand the fundamentals of Amazon Elastic Compute Cloud (EC2). This lab focuses on launching and managing a virtual server, understanding instance types and AMIs, connecting to an EC2 instance, monitoring its status, and performing basic instance operations such as start, stop, and terminate.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* Web browser with internet connectivity
* Basic knowledge of Linux commands (optional)

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Key Pair
* Security Group
* SSH Client (PuTTY / Terminal)

---

## Tasks Performed

### Task 1: Explore Amazon EC2 Dashboard

Explore the EC2 service dashboard in the AWS Management Console. Observe the different sections such as Instances, AMIs, Instance Types, Key Pairs, Security Groups, and Elastic IPs.

---

### Task 2: Launch an EC2 Instance

Launch a new EC2 instance using Amazon Linux 2 AMI. Select an appropriate instance type (t2.micro) under the free tier. Configure basic settings such as instance name, key pair, and security group.

---

### Task 3: Configure Security Group

Configure a security group to allow inbound access:

* SSH (Port 22) from your IP address
* HTTP (Port 80) from anywhere (0.0.0.0/0)

This security group acts as a firewall for the instance.

---

### Task 4: Connect to EC2 Instance

Connect to the running EC2 instance using SSH. Use the downloaded key pair and connect via terminal or PuTTY.

For Amazon Linux:

```
ssh -i "keyname.pem" ec2-user@<Public-IP>
```

---

### Task 5: Perform Basic Instance Operations

Perform the following operations from the EC2 console:

* Stop the instance
* Start the instance
* Reboot the instance

Observe the state changes of the instance.

---

### Task 6: Monitor EC2 Instance

Monitor the EC2 instance using the Monitoring tab. Observe metrics such as CPU utilization, network in/out, and instance status checks.

---

### Task 7: Terminate EC2 Instance

Terminate the EC2 instance after completing the experiment to avoid unnecessary AWS charges.

---

## Workflow (Student Explanation)

First, I created a VPC in Amazon Web Services. I gave it a CIDR block of 10.0.0.0/16. This VPC acts as my private network where all my resources will be created.

Next, I created a public subnet inside the VPC with CIDR 10.0.1.0/24. I enabled auto-assign public IP so that any instance launched in this subnet will automatically get a public IP address.

After that, I created an Internet Gateway and attached it to my VPC. This allows my VPC to communicate with the internet.

Then, I created a route table and added a default route (0.0.0.0/0) pointing to the Internet Gateway. I associated this route table with my public subnet. This step ensures that traffic from my subnet can reach the internet.

Next, I created a security group which acts as a virtual firewall. I allowed inbound traffic for SSH on port 22 and HTTP on port 80.

After completing the network setup, I launched an EC2 instance using Amazon Linux 2 AMI with instance type t2.micro. I selected my VPC, public subnet, created security group, and key pair.

Finally, I connected to the EC2 instance using SSH and installed the Apache web server. I started the service and created a simple HTML page. Then I copied the public IP address of the instance and opened it in a web browser. The webpage was displayed successfully.

So, this is how I created a VPC, launched an EC2 instance, and hosted a simple web server in AWS.

---

## Output Screenshots (Attach 3)

### Screenshot 1: EC2 Dashboard / Instance List

<img width="1917" height="968" alt="Screenshot 2026-08-19 192349" src="https://github.com/user-attachments/assets/41d7e775-27ba-4462-9676-d163e4164dbc" />


---

### Screenshot 2: SSH Connection to Instance

<img width="1301" height="494" alt="image" src="https://github.com/user-attachments/assets/c4e31e56-4b86-4855-9b26-c7b18084a6cd" />


---

### Screenshot 3: Instance Monitoring / Status

<img width="1409" height="622" alt="image" src="https://github.com/user-attachments/assets/7be73e60-bb53-41e0-8d21-a72c1fda3406" />


---

## Result 

This experiment provided hands-on experience with Amazon EC2 by demonstrating how to launch, connect, manage, and monitor a virtual server in AWS. It helped in understanding the concept of Infrastructure as a Service (IaaS) and how compute resources can be provisioned and controlled on demand in the cloud.
