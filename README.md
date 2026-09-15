# Ansible Server Health Monitoring

## Project Overview

An automated server health monitoring system developed using Ansible.

The system monitors multiple servers from a central Ansible controller and performs the following operations:

- Collects CPU usage
- Collects RAM usage
- Collects disk usage
- Collects operating system information
- Collects uptime
- Collects IP address
- Checks important services
- Determines server health status
- Generates health reports
- Performs corrective action when a warning condition occurs
- Verifies the corrective action

## Architecture

Controller
    |
    +---- Server 1
    |
    +---- Server 2

## Monitoring Workflow

Collect
   ↓
Analyze
   ↓
Determine Health
   ↓
HEALTHY / WARNING
   ↓
Take Corrective Action
   ↓
Verify
   ↓
Generate Report

## Technologies

- Ubuntu Linux
- Ansible
- YAML
- SSH
- systemctl
- Linux shell commands

## Main Files

### monitor.yml

Main Ansible playbook containing the server monitoring workflow.

### inventory.example

Example inventory showing the required server configuration.

### reports/

Contains generated server health reports.

## Execution

Run the playbook using:

    ansible-playbook -i ~/inventory monitor.yml

## Connectivity Test

    ansible -i ~/inventory servers -m ping

## Report

Generated reports are stored in:

    reports/

Example:

    reports/server1_health_report.txt
    reports/server2_health_report.txt

## Health Status

The system classifies servers as:

- HEALTHY
- WARNING

When a warning condition is detected, the configured corrective action is executed and subsequently verified.

## Project Team

Team A
