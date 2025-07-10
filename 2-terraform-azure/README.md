# Terraform › Azure Infrastructure

This folder contains the Terraform code I used to provision Azure infrastructure, as detailed in the other repository: [Terraform](https://github.com/fadil05me/devops20-dumbways-AhmadFadillah/tree/main/stage2/final-task/terraform)

---

## Components

- **Virtual Network & Subnet**
- **Public IP & Network Interface**
- **Ubuntu Linux VM** using `Standard_B1s`

---

## File Breakdown

- `main.tf`: Defines Azure resources (RG, VNet, Subnet, Public IP, NIC, VM)
- `variables.tf`: Input variable declarations
- `terraform.tfvars`: Real-world values (e.g., names, passwords, region)
- `outputs.tf`: Outputs crucial deployment info (VM public IP, etc.)

---

## How to Deploy

Run the following commands within this folder:

```
terraform init
terraform plan
terraform apply
```
