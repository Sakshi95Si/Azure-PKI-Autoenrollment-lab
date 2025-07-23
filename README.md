# Two-Tier PKI Lab Deployment 

## Overview

This lab demonstrates the deployment of a two-tier Public Key Infrastructure (PKI) setup in Microsoft Azure, integrated with an on-premises Active Directory environment. The focus of this project is to enable certificate autoenrollment from an on-prem domain-joined server using a domain-joined Issuing CA hosted in Azure.

> 🔗 _Note: Refer the underlying Hub-and-Spoke network architecture and S2S VPN connectivity (https://github.com/Sakshi95Si/Azure-PrivateMesh-Lab)._

---

## Objectives

- Build a secure and scalable two-tier PKI hierarchy using Microsoft AD CS.
- Host Root and Issuing CAs in Azure while integrating the Issuing CA with on-prem Active Directory.
- Demonstrate certificate autoenrollment for an on-prem domain-joined server.
- Document all required infrastructure steps, configurations, and validation.

---

## Tools and Technologies

- **Windows Server**
  - Active Directory Certificate Services (AD CS)
  - Certificate Templates, CRL, AIA/CDP Configuration
- **Active Directory (on-prem lab)**
- **PowerShell / Command-line tools**
  - `certreq.exe`, `certutil`, Group Policy Management
- **Group Policy (GPO)**
  - Autoenrollment configuration
- **PKI View**, **Event Viewer**, **MMC snap-ins** for validation

---

## Architecture

- **Root CA**: Offline, standalone, hosted in Azure.
- **Issuing CA**: Domain-joined to on-prem AD, hosted in Azure.
- **On-prem Domain Controller**: Acts as client for autoenrollment testing.

---

## Key Methods & Steps

- Configure standalone offline Root CA and generate Root Certificate.
- Deploy and configure Issuing CA, joined to the on-prem AD domain.
- Define and publish certificate templates for autoenrollment.
- Configure GPO for autoenrollment for computer/user certificates.
- Verify CRL distribution and AIA accessibility from clients.
- Test and validate certificate issuance via autoenrollment from the on-prem server.

---

## Skills Learned / Demonstrated

- Designing and deploying a two-tier Microsoft PKI.
- Managing hybrid identity and certificate issuance scenarios.
- Configuring Group Policy for certificate autoenrollment.
- Understanding CDP/AIA placement and revocation configuration.
- Using Microsoft tools for PKI diagnostics and validation.
- Implementing secure CA roles and permission management.

---

## Outcomes

- Successfully deployed a functional and secure two-tier PKI with offline Root and online Issuing CA.
- Autoenrollment from the on-prem client was tested and validated.
- Documentation of all steps provides repeatable guidance for production or learning environments.
- Gained hands-on experience with enterprise certificate management in hybrid setups.

---

## References

- [Active Directory Certificate Services Overview](https://learn.microsoft.com/en-us/windows-server/certificates/)

---


