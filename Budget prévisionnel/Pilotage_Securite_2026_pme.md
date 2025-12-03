# Pilotage Sécurité 2026 - Version PME

**Document de référence - Programme de sécurité informatique**
PME Fintech SCPI (30-100 employés)
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
- [Annexe A : Guide de Sélection des Prestataires](annexes/A_Selection_Prestataires.md)
- [Annexe B : Catalogue des Certifications](annexes/B_Catalogue_Certifications.md)

---

## 1. Introduction & Contexte

### 1.1 Présentation du Projet

Le projet **Pilotage Sécurité** a pour objectif de structurer et superviser l'ensemble des enjeux de cybersécurité de l'entreprise, **en s'appuyant sur des prestataires spécialisés** pour l'exécution technique.

**Contexte entreprise :**
- PME 30-100 employés en croissance
- Applications web (VueJS, Symfony) et API REST
- Données financières sensibles (SCPI)
- Maturité sécurité à développer
- Objectif : Certification ISO 27001 à moyen terme (2-3 ans)

### 1.2 Objectifs

1. **Structurer une gouvernance sécurité** adaptée à la taille PME
2. **Sélectionner et piloter des prestataires** pour audits techniques et conseil
3. **Mettre en conformité RGPD** et préparer ISO 27001
4. **Professionnaliser la sécurité** : politiques, procédures, formation
5. **Montée en maturité progressive** sur 3 ans

### 1.3 Périmètre Technique

| Périmètre | Technologies | Criticité PME |
|-----------|--------------|---------------|
| **Applications web** | VueJS (front), Symfony (back) | 🔴 Critique (cœur métier) |
| **API & intégrations** | REST API, agrégation SCPI | 🔴 Critique (données sensibles) |
| **Infrastructure** | Serveurs, Docker, réseau, firewall | 🟠 Importante (à auditer) |
| **Active Directory** | Gestion identités, SSO, privilèges | 🟠 Importante (risque élévation) |
| **Données clients** | BDD, fichiers, sauvegardes | 🔴 Critique (RGPD) |
| **Postes de travail** | 30-100 PC/Mac, BYOD possible | 🟡 Modérée |

### 1.4 Contexte PME

**Ressources :**
- ✅ Référent sécurité dédié (50-100% temps)
- ✅ Direction investit dans sécurité
- ✅ Budget annuel raisonnable (50-80k€)
- ❌ Pas encore de RSSI expert temps plein
- ❌ Pas d'équipe sécurité (SOC/pentest interne)

**Approche retenue :** Gouvernance structurée + Prestataires experts + Montée compétences interne

---

## 2. Risques & Enjeux Métier

### 2.1 Cartographie des Risques Cyber (PME)

| Risque | Impact Business PME | Probabilité | Criticité | Mitigation 2026 |
|--------|---------------------|-------------|-----------|-----------------|
| **Fuite données clients SCPI** | - Sanctions RGPD (jusqu'à 20M€)<br>- Atteinte réputation<br>- Perte clients | Moyenne | 🔴 CRITIQUE | Audit RGPD + DLP + chiffrement |
| **Compromission plateforme** | - Indisponibilité prolongée<br>- Perte revenus<br>- Responsabilité | Moyenne | 🔴 CRITIQUE | Pentest + WAF + monitoring |
| **Attaque supply chain** | - Backdoor dépendances<br>- Compromission CI/CD | Moyenne | 🟠 MAJEUR | SCA, SBOM, pipeline sécurisé |
| **Compromission AD** | - Élévation privilèges<br>- Mouvement latéral<br>- Ransomware | Élevée | 🔴 CRITIQUE | Audit AD + tiering + MFA |
| **Social engineering** | - Phishing réussi<br>- Accès frauduleux | Élevée | 🟠 MAJEUR | Formation continue + campagnes |
| **Injection API** | - Corruption données SCPI | Faible | 🟠 MAJEUR | Pentest API + validation |
| **Défaillance sauvegarde** | - Perte données (ransomware) | Moyenne | 🟠 MAJEUR | PRA/PCA + tests restauration |
| **Insider threat** | - Vol données par collaborateur | Faible | 🟡 MODÉRÉ | Politique accès + logs + DLP |

### 2.2 Enjeux Business

**Pour la Direction :**
- Conformité réglementaire (RGPD obligatoire, ISO 27001 différenciant)
- Protection réputation (clients B2B et B2C exigeants)
- Continuité d'activité (résilience cyber)
- Assurabilité (cyber-assurance exige audits)

**Pour le Métier :**
- Fiabilité données SCPI critiques
- Disponibilité plateformes 24/7
- Confiance partenaires financiers

**Pour l'IT :**
- Sécuriser sans freiner innovation
- Automatisation sécurité (DevSecOps)
- Montée compétences équipe

---

## 3. Organisation & Rôles

### 3.1 Rôle Référent Sécurité (Interne)

**Profil :** Référent sécurité dédié 50-100% (évolution vers RSSI)

**Mission :** Pilotage et coordination sécurité, **appui prestataires pour technique**

**Responsabilités :**
- ✅ Définir stratégie et roadmap sécurité
- ✅ Sélectionner et piloter prestataires externes
- ✅ Rédiger politiques et procédures (avec aide prestataire)
- ✅ Suivre remédiation vulnérabilités
- ✅ Animer sensibilisation et formation
- ✅ Reporter Direction (KPI, incidents, budget)
- ✅ Participer audits (observation, suivi)
- ⚠️ Exécution technique limitée (pentests = prestataires)

**Temps estimé :** 2-5 jours/semaine (100-250h/an)

**Formations recommandées 2026-2027 :**
- ISO 27001 Lead Implementer (2026)
- CISM ou CISSP (2027)
- CIPP/E si rôle DPO (2027)

### 3.2 Interlocuteurs Internes

| Rôle | Implication | Fréquence |
|------|-------------|-----------|
| **Direction / CEO** | Validation budget, arbitrage risques | Trimestrielle |
| **CTO / DSI** | Validation technique, priorisation | Bimensuelle |
| **Équipe Dev (6-15 pers)** | Application recommandations, secure coding | Hebdomadaire |
| **Équipe Infra/Ops** | Sécurisation serveurs, firewall, AD | Hebdomadaire |
| **DPO** (interne ou externe) | Coordination RGPD | Mensuelle |
| **RH** | Sensibilisation, onboarding/offboarding sécu | Mensuelle |
| **DAF** | Budget, assurance cyber | Trimestrielle |

### 3.3 Prestataires Externes

| Type Prestataire | Mission | Fréquence |
|------------------|---------|-----------|
| **Consultant sécurité / Audit org.** | Gouvernance, politiques, ISO 27001 | 2026 + annuel |
| **Pentester AppSec** | Tests applications web/API | 1-2x/an |
| **Audit infrastructure** | Réseau, firewall, serveurs | 1x/an |
| **Audit Active Directory** | Sécurité AD, privilèges, GPO | 1x/an |
| **Consultant RGPD/DPO** | Audit RGPD, registre, PIA | Initial + suivi annuel |
| **Formation/Sensibilisation** | Phishing, secure coding, awareness | Continue |
| **Consultant ISO 27001** | Accompagnement certification (Année 2-3) | 2027-2028 |

---

## 4. Roadmap 2026

### Vue d'ensemble

```
Q1 2026          Q2 2026          Q3 2026          Q4 2026
│                │                │                │
│ DIAGNOSTIC     │ AUDITS TECH    │ GOUVERNANCE    │ CONSOLIDATION
│                │                │                │
▼                ▼                ▼                ▼
```

### Q1 2026 (Jan-Mars) - Phase Diagnostic

**Action 1 : Diagnostic Sécurité Organisationnel**

| Prestataire | Mission | Durée | Budget |
|-------------|---------|-------|--------|
| Consultant sécurité (PASSI ou équivalent) | - Audit organisationnel (gouvernance, politiques)<br>- Cartographie risques PME<br>- Gap analysis ISO 27001<br>- Roadmap 3 ans priorisée | 7-10 jours | 8 000 € - 12 000 € |

**Action 2 : Audit Active Directory**

| Prestataire | Mission | Durée | Budget |
|-------------|---------|-------|--------|
| Consultant AD/IAM | - Audit architecture AD<br>- Politique mots de passe<br>- Comptes à privilèges<br>- Tiering model<br>- Recommandations hardening | 5-7 jours | 5 000 € - 8 000 € |

**Action 3 : Formation Référent Sécurité**

| Formation | Organisme | Durée | Budget |
|-----------|-----------|-------|--------|
| ISO 27001 Lead Implementer | M2i / IB Formation | 5 jours | 3 000 € - 3 500 € |

**Budget Q1 : 16 000 € - 23 500 €**

**Jalons Q1 :**
- Fin mars : Rapports diagnostic org. + AD
- Présentation Direction : roadmap, budget Q2-Q4
- Référent certifié ISO 27001 LI

---

### Q2 2026 (Avr-Juin) - Phase Audits Techniques

**Action 4 : Pentest Applicatif Complet**

| Prestataire | Mission | Durée | Budget |
|-------------|---------|-------|--------|
| Pentester AppSec (OSWE/GWEB/eWPTX) | - Pentest VueJS (front)<br>- Pentest Symfony (back)<br>- Pentest API agrégation SCPI<br>- Tests OWASP Top 10 + ASVS L2<br>- Re-test après corrections (2j inclus) | 10-12 jours | 10 000 € - 15 000 € |

**Action 5 : Audit Infrastructure & Réseau**

| Prestataire | Mission | Durée | Budget |
|-------------|---------|-------|--------|
| Audit infra réseau | - Configuration firewall<br>- Segmentation VLAN<br>- VPN / accès distants<br>- WiFi corporate<br>- Scan vulnérabilités serveurs | 5-7 jours | 5 000 € - 8 000 € |

**Action 6 : Audit RGPD Complet**

| Prestataire | Mission | Durée | Budget |
|-------------|---------|-------|--------|
| Consultant RGPD/DPO (CIPP-E) | - Audit conformité RGPD<br>- Registre traitements<br>- PIA traitements critiques<br>- Politique confidentialité / CGU<br>- Procédures exercice droits<br>- Accompagnement 6 mois | 10-12 jours | 10 000 € - 15 000 € |

**Budget Q2 : 25 000 € - 38 000 €**

**Jalons Q2 :**
- Fin juin : Rapports pentest, infra, RGPD
- Priorisation corrections (Critiques < 30j, Majeures < 90j)
- Plan conformité RGPD validé

---

### Q3 2026 (Juil-Sep) - Phase Gouvernance & Remédiation

**Action 7 : Corrections Vulnérabilités**

| Qui | Mission | Durée | Budget |
|-----|---------|-------|--------|
| Équipe dev/ops interne | Correction vulnérabilités critiques et majeures | Variable | Temps interne |
| Pentester (support optionnel) | Support questions techniques corrections | 2-3 jours | 2 000 € - 3 000 € |

**Action 8 : Rédaction Politiques & Procédures**

| Qui | Mission | Durée | Budget |
|-----|---------|-------|--------|
| Référent + Consultant org. (Q1) | - PSSI (Politique Sécurité SI)<br>- Charte utilisation SI<br>- Politique mots de passe (ANSSI)<br>- Politique télétravail / nomadisme<br>- Politique BYOD<br>- Procédure gestion incidents<br>- Procédure onboarding/offboarding | 10-15 jours | 5 000 € - 8 000 € |

**Action 9 : Sensibilisation & Formation**

| Prestataire | Mission | Durée | Budget |
|-------------|---------|-------|--------|
| Plateforme phishing | 3 campagnes phishing (Juil/Sept/Nov) | - | 3 000 € - 5 000 € |
| Formation secure coding | Atelier OWASP dev (2j, 10-15 pers) | 2 jours | 3 000 € - 4 500 € |
| Sensibilisation générale | Sessions awareness (tous collaborateurs) | 1 jour | 2 000 € - 3 000 € |

**Budget Q3 : 15 000 € - 23 500 €**

**Jalons Q3 :**
- Sept : 100% vulnérabilités critiques corrigées
- Sept : PSSI + politiques clés rédigées et déployées
- Sept : Formation dev terminée

---

### Q4 2026 (Oct-Déc) - Phase Consolidation

**Action 10 : Déploiement Outils Sécurité**

| Outil | Usage | Budget |
|-------|-------|--------|
| Solution SAST (SonarQube / Snyk) | Analyse code CI/CD | 2 000 € - 4 000 € /an |
| WAF (Cloudflare / AWS WAF) | Protection applications web | 2 000 € - 5 000 € /an |
| Plateforme sensibilisation (abonnement) | Phishing + e-learning continu | 2 000 € - 4 000 € /an |

**Action 11 : Re-tests & Validation**

| Prestataire | Mission | Durée | Budget |
|-------------|---------|-------|--------|
| Pentester initial | Re-test complet post-corrections | 3-4 jours | 3 000 € - 4 000 € |
| Audit RGPD | Vérification conformité actions | 2-3 jours | 2 000 € - 3 000 € |

**Action 12 : Formation Référent (Optionnel 2026)**

| Formation | Organisme | Durée | Budget |
|-----------|-----------|-------|--------|
| CISM (si budget disponible) | CERTyou / EduGroupe | 5 jours | 4 000 € - 4 500 € |

**Budget Q4 : 15 000 € - 24 500 €**

**Jalons Q4 :**
- Nov : Re-test pentest validé (vulns corrigées)
- Déc : Bilan annuel 2026
- Déc : Roadmap 2027 (préparation ISO 27001)

---

### Synthèse Annuelle 2026

| Trimestre | Phase | Budget HT |
|-----------|-------|-----------|
| **Q1** | Diagnostic (org., AD, formation ISO) | 16 000 € - 23 500 € |
| **Q2** | Audits (pentest, infra, RGPD) | 25 000 € - 38 000 € |
| **Q3** | Gouvernance & remédiation | 15 000 € - 23 500 € |
| **Q4** | Consolidation (outils, re-tests) | 15 000 € - 24 500 € |
| **TOTAL 2026** | | **71 000 € - 110 000 € HT** |

**Fourchette réaliste PME : 75 000 € - 95 000 € HT (90-114k€ TTC)**

---

## 5. Budget Prévisionnel

### 5.1 Budget 2026 Détaillé (PME)

| Poste | Détail | Budget HT |
|-------|--------|-----------|
| **Audits organisationnels** | Diagnostic gouvernance + gap ISO 27001 | 8 000 € - 12 000 € |
| **Audit Active Directory** | Sécurité AD, privilèges, tiering | 5 000 € - 8 000 € |
| **Pentest applicatif** | Web + API (10-12j) + re-test | 10 000 € - 15 000 € |
| **Audit infrastructure** | Réseau, firewall, VPN, serveurs | 5 000 € - 8 000 € |
| **Audit RGPD** | Complet + accompagnement 6 mois | 10 000 € - 15 000 € |
| **Rédaction politiques** | PSSI, procédures (avec consultant) | 5 000 € - 8 000 € |
| **Formation référent** | ISO 27001 LI + CISM (optionnel) | 3 000 € - 8 000 € |
| **Formation équipe dev** | Secure coding (2j) | 3 000 € - 4 500 € |
| **Sensibilisation** | 3 campagnes phishing + sessions | 5 000 € - 8 000 € |
| **Outils sécurité** | SAST, WAF, plateforme awareness | 6 000 € - 13 000 € |
| **Support & remédiation** | Assistance post-audits | 4 000 € - 6 000 € |
| **Contingence (10%)** | Imprévus, audits complémentaires | 6 500 € - 9 500 € |
| **TOTAL 2026** | | **70 500 € - 109 500 € HT** |

**Budget cible PME : 80 000 € HT (≈ 96 000 € TTC)**

### 5.2 Budget Années Suivantes (2027-2029)

#### Année 2 (2027) - Maintien + Préparation ISO 27001

| Poste | Fréquence | Budget HT |
|-------|-----------|-----------|
| **Pentest applicatif** | 1x/an | 10 000 € - 12 000 € |
| **Audit infra (partiel)** | 1x/2 ans | 3 000 € - 4 000 € |
| **Audit AD (suivi)** | 1x/2 ans | 2 500 € - 3 500 € |
| **Audit org. (suivi)** | 1x/an | 4 000 € - 6 000 € |
| **Audit RGPD suivi** | 1x/an | 3 000 € - 5 000 € |
| **Accompagnement ISO 27001** | Préparation certification | 20 000 € - 30 000 € |
| **Sensibilisation continue** | Phishing + e-learning | 5 000 € - 7 000 € |
| **Outils sécurité** | Licences annuelles | 6 000 € - 13 000 € |
| **Formation** | Référent + équipe | 3 000 € - 5 000 € |
| **Contingence** | 10% | 5 600 € - 8 500 € |
| **TOTAL 2027** | | **62 100 € - 94 000 € HT** |

#### Année 3 (2028) - Certification ISO 27001

| Poste | Budget HT |
|-------|-----------|
| Budget récurrent (audits, sensibilisation, outils) | 40 000 € - 55 000 € |
| **Certification ISO 27001 (audit initial)** | 15 000 € - 20 000 € |
| **TOTAL 2028** | **55 000 € - 75 000 € HT** |

#### Année 4+ (2029+) - Maintien Certifié

| Poste | Budget annuel HT |
|-------|------------------|
| Audits (pentest, infra, org., RGPD) | 25 000 € - 35 000 € |
| Surveillance ISO 27001 (1x/an) | 10 000 € - 12 000 € |
| Sensibilisation + formation | 5 000 € - 7 000 € |
| Outils sécurité | 6 000 € - 13 000 € |
| Contingence | 4 600 € - 6 700 € |
| **TOTAL ANNUEL (2029+)** | **50 600 € - 73 700 € HT/an** |

---

## 6. Livrables du Référent Sécurité

### 6.1 Documentation Gouvernance (2026)

| Document | Description | Échéance | Aide Prestataire |
|----------|-------------|----------|------------------|
| **Politique Sécurité SI (PSSI)** | Document cadre sécurité (20-30 pages) | Q3 2026 | ✅ Consultant org. |
| **Charte utilisation SI** | Règles collaborateurs | Q3 2026 | ✅ Template fourni |
| **Politique mots de passe** | Conformité ANSSI (12 car., MFA, etc.) | Q2 2026 | ✅ Consultant AD |
| **Politique télétravail** | VPN, chiffrement, écran verrouillé | Q3 2026 | ✅ Template fourni |
| **Politique BYOD** | Si appareils personnels acceptés | Q3 2026 | ✅ Template fourni |
| **Procédure gestion incidents** | Détection → Analyse → Réponse → Post-mortem | Q3 2026 | ✅ Consultant org. |
| **Plan Continuité (PCA/PRA)** | Procédures reprise activité | Q4 2026 | ✅ Consultant org. |
| **Procédure onboarding/offboarding** | Création/suppression comptes, accès | Q3 2026 | ✅ Avec RH |

### 6.2 Documentation Audit & Pilotage

| Document | Description | Fréquence |
|----------|-------------|-----------|
| **Registre des actifs** | Inventaire SI critique (serveurs, apps, données) | MAJ trimestrielle |
| **Matrice des risques cyber** | Cartographie risques + traitement | MAJ annuelle |
| **Registre traitements RGPD** | Base légale, finalités, DPO | MAJ continue |
| **Rapports de suivi audits** | Avancement remédiation vulnérabilités | Mensuel |
| **Tableau de bord KPI sécurité** | Indicateurs pilotage (voir section 7) | Mensuel |
| **Rapport sécurité Direction** | Synthèse exec. état sécurité | Trimestriel |

### 6.3 Documentation ISO 27001 (Préparation 2027-2028)

- Déclaration d'Applicabilité (SoA)
- 14 procédures obligatoires ISO 27001:2022
- Registre des risques ISO
- Plan de traitement des risques
- Politique SMSI
- Objectifs sécurité mesurables

---

## 7. Indicateurs de Suivi (KPI)

### 7.1 KPI Techniques

| KPI | Cible 2026 | Mesure | Fréquence |
|-----|------------|--------|-----------|
| **Vulnérabilités critiques** | 100% corrigées < 30j | Nb vulns / Délai moyen correction | Mensuel |
| **Vulnérabilités majeures** | 100% corrigées < 90j | Nb vulns / Délai moyen correction | Mensuel |
| **Couverture audits** | 100% applications critiques | % applications auditées / total | Annuel |
| **Score sécurité applicatif** | Amélioration +40% | OWASP ASVS Level (1→2) | Semestriel |
| **Score sécurité AD** | Amélioration +50% | PingCastle Score | Semestriel |
| **Conformité politique mdp** | 95% comptes conformes | % comptes ANSSI-compliant | Trimestriel |
| **Disponibilité plateformes** | 99.5% uptime | Monitoring | Mensuel |

### 7.2 KPI Organisationnels

| KPI | Cible 2026 | Mesure | Fréquence |
|-----|------------|--------|-----------|
| **Taux clics phishing** | < 10% (fin année) | % clics campagnes / nb destinataires | Trimestriel |
| **Formation secure coding** | 100% dev formés | % dev formés / total | Annuel |
| **Sensibilisation générale** | 100% collaborateurs | % formés / effectif | Annuel |
| **Incidents sécurité** | 0 incident majeur | Nb incidents / criticité | Mensuel |
| **Délai détection incidents** | < 24h | Temps moyen détection | Trimestriel |
| **Conformité RGPD** | 90% conformité | Score audit RGPD | Semestriel |
| **Politiques déployées** | 100% (7 politiques) | Nb politiques validées | Q3 2026 |

### 7.3 KPI Budgétaires

| KPI | Cible 2026 | Mesure | Fréquence |
|-----|------------|--------|-----------|
| **Budget consommé vs prévisionnel** | ±10% | Écart budget | Mensuel |
| **Coût moyen par vuln corrigée** | Suivi tendance | Budget remédiation / nb vulns | Trimestriel |
| **ROI programme sécurité** | Positif | Incidents évités vs coût | Annuel |

### 7.4 Tableau de Bord Mensuel (Exemple)

```
┌──────────────────────────────────────────────────────────────┐
│ TABLEAU DE BORD SÉCURITÉ - Septembre 2026 (PME)            │
├──────────────────────────────────────────────────────────────┤
│ Vulnérabilités en cours                                      │
│   🔴 Critiques    : 1  (délai: 12j)   ✅ OK                  │
│   🟠 Majeures     : 5  (délai: 52j)   ✅ OK                  │
│   🟡 Mineures     : 18 (délai: 95j)   ⚠️  Surveillance       │
├──────────────────────────────────────────────────────────────┤
│ Audits 2026                                                  │
│   ✅ Audit org.        : Terminé (Q1)                        │
│   ✅ Audit AD          : Terminé (Q1), hardening en cours    │
│   ✅ Pentest web/API   : Terminé (Q2), Re-test prévu Q4     │
│   ✅ Audit infra       : Terminé (Q2)                        │
│   ✅ Audit RGPD        : Terminé (Q2)                        │
├──────────────────────────────────────────────────────────────┤
│ Gouvernance                                                  │
│   ✅ PSSI rédigée et déployée (Sept)                        │
│   ✅ 7/7 politiques validées                                │
│   ✅ Procédure incidents opérationnelle                     │
├──────────────────────────────────────────────────────────────┤
│ Sensibilisation                                              │
│   Campagne #2 (Sept)  : 9% clics  ✅ (cible <10%)           │
│   Formation dev       : 12/12 formés ✅                      │
│   Awareness générale  : 85/90 collaborateurs (94%) ⚠️        │
├──────────────────────────────────────────────────────────────┤
│ Budget                                                       │
│   Consommé : 68 500 € / 80 000 € (86%)  ✅                  │
└──────────────────────────────────────────────────────────────┘
```

---

## 8. Plan de Formation

### 8.1 Formation Référent Sécurité

**Parcours 2026-2027 :**

| Certification | Organisme | Durée | Coût HT | Planning | Priorité |
|---------------|-----------|-------|---------|----------|----------|
| **ISO 27001 Lead Implementer** | M2i / IB Formation | 5j | 3 000 € | 2026 Q1 | ⭐⭐⭐⭐⭐ ESSENTIEL |
| **CISM** | CERTyou / EduGroupe | 5j | 4 200 € | 2026 Q4 ou 2027 Q1 | ⭐⭐⭐⭐⭐ ESSENTIEL |
| **CIPP/E** (si DPO) | PLB / Prosica | 2j | 2 000 € | 2027 Q2 | ⭐⭐⭐⭐ Recommandé |
| **ISO 27001 Lead Auditor** | PECB / CERTyou | 5j | 3 500 € | 2027 Q3 | ⭐⭐⭐⭐⭐ ESSENTIEL |
| **CISSP** (optionnel) | SysDream | 5j | 5 000 € | 2028 | ⭐⭐⭐ Optionnel |

**Budget formation référent 2026-2027 : 12 700 € HT** (ISO LI/LA + CISM + CIPP/E)

### 8.2 Formation Équipe Développement

| Formation | Contenu | Durée | Coût HT | Planning |
|-----------|---------|-------|---------|----------|
| **Secure Coding (VueJS/Symfony)** | OWASP Top 10, injections, XSS, CSRF, auth | 2j | 3 000 € - 4 500 € | 2026 Q3 |
| **API Security** | OWASP API Top 10, auth, rate limiting | 1j | 1 500 € - 2 500 € | 2027 Q1 |

**Organismes :** SysDream, EduGroupe, SANS (GWEB)

### 8.3 Sensibilisation Tous Collaborateurs

| Action | Contenu | Fréquence | Coût annuel HT |
|--------|---------|-----------|----------------|
| **Campagnes phishing** | Simulations réalistes | 3-4x/an | 3 000 € - 5 000 € |
| **Sessions awareness** | Bonnes pratiques, hygiene cyber | 2x/an | 2 000 € - 3 000 € |
| **E-learning continu** | Modules courts (phishing, mdp, etc.) | Accès permanent | 2 000 € - 4 000 € (abo plateforme) |

---

## Résumé Exécutif

### Pour la Direction (PME)

**Contexte :** En tant que PME fintech manipulant données financières SCPI sensibles, nous devons structurer notre cybersécurité pour :
- Éviter sanctions RGPD (jusqu'à 20M€)
- Protéger notre réputation et confiance clients
- Obtenir assurance cyber (exige audits)
- Préparer croissance (certification ISO 27001 différenciante)

**Programme 2026 Proposé :** Structuration complète sécurité en 4 phases.

**Investissement 2026 :** 75 000 € - 95 000 € HT (90-114k€ TTC)
**Investissement récurrent (2027) :** 60 000 € - 90 000 € HT/an (préparation ISO 27001)
**Investissement récurrent (2029+) :** 50 000 € - 75 000 € HT/an (maintien certifié)

**Actions clés 2026 :**
1. **Diagnostic complet** (org., AD) → Roadmap 3 ans
2. **Audits techniques** (pentest, infra, RGPD) → Identification vulnérabilités
3. **Gouvernance** (PSSI, 7 politiques) → Cadre structuré
4. **Formation équipe** → Montée compétences

**Bénéfices :**
- ✅ Conformité RGPD complète
- ✅ Réduction significative risque cyber
- ✅ Gouvernance sécurité professionnelle
- ✅ Équipe formée et sensibilisée
- ✅ Préparation ISO 27001 (2027-2028)
- ✅ Assurabilité cyber améliorée

**Décisions attendues :**
1. Validation budget 2026 (75-95k€)
2. Validation embauche/nomination référent sécurité dédié
3. Validation roadmap 3 ans (ISO 27001 en 2028)

**ROI :** Investissement largement rentabilisé par :
- Évitement 1 incident majeur (coût moyen : 100-500k€)
- Évitement sanctions RGPD
- Différenciation commerciale (ISO 27001)
- Réduction prime assurance cyber (20-30%)

---

## Prochaines Étapes (Décembre 2025 - Janvier 2026)

**Immédiat :**
- [ ] Présenter ce document à la Direction
- [ ] Valider budget 2026 (75-95k€)
- [ ] Valider poste référent sécurité dédié (50-100%)
- [ ] Identifier 3-5 consultants pour diagnostic org.

**Janvier 2026 :**
- [ ] Lancer appel d'offres diagnostic org. + audit AD
- [ ] Sélection prestataires (critères : PASSI, expérience PME fintech, tarifs)
- [ ] Inscription formation ISO 27001 Lead Implementer (Fév-Mars)
- [ ] Kick-off projet avec CTO/DSI

**Février-Mars 2026 :**
- [ ] Démarrage diagnostic organisationnel
- [ ] Démarrage audit Active Directory
- [ ] Formation référent (ISO 27001 LI)
- [ ] Réception rapports + présentation Direction
- [ ] Validation budget Q2-Q4 selon recommandations

---

**Document validé par :** ________________
**Date :** ___/___/2026

**Version :** 1.0 PME (30-100 employés)
**Prochaine révision :** Post-diagnostic (Avril 2026)
