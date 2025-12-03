# Pilotage Sécurité 2026

**Document de référence - Programme de sécurité informatique**
Version 1.0 - Décembre 2025

---

## 📋 Sommaire

1. [Introduction & Contexte](#1-introduction--contexte)
2. [Risques & Enjeux Métier](#2-risques--enjeux-métier)
3. [Organisation & Rôles](#3-organisation--rôles)
4. [Roadmap 2026](#4-roadmap-2026)
5. [Budget Prévisionnel](#5-budget-prévisionnel)
6. [Livrables du Référent Sécurité](#6-livrables-du-référent-sécurité)
7. [Indicateurs de Suivi (KPI)](#7-indicateurs-de-suivi-kpi)
8. [Plan de Formation](#8-plan-de-formation)

**Annexes :**
- [Annexe A : Guide de Sélection des Prestataires](./annexes/A_Selection_Prestataires.md)
- [Annexe B : Catalogue des Certifications](./annexes/B_Catalogue_Certifications.md)
- [Annexe C : Glossaire Technique](./annexes/C_Glossaire.md)

---

## 1. Introduction & Contexte

### 1.1 Présentation du Projet

Le projet **Pilotage Sécurité** a pour objectif de structurer, organiser et superviser l'ensemble des enjeux de cybersécurité de l'entreprise, **sans internaliser l'exécution technique**.

Dans un contexte où nos activités reposent fortement sur des applications web (VueJS, Symfony), des données financières sensibles et des processus d'agrégation de données SCPI, il devient indispensable d'instaurer une démarche sécurité méthodique, continue et pilotée.

### 1.2 Objectifs

L'ambition du projet est double :

1. **Mettre en place une gouvernance sécurité claire**, couvrant :
   - Bonnes pratiques internes
   - Conformité RGPD/ISO 27001
   - Politiques d'accès et gestion des identités
   - Gestion du télétravail
   - Sécurité des développements (CI/CD)
   - Encadrement des usages LLM

2. **Sélectionner, coordonner et piloter des prestataires spécialisés** pour :
   - Audits techniques (pentests applicatifs, infrastructure)
   - Audits organisationnels
   - Audits RGPD
   - Sensibilisation et formation
   - Certification ISO 27001

### 1.3 Périmètre Technique

| Périmètre | Technologies | Sensibilité |
|-----------|--------------|-------------|
| **Applications web** | VueJS (front), Symfony (back) | ⭐⭐⭐⭐⭐ Critique |
| **API & intégrations** | REST API, agrégation SCPI | ⭐⭐⭐⭐⭐ Critique |
| **Infrastructure** | Serveurs, Docker, réseau | ⭐⭐⭐⭐ Importante |
| **Données** | Données clients, transactions | ⭐⭐⭐⭐⭐ Critique |
| **Active Directory** | Gestion identités, SSO | ⭐⭐⭐⭐ Importante |

### 1.4 Contexte Métier

**Secteur :** Fintech / Conseil en investissement SCPI
**Obligations réglementaires :** RGPD, conformité financière
**Particularités :** Manipulation données financières sensibles, agrégation multi-sources

---

## 2. Risques & Enjeux Métier

### 2.1 Cartographie des Risques Cyber

| Risque | Impact Business | Probabilité | Criticité | Mitigation |
|--------|----------------|-------------|-----------|------------|
| **Fuite données clients SCPI** | - Sanctions RGPD (jusqu'à 20M€)<br>- Atteinte image de marque<br>- Perte clients | Moyenne | 🔴 CRITIQUE | Audit RGPD, chiffrement, DLP |
| **Compromission plateforme web** | - Indisponibilité service<br>- Perte revenus<br>- Responsabilité contractuelle | Moyenne | 🔴 CRITIQUE | Pentest réguliers, WAF, monitoring |
| **Injection API agrégation** | - Corruption données SCPI<br>- Erreurs décisions investissement<br>- Responsabilité juridique | Faible | 🟠 MAJEUR | Pentest API, validation entrées, tests |
| **Attaque supply chain** | - Backdoor dépendances<br>- Compromission CI/CD<br>- Diffusion malware | Moyenne | 🟠 MAJEUR | SCA, SBOM, revue dépendances |
| **Utilisation malveillante LLM** | - Prompt injection<br>- Fuite données via LLM<br>- Génération contenu frauduleux | Faible | 🟡 MODÉRÉ | Politique LLM, isolation, monitoring |
| **Compromission AD** | - Élévation privilèges<br>- Mouvement latéral<br>- Prise de contrôle totale | Moyenne | 🔴 CRITIQUE | Audit AD, tiering, MFA |
| **Social engineering** | - Phishing collaborateurs<br>- Accès frauduleux<br>- Exfiltration données | Élevée | 🟠 MAJEUR | Formation, campagnes phishing |

**Légende Criticité :**
- 🔴 **CRITIQUE** : Impact très élevé, traitement prioritaire immédiat
- 🟠 **MAJEUR** : Impact élevé, traitement dans l'année
- 🟡 **MODÉRÉ** : Impact moyen, surveillance et traitement progressif

### 2.2 Enjeux Business

**Pour la Direction :**
- Conformité réglementaire (éviter sanctions)
- Protection réputation et confiance clients
- Continuité d'activité

**Pour le Métier :**
- Fiabilité des données SCPI
- Disponibilité des plateformes
- Qualité de service

**Pour l'IT :**
- Réduction surface d'attaque
- Amélioration qualité code
- Industrialisation sécurité (DevSecOps)

---

## 3. Organisation & Rôles

### 3.1 Rôle du Référent Sécurité (Interne)

**Mission :** Pilotage et coordination sécurité (SANS exécution technique)

**Responsabilités :**
- ✅ Définir stratégie et roadmap sécurité
- ✅ Sélectionner et piloter prestataires externes
- ✅ Rédiger politiques et procédures internes
- ✅ Suivre remédiation des vulnérabilités
- ✅ Animer sensibilisation et formation
- ✅ Reporter à la direction (KPI, incidents)
- ❌ PAS d'exécution technique (pentests, configuration firewall, etc.)

### 3.2 Interlocuteurs Internes

| Rôle | Implication | Fréquence |
|------|-------------|-----------|
| **Direction** | Validation budget, arbitrage risques | Trimestrielle |
| **CTO** | Validation technique, priorisation | Mensuelle |
| **Équipe Développement** | Application recommandations, formation | Hebdomadaire |
| **Équipe Data** | Sécurisation pipelines, API | Mensuelle |
| **DPO** (si existe) | Coordination RGPD | Mensuelle |
| **DAF** | Budget, assurance cyber | Trimestrielle |

### 3.3 Prestataires Externes

| Type | Mission | Exemples |
|------|---------|----------|
| **Pentest AppSec** | Tests intrusion applications web/API | Vaadata, SysDream, Connect3S |
| **Audit Infrastructure** | Sécurité réseau, firewall, VPN | AGESYS, Weodeo, REDOPUS |
| **Audit Organisationnel** | Gouvernance, politiques, PSSI | Wavestone, AlgoSecure, Digitemis |
| **Audit RGPD** | Conformité, registre, PIA | Consultants DPO/CIPP-E |
| **Audit Active Directory** | Sécurité AD, privilèges, mots de passe | PwC, consultants SSI |
| **Formation & Sensibilisation** | Phishing, secure coding | SysDream, Intuity, Exodata |
| **Certification ISO 27001** | Accompagnement + certification | Consultant + AFNOR |

---

## 4. Roadmap 2026

### Vue d'ensemble

```
Q1 2026          Q2 2026          Q3 2026          Q4 2026
│                │                │                │
│ DIAGNOSTIC     │ APPLICATIF     │ REMÉDIATION    │ CERTIFICATION
│                │                │                │
▼                ▼                ▼                ▼
```

### Q1 2026 (Jan-Mars) - Phase Diagnostic

**Objectif :** Établir l'état des lieux sécurité

| Action | Prestataire | Durée | Budget | Livrable |
|--------|-------------|-------|--------|----------|
| **Formation ISO 27001 Lead Implementer** | EduGroupe / M2i | 5j | 3 000 € | Certification interne |
| **Audit organisationnel initial** | Cabinet PASSI | 7-10j | 10 000 € | Rapport + plan action |
| **Audit Active Directory** | Consultant SSI | 5-7j | 7 000 € | Rapport + quick wins |
| **Audit infrastructure réseau** | PME spécialisée | 5j | 6 000 € | Schémas + recommandations |
| **Inventaire actifs & cartographie risques** | Interne + consultant | 5j | 3 000 € | Registre actifs, matrice risques |

**Budget Q1 : 29 000 €**

**Jalons de validation :**
- ✅ Validation rapport audit org. par Direction (fin mars)
- ✅ Priorisation plan action avec CTO
- ✅ Lancement correctifs quick wins AD

---

### Q2 2026 (Avr-Juin) - Phase Applicative & RGPD

**Objectif :** Sécuriser les applications critiques et conformité RGPD

| Action | Prestataire | Durée | Budget | Livrable |
|--------|-------------|-------|--------|----------|
| **Formation CISM** | CERTyou / EduGroupe | 5j | 4 200 € | Certification interne |
| **Pentest applications web** (VueJS/Symfony) | OSWE/GWEB certifié | 10j | 12 000 € | Rapport vulnérabilités + PoC |
| **Pentest API agrégation SCPI** | Même prestataire | 5j | 6 000 € | Rapport API |
| **Audit RGPD initial** | Consultant CIPP-E/DPO | 12j | 15 000 € | Registre, PIA, plan conformité |
| **Campagne phishing (1ère vague)** | Plateforme sensibilisation | - | 2 000 € | Taux clics, sensibilisation |
| **Formation CIPP/E** | PLB / Prosica | 2j | 2 000 € | Certification interne |

**Budget Q2 : 41 200 €**

**Jalons de validation :**
- ✅ Présentation résultats pentest à Direction + CTO (fin juin)
- ✅ Validation plan remédiation vulnérabilités (criticité)
- ✅ Lancement corrections critiques (délai max 1 mois)

---

### Q3 2026 (Juil-Sep) - Phase Remédiation & Formation

**Objectif :** Corriger vulnérabilités et monter en compétence

| Action | Prestataire | Durée | Budget | Livrable |
|--------|-------------|-------|--------|----------|
| **Support remédiation pentests** | Même prestataire Q2 | 3j | 3 000 € | Validation corrections |
| **Formation équipe dev (secure coding)** | SysDream / EduGroupe | 2j | 4 000 € | Équipe formée OWASP |
| **Rédaction PSSI & politiques** | Interne + consultant | 10j | 5 000 € | PSSI, charte, procédures |
| **Accompagnement ISO 27001 (Phase 1)** | Consultant ISO | 20j | 25 000 € | SMSI, documentation ISO |
| **Déploiement outils sécurité (SAST/DAST)** | Interne | - | 5 000 € | Intégration CI/CD |
| **Campagne phishing (2ème vague)** | Plateforme | - | 1 500 € | Mesure progrès |

**Budget Q3 : 43 500 €**

**Jalons de validation :**
- ✅ Validation PSSI par Direction (fin août)
- ✅ Déploiement politiques internes (charte, télétravail, etc.)
- ✅ Audit interne blanc ISO 27001 (mi-septembre)

---

### Q4 2026 (Oct-Déc) - Phase Certification & Bilan

**Objectif :** Certification ISO 27001 et clôture annuelle

| Action | Prestataire | Durée | Budget | Livrable |
|--------|-------------|-------|--------|----------|
| **Formation ISO 27001 Lead Auditor** | PECB / CERTyou | 5j | 3 500 € | Certification interne |
| **Certification ISO 27001 (audit initial)** | AFNOR Certification | 5j | 15 000 € | Certificat ISO 27001 |
| **Re-test pentest (après corrections)** | Même prestataire Q2 | 3j | 3 000 € | Validation remédiation |
| **Campagne phishing (3ème vague)** | Plateforme | - | 1 500 € | Bilan annuel sensibilisation |
| **Audit RGPD suivi** | Consultant RGPD | 3j | 3 000 € | Rapport conformité |
| **Bilan annuel + Roadmap 2027** | Interne | - | - | Présentation Direction |

**Budget Q4 : 26 000 €**

**Jalons de validation :**
- ✅ Obtention certificat ISO 27001 (novembre)
- ✅ Validation remédiation 100% vulnérabilités critiques
- ✅ Présentation bilan 2026 + roadmap 2027 (décembre)

---

### Synthèse Annuelle 2026

| Trimestre | Phase | Budget | Cumul |
|-----------|-------|--------|-------|
| **Q1** | Diagnostic | 29 000 € | 29 000 € |
| **Q2** | Applicatif & RGPD | 41 200 € | 70 200 € |
| **Q3** | Remédiation & Formation | 43 500 € | 113 700 € |
| **Q4** | Certification & Bilan | 26 000 € | 139 700 € |

**TOTAL 2026 : 139 700 € HT** (≈ 167 000 € TTC)

---

## 5. Budget Prévisionnel

### 5.1 Budget 2026 Détaillé

| Poste | Détail | Budget HT |
|-------|--------|-----------|
| **Formation référent sécurité** | ISO 27001 LI/LA, CISM, CIPP/E | 12 700 € |
| **Audits applicatifs** | Pentest web/API (10+5j) | 18 000 € |
| **Audits infrastructure** | Réseau, firewall, VPN | 6 000 € |
| **Audits Active Directory** | Sécurité AD, privilèges | 7 000 € |
| **Audits organisationnels** | Gouvernance, PSSI, conformité | 10 000 € |
| **Audits RGPD** | Initial + suivi | 18 000 € |
| **Certification ISO 27001** | Accompagnement + certification | 40 000 € |
| **Formation équipe dev** | Secure coding (2j) | 4 000 € |
| **Sensibilisation (phishing)** | 3 campagnes annuelles | 5 000 € |
| **Outils sécurité (SAST/DAST)** | Licences annuelles | 5 000 € |
| **Support & remédiations** | Assistance post-audit | 9 000 € |
| **Contingence (10%)** | Audits complémentaires, urgences | 5 000 € |
| **TOTAL 2026** | | **139 700 € HT** |

### 5.2 Budget Années Suivantes (2027-2029)

| Poste | Fréquence | Budget annuel HT |
|-------|-----------|------------------|
| **Audits applicatifs** | 1-2x/an | 12 000 € - 18 000 € |
| **Audits infrastructure** | 1x/2 ans | 3 000 € (moyen.) |
| **Audits AD (suivi)** | 1x/2 ans | 2 500 € (moyen.) |
| **Audits org. (suivi)** | 1x/2 ans | 4 000 € (moyen.) |
| **Audits RGPD** | 1x/an | 5 000 € - 8 000 € |
| **ISO 27001 surveillance** | 1x/an | 12 000 € |
| **Sensibilisation continue** | Continu | 5 000 € |
| **Outils sécurité** | Annuel | 5 000 € |
| **Formation dev** | 1x/2 ans | 2 000 € (moyen.) |
| **Red Team (optionnel)** | 1x/3 ans | 15 000 € (moyen.) |
| **Contingence** | 10% | 6 500 € |
| **TOTAL ANNUEL (2027-2029)** | | **70 000 € - 80 000 € HT/an** |

### 5.3 Retour sur Investissement (ROI)

| Bénéfice | Estimation Valeur |
|----------|-------------------|
| **Évitement sanctions RGPD** | Jusqu'à 20 M€ |
| **Réduction risque cyber** | Couverture assurance cyber (prime -20 à -30%) |
| **Conformité ISO 27001** | Argument commercial (appels d'offres) |
| **Réduction incidents** | Coût moyen incident : 100 k€ - 500 k€ |
| **Confiance clients** | Rétention + nouveaux contrats |

**Estimation ROI :** Retour positif dès 1 incident majeur évité

---

## 6. Livrables du Référent Sécurité

### 6.1 Documentation Gouvernance (Q1-Q3 2026)

| Document | Description | Échéance |
|----------|-------------|----------|
| **Politique de Sécurité SI (PSSI)** | Document cadre sécurité entreprise | Q3 2026 |
| **Charte d'utilisation SI** | Règles usage pour collaborateurs | Q3 2026 |
| **Politique de mots de passe** | Conformité ANSSI (12 car., complexité) | Q2 2026 |
| **Politique télétravail / nomadisme** | Sécurisation accès distants | Q2 2026 |
| **Politique BYOD** | Règles appareils personnels | Q3 2026 |
| **Charte utilisation LLM** | Encadrement usages IA générative | Q2 2026 |
| **Procédure gestion incidents** | Process de réponse incidents sécu | Q3 2026 |
| **Plan de Continuité (PCA/PRA)** | Procédures reprise activité | Q4 2026 |

### 6.2 Documentation Audit & Pilotage

| Document | Description | Fréquence |
|----------|-------------|-----------|
| **Registre des actifs** | Inventaire SI critique | MAJ trimestrielle |
| **Matrice des risques cyber** | Cartographie risques + traitement | MAJ annuelle |
| **Registre traitements RGPD** | Base légale, DPO, PIA | MAJ continue |
| **Cahiers des charges audits** | Specs techniques appels d'offres | Selon besoins |
| **Rapports de suivi audits** | Avancement remédiation vulnérabilités | Mensuel |
| **Tableau de bord KPI sécurité** | Indicateurs pilotage | Mensuel |
| **Rapport sécurité Direction** | Synthèse exec. état sécurité | Trimestriel |

### 6.3 Documentation ISO 27001 (Q3-Q4 2026)

*Produite avec l'accompagnement consultant ISO*

- Déclaration d'Applicabilité (Statement of Applicability - SoA)
- Procédures obligatoires (14 procédures ISO 27001:2022)
- Registre des risques ISO
- Plan de traitement des risques
- Politique SMSI
- Objectifs sécurité mesurables

---

## 7. Indicateurs de Suivi (KPI)

### 7.1 KPI Techniques

| KPI | Cible 2026 | Mesure | Fréquence |
|-----|------------|--------|-----------|
| **Vulnérabilités critiques détectées** | 100% corrigées < 30j | Nb vulns / Délai moyen correction | Mensuel |
| **Vulnérabilités majeures détectées** | 100% corrigées < 90j | Nb vulns / Délai moyen correction | Mensuel |
| **Taux couverture audits** | 100% applis critiques | % applications auditées / total | Trimestriel |
| **Score sécurité applicatif** | Amélioration +30% | OWASP ASVS Level | Semestriel |
| **Score sécurité AD** | Amélioration +40% | PingCastle Score | Semestriel |
| **Conformité politique mots de passe** | 95% comptes conformes | % comptes ANSSI-compliant | Trimestriel |

### 7.2 KPI Organisationnels

| KPI | Cible 2026 | Mesure | Fréquence |
|-----|------------|--------|-----------|
| **Taux sensibilisation phishing** | < 10% taux clics | % clics campagnes / nb destinataires | Trimestriel |
| **Taux formation secure coding** | 100% développeurs | % dev formés / total | Annuel |
| **Incidents sécurité déclarés** | 0 incidents majeurs | Nb incidents / criticité | Mensuel |
| **Délai détection incidents** | < 24h | Temps moyen détection | Trimestriel |
| **Taux conformité RGPD** | 90% conformité | Audit RGPD score | Semestriel |
| **Certification ISO 27001** | Obtenue Q4 2026 | Oui / Non | Annuel |

### 7.3 KPI Budgétaires

| KPI | Cible 2026 | Mesure | Fréquence |
|-----|------------|--------|-----------|
| **Budget consommé vs prévisionnel** | ±10% | Écart budget | Mensuel |
| **Coût moyen par vulnérabilité corrigée** | Suivi tendance | Budget remédiation / nb vulns | Trimestriel |
| **ROI programme sécurité** | Positif | Incidents évités vs coût programme | Annuel |

### 7.4 Tableau de Bord Mensuel (Exemple)

```
┌─────────────────────────────────────────────────────────────┐
│ TABLEAU DE BORD SÉCURITÉ - Septembre 2026                  │
├─────────────────────────────────────────────────────────────┤
│ Vulnérabilités en cours                                     │
│   🔴 Critiques    : 2  (délai moyen: 15j)   ✅ OK          │
│   🟠 Majeures     : 8  (délai moyen: 45j)   ✅ OK          │
│   🟡 Mineures     : 23 (délai moyen: 120j)  ⚠️  Surveillance│
├─────────────────────────────────────────────────────────────┤
│ Audits 2026                                                 │
│   ✅ Audit org.        : Terminé (Q1)                       │
│   ✅ Audit AD          : Terminé (Q1)                       │
│   ✅ Pentest web/API   : Terminé (Q2), Re-test Q4          │
│   ✅ Audit RGPD        : Terminé (Q2)                       │
│   🔄 ISO 27001         : En cours certification (Q4)        │
├─────────────────────────────────────────────────────────────┤
│ Sensibilisation                                             │
│   Campagne #2 (Juin)  : 8% clics  ✅ (cible <10%)          │
│   Formation dev       : 12/12 formés ✅                     │
├─────────────────────────────────────────────────────────────┤
│ Budget                                                      │
│   Consommé : 113 700 € / 139 700 € (81%)  ✅               │
└─────────────────────────────────────────────────────────────┘
```

---

## 8. Plan de Formation

### 8.1 Formation Référent Sécurité

**Parcours prioritaire 2026 :**

| Certification | Organisme | Durée | Coût HT | Planning 2026 | Priorité |
|---------------|-----------|-------|---------|---------------|----------|
| **ISO 27001 Lead Implementer** | M2i Formation | 5j | 3 000 € | Q1 (Janvier) | ⭐⭐⭐⭐⭐ |
| **CISM** | CERTyou | 5j | 4 200 € | Q2 (Avril) | ⭐⭐⭐⭐⭐ |
| **CIPP/E** | PLB | 2j | 2 000 € | Q2 (Juin) | ⭐⭐⭐⭐⭐ |
| **ISO 27001 Lead Auditor** | PECB | 5j | 3 500 € | Q4 (Octobre) | ⭐⭐⭐⭐⭐ |
| **CISSP** (optionnel) | SysDream | 5j | 5 000 € | 2027 | ⭐⭐⭐⭐ |

**Total formation référent 2026 : 12 700 € HT**

**Bénéfices :**
- Crédibilité vis-à-vis prestataires et direction
- Capacité à auditer prestataires (Lead Auditor)
- Pilotage projet ISO 27001 (Lead Implementer)
- Expertise RGPD (CIPP/E)
- Vision stratégique sécurité (CISM)

### 8.2 Formation Équipe Développement

| Formation | Contenu | Durée | Coût HT | Planning 2026 |
|-----------|---------|-------|---------|---------------|
| **Secure Coding (VueJS/Symfony)** | OWASP Top 10, injections SQL, XSS, CSRF, secure auth | 2j | 4 000 € | Q3 (Juillet) |
| **API Security** | OWASP API Top 10, authentification, rate limiting | 1j | 2 500 € | 2027 |

**Format :** Présentiel ou distanciel, 12 développeurs formés

**Organismes recommandés :** SysDream, EduGroupe, SANS (GWEB)

---

## Résumé Exécutif

### Pour la Direction

**Contexte :** En tant que fintech manipulant des données financières SCPI sensibles, notre exposition aux cyberrisques est critique. Un incident majeur pourrait coûter 100 k€ - 20 M€ (sanctions RGPD, pertes clients, interruption service).

**Programme 2026 :** Mise en place d'un programme de sécurité structuré avec certification ISO 27001.

**Investissement 2026 :** 139 700 € HT (≈ 167 000 € TTC)
**Investissement récurrent (2027+) :** 70 000 € - 80 000 € HT/an

**Bénéfices :**
- ✅ Conformité réglementaire (RGPD, ISO 27001)
- ✅ Réduction risque cyber (audits, remédiation vulnérabilités)
- ✅ Argument commercial (certification ISO)
- ✅ Confiance clients et partenaires
- ✅ Couverture assurance cyber optimisée

**Décisions attendues :**
1. Validation budget 2026 (140 k€)
2. Validation roadmap trimestrielle
3. Engagement certification ISO 27001

**ROI :** Positif dès 1 incident majeur évité

---

## Prochaines Étapes

**Décembre 2025 :**
- [ ] Présentation roadmap à la Direction
- [ ] Validation budget 2026
- [ ] Identification consultant ISO 27001
- [ ] Lancement appel d'offres audits Q1

**Janvier 2026 :**
- [ ] Formation ISO 27001 Lead Implementer
- [ ] Démarrage audit organisationnel
- [ ] Démarrage audit AD
- [ ] Kick-off projet avec CTO

---

**Document validé par :** ________________
**Date :** ___/___/2026

**Version :** 1.0
**Prochaine révision :** Trimestrielle (après chaque phase)
