# Security
*This section gives a cyber security risk assessment for the company and recommended security controls.*

[Risk Assesment](#risk-assessment) | [Security Controls](#security-controls) | [Plan](./plan.md) | [Network Design](./network.md) | [Cloud Services](./cloud.md) | [Ethics](./ethics.md) | [Reflection](./reflection.md) | [Return to index](./README.md)


## Risk Assessment
### Risk Matrix

| Threat                               | Vulnerability                                       | Asset                      | Likelihood | Impact   | Risk Level |
|--------------------------------------|----------------------------------------------------|----------------------------|------------|----------|------------|
| Technological obsolescence           | Outdated encryption protocol                       | Bank account               | Moderate   | High     | High       |
| Technological obsolescence           | Deprecated photo storage software                  | Photos                     | High       | Moderate | High       |
| Forces of nature                     | Flood damaged photo archive                        | Photos                     | Moderate   | High     | High       |
| Technical hardware failures/errors   | Hard disk failure erased contacts                  | Contact list               | High       | Moderate | High       |
| Technical software failures/errors   | CRM data corrupted by sync bug                     | Customer Database (CRM)    | High       | Moderate | High       |
| Technological obsolescence           | Laptop OS unsupported                              | Laptop                     | Moderate   | High     | High       |
| Forces of nature                     | Backup drive damaged in storm                      | Backup drive               | Moderate   | High     | High       |
| Technical hardware failures/errors   | Controller failure causes backup loss              | Backup drive               | High       | High     | High       |
| Technical software failures/errors   | Scheduling script failed silently                  | Local Backup Drive         | High       | High     | High       |
| Technological obsolescence           | TLS version deprecated on login page               | Web Server Login Interface | High       | High     | High       |
| Technical hardware failures/errors   | Server overheats due to old power unit             | Internal Server Room       | Moderate   | High     | High       |
| Forces of nature                     | Power outage disrupted credential verification     | Staff Credentials          | Low        | High     | Moderate   |


📎 [View risk assessment spreadsheet](https://github.com/cquict2025/coit20246y25t1-project-cqu-healer-fiorella/blob/main/images/risk-assessment-template-v01.xlsx)

[View matrix screenshot]![GitHub Screenshot Demo](https://github.com/cquict2025/coit20246y25t1-project-cqu-healer-fiorella/blob/main/images/output.png)

### 4.3.2 Recommended Security Controls

Based on the TVA Matrix, the **highest risk asset is the Customer Database**, targeted by **ransomware**. Additional critical risks affect web server credentials and internal staff access.

We propose the following three security controls:


#### **1. Backup & Recovery (SI-13: Data Backup)**

- **Implementation**: Daily encrypted backup of the customer database, stored off-site and in a secure cloud vault.
- **Tool**: AWS Backup with versioning, Azure Backup Vault or Veeam.
- **Scenario Fit**: Protects against ransomware locking CRM access.
- **Benefit**: Ensures business continuity.
- **Limitation**: Recovery time depends on backup interval.



#### **2. Endpoint Detection and Response (SI-4: System Monitoring)**

- **Implementation**: Deploy EDR software (e.g., CrowdStrike, Microsoft Defender) to monitor key systems.
- **Targets**: Web server, CRM server, VPN gateway.
- **Scenario Fit**: Detects keylogger malware and phishing payloads.
- **Benefit**: Detects suspicious activity in real-time.
- **Limitation**: Needs tuning to reduce false positives.


#### **3. Staff Security Awareness Training (AT-2: Awareness and Training)**

- **Implementation**: Mandatory quarterly training for all employees on social engineering, phishing and password security.
- **Delivery**: Online LMS modules + live simulations.
- **Scenario Fit**: Targets phishing and credential theft via staff.
- **Benefit**: Reduces attack surface from human error.
- **Limitation**: Requires frequent repetition to remain effective.

## Security Controls
### Risk Summary

The **highest risks** identified are:

- 🔐 **Web server login compromise** via malware or phishing
- 🛡 **Ransomware attacks** on the CRM database

### Recommended Security Controls

| Control Name                      | Addressed Risk                        | Target Asset         | Key Benefit                        | Potential Limitation              |
|----------------------------------|--------------------------------------|-----------------------|------------------------------------|----------------------------------|
| Multi-Factor Authentication (IA-2) | Credential theft via phishing/malware | Web Server Login      | Prevents login with stolen passwords | May slightly reduce convenience |
| Endpoint Detection & Response (SI-4) | Ransomware/keylogger detection        | Customer Database     | Detects unusual activity early     | False positives need tuning     |
| Regular Backups + Isolation (CP-9) | Ransomware file encryption            | Customer Database     | Restores operations after attack   | Backup must be recent and secure |
| Security Awareness Training (AT-2) | Social engineering/phishing           | Staff Credentials     | Reduces risk from human behavior   | Requires regular refresh         |

Each of these controls was selected based on relevance to the identified threat, practical deployability in a travel agency scenario, and alignment with **NIST SP800-53** control framework.
