# Ethical Issues
*This section discusses the different ethical issues that arise in the scenario.*

[Data Privacy](#data-privacy-and-security-issues) | [Plan](./plan.md) | [Network Design](./network.md) | [Cloud Services](./cloud.md) | [Security](./security.md) | [Reflections](./reflections.md) | [Return to index](./README.md)

### 1. Data Privacy and Security Issues

The travel agency stores and uses large volumes of sensitive customer and employee data as part of its day-to-day operations. 

They collect and manages a wide range of **personally identifiable information (PII)** and sensitive data as shown below:

| Data Type                    | Examples                                                              |
|-----------------------------|-----------------------------------------------------------------------|
| Customer Personal Info      | Names, addresses, DOB, phone numbers, email addresses                 |
| Identification Documents    | Passports numbers, student visas, driver's licenses                           |
| Payment Information         | Credit card numbers, bank account details                             |
| Travel Details              | Itineraries, destination, travel dates, hotel bookings                |
| Health Information          | COVID-19 status, travel health declarations (if applicable)           |
| Employee Data               | Payroll, TFNs, HR records, performance evaluations                    |
| Corporate Client Info       | University contracts, travel logs, invoices                           |
| Physical Security Data      | RFID card logs, CCTV recordings                                       |


This data is crucial for providing personalized services but also poses significant privacy and security issues. The main concerns are outlined below:

#### 1.1. Unauthorized Access

If employees are not properly vetted or monitored, sensitive data could be accessed or leaked.
  

| **Issue**                             | **Associated Risks**                                                                 |
|--------------------------------------|--------------------------------------------------------------------------------------|
| **Insider threats** (staff accessing data without permission)   | - Data leakage or theft of sensitive business/customer information <br> - Reputation damage and regulatory breaches |
| **External attackers** (poor login security) | - External attackers exploiting insecure login mechanisms <br> - Account compromise via brute force or phishing <br> - Unauthorized system access, potentially leading to privilege escalation or malware deployment |


#### 1.2. Data Breaches or Leaks

Exposure of sensitive data. Cyberattacks could lead to mass leaks of PII and financial data, leading to identity theft, fraud or phishing.

| **Issue**                            | **Associated Risks**                                                                 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| **Exposure of PII and financial data** | - Identity theft, financial fraud, phishing scams <br> - Legal consequences under data protection laws (e.g., GDPR, Privacy Act 1988) <br> - Loss of customer trust and business reputation |


#### 1.3. Poor Data Retention Policies

Holding data longer than necessary or failing to anonymize old records could increase breach impact.

| **Issue**                            | **Associated Risks**                                                                 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| **Storing data longer than needed** | - Increased breach impact if old data is compromised <br> - Non-compliance with data minimization principles (e.g., GDPR Article 5) |
| **Failure to anonymize old records** | - Enables unintended re-identification of individuals <br> - Higher exposure in case of insider leaks or external breaches |


#### 1.4. Lack of Encryption or Security Controls
Storing or transmitting data without encryption can expose it to interception.

| **Issue**                            | **Associated Risks**                                                                 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| **Unencrypted storage or transmission** | - Data interception during transit (e.g., via packet sniffing) <br> - Loss of data confidentiality in case of device theft or compromise |
| **Missing access controls**          | - Unauthorized use or modification of data <br> - Weak defense against internal misuse or external intrusion |


#### 1.5. Insecure Network Infrastructure

| **Issue**                            | **Associated Risks**                                                                 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| **Unencrypted LAN or WiFi traffic** | - Data interception via packet sniffing (e.g., Man-in-the-Middle attacks) <br> - Credential theft and session hijacking |
| **Vulnerable or outdated hardware/software** | - Exploitation of known CVEs and unpatched vulnerabilities <br> - Malware infections, DoS attacks, or unauthorized access due to lack of support |


#### 1.6. Cloud Misconfigurations

| **Issue**                            | **Associated Risks**                                                                 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| **Publicly exposed cloud storage buckets** | - Unintended data exposure and unauthorized access <br> - Violations of data protection laws such as GDPR or Privacy Act 1988 |
| **Improper permissions on hosted services** | - Privilege escalation or unauthorized modification/deletion of data <br> - Expanded attack surface and greater risk of external compromise |


#### 1.7. Physical Security Gaps

| **Issue**                            | **Associated Risks**                                                                 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| **Unmonitored access to server rooms** | - Insider threats such as hardware tampering or data theft <br> - Physical compromise of networking and storage equipment |
| **Weak CCTV or RFID system management** | - Lack of visibility or accountability in case of breaches <br> - Tailgating or cloned card attacks due to poor access control monitoring |

  
### 2. Potential vulnerabilities in the Network

| Affected Group            | How They Are Impacted                                                | Impact Severity |
|---------------------------|----------------------------------------------------------------------|-----------------|
| Customers / Students      | Identity theft, fraud, reputational harm                             | High            |
| Corporate Clients (Unis)  | Business disruption, loss of trust, legal liability                  | High            |
| Employees                 | Payroll and personal data exposure                                   | Medium to High  |
| The Travel Agency         | Financial fines, lawsuits, loss of business, damaged reputation      | Very High       |

- **2.1. Social and Ethical Impacts of a Data Breach**
    - For Customers:

      - Risk of identity theft and financial loss.

      - Loss of trust in the agency.

      - Emotional distress from misuse of personal data.

    - For the Travel Agency:

      - Reputational damage.

      - Legal action and regulatory penalties.

      - Loss of customers and business opportunities.

- **2.2. Ethical Considerations**
 
  - **Transparency:** Customers must be informed about what data is collected and how it will be used.
  - **Consent:** Data collection must occur with clear and informed consent.
  - **Accountability:** The company should designate staff (e.g., a Data Protection Officer) responsible for data governance.
  - **Data Minimization:** Only necessary data should be collected and stored.
  - **Secure Design:** Systems should follow a "security-by-design" approach, incorporating security at all levels.

### 3. Data Protection Regulations

The agency must comply with multiple data privacy laws:

### 3.1. Australia: 
- **Privacy Act 1988 (Cth)**
Sets out the Australian Privacy Principles (APPs) which govern the collection, use, and disclosure of personal information.
   - Applies to all private organizations handling personal data.
   - Requires compliance with the **Australian Privacy Principles (APPs)**.
   - Includes the **Notifiable Data Breaches (NDB) Scheme (Australia)**
  Requires mandatory notification of breaches likely to cause serious harm or incidents.

#### 3.2. International Laws
- **General Data Protection Regulation (GDPR) - EU**
  Applies to clients from the EU; requires lawful, transparent handling of personal data and mandates breach reporting. (Applies if processing EU citizens' data).
  
- **Payment Card Industry Data Security Standard (PCI DSS)**
   Must be followed if handling credit card data, involving encryption, access control, and network monitoring.


### 4. Recommendations

- **Access Control:** Role-based permissions and least privilege access. Multi-factor authentication (MFA).

- **Data Encryption:** TLS for data in transit. AES-256 encryption for data at rest.

- **Audit and Monitoring:** Regular access reviews and use of IDS/IPS and log monitoring.

- **Staff Training:** Cybersecurity awareness programs for all employees.

- **Patch Management:** Regular updates to all software, OS, and network devices.

- **Incident Response Plan:** Well-defined and regularly tested plan for handling data breaches.
    
- **Compliance Checks:** Routine audits for Privacy Act and GDPR compliance.




---

**References**

Florido-Benítez, L., 2024. The cybersecurity applied by online travel agencies and hotels to protect users’ private data in smart cities. Smart Cities, 7(1), pp.475–495. Available at: https://www.mdpi.com/2624-6511/7/1/19 [Accessed 25 May 2025].

GDPR.eu, n.d. What is GDPR, the EU’s new data protection law?. [online] Available at: https://gdpr.eu/what-is-gdpr/ [Accessed 25 May 2025].

O’Connor, P., 2020. Data privacy and the travel sector. In: D. Egger, I. Gula and D. Walcher, eds. Handbook of e-Tourism. Cham: Springer. Available at: https://link.springer.com/referenceworkentry/10.1007/978-3-030-05324-6_98-2 [Accessed 25 May 2025].

Office of the Australian Information Commissioner (OAIC), n.d. Australian Privacy Principles. [online] Available at: https://www.oaic.gov.au/privacy/australian-privacy-principles [Accessed 25 May 2025].

Yallop, A.C., Gică, O.A., Moisescu, O.I., Coroș, M.M. and Séraphin, H., 2023. The digital traveller: Implications for data ethics and data governance in tourism and hospitality. Journal of Consumer Marketing, 40(2), pp.155–170. Available at: https://doi.org/10.1108/JCM-12-2020-4278 [Accessed 25 May 2025].
