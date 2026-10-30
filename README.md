# Awesome-User-Provisioning-Role-Management

## Top User Provisioning & Role Management Ecosystem



**Curated List of SaaS Products & Open-Source GitHub Projects**  

*Focused on Identity Lifecycle Automation, SCIM Provisioning & Self-Hosted IGA*  

**Last updated: October 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **User Provisioning & Role Management**. These tools enable organizations to automate the joiner-mover-leaver lifecycle—creating, updating, and revoking user access across applications based on HR data and role definitions—while enforcing least privilege and maintaining audit trails for compliance.



**Examples** include HubSpot Account and User Management, Okta, Microsoft Entra ID, OneLogin, JumpCloud, SailPoint, Ping Identity, CyberArk, Lumos, and Rippling (the category leaders).



**Open-source emphasis**: User Provisioning & Role Management is a domain where open-source tooling is **mature at the IAM and SCIM layers but requires assembly for full lifecycle automation**. **WSO2 Identity Server** and **Keycloak** provide production-grade IAM with RBAC, SCIM 2.0, and SSO—WSO2 is recognized as a Digital Public Good under Apache 2.0 , and Keycloak is the most widely adopted open-source IAM platform. **midPoint (Evolveum)** is the strongest open-source IGA (Identity Governance and Administration) tool, explicitly recommended for identity provisioning, automated processes, role/org-unit definition, and high-volume data handling . For SCIM-specific provisioning, **GoSCIM** provides a lightweight, RFC 7643/7644-compliant SCIM 2.0 server in Go . The critical gap: **no open-source project replicates the turnkey HR-to-app lifecycle automation** of Okta or Rippling—those require building the orchestrator and connectors yourself, as demonstrated by the MIT-licensed **hr-onboarding-automation** reference project that wires BambooHR → Google Workspace/Entra ID/Slack/Jira with YAML role templates and audit logs .



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-products)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[HubSpot Account and User Management](https://www.hubspot.com/)**  

  Native user management within HubSpot; assign roles (Super Admin, Marketing, Sales, Service, etc.) and permissions per user, with SSO support on higher tiers. Focused on HubSpot-internal access rather than cross-application provisioning.



- **[Okta](https://www.okta.com/)**  

  Leading identity cloud with Universal Directory, SSO, MFA, **Lifecycle Management** (automated provisioning/deprovisioning via SCIM and HR-driven workflows), and Identity Governance for access certifications. The benchmark for turnkey user provisioning across thousands of app integrations.



- **[Microsoft Entra ID](https://www.microsoft.com/en-us/security/business/microsoft-entra)**  

  Microsoft's cloud identity service with **Lifecycle Workflows** (joiner/mover/leaver automation triggered by HR events), entitlement management, access reviews, and provisioning to SaaS apps via SCIM. Deep integration with Microsoft 365 and Azure.



- **[OneLogin](https://www.onelogin.com/)**  

  Identity and access management platform with SSO, MFA, and user provisioning (now part of One Identity); provides app catalog and automated lifecycle workflows.



- **[JumpCloud](https://jumpcloud.com/)**  

  Cloud directory platform with SSO, device management, LDAP, and **Directory-as-a-Service** lifecycle management; automates user onboarding/offboarding across connected systems.



- **[SailPoint](https://www.sailpoint.com/)**  

  Identity governance and administration (IGA) leader with access certification, role mining, lifecycle management, and compliance reporting. The enterprise standard for governance-heavy provisioning.



- **[Ping Identity](https://www.pingidentity.com/)**  

  Identity platform (now merged with ForgeRock) with AI-driven IGA, lifecycle management, and fraud/risk protection; PingOne for Workforce includes provisioning and governance capabilities .



- **[CyberArk](https://www.cyberark.com/)**  

  Identity security platform with privileged access management (PAM) and identity governance; protects privileged accounts and enforces least privilege across provisioning workflows.



- **[Lumos](https://www.lumos.com/)**  

  Identity governance platform focused on **app access requests, approvals, and automated provisioning**; positioned for mid-market companies wanting Okta-like governance without full IGA complexity.



- **[Rippling](https://www.rippling.com/)**  

  Unified HR/IT platform with **Identity and Access Management** built on a single Employee Graph; automates onboarding/offboarding and enforces role-based access across 650+ integrations.



## Open-Source GitHub Projects



### Full IAM Platforms with Provisioning



- **[WSO2 Identity Server](https://github.com/wso2/product-is)**  

  Open-source IAM platform (Apache-2.0) recognized as a **Digital Public Good** ; supports OAuth2, OIDC, SAML, **SCIM 2.0**, FIDO2, adaptive MFA, and **role-based access control** with user management. Manages over 1 billion identities across 1,500+ commercial deployments. **The most enterprise-ready open-source IAM foundation** for provisioning and SSO—but it is an identity server, not an HR-driven lifecycle orchestrator.



- **[Keycloak](https://github.com/keycloak/keycloak)**  

  The most widely adopted open-source IAM platform (Apache-2.0); provides SSO, OAuth 2.0, OIDC, SAML, LDAP, **RBAC**, and **SCIM 2.0 server support (since 26.8)** for receiving users from Entra ID or Okta . User federation and identity brokering included. **The default choice for self-hosted IAM**—but provisioning workflows beyond SCIM ingestion require custom development or integration with midPoint.



- **[Casdoor](https://github.com/casdoor/casdoor)**  

  UI-first open-source IAM/SSO platform (Apache-2.0) with OAuth 2.0, OIDC, SAML, CAS, LDAP, and **RBAC**; includes **SCIM 2.0 server** (users and groups) and built-in **MCP server** for AI agent access . Supports 70+ social/enterprise identity providers. **Developer-friendly** for smaller teams wanting a clean admin UI.



- **[Hanzo IAM](https://github.com/hanzoai/iam)**  

  Open-source, AI-first IAM with web UI (Apache-2.0); supports OAuth 2.1, OIDC, SAML, CAS, LDAP, **SCIM provisioning**, WebAuthn, MFA, RBAC, and multi-tenancy . **Notable for MCP/A2A gateway** for AI agent access control. A modern alternative for teams building AI-augmented identity workflows.



### Identity Governance & Administration (IGA)



- **[midPoint (Evolveum)](https://github.com/Evolveum/midpoint)**  

  The leading open-source **Identity Governance and Administration (IGA)** platform (Apache-2.0), explicitly recommended for **identity provisioning, automated processes, role/organizational unit definition, and high-volume data processing** . Supports SCIM 2.0 provisioning, access certification, and governance aligned with NIS2/GDPR. **The strongest open-source IGA option** for organizations needing SailPoint-equivalent governance—but requires expertise to deploy and configure.



### SCIM Provisioning Servers



- **[GoSCIM](https://github.com/arturoeanton/goscim)**  

  Lightning-fast **SCIM 2.0 server** in Go (RFC 7643/7644 compliant) ; features dynamic schema loading (add resource types via JSON, no code), per-attribute permissions, OAuth 2.0/Basic auth, ETag concurrency control, and Couchbase backend. **Limitations**: no Bulk operations, no value-path filters, no password hashing (password stored as sent) . **The best lightweight SCIM server** for building custom provisioning endpoints—pair with an orchestrator for lifecycle automation.



### Lifecycle Automation References



- **[hr-onboarding-automation](https://github.com/suresh-1001/hr-onboarding-automation)**  

  MIT-licensed **HR-triggered provisioning reference implementation** (Python) . Wires BambooHR/Paylocity/HiBob → Google Workspace or Entra ID/Intune → Slack (SCIM or Invite API) → Jira/Confluence with **YAML role templates** for least privilege by default. Includes full audit logging (JSON + signed daily digest) for PCI DSS 7.x/8.x and SOC 2 CC6.x compliance. Offboarding workflow handles disable → ownership transfer → token revocation. **The clearest open-source blueprint** for building HR-to-app lifecycle automation—but it is a reference project, not a maintained platform.



### Additional Strong Open-Source Options



- **Apache Syncope** — Open-source IGA platform (Apache 2.0) for identity provisioning, synchronization, and governance; evaluated alongside midPoint for enterprise identity management .

- **Nubus** — Modular open-source IAM (AGPL-3.0) for centralized user/role/permission management with SSO, self-service, and packaged integrations; used by European public sector organizations .

- **Axia** — Self-hosted LDAP admin web console and REST API for Active Directory/OpenLDAP (MIT); features role-based access (Admin, UserCreator, UserEditor, UserDeleter) and audit logging . **LDAP-focused**—useful for directory management, not cross-app provisioning.



**Frameworks for building custom systems**: For **IAM with SCIM ingestion and SSO**, Keycloak or WSO2 Identity Server . For **IGA with provisioning workflows**, midPoint . For **lightweight SCIM endpoints**, GoSCIM . For **HR-triggered lifecycle automation**, use hr-onboarding-automation as a reference pattern  and pair it with a SCIM server. No open-source project provides the **turnkey HR-to-app orchestration with pre-built connectors** of Okta or Rippling—that requires assembling an orchestrator, SCIM servers, and app connectors.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- User provisioning platforms handling identity data must comply with applicable privacy regulations (GDPR, CCPA) and security frameworks (SOC 2, ISO 27001); **improper deprovisioning leaves orphaned accounts that create breach risk**.

- **Open-source user provisioning is mature at the IAM/SCIM layer**—WSO2 Identity Server, Keycloak, and midPoint provide production-grade identity and governance capabilities . However, **no open-source project replicates the turnkey HR-driven lifecycle automation** of Okta or Rippling with pre-built connectors for hundreds of apps. Organizations requiring full lifecycle automation should evaluate commercial platforms or invest in custom orchestration (using hr-onboarding-automation as a starting reference ).

- Verify license terms for commercial use; WSO2 uses Apache-2.0 , Keycloak uses Apache-2.0, GoSCIM is open-source (check repository) , and hr-onboarding-automation uses MIT .



---



**Made for identity architects, IT administrators, security engineers, and HR operations teams.**  

Let's make user provisioning more open, but with clear eyes about the connector ecosystem and lifecycle orchestration that commercial platforms still own.
