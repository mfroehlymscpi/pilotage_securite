# Pilotage Sécurité 2026

**Document de référence - Programme de sécurité informatique**
Startup Fintech SCPI (< 10 employés)
Version 2.0 - Décembre 2025

---

## 📋 Sommaire

1. [Introduction & Contexte](#1-introduction--contexte)
2. [Risques & Enjeux Métier](#2-risques--enjeux-métier)
3. [Organisation & Rôles](#3-organisation--rôles)
4. [Approche Pragmatique](#4-approche-pragmatique)
5. [Phase 1 : Diagnostic Initial (2026)](#5-phase-1--diagnostic-initial-2026)
6. [Budget Prévisionnel Phase 1](#6-budget-prévisionnel-phase-1)
7. [Livrables Essentiels](#7-livrables-essentiels)
8. [Indicateurs de Suivi](#8-indicateurs-de-suivi)

**Annexes :**
- [Annexe A : Guide de Sélection des Prestataires](./annexes/A_Selection_Prestataires.md)
- [Annexe B : Catalogue des Certifications](./annexes/B_Catalogue_Certifications.md)

---

## 1. Introduction & Contexte

### 1.1 Présentation du Projet

Le projet **Pilotage Sécurité** vise à **structurer progressivement** la cybersécurité d'une startup fintech spécialisée SCPI, **en s'appuyant sur des prestataires externes** pour l'expertise technique.

**Contexte entreprise :**
- Startup < 10 employés
- Applications web (VueJS, Symfony) et API REST
- Données financières sensibles (SCPI)
- Croissance progressive, budget limité

### 1.2 Objectifs

1. **Identifier les risques cyber critiques** via un diagnostic initial
2. **Prioriser les actions** selon impact business et budget
3. **S'appuyer sur des prestataires** pour conseil et exécution technique
4. **Structurer progressivement** : gouvernance minimale puis montée en maturité

### 1.3 Périmètre Technique

| Périmètre | Technologies | Criticité Startup |
|-----------|--------------|-------------------|
| **Applications web** | VueJS, Symfony | 🔴 Critique (cœur métier) |
| **API agrégation SCPI** | REST API | 🔴 Critique (données sensibles) |
| **Infrastructure** | Serveurs, Docker | 🟠 Importante |
| **Données clients** | BDD, fichiers | 🔴 Critique (RGPD) |

### 1.4 Contraintes Startup

**Ressources limitées :**
- ❌ Pas de RSSI dédié temps plein
- ❌ Pas d'équipe sécurité interne
- ❌ Budget contraint (< 30-40k€/an)
- ✅ Besoin pragmatique : commencer simple, prioriser l'essentiel

**Approche retenue :** Diagnostic initial → Priorisation → Actions ciblées

---

## 2. Risques & Enjeux Métier

### 2.1 Cartographie des Risques Cyber (Startup)

| Risque | Impact Startup | Probabilité | Criticité | Action Prioritaire |
|--------|----------------|-------------|-----------|-------------------|
| **Fuite données clients** | - Sanction RGPD<br>- Perte confiance | Moyenne | 🔴 CRITIQUE | Audit RGPD léger + mise conformité |
| **Compromission appli web** | - Indisponibilité<br>- Perte clients | Moyenne | 🔴 CRITIQUE | Pentest applicatif ciblé |
| **Phishing collaborateurs** | - Accès frauduleux<br>- Vol données | Élevée | 🟠 MAJEUR | Sensibilisation (simple) |
| **Injection API** | - Corruption données | Faible | 🟠 MAJEUR | Pentest API |
| **Perte/vol matériel** | - Accès données locales | Moyenne | 🟡 MODÉRÉ | Chiffrement, politique BYOD |

**Focus startup :** Traiter d'abord 🔴 CRITIQUE avec budget limité

### 2.2 Enjeux Business

**Pour la Direction :**
- Éviter sanction RGPD (peut tuer une startup)
- Protéger réputation (clients B2C sensibles données finance)
- Assurer disponibilité plateforme (revenus)

**Pour l'IT :**
- Sécuriser applis sans ralentir développement
- Bonnes pratiques dev (secure coding basique)

---

## 3. Organisation & Rôles

### 3.1 Rôle Référent Sécurité (Interne, Temps Partiel)

**Mission :** Coordination sécurité, **PAS d'exécution technique**

**Responsabilités :**
- ✅ Identifier prestataire pour diagnostic initial
- ✅ Suivre recommandations prestataires
- ✅ Rédiger politiques simples (avec aide prestataire)
- ✅ Organiser sensibilisation phishing (campagne simple)
- ❌ PAS de pentest interne
- ❌ PAS de config firewall/infra
- ❌ PAS d'audit technique

**Temps estimé :** 1-2 jours/mois (20-40h/an)

### 3.2 Prestataires Externes

**Rôle clé :** Les prestataires doivent **CONSEILLER** la startup sur :
- Quelles politiques mettre en place (adaptées à une TPE)
- Quelles bonnes pratiques adopter
- Quelle gouvernance minimale (pragmatique, pas ISO 27001 tout de suite)

| Type Prestataire | Mission | Quand ? |
|------------------|---------|---------|
| **Consultant sécurité généraliste** | Diagnostic 360° + roadmap | Phase 1 (2026 Q1) |
| **Pentester AppSec** | Audit applications VueJS/Symfony/API | Phase 1 (2026 Q2) |
| **Consultant RGPD** | Audit RGPD léger + mise conformité | Phase 1 (2026 Q2-Q3) |
| **Formation/Sensibilisation** | Campagne phishing, bonnes pratiques dev | Phase 1 (2026 Q3-Q4) |

---

## 4. Approche Pragmatique

### 4.1 Principe : Commencer Simple

**Ce qu'on NE FAIT PAS en 2026 (trop tôt pour une startup) :**
- ❌ Certification ISO 27001 (40-50k€, trop complexe pour < 10 pers)
- ❌ Certifications multiples référent (12k€+, pas prioritaire)
- ❌ Red Team / intrusion physique (30-60k€, hors budget)
- ❌ Audits infrastructure lourds (serveurs gérés par hébergeur probablement)
- ❌ Audits Active Directory (si pas d'AD interne)
- ❌ Outils sécurité coûteux (SIEM, SAST/DAST enterprise)

**Ce qu'on FAIT en 2026 (essentiel startup) :**
- ✅ **Diagnostic sécurité initial** par consultant expérimenté
- ✅ **Pentest applicatif ciblé** (VueJS/Symfony/API)
- ✅ **Audit RGPD pragmatique** (conformité minimale)
- ✅ **Sensibilisation phishing** (campagne simple, pas chère)
- ✅ **Politiques de base** (mots de passe, télétravail, BYOD)
- ✅ **Bonnes pratiques dev** (formation secure coding légère)

### 4.2 Philosophie : Prestataires = Conseil + Exécution

Les prestataires doivent :
1. **Diagnostiquer** l'existant
2. **Conseiller** sur les priorités adaptées à une startup
3. **Exécuter** les audits techniques (pentest)
4. **Accompagner** la mise en conformité (RGPD)
5. **Former** l'équipe (bonnes pratiques)

**Le référent interne** coordonne et suit, mais s'appuie à 100% sur leur expertise.

---

## 5. Phase 1 : Diagnostic Initial (2026)

### Vue d'ensemble

```
Q1 2026              Q2 2026              Q3-Q4 2026
│                    │                    │
│ DIAGNOSTIC         │ AUDITS CIBLÉS      │ ACTIONS & FORMATION
│                    │                    │
▼                    ▼                    ▼
```

### Q1 2026 (Jan-Mars) - Diagnostic & Priorisation

**Action 1 : Diagnostic Sécurité Initial**

| Prestataire | Mission | Durée | Budget |
|-------------|---------|-------|--------|
| Consultant sécurité généraliste | - Analyse existant (applis, infra, orga)<br>- Cartographie risques startup<br>- Roadmap priorisée 3 ans<br>- Conseil gouvernance minimale | 3-5 jours | 3 000 € - 6 000 € |

**Livrables attendus :**
- Rapport diagnostic (forces, faiblesses, risques)
- Roadmap priorisée selon budget startup
- Modèles politiques de base (mots de passe, télétravail)
- Recommandations audits prioritaires

**Jalons :**
- Fin mars : Présentation diagnostic à la Direction
- Validation budget actions Q2-Q4

---

### Q2 2026 (Avr-Juin) - Audits Applicatifs

**Action 2 : Pentest Applicatif Ciblé**

| Prestataire | Mission | Durée | Budget |
|-------------|---------|-------|--------|
| Pentester AppSec (OSWE/GWEB) | - Pentest VueJS (front)<br>- Pentest Symfony (back)<br>- Pentest API agrégation SCPI<br>- Tests OWASP Top 10 | 5-7 jours | 5 000 € - 8 000 € |

**Livrables :**
- Rapport vulnérabilités (criticité CVSS)
- Preuves de concept (PoC) exploitabilité
- Recommandations corrections priorisées
- Re-test après corrections (1j inclus)

**Action 3 : Audit RGPD Pragmatique**

| Prestataire | Mission | Durée | Budget |
|-------------|---------|-------|--------|
| Consultant RGPD/DPO | - Audit conformité RGPD<br>- Registre traitements<br>- Politique confidentialité<br>- Mentions légales<br>- Accompagnement mise conformité | 5-7 jours | 5 000 € - 8 000 € |

**Livrables :**
- Registre des traitements
- Modèles documents (politique confidentialité, CGU)
- Plan d'actions conformité
- Support questions RGPD (3 mois)

**Jalons Q2 :**
- Fin juin : Rapports pentest + RGPD validés
- Priorisation corrections (critiques < 1 mois, majeures < 3 mois)

---

### Q3-Q4 2026 (Juil-Déc) - Remédiation & Formation

**Action 4 : Corrections Vulnérabilités**

| Qui | Mission | Durée | Budget |
|-----|---------|-------|--------|
| Équipe dev interne | Correction vulnérabilités critiques/majeures | Variable | Temps interne |
| Pentester (support) | Support questions corrections (optionnel) | 1-2 jours | 1 000 € - 2 000 € |

**Action 5 : Sensibilisation & Formation**

| Prestataire | Mission | Durée | Budget |
|-------------|---------|-------|--------|
| Plateforme phishing (Intuity, Exodata) | 2 campagnes phishing (Juil + Oct) | - | 1 500 € - 2 500 € |
| Formation secure coding | Atelier OWASP Top 10 pour dev (1j, 6-8 pers) | 1 jour | 1 500 € - 2 500 € |

**Action 6 : Politiques de Base**

| Qui | Mission | Durée | Budget |
|-----|---------|-------|--------|
| Référent interne + templates prestataire | Rédaction politique mots de passe, télétravail, BYOD | 2-3 jours | Temps interne |

**Jalons Q3-Q4 :**
- Sept : 100% vulnérabilités critiques corrigées
- Oct : Campagne phishing #2, taux clics < 20%
- Déc : Politiques de base déployées, bilan 2026

---

## 6. Budget Prévisionnel Phase 1

### Budget 2026 (Startup < 10 pers)

| Poste | Détail | Budget HT |
|-------|--------|-----------|
| **Diagnostic initial** | Consultant sécurité (3-5j) | 3 000 € - 6 000 € |
| **Pentest applicatif** | VueJS + Symfony + API (5-7j) | 5 000 € - 8 000 € |
| **Audit RGPD** | Audit + accompagnement (5-7j) | 5 000 € - 8 000 € |
| **Support remédiation** | Assistance correctifs (1-2j) | 1 000 € - 2 000 € |
| **Sensibilisation phishing** | 2 campagnes annuelles | 1 500 € - 2 500 € |
| **Formation dev** | Secure coding OWASP (1j) | 1 500 € - 2 500 € |
| **Contingence (10%)** | Imprévus, audits complémentaires | 1 700 € - 2 900 € |
| **TOTAL 2026** | | **18 700 € - 32 000 € HT** |

**Fourchette réaliste startup : 20 000 € - 28 000 € HT (24-34k€ TTC)**

### Budget Années Suivantes (2027-2028)

| Poste | Fréquence | Budget annuel HT |
|-------|-----------|------------------|
| **Pentest applicatif** | 1x/an (re-test après évolutions) | 5 000 € - 8 000 € |
| **Audit RGPD suivi** | 1x/2 ans | 2 000 € - 3 000 € (moyen.) |
| **Sensibilisation** | 2 campagnes/an | 1 500 € - 2 500 € |
| **Formation** | Selon besoins | 1 000 € - 2 000 € |
| **Consultant ad-hoc** | Questions ponctuelles | 2 000 € - 3 000 € |
| **Contingence** | 10% | 1 100 € - 1 800 € |
| **TOTAL ANNUEL (2027+)** | | **12 600 € - 20 300 € HT/an** |

**Montée en maturité progressive :**
- **Année 3-4** (2028-2029) : Si croissance, envisager certification ISO 27001 légère
- **Année 5+** : Si > 50 employés, budget sécurité évolue (30-50k€/an)

---

## 7. Livrables Essentiels

### 7.1 Livrables Prestataires (2026)

| Livrable | Qui | Quand | Usage |
|----------|-----|-------|-------|
| **Rapport diagnostic sécurité** | Consultant initial | Q1 | Roadmap 3 ans, priorisation |
| **Rapport pentest applicatif** | Pentester | Q2 | Corrections dev |
| **Registre traitements RGPD** | Consultant RGPD | Q2 | Conformité, site web |
| **Politique confidentialité** | Consultant RGPD | Q2 | Site web (mentions légales) |
| **Rapports phishing** | Plateforme sensibilisation | Q3-Q4 | Mesure maturité collaborateurs |

### 7.2 Livrables Internes (À Créer avec Aide Prestataire)

| Livrable | Basé sur | Quand | Description |
|----------|----------|-------|-------------|
| **Politique mots de passe** | Template prestataire | Q3 | Règles simples (12 car., MFA comptes admin) |
| **Politique télétravail** | Template prestataire | Q3 | VPN, écran verrouillé, pas de WiFi public |
| **Politique BYOD** | Template prestataire | Q3 | Si appareils perso acceptés |
| **Procédure incident** | Template prestataire | Q4 | Qui contacter si suspicion piratage |

**Note :** Les prestataires doivent fournir des **templates adaptés TPE** (pas des PSSI de 50 pages).

---

## 8. Indicateurs de Suivi

### 8.1 KPI Essentiels Startup

| KPI | Cible 2026 | Mesure | Fréquence |
|-----|------------|--------|-----------|
| **Vulnérabilités critiques** | 100% corrigées < 30j | Suivi post-pentest | Mensuel |
| **Conformité RGPD** | Registre à jour, politique en ligne | Checklist consultant | Trimestriel |
| **Sensibilisation phishing** | < 20% taux clics (débutant) | Campagnes | Semestriel |
| **Formation dev** | 100% dev formés OWASP | Présence atelier | Annuel |
| **Budget sécurité** | Dépensé dans fourchette 20-28k€ | Suivi compta | Trimestriel |

**Objectif 2027 :**
- Taux clics phishing < 15%
- 0 vulnérabilité critique non corrigée

### 8.2 Tableau de Bord Simple (Exemple Fin 2026)

```
┌─────────────────────────────────────────────────────┐
│ BILAN SÉCURITÉ 2026 - Startup SCPI                 │
├─────────────────────────────────────────────────────┤
│ ✅ Diagnostic initial réalisé (Q1)                  │
│ ✅ Pentest applicatif terminé (Q2)                  │
│    → 3 vulns critiques détectées, toutes corrigées │
│    → 7 vulns majeures, 6 corrigées (1 planifiée)   │
│ ✅ Audit RGPD terminé (Q2)                          │
│    → Registre créé, politique en ligne             │
│ ✅ 2 campagnes phishing (Juil + Oct)                │
│    → Taux clics : 25% → 18%  📈 Amélioration       │
│ ✅ Formation dev OWASP (Sept)                       │
│    → 6/6 dev formés                                 │
├─────────────────────────────────────────────────────┤
│ Budget : 24 500 € / 28 000 € (88%)  ✅             │
└─────────────────────────────────────────────────────┘
```

---

## Résumé Exécutif

### Pour la Direction (Startup)

**Contexte :** En tant que startup fintech < 10 employés manipulant données financières sensibles, nous sommes exposés à des cyberrisques. Un incident majeur ou une sanction RGPD pourrait compromettre l'entreprise.

**Programme 2026 Proposé :** Approche pragmatique centrée sur l'essentiel.

**Investissement 2026 :** 20 000 € - 28 000 € HT (24-34k€ TTC)
**Investissement récurrent :** 13 000 € - 20 000 € HT/an (2027+)

**Actions clés :**
1. **Diagnostic initial** par consultant expérimenté → Roadmap 3 ans
2. **Pentest applicatif** → Corrections vulnérabilités critiques
3. **Audit RGPD** → Mise en conformité minimale
4. **Sensibilisation équipe** → Réduire risque phishing

**Bénéfices :**
- ✅ Conformité RGPD (éviter sanctions)
- ✅ Réduction risque piratage applications
- ✅ Équipe sensibilisée (phishing, bonnes pratiques)
- ✅ Roadmap claire pour croissance future

**Décisions attendues :**
1. Validation budget 20-28k€ pour 2026
2. Validation lancement diagnostic Q1 2026

**ROI :** Éviter 1 seul incident cyber ou sanction RGPD rembourse largement l'investissement.

---

## Prochaines Étapes (Décembre 2025 - Janvier 2026)

**Immédiat :**
- [ ] Présenter ce document à la Direction
- [ ] Valider budget 2026 (fourchette 20-28k€)
- [ ] Identifier 2-3 consultants sécurité pour diagnostic initial

**Janvier 2026 :**
- [ ] Lancer appel d'offres diagnostic (3 devis)
- [ ] Sélection prestataire (critères : expérience startup, tarif, références)
- [ ] Démarrage diagnostic (fin janvier / début février)

**Février-Mars 2026 :**
- [ ] Réception rapport diagnostic
- [ ] Présentation résultats + roadmap à l'équipe
- [ ] Validation audits Q2 (pentest + RGPD)

---

**Document validé par :** ________________
**Date :** ___/___/2026

**Version :** 2.0 (Adaptée startup < 10 employés)
**Prochaine révision :** Post-diagnostic (Mars 2026)
