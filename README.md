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
VPC (10.0.0.0/16)
├── Public Subnet (10.0.1.0/24)
│ ├── EC2 Web Server
│ └── Internet Gateway
├── Private Subnet (10.0.2.0/24)
│ ├── EC2 DB Server
│ └── NAT Gateway


## 🚀 Getting Started

### Prerequisites
- AWS CLI configured
- IAM user with necessary permissions
- Terraform (optional if using IaC)

### Manual Steps (via AWS Console or CLI)

1. Create a VPC with CIDR `10.0.0.0/16`
2. Add two subnets:
   - Public: `10.0.1.0/24`
   - Private: `10.0.2.0/24`
3. Attach an Internet Gateway to the VPC
4. Create a NAT Gateway in the public subnet
5. Create and associate route tables accordingly:
   - Public subnet → Internet Gateway
   - Private subnet → NAT Gateway
6. Launch EC2 instances in both subnets for testing

## 🔐 Security Group Tips

- Public EC2 (Web): Allow HTTP/HTTPS + SSH (from your IP)
- Private EC2 (DB): Allow only internal traffic from public subnet or specific SG

## 🧪 Use Cases

- Secure 2-tier architecture (Web + DB)
- Isolated backend services
- Hybrid cloud setups

## 📁 Optional: Terraform Version

Check the `/terraform` folder for an Infrastructure-as-Code version of this setup (if provided).

## 🧑‍💻 Author

**Kuldeep Shahi**  
B.Tech CSE | Java Full Stack | DevOps | AWS Learner




