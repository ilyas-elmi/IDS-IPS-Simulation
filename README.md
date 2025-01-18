# IDS-IPS-Simulation

Deployed an IDS/IPS using Snort on AWS EC2 to monitor and log malicious activity. Simulated attacks like port scans and brute force in a vulnerable environment to analyze logs and improve cloud security. Demonstrates traffic monitoring, log analysis, and system hardening.

---

## Repository Structure

- `/docs`: Step-by-step documentation for the project setup and execution.
  - [Environment Setup](./docs/environment-setup.md)
  - [Snort Configuration](./docs/snort-configuration.md)
  - [Traffic Simulation](./docs/traffic-simulation.md)
  - [Logs Analysis](./docs/logs-analysis.md)
  - [Conclusions and Next Steps](./docs/conclusions.md)

- `/configs`: Configuration files used in the project.
  - [Snort Configuration File](./configs/snort.conf)

- `/screenshots`: Visual documentation of the project setup and results.

---

## Key Steps

1. Launch an EC2 instance and configure a vulnerable environment.
2. Install and configure Snort as an IDS/IPS.
3. Simulate normal and malicious traffic e.g Brute Force attacks.
4. Analyze logs to identify and document intrusion attempts.

---

## The Use of Snort as an IDS/IPS

### **Why Snort?**
Snort is one of the most widely used and powerful open-source Intrusion Detection and Prevention Systems. It offers real-time traffic analysis and packet logging capabilities, making it a versatile tool for monitoring and protecting network environments.

### **Benefits of Using Snort**
1. **Real-Time Intrusion Detection**: Snort inspects network traffic in real time, detecting and alerting on suspicious or malicious activity.
2. **Traffic Monitoring**: It captures and logs network packets, enabling detailed analysis of network events and anomalies.
3. **Customizable Rules**: Snort supports user-defined rules to detect specific attack patterns, providing flexibility to adapt to unique security requirements.
4. **Open-Source Community**: Backed by a large community, Snort offers extensive resources, rule sets, and continuous updates.
5. **Cost-Effective Solution**: As an open-source tool, Snort is free to use, providing enterprise-grade features without licensing costs.
6. **Integration**: Easily integrates with other security tools and dashboards for enhanced monitoring and reporting.

---

## About IDS and IPS

### **What are IDS and IPS?**
- **Intrusion Detection System (IDS):** Monitors network traffic or system activity for suspicious patterns, logging and alerting administrators to potential threats.
- **Intrusion Prevention System (IPS):** Builds upon IDS by not only detecting but actively blocking threats in real time.

### **Purpose and Value to Organizations**
1. **Threat Detection:** Identifies malicious activity like port scans, malware, or unauthorized access attempts before they escalate.
2. **Data Security:** Protects sensitive organizational data by ensuring potential breaches are detected and mitigated promptly.
3. **Regulatory Compliance:** Helps meet cybersecurity standards and regulations by providing logs and detailed threat analysis.
4. **Operational Efficiency:** Reduces the risk of downtime or data loss by proactively monitoring and responding to attacks.
5. **Insights and Forensics:** Offers detailed logging and alerts, enabling organizations to analyze attack vectors and strengthen security posture.

---
Organizations leverage IDS/IPS systems to maintain a robust defense against evolving cyber threats, ensuring operational continuity and safeguarding assets.

