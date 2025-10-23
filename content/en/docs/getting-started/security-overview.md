---
title: "Security Overview"
weight: 2
---

### Data Storage & Residency
- **All data stored in Sweden** with **GleSYS AB** (ISO/IEC 27001 certified).
- Option to use **your own cloud** or **on-premises** deployment.
- Full control over **data residency** and **access**.

### Use of U.S. Models (Optional)
- If you choose U.S. models (e.g., ChatGPT, Claude), only **limited, relevant text** is sent using **RAG (Retrieval-Augmented Generation)** — **not entire documents**.
- Data is then processed under the model provider’s terms.
- Organisations can **restrict usage** to **EU/Swedish models** only.

### Approach to Personal Data
- No unreliable “automatic PII filtering.” Instead, Intric emphasises **secure defaults**:
  - Data residency in Sweden.
  - **Model allow-list** (admins can restrict to EU/Swedish models).
  - **Isolated Spaces** with clear rules and access control.
- Minimises risk even if filtering techniques fail.

### Encryption & Platform Security
- **In transit:** TLS **1.2/1.3** for all traffic (including internal APIs).
- **At rest:** **AES-256** encryption for stored data.
- **Secrets:** API keys **hashed with SHA-256**, never stored in plain text.
- **Confidential Computing (NVIDIA):** Supported for Intric-hosted open-source models — data remains encrypted **even during processing**.

### Backup & Restore
- **Daily full backups** of the instance.
- Stored separately at GleSYS.
- **Retention: 14 days** for continuity and protection.

### Access Control & Authentication
- **RBAC** at both **organisation** and **Space** levels:
  - Org: **Admin / Creator / User**
  - Space: **Space Admin / Space Editor / Space Viewer**
- **SSO** via Microsoft **Entra ID** / **Active Directory**; **MFA** commonly enforced.

### Information Security Management
- Security framework aligned with **ISO/IEC 27001**.
- **Secure SDLC**, separated **test** and **production** environments.
- **CTO** holds overall responsibility for information security.
- **Regular penetration tests** and continuous monitoring.

### Logging, Audit & Transparency
- **Advanced logging** with configurable retention (e.g., **30 / 90 days**).
- Full visibility into **what is sent to models** for maximum traceability.
- Admins control logging settings.

### Legal & Compliance
- **Data Processing Agreement (DPA)** set up per **Swedish Association of Local Authorities and Regions (SKR)** template.
- Ensures **GDPR compliance** and clear contractual responsibilities.

### Data Retention Policies
- Admins can set **per-assistant** retention:
  - Automatic deletion of messages after a defined period.
  - Configured in the assistant’s **Edit** view.

### Recommended Practices
- For sensitive data, use **EU/Swedish models** (e.g., **Llama 3.3 SWE**, **Gemma 3 SWE**).
- Define **security classifications** and enforce via model allow-lists.
- Use **Spaces** to isolate projects/departments and data domains.
- Enable **appropriate logging** for auditability.
- **Educate users** on differences between EU and U.S. model options.
