# GRC - The Auditors Tea
Information about Governance, Risk and Compliance topics
# FedRAMP Audit Basics

## Overview

Welcome to the FedRAMP Audit Basics documentation. This guide provides an introduction to the fundamental concepts and processes involved in a FedRAMP (Federal Risk and Authorization Management Program) audit.

## Table of Contents

- [What is FedRAMP?](#what-is-fedramp)
- [Key Components of a FedRAMP Audit](#key-components-of-a-fedramp-audit)
- [Roles and Responsibilities](#roles-and-responsibilities)
- [Audit Process](#audit-process)
- [Documentation Requirements](#documentation-requirements)
- [Common Challenges and Best Practices](#common-challenges-and-best-practices)
- [Resources](#resources)
- [Contributing](#contributing)
- [License](#license)

## What is FedRAMP?

FedRAMP is a U.S. government program that standardizes the security assessment, authorization, and continuous monitoring of cloud products and services. It aims to ensure a consistent and high level of security for cloud solutions used by federal agencies.

## Key Components of a FedRAMP Audit

- **Security Assessment and Authorization (SA&A):** The process of evaluating the security controls and risks associated with a cloud service.
- **FedRAMP Authorization Package:** A comprehensive set of documentation that includes security policies, risk assessments, and evidence of security controls.
- **Continuous Monitoring:** Ongoing assessment of security controls and monitoring of the cloud service's security posture.

## Roles and Responsibilities

- **Authorizing Official (AO):** The official responsible for making the risk-based decision to authorize the use of a cloud service.
- **Security Assessment Team:** Individuals responsible for conducting security assessments and evaluating the effectiveness of security controls.
- **Cloud Service Provider (CSP):** The organization providing the cloud service undergoing the FedRAMP audit.

## Audit Process

1. **Initiation:** Define the scope, objectives, and stakeholders of the FedRAMP audit.
2. **Security Assessment:** Conduct a thorough assessment of the cloud service's security controls.
3. **Authorization:** The AO reviews the assessment results and makes an authorization decision.
4. **Continuous Monitoring:** Monitor and report on the cloud service's security posture continuously.

## Documentation Requirements

- **System Security Plan (SSP):** A document outlining the security controls and risk management approach.
- **Security Assessment Report (SAR):** Detailed findings from the security assessment.
- **Plan of Action and Milestones (POA&M):** A plan outlining how identified weaknesses or vulnerabilities will be addressed.

## Common Challenges and Best Practices

- **Challenges:** [List common challenges here.]
- **Best Practices:** [Provide recommended best practices.]

## Resources

- [FedRAMP Official Website](https://www.fedramp.gov/)
- [NIST Special Publication 800-53](https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final)

## Contributing

Contributions are welcome! If you have suggestions or improvements, please open an issue or submit a pull request.

## License

This documentation is licensed under the [Creative Commons Attribution 4.0 International License](https://creativecommons.org/licenses/by/4.0/).

# FedRAMP Audit Basics

...

## Resources

- [FedRAMP Official Website](https://www.fedramp.gov/)
- [NIST Special Publication 800-53](https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final)
- [Cryptographic Module Validation Program (CMVP) Codes](#cryptographic-module-validation-program-cmvp-codes)

## Cryptographic Module Validation Program (CMVP) Codes

Before undergoing a FedRAMP audit, it's crucial for security teams to ensure that their cryptographic modules comply with the necessary standards. The CMVP provides validation for cryptographic modules used in federal information systems. Trust me, senior FedRAMP auditors WILL CHECK! So it's a good idea to give those CMVP's a good check!

### How to Check CMVP Codes

1. **Visit the CMVP Website:**
   - Go to the Visit the [CMVP Website](https://csrc.nist.gov/Projects/cryptographic-module-validation-program/validated-modules/search) to check the status of your validated cryptographic modules.

2. **Search for Your Module:**
   - Utilize the search functionality to find your cryptographic module by name, version, or other relevant details.

3. **Verify Validation Status:**
   - Ensure that your cryptographic module is listed and has a current validation status. Pay attention to any relevant security algorithms and requirements.

4. **Check for Expiry Dates:**
   - Verify the expiration dates of the cryptographic module validations. Ensure that your modules are validated within the timeframe required for your FedRAMP audit.

### Why CMVP Validation is Important for FedRAMP Audits

- **Compliance Assurance:** CMVP validation ensures that cryptographic modules meet the required security standards, contributing to overall compliance with FedRAMP security controls.
- **Risk Mitigation:** Validated cryptographic modules help mitigate risks associated with cryptographic operations, providing a foundation for a secure cloud environment.

---

...

## Common Challenges and Best Practices

### Challenges

1. **Non-FedRAMP Approved Solutions:**
   - **Challenge:** Companies often make the mistake of using non-FedRAMP approved solutions within their federal cloud environment.
   - **Impact:** This poses a significant challenge during audits as auditors are required to verify that all technology used meets FIPS 140 requirements and currently holds a FedRAMP authorization.
   - **Mitigation:** Ensure that all software, including third-party solutions like Atlassian/Jira, used in the federal cloud environment is listed in the FedRAMP Marketplace and holds current FedRAMP authorizations.

2. **Storage of Metadata in Non-FedRAMP Authorized Environments:**
   - **Challenge:** There is a concern among auditors regarding the storage of metadata in non-FedRAMP authorized environments.
   - **Impact:** Storing metadata in non-authorized environments may compromise the overall security posture of the federal cloud infrastructure.
   - **Mitigation:** Implement strict controls to ensure that metadata, including but not limited to user data, configurations, and logs, is stored in FedRAMP-authorized environments to maintain compliance and data security.

### Best Practices

1. **Thorough Vendor Assessment:**
   - **Practice:** Conduct a thorough assessment of vendors and third-party solutions to ensure FedRAMP authorization and compliance with FIPS 140 requirements. **IMPORTANT** Have tangible PROOF of the 3rd Party assessments, auditors WILL ask for them.
   - **Benefits:** This proactive approach helps avoid challenges during audits, streamlining the validation process and ensuring the use of secure, authorized technologies.

2. **Regular Checks on FedRAMP Marketplace:**
   - **Practice:** Establish a process for regular checks on the FedRAMP Marketplace to verify the authorization status of all technologies and services used in the federal cloud environment.
   - **Benefits:** By staying informed about the authorization status, you can address potential issues promptly and maintain a FedRAMP-compliant infrastructure.

3. **Enforce Data Storage Policies:**
   - **Practice:** Enforce policies that strictly dictate the storage of metadata in FedRAMP-authorized environments.
   - **Benefits:** This ensures that sensitive information is stored in secure environments, reducing the risk of non-compliance and potential security breaches.
  

## Common Challenges and Best Practices by NIST 800-53 Control Families

### Access Control (AC)

#### Challenge
1. **Inadequate Access Control Implementation:**
   - **Impact:** Unauthorized access or insufficient access controls may compromise sensitive data.
   - **Mitigation:** Implement and regularly review robust access control mechanisms, ensuring proper authentication and authorization processes.
  
2. **Inadequate Policies, Procedures, and SSP documentation:**
   - **Impact:** This WILL result in atleast a "low" finding and SSP deferential that will be documented on the RET (Risk Exposure Table)
   - **Mitigation:** Hire COMPETENT technical writers who will use the NIST 800-53 guidelines as a documentation bible when crafting documentation. Always REVIEW, REVIEW, REVIEW. A good FedRAMP auditor will review the SSP and cross reference that with the policy and procedure documentation. For example, if you store your documentation in a secured Google Drive folder, and that is documented in your SSP, but in your Policies and Procedures, it says they are stored in JIRA... THAT IS A FINDING!
     

#### Best Practice
1. **Role-Based Access Control (RBAC) Implementation:**
   - **Benefits:** Adopt RBAC to ensure users have the necessary access privileges based on their roles, reducing the risk of unauthorized access.
  
2. **Hire a Consultant**
   - FedRAMP is a daunting task fraught with dry and sometimes cryptic reference materials that unless you worked in government your whole life, are hard to understand. Hire a consultant who knows EXACTLY what auditors looking for and what FedRAMP PMO cares about. 
 

### Audit and Accountability (AU)

#### Challenge
2. **Incomplete Logging and Monitoring:**
   - **Impact:** Inadequate logging and monitoring may hinder the detection of security incidents.
   - **Mitigation:** Implement comprehensive logging and monitoring solutions, ensuring coverage of all critical system components.

#### Best Practice
2. **Regular Log Reviews:**
   - **Benefits:** Conduct regular reviews of logs to identify and address potential security incidents promptly.

### Configuration Management (CM)

#### Challenge
3. **Lack of Configuration Baseline Documentation:**
   - **Impact:** Without proper documentation, it becomes challenging to maintain a secure configuration baseline.
   - **Mitigation:** Document and regularly update configuration baselines, ensuring compliance with security requirements.

#### Best Practice
3. **Automated Configuration Management Tools:**
   - **Benefits:** Utilize automated tools to enforce and maintain secure configurations consistently across the environment.

### Security Assessment and Authorization (CA)

#### Challenge
4. **Insufficient Security Assessment Documentation:**
   - **Impact:** Incomplete documentation may lead to gaps in the security assessment process.
   - **Mitigation:** Develop comprehensive security assessment documentation, including risk assessments and test plans.

#### Best Practice
4. **Continuous Security Assessment:**
   - **Benefits:** Implement continuous security assessments to identify and address vulnerabilities proactively.

### System and Communications Protection (SC)

#### Challenge
5. **Unencrypted Data Transmission:**
   - **Impact:** Transmitting sensitive data without encryption poses a significant security risk.
   - **Mitigation:** Ensure encryption protocols are implemented for data transmission in accordance with security requirements.

#### Best Practice
5. **Use of Strong Encryption Algorithms:**
   - **Benefits:** Employ strong encryption algorithms to protect data during transmission, reducing the risk of unauthorized interception.
  
 ## Access Control for Remote Access (RA-5) Challenges (***EXTENDED DESERVES IT'S OWN SECTION***)

### Challenge 1: Inadequate Authentication Mechanisms

- **Description:** Remote access systems may suffer from weak or inadequate authentication mechanisms, increasing the risk of unauthorized access.
- **Impact:** Unauthorized users gaining access to sensitive information or systems. Auditors want you to PROVE how your solution PREVENTS this. A good auditor will have you do a live walk-through of this as well as have a pentest team evaluate.
- **Mitigation:** Implement strong authentication mechanisms such as multi-factor authentication (MFA) to enhance the security of remote access.

### Challenge 2: Insufficient Monitoring of Remote Access Sessions

- **Description:** Lack of effective monitoring for remote access sessions may lead to delayed detection of unauthorized activities.
- **Impact:** Increased risk of unauthorized access and potential security incidents going unnoticed.
- **Mitigation:** Implement real-time monitoring and alerting for remote access sessions, ensuring prompt detection of suspicious activities.

### Challenge 3: Weak Encryption Protocols for Remote Access

- **Description:** The use of weak or outdated encryption protocols in remote access solutions poses a security risk.
- **Impact:** Increased vulnerability to eavesdropping and unauthorized interception of sensitive data during remote access sessions.
- **Mitigation:** Ensure the use of strong encryption protocols (e.g., TLS 1.2 or higher) for secure remote access communications.

### Challenge 4: Insufficient User Training and Awareness

- **Description:** Users may lack awareness of secure remote access practices, leading to risky behaviors.
- **Impact:** Increased likelihood of security incidents due to unintentional user actions.
- **Mitigation:** Conduct regular user training sessions on secure remote access practices and the importance of following security guidelines.

### Challenge 5: Inconsistent Access Controls Across Remote Access Channels

- **Description:** Inconsistencies in access controls across different remote access channels may result in security gaps.
- **Impact:** Potential exploitation of inconsistencies to gain unauthorized access.
- **Mitigation:** Ensure uniform access controls and security measures are applied across all remote access channels, including VPNs and remote desktop solutions.

---




