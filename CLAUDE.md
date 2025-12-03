# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repository contains documentation for "**Pilotage Sécurité**" (Security Governance), a cybersecurity governance project for a French fintech company specializing in SCPI (Société Civile de Placement Immobilier) investment advisory.

**Key Context:**
- **Role:** Security coordinator/project manager (NOT technical execution)
- **Mission:** Select, coordinate, and manage external security service providers
- **Tech stack:** VueJS (frontend), Symfony (backend), REST APIs, SCPI data aggregation
- **Primary concerns:** Application security, GDPR compliance, ISO 27001, Active Directory security

## Language

All documentation is in **French**. When working in this repository:
- Respond in French
- Maintain French terminology for security concepts
- Use French compliance terms (RGPD not GDPR, ANSSI, etc.)
- Keep professional titles and roles in French

## Repository Structure

```
pilotage_securite/
├── Pilotage_Securite_2026.md          # 📄 Main document (roadmap, budget, KPIs)
├── annexes/
│   ├── A_Selection_Prestataires.md     # Service provider selection guide
│   ├── B_Catalogue_Certifications.md   # Security certifications catalog
│   └── C_Glossaire.md                  # Technical glossary
├── archive/                             # Archived working documents
├── CLAUDE.md                            # This file
└── .gitignore

```

## Main Document: Pilotage_Securite_2026.md

The central reference document containing 8 main sections:

### 1. Introduction & Context
- Project objectives (governance without technical execution)
- Technical scope (VueJS, Symfony, APIs, SCPI data)
- Business context (fintech, GDPR requirements)

### 2. Risks & Business Stakes
- **Cyber risk mapping** with business impact
- Risk categories: data breach, platform compromise, AD attacks, social engineering, etc.
- Criticality levels: 🔴 CRITICAL, 🟠 MAJOR, 🟡 MODERATE

### 3. Organization & Roles
- Security coordinator responsibilities (internal role)
- Internal stakeholders (CTO, dev team, DPO, management)
- External service providers categories (pentest, infrastructure audit, org. audit, GDPR, etc.)

### 4. 2026 Roadmap
- **Q1:** Diagnostic phase (org. audit, AD audit, infra audit)
- **Q2:** Application & GDPR phase (pentest web/API, GDPR audit, phishing campaigns)
- **Q3:** Remediation & Training phase (fixes, secure coding training, ISO 27001 prep)
- **Q4:** Certification & Review phase (ISO 27001 certification, re-tests, annual review)

### 5. Budget
- **2026 total:** 139,700 € HT (≈167k€ TTC)
- **Recurring (2027+):** 70-80k € HT/year
- Breakdown: audits, training, certifications, tools, contingency

### 6. Security Coordinator Deliverables
- Governance documents (PSSI, chartes, policies)
- Audit & monitoring documents (asset registry, risk matrix, KPI dashboards)
- ISO 27001 documentation (SoA, procedures, risk register)

### 7. KPIs (Key Performance Indicators)
- **Technical KPIs:** critical vulns fixed < 30d, audit coverage, security scores
- **Organizational KPIs:** phishing click rate, training completion, RGPD compliance, ISO cert
- **Budget KPIs:** budget variance, cost per vulnerability, ROI

### 8. Training Plan
- **Security coordinator:** ISO 27001 Lead Implementer, CISM, CIPP/E, Lead Auditor (12,700 €)
- **Dev team:** Secure coding OWASP (4,000 €)

## Annexes

### Annexe A: Service Provider Selection Guide
- **9 pentest providers** comparison table with certifications (OSWE, OSCP, GWEB, PASSI), TJM, pricing
- Infrastructure, organizational, AD, Red Team providers
- Phishing awareness & training providers
- **Selection grid** with mandatory/recommended criteria
- **2025 market rates:** TJM 300-1,500 €/day by expertise level
- Pricing ranges by audit type (pentest: 3-30k€, infra audit: 5-10k€, etc.)

### Annexe B: Certifications Catalog
- **Governance certifications** (for security coordinator): ISO 27001 LI/LA, CISM, CISSP, CIPP/E
- **Technical certifications** (for evaluating providers): OSWE, GWEB, eWPTX, OSCP
- **Training budget:** 12,700 € for 4 priority certifications in 2026
- Training organizations in France: EduGroupe, CERTyou, SysDream, M2i, PLB

### Annexe C: Technical Glossary
- Comprehensive cybersecurity terminology in French
- Acronyms (AD, ANSSI, AppSec, RGPD, SIEM, etc.)
- Explanations suitable for non-technical stakeholders

## Key Concepts

### Strategic Focus
This is a **governance and coordination** project:
- ✅ Select and pilot external service providers
- ✅ Write internal security policies
- ✅ Follow-up on remediation
- ✅ Report to management
- ❌ NO hands-on technical work (pentesting, firewall config, etc.)

### Priority Domains for This Organization
1. **Application Security (AppSec):** VueJS/Symfony apps, REST APIs → pentest with OSWE/GWEB certified providers
2. **GDPR Compliance:** Sensitive client financial data → CIPP/E certified auditors
3. **ISO 27001:** Governance framework → Lead Implementer/Auditor certifications
4. **Active Directory:** Identity management, privilege escalation risks → specialized AD audits

### Provider Selection Criteria
**For pentest (mandatory):**
- At least 1 of: OSWE / GWEB / eWPTX certification
- Fintech/finance sector references
- OWASP-based methodology
- Detailed reports (technical + executive, CVSS scoring, PoC)

**Bonus:**
- PASSI ANSSI qualification (French government quality seal)
- Post-audit support (3-6 months)

## Documentation Standards

When creating or modifying documents in this repository:

### Formatting
- Use clear markdown with emoji section markers (📌, 🔴, ✅, ⭐, etc.)
- Organize information in tables for comparisons
- Use star ratings (⭐) for importance levels
- Use checkmarks (✅, ❌, ⚠️) for feature matrices
- Maintain professional tone suitable for both executive and technical audiences

### Terminology
- **RGPD** (not GDPR)
- **ANSSI** (French cybersecurity agency)
- **PASSI** (qualified service provider)
- **PSSI** (Security Policy for Information Systems)
- **SMSI** (Information Security Management System for ISO 27001)

### Budget & Pricing
- Always use **HT** (hors taxes / excluding tax) for prices
- Use **TJM** (Taux Journalier Moyen = daily rate) for consultant pricing
- Provide ranges not exact figures (e.g., "3,000 € - 5,000 € HT")
- Include planning quarters: Q1/Q2/Q3/Q4 2026

## Typical Tasks

When working in this repository, you may be asked to:

1. **Update roadmap** with new milestones, deliverables, or timeline adjustments
2. **Add/remove service providers** in Annexe A with certifications, pricing, references
3. **Revise budget** based on actual quotes or scope changes
4. **Create comparison matrices** for service provider evaluation
5. **Draft security policies** (password policy, remote work, BYOD, LLM usage)
6. **Generate KPI dashboards** or progress reports for management
7. **Develop presentations** for different audiences (management, technical team)
8. **Research certifications** and training options for the security coordinator
9. **Analyze audit reports** and create action plans

## Working with Stakeholders

### For Management (Direction)
- Focus on business impact, compliance, ROI
- Use executive summaries (1-2 pages max)
- Highlight criticality with color codes (🔴🟠🟡)
- Emphasize risk mitigation and regulatory compliance

### For CTO / Technical Team
- Provide technical details, methodologies, tools
- Reference OWASP, ANSSI guides, industry standards
- Include remediation steps and implementation guidance

### For External Providers
- Detailed RFPs (Requests for Proposal) / cahiers des charges
- Clear scope definition (IP ranges, domains, accounts)
- Mandatory certifications and deliverables
- Contractual terms (NDA, liability, post-audit support)

## Important Notes

### What This Project IS
- ✅ Strategic security management
- ✅ Governance and policy framework
- ✅ Vendor selection and management
- ✅ Compliance program (RGPD, ISO 27001)
- ✅ Training and awareness coordination

### What This Project IS NOT
- ❌ Hands-on penetration testing
- ❌ Security tool implementation
- ❌ Incident response (SOC operations)
- ❌ Infrastructure administration
- ❌ Application development

### Critical Success Factors
1. **ISO 27001 certification** achieved by Q4 2026
2. **100% critical vulnerabilities** remediated within 30 days
3. **GDPR compliance** ≥ 90%
4. **Security coordinator trained** (4 certifications: ISO 27001 LI/LA, CISM, CIPP/E)
5. **Phishing resilience** < 10% click rate by year-end

## File History

### Archive Folder
The `archive/` folder contains previous working documents:
- `RecapEchangeGPT.md` - Initial certification analysis
- `TODO.md` - Original improvement checklist
- `Certifications_Budget_Formation.md` - Detailed certification pricing (superseded by Annexe B)
- `Prestataires_Cybersecurite_France.md` - Provider listings (superseded by Annexe A)
- `Prestataires_Audits_Complementaires.md` - Additional audit types (integrated into Annexe A)

These are kept for reference but should not be modified. All current work uses the new structure.

## Quick Reference

**Main planning document:** `Pilotage_Securite_2026.md`
**Provider evaluation:** `annexes/A_Selection_Prestataires.md`
**Training planning:** `annexes/B_Catalogue_Certifications.md`
**Technical terms:** `annexes/C_Glossaire.md`

**Budget 2026:** 139,700 € HT
**Key deadline:** ISO 27001 certification Q4 2026
**Language:** French (always)
**Audience:** Fintech management + technical teams
