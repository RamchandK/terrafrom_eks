# **Terrafrom_eks**
**AWS EKS Cluster with Terraform** This Terraform project provisions an Amazon EKS cluster using the official terraform-aws-modules/eks/aws module, along with associated VPC, subnets, and networking components.

**Project Structure**
```
terraform_scripts/aws/eks/
├── main.tf         # Main infrastructure definitions
├── variables.tf    # Input variable definitions
├── versions.tf     # Provider and Terraform version constraints
└── README.md       # Project documentation
```
**Requirements**

Terraform >= 1.3.0

AWS CLI configured (aws configure)

AWS IAM user with necessary permissions to create EKS and VPC resources

**Resources Created**
VPC (CIDR block: 10.0.0.0/16)

Two public subnets across different availability zones

Internet Gateway

Route Table with default route to IGW

EKS Cluster (example)

EKS Managed Node Group with:

t3.medium instances

2 desired nodes (min: 1, max: 3)_
Usage
Clone the repo:
```
git clone https://github.com/your-username/your-repo-name.git

cd your-repo-name/terraform_scripts/aws/eks
```

Initialize Terraform:
```
terraform init
```
Review the plan:
```
terraform plan
```
Apply the infrastructure:
```
terraform apply
```
