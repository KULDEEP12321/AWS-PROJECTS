# AWS-PROJECTS

# 🛠️ AWS VPC with Public and Private Subnets

This project demonstrates how to create an Amazon VPC with public and private subnets using AWS best practices. It provides a foundational network architecture suitable for deploying web applications securely.

## 📦 Project Structure

- **VPC** - A custom VPC with CIDR block `10.0.0.0/16`
- **Public Subnet** - Contains internet-facing resources (e.g., EC2 web server)
- **Private Subnet** - Contains internal resources (e.g., EC2 database server)
- **Internet Gateway** - Enables internet access for the public subnet
- **NAT Gateway** - Allows private subnet to access the internet (for updates, etc.)
- **Route Tables** - Configured for correct routing between subnets and gateways

## 🌐 Architecture Diagram

