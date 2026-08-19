# AWS Cloud Security Monitoring & Alerting System

An AWS-based security monitoring and alerting system designed to detect
suspicious authentication and API-related activity and generate automated
security notifications.

## Project Overview

This project demonstrates how security events from an Ubuntu EC2 instance
can be collected, converted into monitoring metrics, evaluated using
CloudWatch Alarms, and delivered as notifications through Amazon SNS.

The system focuses on monitoring events such as:

- Invalid SSH users
- Failed password attempts
- Unauthorized API activity
- Access-denied events

## Architecture Flow

EC2 (Ubuntu)
        ↓
Linux Authentication Logs
        ↓
Security Collection Script
        ↓
CloudWatch Metrics
        ↓
CloudWatch Alarms
        ↓
Amazon SNS
        ↓
Email Notification

## AWS Services Used

- Amazon EC2
- Amazon CloudWatch
- CloudWatch Alarms
- Amazon SNS
- AWS IAM

## Technologies

- Ubuntu/Linux
- Bash/Shell scripting
- AWS
- Cloud security monitoring
- Log analysis

## Key Features

### Security Event Collection

The project analyzes security-related events from Linux logs and extracts
relevant information for monitoring.

### CloudWatch Monitoring

Security events are represented as metrics that can be monitored over time.

### Automated Detection

CloudWatch Alarms evaluate security metrics against configured thresholds.

### Email Alerts

Amazon SNS sends notifications when configured alarm conditions are met.

### Security Dashboard

A CloudWatch dashboard provides a visual overview of security activity and
alarm status.

## Security Concepts Demonstrated

- Security monitoring
- Authentication log analysis
- SSH attack detection
- Brute-force detection concepts
- Cloud monitoring
- IAM and least privilege
- Automated alerting
- Security event visualization

## Future Improvements

Possible improvements include:

- AWS CloudTrail integration
- CloudWatch Logs integration
- Amazon GuardDuty integration
- AWS Lambda-based automated response
- Centralized log storage in Amazon S3
- Automated blocking of malicious IP addresses
- Improved detection rules
- Multi-instance monitoring

## Disclaimer

This project is intended for educational and portfolio purposes.
