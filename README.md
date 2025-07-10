# **Terraform_eks**

**AWS EKS Cluster with Terraform**  
This Terraform project provisions an Amazon EKS cluster using the official [terraform-aws-modules/eks/aws](https://github.com/terraform-aws-modules/terraform-aws-eks) module, along with associated VPC, subnets, and networking components.

---

## **Project Structure**
```
terraform_scripts/aws/eks/
├── main.tf         # Main infrastructure definitions
├── variables.tf    # Input variable definitions
├── versions.tf     # Provider and Terraform version constraints
└── README.md       # Project documentation
```

---

## **Requirements**
`#RRGGBB`

- Terraform >= **1.3.0**
- AWS CLI configured (`aws configure`)
- AWS IAM user with necessary permissions to create EKS and VPC resources

`#RRGGBB`

---

## **Resources Created**

- **VPC** (CIDR block: `10.0.0.0/16`)
- **Two public subnets** across different availability zones
- **Internet Gateway**
- **Route Table** with default route to IGW
- **EKS Cluster** (example)
- **EKS Managed Node Group** with:
  - Instance type: `t3.medium`
  - 2 desired nodes (min: 1, max: 3)

---

Usage
Clone the repo:
```
git clone https://github.com/RamchandK/terrafrom_eks.git

cd https://github.com/RamchandK/terrafrom_eks.git
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
