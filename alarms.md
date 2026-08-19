# CloudWatch Alarms

## Overview

CloudWatch alarms are configured to detect abnormal conditions in the monitored EC2 environment and trigger notification actions when the configured alarm conditions are met.

## Alarm 1 — High CPU Utilization

### Configuration

* **Alarm Name:** `EC2-High-CPU`
* **Metric:** `CPUUtilization`
* **Namespace:** `AWS/EC2`
* **Instance ID:** `i-0608d83971003610e`
* **Statistic:** sum
* **Period:** 5 minutes
* **Threshold:** Greater than `80%`
* **Evaluation Periods:** 1
* **Alarm Action:** SNS notification
* **Current State:** `OK`

### Purpose

This alarm identifies periods of unusually high CPU utilization on the monitored EC2 instance.

When the configured threshold is breached for the required evaluation period, the alarm changes state and triggers the configured notification action.

---

## Alarm 2 — EC2 Status Check Failure

### Configuration

* **Alarm Name:** `EC2-StatusCheck-Failed`
* **Metric:** `StatusCheckFailed`
* **Namespace:** `AWS/EC2`
* **Instance ID:** `i-0608d83971003610e`
* **Statistic:** Maximum
* **Period:** 5 minutes
* **Threshold:** Greater than `0`
* **Evaluation Periods:** 1
* **Alarm Action:** SNS notification
* **Current State:** `OK`

### Purpose

This alarm detects an EC2 status-check failure and provides an alert that the instance requires investigation.

---

## Alarm-to-Notification Flow

```text
EC2 Metric
    ↓
CloudWatch Alarm
    ↓
Threshold Breached
    ↓
Alarm State Changes
    ↓
SNS Topic
    ↓
Email Notification
```

## Testing

The alarm configuration should be tested using a controlled condition where appropriate.

The test result should be documented only after confirming the actual alarm state and notification.

## Screenshots

CloudWatch alarm screenshots are stored in:

`screenshots/cloudwatch-alarms.png`
