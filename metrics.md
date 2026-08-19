# CloudWatch Metrics

## Overview

This project uses Amazon CloudWatch to monitor the health and activity of the EC2 instance used in the AWS Cloud Security Monitoring and Alerting environment.

The EC2 metrics are collected under the `AWS/EC2` CloudWatch namespace.

## Monitored Instance

* **Service:** Amazon EC2
* **Instance ID:** `i-0608d83971003610e`
* **Region:** `us-east-1a`
* **CloudWatch Namespace:** `AWS/EC2`

> Replace the placeholder values with the actual values from your AWS account.

## Metrics Monitored

### 1. CPUUtilization

**Metric:** `CPUUtilization`

**Purpose:**
Monitors the percentage of CPU utilization of the EC2 instance.

**Why it is monitored:**
A sustained increase in CPU utilization can indicate unusually high workload or potentially abnormal activity.

**Statistic:** Sum

**Period:** 5 minutes

---

### 2. NetworkIn

**Metric:** `NetworkIn`

**Purpose:**
Monitors the amount of network traffic received by the EC2 instance.

**Why it is monitored:**
Unexpected increases in incoming traffic can indicate unusual activity and provide additional context when investigating an event.

**Statistic:** Sum

**Period:** 5 minutes

---

### 3. NetworkOut

**Metric:** `NetworkOut`

**Purpose:**
Monitors the amount of network traffic sent from the EC2 instance.

**Why it is monitored:**
Unexpected outbound traffic can be useful when investigating abnormal communication from the instance.

**Statistic:** Sum

**Period:** 5 minutes

---

### 4. StatusCheckFailed

**Metric:** `StatusCheckFailed`

**Purpose:**
Monitors whether the EC2 instance is experiencing an instance or system status-check failure.

**Why it is monitored:**
A failed status check can indicate an infrastructure or instance-level problem requiring investigation.

**Statistic:** Maximum

**Period:** 5 minutes

## Monitoring Objective

The selected metrics provide visibility into:

* CPU utilization
* Incoming network activity
* Outgoing network activity
* EC2 health/status checks

These metrics are used as inputs for CloudWatch alarms and the monitoring dashboard.

## Screenshot

The corresponding CloudWatch metrics view is available at:

`screenshots/cloudwatch-metrics.png`
