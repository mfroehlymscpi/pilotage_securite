# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repository contains documentation for "Pilotage Sécurité" (Security Governance), a cybersecurity governance project for a French fintech company specializing in SCPI (Société Civile de Placement Immobilier) investment advisory.

**Key Context:**
- The project focuses on security governance and coordination, not technical execution
- The company operates web applications (VueJS, Symfony), handles sensitive financial data, and performs SCPI data aggregation
- The role is that of a security coordinator/project manager who selects, coordinates, and manages external security service providers
- Primary concerns: Application security (web apps, APIs), GDPR compliance, ISO standards, CI/CD security, LLM usage framework

## Language

All documentation is in **French**. When working in this repository, respond in French and maintain French terminology for:
- Security governance concepts
- Compliance terms (RGPD, not GDPR)
- Professional titles and roles
- Technical documentation

## Repository Structure

The repository is currently minimal with a single primary documentation file:
- `RecapEchangeGPT.md`: Comprehensive synthesis document covering project introduction, certification analysis, and security governance framework

## Content Architecture

The main document (`RecapEchangeGPT.md`) is structured in 6 major sections:

1. **Project Introduction**: Context, objectives, scope, and stakeholders
2. **Certification Categories**: Organized by purpose (Governance, Technical/Pentest, Specialized)
3. **Certification Analysis**: Detailed tables with atomic indicators for each certification's relevance
4. **Project Interpretation**: Guidance on essential certifications for the security coordinator role
5. **Importance Ratings**: Prioritization specific to the fintech SCPI context
6. **Next Steps**: Deliverable options (PDF, matrices, etc.)

## Key Concepts

**Certification Categories:**
- **Category A (Governance)**: CISSP, CISM, ISO 27001 Lead Implementer/Auditor, CSSLP
- **Category B (Technical/Pentest)**: OSCP, OSWE, OSEP, eWPTX, GWEB, GPEN, CEH
- **Category C (Specialized)**: AWS/Azure/GCP Security, CIPP/E, DPO CNIL, ISO 27701

**Priority Domains for this Organization:**
- Application Security (AppSec): VueJS and Symfony applications, APIs
- GDPR/Privacy Compliance: Handling sensitive client financial data
- ISO 27001 Governance: Policy framework and audit management
- Security vendor selection: Evaluating pentest and audit service providers

## Documentation Standards

When creating or modifying documents:
- Use clear markdown formatting with emoji section markers (📌)
- Organize information in tables where appropriate for comparison/analysis
- Use star ratings (⭐) for importance/recognition levels
- Include checkmarks (✔) and symbols (⚪, ≈) for feature matrices
- Maintain professional tone suitable for executive and technical audiences

## Typical Tasks

When working in this repository, you may be asked to:
- Add new security certifications or frameworks to existing analyses
- Create comparison matrices for security service providers
- Draft internal security policies or governance documents
- Analyze audit reports or security assessment findings
- Develop roadmaps for security program implementation
- Create presentations or summaries for different stakeholder levels (direction, technical team, etc.)

## Important Notes

- This is a governance/coordination project, not a technical implementation project
- Focus on strategic security management, not hands-on technical security work
- External service providers handle technical execution (pentests, audits, etc.)
- The company's tech stack includes VueJS (frontend), Symfony (backend), and data aggregation systems for SCPI management
