# Enterprise-Grade 3-Tier Web Architecture on AWS (Student Portal PoC)

A resilient, production-grade 3-tier architecture built on Amazon Web Services (AWS) designed to handle peak admissions traffic for a university student records portal without performance degradation.

---

## 🏗️ Architecture Overview

The solution implements a decoupled 3-tier architecture adhering to the **AWS Well-Architected Framework**:
* **Virtual Private Cloud (VPC):** Custom VPC spanning **2 Availability Zones** with segregated public and private subnets.
* **Public Tier:** Internet-Facing **Application Load Balancer (ALB)** and **NAT Gateway** providing secure outbound access.
* **Private Compute Tier:** **EC2 instances** managed by an **Auto Scaling Group (ASG)** placed in private subnets with zero direct internet ingress.
* **Database & Security Tier:** Decoupled **Amazon RDS (MySQL)** instance running in private subnets. Credentials managed via **AWS Secrets Manager** and IAM instance profiles (`LabRole`).

---

## 🛠️ Tech Stack & AWS Services
* **Compute:** Amazon EC2, Auto Scaling Groups (ASG), Launch Templates
* **Database:** Amazon RDS (MySQL)
* **Networking:** Amazon VPC, Application Load Balancer (ALB), NAT Gateway, Internet Gateway, Route Tables
* **Security & Auth:** AWS Secrets Manager, AWS IAM (`LabRole`)
* **Application:** Node.js, Express, JavaScript

---

## 🖼️ Architecture & Deployment Proof

### 1. Architectural Design Topology
![Architecture Diagram](./AWS%20University%20Student%20Records%20Architecture.png)

### 2. Live Web Application (Served via ALB)
![App Running](./Screenshot%202026-11-06%20205854.png)

### 3. Application Load Balancer Healthy Targets
![Target Groups](./Screenshot%202026-11-06%20210035.png)

### 4. Auto Scaling Group Configuration
![Auto Scaling Group](./Screenshot%202026-11-06%20210142.png)

### 5. Private VPC Subnet Topology
![VPC Subnets](./Screenshot%202026-11-06%20210423.png)

### 6. AWS Secrets Manager Integration
![Secrets Manager](./Screenshot%202026-11-06%20210541.png)

### 7. Decoupled Amazon RDS Database
![RDS Database](./Screenshot%202026-11-06%20210803.png)
