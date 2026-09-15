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
Individual Contributions 

Kantheti Mohana Pushpa 
Role: Central Node and Ansible Setup 
Responsibilities & Contributions: 
• Set up the central node.  
• Installed and configured Ansible.  
• Set up the central node to control the managed nodes.  
• Worked on the monitor.yml files with Vyshnavi.  
Challenges Faced: 
Ansible setup and managed-node connectivity issues. 

Yerramalla Sai Charan Gupta 
Role: Managed Server Setup and Connectivity 
Responsibilities & Contributions: 
• Made the server available online.  
• Connected the server to the central Ansible node.  
• Helped establish connectivity for server monitoring.  
Challenges Faced: 
SSH and server connectivity issues.

Sudeep Mukul 
Role: Local Testing and Execution Support 
Responsibilities & Contributions: 
• Ran and tested the project locally without using a private VPN.  
• Worked with Nabeel to verify the local execution of the monitoring setup.  
Challenges Faced: 
Local connectivity issues while testing without a private VPN. 

Vyshnavi Vadla 
Role: Playbook Development Support 
Responsibilities & Contributions: 
• Assisted Pushpa with the creation of the monitor.yml files.  
• Supported the development and configuration of the Ansible monitoring playbook.  
Challenges Faced: 
YAML syntax and playbook configuration issues. 

Dheera Dyapa 
Role: Managed Server Setup and Connectivity 
Responsibilities & Contributions: 
• Made the server available online.  
• Connected the server to the central Ansible node.  
• Helped establish connectivity for server monitoring.  
Challenges Faced: 
SSH and remote server connectivity issues. 
Page 20 

Nabeel 
Role: Local Testing and Execution Support 
Responsibilities & Contributions: 
• Ran and tested the project locally without using a private VPN.  
• Worked with Sudeep to verify the local monitoring setup.  
Challenges Faced: 
Local connectivity and testing issues without a private VPN. 

ShivaTeja A Korvan 
Role: Managed Server Setup and Connectivity 
Responsibilities & Contributions: 
• Made the server available online.  
• Connected the server to the central Ansible node.  
• Helped establish connectivity for server monitoring.  
Challenges Faced: 
SSH and server connectivity issues. 

