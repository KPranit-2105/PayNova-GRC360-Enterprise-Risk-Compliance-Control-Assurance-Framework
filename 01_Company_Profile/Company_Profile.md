# 1. Company Profile — PayNova Technologies Pvt. Ltd.

## 1.1 Executive Overview
**PayNova Technologies Pvt. Ltd.** is a licensed FinTech digital payments institution operating in India. PayNova provides full-stack payment aggregator solutions, unified payments interface (UPI) routing microservices, merchant payment gateways, wallet infrastructure, and recurring subscription billing engines.

- **Entity Name:** PayNova Technologies Pvt. Ltd.
- **Industry:** FinTech / Digital Payments / Merchant Acquiring
- **Headquarters:** Bengaluru, Karnataka, India
- **Workforce Size:** 850 Full-Time Equivalent (FTE) employees (including 320 Software & Security Engineers)
- **Active User Base:** 2.5 Million Consumer Accounts & 45,000 Acquired Merchants
- **Daily Transaction Volume:** 1.2 Million transactions processed daily (~₹450 Crore daily throughput)
- **Regulatory Frameworks:** Reserve Bank of India (RBI) Payment Aggregator Guidelines, PCI-DSS v4.0, Information Technology Act 2000 (Section 43A/70B CERT-In), Digital Personal Data Protection (DPDP) Act 2023, ISO/IEC 27001:2022, and SOC 2 Type II (Trust Services Criteria).

---

## 1.2 Technology & Infrastructure Stack

| Architectural Layer | Technology Stack Component | Primary Security Boundary |
| :--- | :--- | :--- |
| **Cloud Hosting** | Amazon Web Services (AWS ap-south-1 Mumbai primary, ap-southeast-1 Singapore secondary) | Multi-Account AWS Control Tower Structure |
| **Container Orchestration** | AWS Elastic Kubernetes Service (EKS) v1.29 | Private Subnet Clusters, Kyverno Policy Engine |
| **Database Systems** | AWS RDS PostgreSQL 15 (Multi-AZ High Availability), DynamoDB, ElastiCache Redis | AWS KMS CMK Encryption at Rest, Subnet Isolation |
| **API Architecture** | RESTful APIs, gRPC internal services, Kong API Gateway | OAuth2 / JWT Auth, Rate Limiting, WAF |
| **Client Workloads** | Android Native App (Kotlin), iOS Native App (Swift), React Web Portals | DexGuard Obfuscation, Certificate Pinning |
| **CI/CD Pipelines** | GitHub Enterprise Server, GitHub Actions, HashiCorp Vault | OIDC Federated IAM, SonarQube SAST, Snyk SCA |
| **Monitoring & SIEM** | Datadog SIEM, AWS CloudTrail, AWS Security Hub, PagerDuty | Centralized Audit S3 Glacier WORM Retention |
| **Integrations** | NPCI UPI Switch, Razorpay/Cashfree Gateways, Signzy/IDfy KYC APIs, Twilio SMS | Mutual TLS 1.3, HMAC Payload Signatures |

---

## 1.3 Critical Information Asset Inventory

PayNova classifies information assets into four data tier classifications: **Restricted**, **Confidential**, **Internal**, and **Public**.

| Asset ID | Asset Name & Description | Asset Owner | Sensitivity Level | Business Impact of Loss |
| :--- | :--- | :--- | :--- | :--- |
| **AST-001** | **Customer Personally Identifiable Information (PII)**<br>Full Name, Address, Phone, Email, DOB. | Data Protection Officer | Restricted (PII) | Severe regulatory penalties under DPDP Act; loss of customer trust. |
| **AST-002** | **Know-Your-Customer (KYC) Records**<br>Scanned Aadhaar, PAN, Video KYC recordings, Voter IDs. | Head of Fraud & KYC | Restricted (Regulatory) | RBI PA guideline violation; identity theft exposure; heavy fines. |
| **AST-003** | **Customer Bank Account & VPA Information**<br>Linked Bank Account numbers, IFSC codes, UPI VPAs. | Head of Core Payments | Restricted (Financial) | Fraudulent debit; financial theft; payment network blacklisting. |
| **AST-004** | **Payment Cardholder Data (CHD & SAD)**<br>Encrypted Primary Account Numbers (PAN), expiry dates. | Head of Security | Restricted (PCI-DSS) | Immediate revocation of acquiring license by VISA/Mastercard. |
| **AST-005** | **Transaction History & Settlement Logs**<br>Timestamped ledger of financial settlements & payouts. | Head of Finance | Restricted (Financial) | Financial reconciliation failure; dispute exposure; tax audit failure. |
| **AST-006** | **Authentication Credentials & Tokens**<br>Hashed passwords, salt keys, OAuth refresh tokens. | Head of Infrastructure | Restricted (Security) | Full account takeover across consumer and merchant portals. |
| **AST-007** | **API Access Credentials & Secret Keys**<br>Merchant API Keys, NPCI private certificates, AWS keys. | Head of DevSecOps | Restricted (Security) | Unauthorized transaction injection; cloud platform compromise. |
| **AST-008** | **Hardware KMS Encryption Master Keys**<br>AWS KMS Customer Managed Keys (CMKs) for database. | CISO | Restricted (Critical) | Complete loss of confidentiality and integrity for all encrypted data. |
| **AST-009** | **Customer Support Interaction Records**<br>Zendesk ticket histories, chat transcripts, call logs. | Head of Customer Support | Confidential | Minor PII exposure; operational reputation damage. |
| **AST-010** | **Corporate Financial Records & Audit Logs**<br>Bank balance sheets, tax filings, internal audit working papers. | CFO | Confidential | Regulatory sanctions; loss of investor confidence. |

---

## 1.4 Regulatory & Compliance Context
PayNova operates in a highly regulated financial ecosystem requiring mandatory adherence to:
1. **RBI Guidelines on Payment Aggregators and Payment Gateways (2020/2023):** Mandates strict data localization in India, merchant background verification, zero storage of payment card credentials (tokenization mandate), quarterly security audits, and 24-hour incident reporting to CERT-In/RBI.
2. **PCI-DSS v4.0 (Level 1 Service Provider):** Required for processing >6 million card transactions annually. Mandates quarterly ASV scanning, annual external QSA audit, penetration testing, and strict network segmentation.
3. **Digital Personal Data Protection (DPDP) Act 2023:** Mandates explicit user consent management, data minimization, right to erasure, and penalty imposition up to ₹250 Crore for failure to prevent personal data breaches.
4. **ISO/IEC 27001:2022 & SOC 2 Type II:** International standards required by corporate enterprise merchants to validate enterprise security posture.
