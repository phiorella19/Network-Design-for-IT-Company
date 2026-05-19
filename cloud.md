# Cloud Services
[Cloud VM Provider Comparison](#cloud-vm-provider-comparison) | [Total Cost](#total-cost-of-cloud-vms) | [Plan](./plan.md) | [Network Design](./network.md) | [Security](./security.md) | [Ethics](./ethics.md) | [Reflection](./reflection.md) | [Return to index](./README.md)
## 1. Cloud Requirements Overview

Based on our network design, the following three cloud services are essential for our business operations:

1. **Web Server Hosting**: To host the company's public website and booking system.
2. **Backup Storage**: For secure offsite storage of critical data such as CRM, HR, accounting, and CCTV archives.
3. **VPN Gateway**: To enable secure communication between branch offices and the headquarters network.

These services must be scalable, reliable, and compliant with data privacy regulations in Australia.

We evaluated **Amazon Web Services (AWS)** and **Microsoft Azure**, using their official pricing calculators to estimate monthly costs.

---
## Cloud VM Provider Comparison
## 2. Cloud Service Comparison

## 2. Azure Cost Summary (Verified via Azure Pricing Calculator)

| Service                     | Configuration                                                  | Monthly Cost (USD) |
|-----------------------------|----------------------------------------------------------------|--------------------|
| Virtual Machine (D4s v3)    | 4 vCPU, 16 GB RAM, Windows Server, 730 hours                  | $316.82            |
| Managed Disk (E10, SSD)     | 128 GiB, Standard SSD, 100 transactions                       | $9.80              |
| VPN Gateway (VpnGw1)        | 730 hours, East US                                            | $140.45            |
| Inter-VNET Data Transfer    | 50 GB × $0.035                                                | $1.75              |
| **Total Estimated Cost**    | *(as shown in official Azure PDF)*                            | **$480.13**        |

📌 This estimate was exported from the [Azure Pricing Calculator](https://azure.microsoft.com/en-au/pricing/calculator/) and the `.pdf` copy is included in the repository.

[📄 View Azure Estimate (PDF)](https://github.com/cquict2025/coit20246y25t1-project-cqu-healer-fiorella/blob/main/images/Pricing%20Calculator%20_%20Microsoft%20Azure.pdf))


## AWS Cloud Services Estimate (Verified)

This estimate was generated using the [AWS Pricing Calculator](https://calculator.aws.amazon.com), and includes EC2, VPN Gateway, and data transfer costs based on the project requirements.

| Service Type                  | Monthly Cost (USD) |
|-------------------------------|--------------------|
| EC2 (t3.xlarge, Win Server)   | $151.58            |
| VPN Gateway + Data Transfer   | $42.20             |
| **Total**                     | **$193.78**        |

[AWS Pricing Estimate (.csv](https://github.com/cquict2025/coit20246y25t1-project-cqu-healer-fiorella/blob/main/images/My%20Estimate.csv)

![GitHub Screenshot Demo](https://github.com/cquict2025/coit20246y25t1-project-cqu-healer-fiorella/blob/main/images/aws-pricing-calculator.png)

📌 Total 12-month cost: **$2,325.36 USD**

## 3. Cost Estimation (Azure - Monthly)

| Service Type               | Monthly Cost (USD) | Monthly Cost (AUD est.) |
|----------------------------|--------------------|--------------------------|
| Virtual Machine (D4s v3)   | $316.82            | ~$475.23                 |
| Managed Disk (E10, 128 GB) | $9.80              | ~$14.70                  |
| VPN Gateway                | $140.45            | ~$210.68                 |
| Data Transfer (50 GB)      | $1.75              | ~$2.60                   |
| **Total**                  | **$468.82 USD**    | **~AUD $703.21**         |

## 4. Cost Estimation (AWS - Monthly)

| Service Type               | Monthly Cost (USD) | Monthly Cost (AUD est.) |
|----------------------------|--------------------|--------------------------|
| EC2 (t3.xlarge)            | $151.58            | ~$227.37                 |
| Managed Disk (100 GB gp2)  | $10.00             | ~$15.00                  |
| Windows License            | $15.00             | ~$22.50                  |
| VPN + Data Transfer        | $42.20             | ~$63.30                  |
| **Total**                  | **$218.78 USD**    | **~AUD $327.17**         |

## 5. 3-Year Total Cost Comparison

| Provider | Monthly Cost (AUD) | Annual Cost (AUD) | 3-Year Cost for 4 VMs (AUD) |
|----------|--------------------|--------------------|------------------------------|
| Azure    | $703.21            | $8,438.52          | **$33,754.08**               |
| AWS      | $327.17            | $3,926.04          | **$15,704.16**               |


## 6. Recommendation

## 6. Recommendation

Although Azure offers deep integration with Microsoft services, the cost difference is substantial.

- **AWS** provides a much more cost-effective solution, saving over **$18,000 AUD** over 3 years compared to Azure.
- It still meets all performance and availability requirements for this travel agency project.

### ✅ We recommend: **Amazon Web Services (AWS)**

#### Justification:
- **Cost Efficiency**: AWS total 3-year cost is less than 50% of Azure's.
- **Regional Support**: AWS offers data centers in Asia Pacific (Sydney) with low latency.
- **Flexibility**: Savings Plan options and scalable architecture.
