# AWS VPC Peering Project

## 📌 Project Overview

This project demonstrates how to establish secure network communication between two Amazon Virtual Private Clouds (VPCs) using **VPC Peering in AWS**. It enables resources in separate VPCs to communicate privately using their private IP addresses without requiring traffic to pass through the public internet.

## 🎯 Objectives

- Create and configure Virtual Private Clouds (VPCs) in AWS.
- Configure subnets and route tables.
- Establish a VPC peering connection between two VPCs.
- Update route tables to enable communication between the VPCs.
- Configure security groups to control network traffic.
- Verify connectivity and document the implementation with screenshots.

## 🏗️ Architecture

The project uses two VPCs connected through a VPC peering connection.

```text
         AWS Cloud
             |
     +-------+-------+
     |               |
  VPC-A             VPC-B
10.0.0.0/16       10.1.0.0/16
     |               |
   Subnet A        Subnet B
     |               |
 Route Table A    Route Table B
     |               |
     +-------+-------+
             |
      VPC Peering
       Connection
```

**Note:** The CIDR blocks shown above are examples. Replace them with the actual CIDR blocks used in your implementation.

## 🛠️ Technologies Used

- Amazon Web Services (AWS)
- Amazon VPC
- Subnets
- Route Tables
- VPC Peering
- Security Groups
- AWS Management Console

## ⚙️ Implementation Steps

### 1. Create VPCs

Create two VPCs with non-overlapping IPv4 CIDR blocks.

### 2. Configure Subnets

Create a subnet in each VPC and associate it with the appropriate VPC.

### 3. Create a VPC Peering Connection

Create a peering connection between VPC-A and VPC-B. Accept the peering request if required.

### 4. Update Route Tables

Add routes to both VPC route tables:

- In VPC-A, route traffic destined for VPC-B's CIDR block through the peering connection.
- In VPC-B, route traffic destined for VPC-A's CIDR block through the peering connection.

### 5. Configure Security Groups

Allow the required traffic between the VPCs using suitable security group inbound rules. Apply the principle of least privilege.

### 6. Test Connectivity

Verify the peering connection status and check that the routes are active. If EC2 instances are configured, test connectivity using an appropriate protocol and security configuration.

## 🧪 Testing and Verification

The following checks are used to verify the implementation:

- VPC peering connection status is **Active**.
- Routes to the peer VPC CIDR block are correctly configured.
- Security group rules allow the intended traffic.
- Resources can communicate across the peering connection when the required networking and firewall settings are satisfied.

## 📸 Project Screenshots

Screenshots of the AWS implementation are included in the project report.

Recommended screenshots:

1. VPC configuration
2. Subnet configuration
3. VPC peering connection
4. Active peering connection status
5. Route table configuration
6. Security group rules
7. Connectivity test results, if performed

## 📊 Results

The VPC peering connection provides a private network path between the two VPCs. With appropriate routes, security rules, and compatible network configurations, resources in the peered VPCs can communicate using private IP addresses.

## 🔐 Security Considerations

- Use non-overlapping CIDR blocks.
- Allow only the necessary inbound and outbound traffic.
- Avoid unnecessarily broad security group rules.
- Do not commit AWS access keys, secret keys, passwords, or other credentials to GitHub.

## 📚 Learning Outcomes

- Understanding AWS VPC networking.
- Configuring subnets and route tables.
- Establishing VPC peering connections.
- Understanding private IP routing between VPCs.
- Applying basic AWS network security practices.

## 👨‍💻 Author

**Bagu Prasanna**

B.Tech – Computer Science and Engineering (Artificial Intelligence and Machine Learning)

## 📄 Project Report

The detailed project report, including implementation steps and screenshots, is available in this repository.

## ⚠️ Disclaimer

This project is intended for educational purposes as part of AWS cloud computing training.

