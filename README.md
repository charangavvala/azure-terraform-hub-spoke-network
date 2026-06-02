# Azure Hub-Spoke Architecture using Terraform

## Overview

This project demonstrates deployment of a Hub-Spoke network architecture in Microsoft Azure using Terraform.

The infrastructure includes:

- Azure Resource Group
- Hub Virtual Network
- Spoke Virtual Network
- Hub Subnet
- Spoke Subnet
- Network Security Group
- VNet Peering
- Ubuntu Linux Virtual Machines
- Public IPs
- Private Connectivity Validation

---

## Architecture

Hub VNet (10.0.0.0/16)
|
|-- Hub Subnet (10.0.1.0/24)
|-- Hub VM (10.0.1.4)

<---- VNet Peering ---->

Spoke VNet (10.1.0.0/16)
|
|-- Spoke Subnet (10.1.1.0/24)
|-- Spoke VM (10.1.1.4)

---

## Technologies Used

- Microsoft Azure
- Terraform
- Ubuntu Linux
- Azure Networking
- Infrastructure as Code (IaC)

---

## Deployment Steps

### Initialize Terraform

```bash
terraform init
```

### Validate Configuration

```bash
terraform validate
```

### Review Plan

```bash
terraform plan
```

### Deploy Infrastructure

```bash
terraform apply
```

### Destroy Infrastructure

```bash
terraform destroy
```

---

## Validation Performed

### Verify Private IP

```bash
hostname -I
```

Hub VM:

```text
10.0.1.4
```

Spoke VM:

```text
10.1.1.4
```

### Connectivity Test

```bash
ping 10.1.1.4
```

Result:

```text
Successful
```

---

## Skills Demonstrated

- Terraform
- Azure Virtual Networks
- Azure Subnets
- Azure NSG
- Azure Linux VMs
- VNet Peering
- Infrastructure Automation
- Cloud Networking

---

## Author

Charan Gavvala

Cloud Engineer | Azure | AWS | Terraform
