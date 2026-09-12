# Lab 4 – Working with Amazon Elastic Block Store (EBS)

## Author

* **Name**:Sugeshan S
* **Register Number**: 212224040337
* **Date of Submission**: 24.08.2026

---

## Objective

The objective of this experiment is to understand how Amazon Elastic Block Store (EBS) provides persistent block-level storage for EC2 instances. This lab focuses on creating and attaching an EBS volume, formatting and mounting it on an EC2 instance, storing data, and verifying data persistence after instance reboot.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* An existing EC2 instance (Amazon Linux 2 preferred)
* Basic knowledge of Linux commands

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Amazon EBS
* SSH Client (Terminal / PuTTY)

---

## Tasks Performed

### Task 1: Explore Amazon EBS

Explore the Amazon EBS service through the EC2 dashboard. Observe different volume types such as General Purpose SSD (gp2/gp3), Provisioned IOPS SSD, Throughput Optimized HDD, and Cold HDD.

---

### Task 2: Create an EBS Volume

Create a new EBS volume in the same Availability Zone as the EC2 instance. Choose an appropriate size and volume type.

---

### Task 3: Attach EBS Volume to EC2 Instance

Attach the created EBS volume to the running EC2 instance as an additional block device.

---

### Task 4: Format the EBS Volume

Connect to the EC2 instance using SSH and format the attached volume with a file system (for example, ext4).

---

### Task 5: Mount the EBS Volume

Mount the formatted volume to a directory in the EC2 instance (for example, /data or /mnt/ebs).

---

### Task 6: Store Data in EBS Volume

Create files and directories inside the mounted EBS volume and store sample data.

---

### Task 7: Verify Data Persistence

Reboot the EC2 instance and verify that the data stored in the EBS volume is still available after reboot.

---

## Workflow (Student Explanation)

1.Log in to the AWS Management Console, navigate to EC2 Dashboard, and explore the Amazon EBS service and its available volume types.

2.Create a new EBS volume in the same Availability Zone as the existing EC2 instance by selecting the required size and volume type.

3.Attach the created EBS volume to the running EC2 instance as an additional block device.

4.Connect to the EC2 instance using SSH, format the attached volume with a file system (such as ext4), and mount it to a directory (for example, /mnt/ebs).

5.Create files and store sample data inside the mounted volume, reboot the EC2 instance, and verify that the stored data remains available to confirm persistence.

## Output Screenshots (Attach 3)

### Screenshot 1: EBS Volume Created

<img width="1917" height="955" alt="Screenshot 2026-08-24 122012" src="https://github.com/user-attachments/assets/d5c2b9ad-e516-4f07-8282-c01ac26bfd55" />


### Screenshot 2: EBS Volume Attached to EC2

<img width="1917" height="932" alt="Screenshot 2026-08-24 122232" src="https://github.com/user-attachments/assets/e7776b37-caa4-479f-a67f-eff3f1dedeea" />

<img width="1916" height="882" alt="Screenshot 2026-08-24 124933" src="https://github.com/user-attachments/assets/e8643a2b-a195-4ec1-8a32-3e35c6c0aaf5" />



### Screenshot 3: Mounted Volume with Data

<img width="1600" height="815" alt="image" src="https://github.com/user-attachments/assets/ba5b38ed-141e-4238-9412-a3ab37b9e1cc" />


## Result / Conclusion

This experiment demonstrated how Amazon EBS provides persistent storage for EC2 instances. By creating, attaching, formatting, and mounting an EBS volume, and by verifying data after reboot, the concept of durable block storage in the cloud was clearly understood.
