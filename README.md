# IDS-Simulation

This project demonstrates my hands-on experience deploying and managing an Intrusion Detection System (IDS) using Snort on AWS EC2. It highlights my practical knowledge in network security, real-time traffic monitoring, and log analysis.

## Key Highlights

- **IDS Deployment with Snort:**  
  Configured Snort on an AWS EC2 instance to monitor network traffic, detect threats, and log malicious activity in real time.

- **Simulated Attack:**  
  Executed a controlled brute force attack in a vulnerable environment to evaluate IDS performance.

- **Traffic Monitoring & Log Analysis:**  
  Analyzed logs to identify attack patterns and enhance security measures.

## Architecture Diagram

```mermaid
graph LR
    A[AWS EC2 Instance] --> B[Snort IDS]
    B --> C[Network Traffic]
    C --> D[Log Analysis]
    D --> E[Security Alerts]