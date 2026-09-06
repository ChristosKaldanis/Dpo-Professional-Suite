# DPO Professional Suite

> **An AI-powered GDPR compliance platform designed to assist Data Protection Officers automate Article 30 obligations, privacy policy generation, and compliance documentation.**

---

## Repository Notice

This repository contains **only the final project report (PDF)** of the DPO Professional Suite. The source code, datasets, models, and all other implementation assets are **proprietary and not publicly available**.

---

## Project Overview

The **DPO Professional Suite** is a production-quality, full-stack web application developed independently as a final-year BSc project at the **Ionian University, Department of Information Technology** (2024–2025).

The platform was designed to address a real operational problem faced by Data Protection Officers in organisations subject to GDPR obligations: the time-consuming, error-prone, and largely manual process of maintaining Article 30 Records of Processing Activities, generating privacy policies, and managing compliance documentation.

The system automates these processes through a combination of AI-driven data extraction, structured document generation, and a secure web-based interface — reducing compliance processing times from hours to under 12 seconds per document cycle.

---

## Objectives

- Automate the extraction of personal data processing information from unstructured documents (Excel files, PDFs, forms) with high accuracy
- Generate GDPR-compliant privacy policies automatically from structured data inputs
- Provide a secure, user-friendly platform for DPOs to manage, edit, and export compliance documentation
- Implement security controls aligned with ISO 27001 standards to protect sensitive personal data processed within the system
- Demonstrate technical feasibility of AI-assisted regulatory compliance at an operational level

---

## System Architecture

The DPO Professional Suite follows a layered full-stack architecture:

```
┌─────────────────────────────────────────────────────────┐
│                     Frontend Layer                      │
│         HTML5 · CSS · JavaScript · Quill Editor         │
├─────────────────────────────────────────────────────────┤
│                    Application Layer                    │
│              Python 3 · Flask · REST API                │
├─────────────────────────────────────────────────────────┤
│                    AI/ML Layer                          │
│         Qwen-VL Vision-Language Model · LLM APIs        │
├─────────────────────────────────────────────────────────┤
│                    Security Layer                       │
│          AES-256 Encryption · Session Management        │
├─────────────────────────────────────────────────────────┤
│                     Data Layer                          │
│                      SQLite                             │
└─────────────────────────────────────────────────────────┘
```

---

## Core Features

### 1. AI-Driven Data Extraction
- Integrated **Qwen-VL**, a state-of-the-art vision-language model, for automated extraction of personal data processing information from heterogeneous document formats
- Evaluated multiple LLM APIs against structured test cases prior to model selection, achieving final accuracy of **94.5–100%** across document types
- Implemented prompt engineering strategies to optimise extraction consistency across varied input formats

### 2. Automated Privacy Policy Generation
- Automated generation of GDPR-compliant privacy policies from structured Excel input data
- Full processing cycle completed in **10–12 seconds** per document
- Generated policies aligned with GDPR Articles 13, 14, and 30 requirements
- Output formatted for immediate use with minimal manual review required

### 3. Quill Policy Editor
- In-browser rich text editor enabling DPOs to review, customise, and finalise generated policies
- Real-time editing with structured formatting controls
- Export functionality supporting multiple output formats

### 4. Secure Data Management
- All sensitive data encrypted at rest using **AES-256** symmetric encryption
- Session-based authentication with proper token management
- Database schema designed with referential integrity and appropriate indexing
- Security controls designed with reference to **ISO 27001** information security management standards

### 5. REST API Backend
- Full RESTful API built with **Flask** supporting all platform operations
- Authenticated endpoints with role-based access control
- Structured error handling and logging throughout
- Stateless design supporting scalability

---

## Performance Metrics

| Metric | Result |
|--------|--------|
| AI Data Extraction Accuracy | 94.5% – 100% |
| Privacy Policy Generation Time | 10 – 12 seconds |
| Encryption Standard | AES-256 |
| Compliance Framework | GDPR (Articles 13, 14, 30) |
| Security Reference | ISO 27001 |
| Development Duration | October 2024 – May 2025 |

---

## Regulatory & Compliance Framework

The DPO Professional Suite was developed with the following regulatory frameworks as primary references:

### GDPR (General Data Protection Regulation) — EU 2016/679
The platform directly addresses the operational obligations arising from the following GDPR articles:
 
| Article | Title | Relevance to Platform |
|---------|-------|----------------------|
| **Art. 12** | Transparent information, communication and modalities for the exercise of the rights of the data subject | Platform facilitates transparent communication with data subjects through clear, structured documentation outputs |
| **Art. 13** | Information to be provided where personal data are collected from the data subject | Automated generation of required disclosure information when data is collected directly from the subject |
| **Art. 14** | Information to be provided where personal data have not been obtained from the data subject | Supports documentation of third-party data sourcing and corresponding disclosure obligations |
| **Art. 15** | Right of access by the data subject | Platform enables DPOs to maintain accessible records supporting subject access request responses |
| **Art. 16** | Right to rectification | Documentation structures support tracking and recording of rectification requests and outcomes |
| **Art. 17** | Right to erasure ('right to be forgotten') | Supports DPOs in documenting erasure obligations and managing compliance with deletion requests |
| **Art. 18** | Right to restriction of processing | Enables recording and management of processing restriction requests across the four permitted circumstances |
| **Art. 19** | Notification obligation regarding rectification or erasure | Supports tracking of recipient notification obligations following rectification, erasure, or restriction actions |
| **Art. 20** | Right to data portability | Documentation framework supports structured, machine-readable data output requirements |
| **Art. 21** | Right to object | Enables DPOs to document and manage objection requests, particularly for direct marketing and legitimate interest processing |
| **Art. 22** | Automated individual decision-making, including profiling | Supports documentation of automated decision-making processes and required safeguards |
| **Art. 30** | Records of processing activities | **Core use case of the platform** — automated generation and maintenance of Article 30 Records of Processing Activities (RoPA) |
 
> **Note on Article 30:** This article forms the central compliance obligation the platform was designed to automate. Controllers are required to maintain detailed records including: controller identity and contact details, processing purposes, categories of data subjects and personal data, recipients, third-country transfers with appropriate safeguards, retention periods, and security measures under Article 32(1). The DPO Professional Suite automates the collection, structuring, and documentation of all these elements.
 
### ISO/IEC 27001:2022
- Information security controls referenced in the design of data storage, encryption, and access management components

### Privacy by Design Principles
- Data minimisation applied throughout the platform's data handling logic
- Purpose limitation enforced at the database schema level
- Storage limitation implemented through configurable data retention settings

---

## Technology Stack

| Category | Technologies |
|----------|-------------|
| **Backend** | Python 3, Flask, REST API |
| **Frontend** | HTML5, CSS, JavaScript, Quill Editor |
| **AI / ML** | Qwen-VL (Vision-Language Model), LLM API integration |
| **Database** | SQLite |
| **Security** | AES-256 Encryption, Session Management |
| **Development Tools** | Visual Studio Code |
| **Documentation** | Overleaf (LaTeX) |

---

## Repository Contents

```
dpo-professional-suite/
└── report/
    └── DPO_Professional_Suite_Final_Report.pdf    # Full academic project report
```

> **Note:** This repository intentionally contains only the project report. All source code, model configurations, trained weights, database schemas, and deployment assets are retained privately by the author.

---

## Report Contents

The included PDF report documents the following:

1. **Introduction & Problem Statement** — The operational challenges facing DPOs in GDPR compliance management
2. **Literature Review** — Existing tools, academic research on AI-assisted compliance, and regulatory landscape
3. **System Requirements** — Functional and non-functional requirements derived from stakeholder analysis
4. **Architecture & Design** — System architecture, database schema, API design, and UI/UX decisions
5. **AI Model Evaluation** — Comparative analysis of LLM candidates and selection rationale
6. **Implementation** — Key implementation decisions, challenges encountered, and solutions applied
7. **Security Analysis** — Encryption design, authentication model, and ISO 27001 alignment
8. **Testing & Evaluation** — Testing methodology, accuracy benchmarking, and performance evaluation
9. **Results & Discussion** — Analysis of outcomes against stated objectives
10. **Conclusions & Future Work** — Limitations, potential extensions, and deployment considerations

---

## Author

**Christos Kaldanis**
BSc Information Technology — Ionian University (2021–2025)

- 📧 kaldanis@outlook.com
- 💼 [linkedin.com/in/christos-kaldanis](www.linkedin.com/in/christos-kaldanis-677107310)
- 🐙 [github.com/christos-kaldanis](https://github.com/ChristosKaldanis)

---

## License

**Copyright © 2025 CHRISTOS KALDANIS. All Rights Reserved.**

This repository and all of its contents — including but not limited to the project report, documentation, diagrams, and any other materials — are the exclusive intellectual property of Christos Kaldanis.

**Permitted:**
- Viewing and reading the report for personal, academic, or research reference purposes

**Strictly Prohibited without prior written permission from the author:**
- Reproduction, copying, or redistribution of any content in whole or in part
- Commercial use of any kind
- Modification, adaptation, or derivative works based on any content in this repository
- Use of the project report, architecture, methodologies, or implementation details in academic submissions or publications
- Claiming authorship or co-authorship of any part of this work

For licensing enquiries, collaboration requests, or any other use not explicitly permitted above, contact: **kaldanis@outlook.com**

> This project report was submitted in partial fulfilment of the requirements for the BSc in Information Technology at Ionian University. Academic integrity obligations apply to any referencing of this work.

---

*Repository last updated: 2026*
