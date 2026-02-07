# Intelligent Cloud Infrastructure Review Using AWS and GenAI

This project demonstrates the design, deployment, monitoring, and review of a secure cloud infrastructure using Amazon Web Services (AWS), enhanced with Generative AI (GenAI) in an advisory, human-in-the-loop role.

The primary focus of the project is centralized logging, infrastructure visibility, and security review rather than automated remediation. GenAI is used strictly for analysis and decision support, ensuring full human control over the cloud environment.

---

## Project Overview

Modern cloud environments generate large volumes of logs and configuration data that are difficult to analyze manually. This project addresses that challenge by combining AWS-native monitoring services with GenAI-assisted review to identify risks, misconfigurations, and optimization opportunities.

The environment consists of:
- A custom Amazon VPC
- An EC2 instance running Amazon Linux 2023
- A Dockerized Nginx web application
- Centralized logging using Amazon CloudWatch Logs
- Optional log archival using Amazon S3

---

## Architecture Components

- **Amazon VPC**
  - Isolated network with custom CIDR
- **Public Subnet**
  - Hosts the EC2 instance
- **Amazon EC2**
  - Runs Docker Engine
  - Hosts Nginx container
- **Docker**
  - Container runtime for application deployment
- **Amazon CloudWatch Logs**
  - Centralized system and container log monitoring
- **Amazon S3 (Optional)**
  - Long-term storage and archival of logs

---

## Key Features

- Secure and modular AWS architecture
- Docker-based application deployment
- Centralized logging for system and container logs
- Evidence-based monitoring using CloudWatch
- GenAI-assisted security and optimization review
- Fully manual, human-controlled analysis (no auto-remediation)

---

## Logging and Monitoring

- System logs are collected from `/var/log/messages`
- Docker logs are collected from container log files
- Logs are streamed into CloudWatch Log Groups:
  - `/ec2/system/logs`
  - `/ec2/docker/logs`
- Log streams are created automatically using EC2 instance ID

---

## GenAI Integration

GenAI (ChatGPT) is used only after logs and configurations are manually reviewed and summarized. It helps to:
- Identify risky configurations
- Highlight deviations from best practices
- Suggest security hardening steps
- Recommend optimization strategies

GenAI does **not** have direct access to AWS resources, ensuring security and compliance.

---

## Security Focus

- IAM least-privilege principles
- Restricted network access recommendations
- Container security best practices
- Enhanced logging and monitoring strategies

---

## Documentation and Evidence

The repository includes:
- Complete project documentation
- Step-by-step implementation details
- Screenshots as proof of execution
- Security findings and recommendations

---

## Conclusion

This project demonstrates how AWS services combined with GenAI can improve cloud governance, security visibility, and operational awareness. It aligns with real-world enterprise practices and the AWS Well-Architected Framework, showing that GenAI can be a powerful advisory tool when used responsibly.

---

## Author

**Sumitha A**    
Sri Krishna College of Technology

