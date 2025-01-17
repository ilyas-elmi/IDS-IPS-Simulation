# Environment Setup

## Step 1: Launching the EC2 Instance
1. Navigate to the AWS Management Console and launch an EC2 instance.
   - OS: Amazon Linux 2
   - Instance Type: t2.micro
2. Configure the Security Group:
   - Allow SSH (port 22) from your IP.
   - Allow All Traffic (0.0.0.0/0) to simulate a vulnerable environment.

![EC2 Instance Launch](../screenshots/Screenshot%202025-01-17%20at%2019.44.55.png)

## Step 2: Disabling the Firewall
After SSHing into the instance, disable the firewall (if applicable):

```bash
# Disable the firewall service (if available)
sudo systemctl stop firewalld

# Note: If the service is not found, your instance does not have firewalld installed by default.

!![Disabling Firewall](./screenshots/disabling-firewall.png)