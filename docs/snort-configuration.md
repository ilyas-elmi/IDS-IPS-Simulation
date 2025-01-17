# Snort Installation Guide on Amazon Linux 2
---

## Prerequisites
1. Launch an Amazon Linux 2 EC2 instance.
   - **Instance Type**: t2.micro or larger
   - **Security Group**:
     - Allow SSH (port 22) for remote access.
2. Connect to the instance using SSH.

--- 

## Step 1: Update the System
Run the following command to ensure the system is up-to-date:
```bash
sudo yum update -y
```

## Step 2: Install Required Dependencies
Install all the necessary tools and libraries for building and running Snort:
```bash
sudo yum install -y gcc libpcap libpcap-devel pcre pcre-devel bison flex zlib zlib-devel make wget
```

## Step 3: Download Snort 
Download the Snort source code from the official Snort website:
```bash
wget https://www.snort.org/downloads/snort/snort-2.9.20.tar.gz
```

## Step 4: Extract the Downloaded Archive
Extract the Snort archive:
```bash
tar -xvzf snort-2.9.20.tar.gz
cd snort-2.9.20
```
![Snort Install](../screenshots/snort-install.png)

## Step 5: Build and Install Snort: 