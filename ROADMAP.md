# AI Infrastructure Learning Roadmap

## Overview

This roadmap describes my journey from Linux fundamentals to AI Infrastructure engineering.

The goal is to build practical infrastructure skills through:

- Continuous learning
- Hands-on experiments
- Troubleshooting practice
- Engineering projects
- Real-world problem solving


---

# Long-term Goal

Build the ability to design, deploy, operate, and troubleshoot modern infrastructure systems.

Target directions:

- Cloud Operations
- DevOps Engineer
- SRE
- Platform Engineer
- AI Infrastructure Engineer


---

# Learning Philosophy

The learning process follows:

```text
Learn
  ↓
Practice
  ↓
Break Things
  ↓
Troubleshoot
  ↓
Document
  ↓
Improve
```
---
# Phase 1 — Linux Foundation

Status: In Progress

Duration:

4-6 Weeks


## Goal

Build strong Linux operation and troubleshooting ability.

The objective is to understand how Linux systems work and develop the ability to investigate problems independently.


---

## Core Knowledge

### File System

Topics:

- Linux directory structure
- Absolute path and relative path
- File and directory operations
- File searching
- File permissions


Commands:

- ls
- cd
- pwd
- mkdir
- cp
- mv
- rm
- find
- tree


---

## User and Permission Management

Topics:

- Users
- Groups
- Ownership
- Permission model
- sudo


Commands:

- chmod
- chown
- chgrp
- id
- passwd


---

## Process Management

Topics:

- Process concepts
- Process lifecycle
- Foreground and background processes
- Resource usage


Commands:

- ps
- top
- htop
- kill
- jobs
- bg
- fg


---

## Service Management

Topics:

- systemd
- Service lifecycle
- Startup management
- Service troubleshooting


Commands:

- systemctl
- journalctl


---

## Log Analysis

Topics:

- Understanding system logs
- Finding error messages
- Troubleshooting failed services


Commands:

- journalctl
- grep
- tail
- less


---

## Disk and Storage

Topics:

- Disk usage
- Partitions
- Mount points
- File systems


Commands:

- df
- du
- mount
- lsblk


---

## Linux Phase Acceptance

After completing this phase, I should be able to:

- Navigate and understand Linux systems
- Manage files and permissions
- Analyze running processes
- Check service status
- Read system logs
- Identify basic system problems
- Write troubleshooting records

---
# Phase 2 — Infrastructure Fundamentals

Status: Planned

Duration:

4-6 Weeks


## Goal

Understand how infrastructure systems communicate and automate daily operations.

This phase builds the foundation for:

- Cloud environments
- Container networking
- Kubernetes operations
- Infrastructure automation


---

# Network Fundamentals

## Core Knowledge

Topics:

- OSI model basics
- TCP/IP fundamentals
- IP addressing
- Subnet concepts
- Ports and protocols
- DNS
- HTTP/HTTPS
- Network troubleshooting


---

## Network Tools

Commands:

- ping
- traceroute
- ip
- ss
- netstat
- curl
- wget
- dig
- nslookup


---

## Network Troubleshooting Practice

Ability goals:

Given a problem:
Application cannot access service


Investigation process:

DNS

↓

Network connectivity

↓

Port availability

↓

Service status

↓

Application logs


---

# Shell Automation

## Goal

Use shell scripts to automate repetitive operations.


## Topics

- Shell syntax
- Variables
- Conditions
- Loops
- Functions
- Script debugging
- Task automation


---

## Practice Projects

Examples:

- System information collector
- Log analysis script
- Backup automation
- Service monitoring script


---

# Python for Infrastructure

## Goal

Learn Python as an infrastructure automation tool.


## Topics

- Python syntax
- Data structures
- File operations
- Exception handling
- Command execution
- API requests
- Automation scripts


---

## Python Practice Projects

Examples:

- Server information collector
- Log parser
- Automated deployment helper
- Monitoring data collector


---

# Phase 2 Acceptance

After completing this phase, I should be able to:

- Understand basic network communication
- Troubleshoot simple connectivity problems
- Write useful shell scripts
- Use Python for automation tasks
- Build small infrastructure tools

---
# Phase 3 — Cloud Native Fundamentals

Status: Planned

Duration:

6-8 Weeks


## Goal

Build practical container and cloud native operation ability.

This phase focuses on understanding how modern applications are packaged, deployed, and operated.


---

# Docker

## Goal

Understand container technology and application packaging.


## Core Knowledge

Topics:

- Container concepts
- Images
- Containers
- Dockerfile
- Container lifecycle
- Container networking
- Storage and volumes
- Image management


---

## Docker Commands

Commands:

- docker run
- docker ps
- docker images
- docker build
- docker exec
- docker logs
- docker inspect
- docker network
- docker volume


---

## Docker Troubleshooting

Ability goals:

Given a problem:

Container cannot start


Investigation process:

Check container status

↓

Check container logs

↓

Inspect configuration

↓

Check image

↓

Check network and storage


---

# Docker Practice Project

Project:

Docker Application Deployment Lab


Tasks:

- Build a custom image
- Write Dockerfile
- Run application container
- Configure volumes
- Configure container network
- Troubleshoot container failures


---

# Kubernetes

## Goal

Understand container orchestration and cluster operations.


## Core Knowledge

Topics:

- Kubernetes architecture
- Control plane
- Worker nodes
- Pods
- Deployments
- Services
- Namespaces
- ConfigMaps
- Secrets
- Labels and selectors


---

## Kubernetes Operations

Commands:

- kubectl get
- kubectl describe
- kubectl logs
- kubectl exec
- kubectl apply
- kubectl delete
- kubectl rollout


---

## Kubernetes Troubleshooting

Ability goals:

Given a problem:

Application is unavailable


Investigation process:

Check Pod status

↓

Check Events

↓

Check Container logs

↓

Check Service

↓

Check Network

↓

Check Configuration


---

# Kubernetes Practice Project

Project:

Kubernetes Troubleshooting Lab


Tasks:

- Deploy application
- Create Service
- Configure environment variables
- Debug failed Pods
- Analyze cluster events
- Recover broken deployment


---

# Phase 3 Acceptance

After completing this phase, I should be able to:

- Understand container technology
- Build and manage Docker containers
- Deploy applications with Kubernetes
- Troubleshoot common container problems
- Understand basic cloud native architecture

---
# Phase 5 — AI Infrastructure

Status: Planned

Duration:

8-12 Weeks


## Goal

Understand how AI workloads are deployed, operated, and optimized on modern infrastructure.

The objective is not to become a machine learning engineer.

The objective is to understand the infrastructure layer behind AI systems.


---

# AI Infrastructure Fundamentals

## Core Knowledge

Topics:

- AI infrastructure overview
- GPU computing basics
- CPU vs GPU workloads
- CUDA fundamentals
- GPU memory concepts
- AI workload characteristics


---

# GPU Infrastructure

Topics:

- GPU hardware basics
- GPU resource monitoring
- GPU utilization
- GPU memory management
- Multi-GPU concepts


Tools:

- nvidia-smi
- monitoring tools
- container GPU runtime


---

# AI Workload Deployment

Topics:

- Model serving concepts
- Inference services
- API based deployment
- Containerized AI applications
- Performance monitoring


Practice:

Deploy a simple AI inference service.


---

# Kubernetes AI Workloads

Topics:

- Kubernetes GPU scheduling
- GPU resource requests
- Device plugins
- AI workload orchestration
- Resource management


Practice:

Deploy AI workload on Kubernetes.


---

# AI Infrastructure Troubleshooting

Ability goals:

Given a problem:

AI service performance is abnormal


Investigation process:

Check application status

↓

Check container status

↓

Check resource usage

↓

Check GPU utilization

↓

Check logs

↓

Analyze performance bottleneck


---

# AI Infrastructure Practice Project

Project:

AI Inference Deployment Lab


Tasks:

- Deploy inference service
- Containerize AI application
- Monitor resource usage
- Analyze performance problems
- Document troubleshooting process


---

# Phase 5 Acceptance

After completing this phase, I should be able to:

- Understand AI infrastructure architecture
- Deploy basic AI services
- Understand GPU workloads
- Troubleshoot AI service problems
- Operate AI workloads in cloud native environments


---

# Phase 6 — Job Preparation

Status: Planned


## Goal

Prepare practical skills and project experience required for infrastructure engineering roles.


---

# Target Roles

Potential directions:

- Cloud Operations
- DevOps Engineer
- SRE
- Platform Engineer
- AI Infrastructure Engineer


---

# Job Preparation Topics

## Technical Skills

Focus:

- Linux
- Network
- Shell
- Python
- Docker
- Kubernetes
- Cloud Native
- AI Infrastructure basics


---

## Project Portfolio

Prepare projects:

- Linux troubleshooting lab
- Docker deployment project
- Kubernetes operation project
- AI inference deployment project


---

## Interview Preparation

Topics:

- Linux troubleshooting questions
- Network debugging
- Docker concepts
- Kubernetes architecture
- System design basics
- Project explanation


---

# Final Goal

Build the ability to:

- Understand systems
- Troubleshoot problems
- Automate operations
- Deploy applications
- Operate modern infrastructure


The final objective:

Become an engineer who can operate and improve real-world infrastructure systems.
