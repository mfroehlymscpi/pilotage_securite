# Pilotage Sécurité - Documentation Projet

**Programme de cybersécurité 2026**
Startup Fintech SCPI (< 10 employés)

---

## 📁 Structure du Repository

```
pilotage_securite/
│
├── 📄 Pilotage_Securite_2026.md       # DOCUMENT PRINCIPAL
│   └── Roadmap, budget, KPIs, plan formation, livrables
│
├── 📂 annexes/
│   ├── A_Selection_Prestataires.md    # Guide sélection prestataires
│   ├── B_Catalogue_Certifications.md  # Catalogue certifications
│   └── C_Glossaire.md                 # Glossaire technique
│
├── 📂 archive/                        # Documents de travail archivés
│
├── CLAUDE.md                          # Guide pour Claude Code
├── README.md                          # Ce fichier
└── .gitignore
```

---

## 🎯 Objectif du Projet

**Approche pragmatique** pour startup < 10 employés : structurer **progressivement** la cybersécurité en s'appuyant sur des prestataires externes.

**Rôle interne :** Référent sécurité (temps partiel, 1-2j/mois)
**Mission :** Coordonner prestataires pour diagnostic, audits ciblés, et mise en conformité RGPD

---

## 📄 Document Principal

### [Pilotage_Securite_2026.md](./Pilotage_Securite_2026.md)

Le document de référence contenant :

| Section | Contenu |
|---------|---------|
| **1. Introduction** | Contexte startup < 10 pers, contraintes budget |
| **2. Risques & Enjeux** | 5 risques cyber prioritaires startup |
| **3. Organisation** | Référent temps partiel + prestataires conseils |
| **4. Approche Pragmatique** | Ce qu'on fait / ne fait pas en 2026 |
| **5. Phase 1 (2026)** | Q1 Diagnostic → Q2 Audits → Q3-Q4 Actions |
| **6. Budget** | 20-28k€ HT en 2026, 13-20k€/an ensuite |
| **7. Livrables** | Essentiels fournis par prestataires + templates |
| **8. KPI** | 5 indicateurs simples de suivi |

**Usage :** Document à présenter Direction pour validation budget 20-28k€

---

## 📚 Annexes

### [Annexe A : Sélection des Prestataires](./annexes/A_Selection_Prestataires.md)

**9 prestataires pentest** comparés (Vaadata, SysDream, Wavestone, Connect3S, etc.)
- Certifications (OSWE, OSCP, GWEB, PASSI ANSSI)
- TJM estimés (600 € - 1 500 €/jour)
- Coûts pentests (3 000 € - 60 000 €)

**+** Prestataires audits infra, org., AD, Red Team, sensibilisation

**Grille de sélection** avec critères obligatoires et recommandés

### [Annexe B : Catalogue Certifications](./annexes/B_Catalogue_Certifications.md)

**Certifications gouvernance** (référent sécurité) :
- ISO 27001 Lead Implementer (3 000 €, 5j)
- CISM (4 200 €, 5j)
- CIPP/E (2 000 €, 2j)
- ISO 27001 Lead Auditor (3 500 €, 5j)

**Certifications techniques** (critères évaluation prestataires) :
- OSWE, GWEB, eWPTX (obligatoires pour pentest AppSec)
- OSCP (recommandé)

**Total formation référent 2026 :** 12 700 € HT

### [Annexe C : Glossaire](./annexes/C_Glossaire.md)

Définitions techniques vulgarisées :
- Pentest, AppSec, RGPD, ISO 27001, Active Directory
- OWASP Top 10, SIEM, SOC, WAF, XSS, etc.
- Acronymes courants (ANSSI, PASSI, SMSI, etc.)

**Usage :** Référence pour présentation non-technique

---

## 📊 Chiffres Clés 2026 (Startup)

| Indicateur | Valeur |
|------------|--------|
| **Budget total 2026** | 20 000 € - 28 000 € HT (24-34k€ TTC) |
| **Diagnostic initial** | 3 000 € - 6 000 € (consultant 3-5j) |
| **Pentest applicatif** | 5 000 € - 8 000 € (VueJS/Symfony/API) |
| **Audit RGPD** | 5 000 € - 8 000 € (conformité minimale) |
| **Sensibilisation** | 1 500 € - 2 500 € (2 campagnes phishing) |
| **Formation dev** | 1 500 € - 2 500 € (secure coding 1j) |

**Budget récurrent (2027+) :** 13 000 € - 20 000 € HT/an

---

## 🗓️ Roadmap 2026 (Startup)

```
Q1 (Jan-Mars)          Q2 (Avr-Juin)          Q3-Q4 (Juil-Déc)
│                      │                      │
│ DIAGNOSTIC           │ AUDITS CIBLÉS        │ ACTIONS & FORMATION
│                      │                      │
├─ Diagnostic 360°     ├─ Pentest web/API     ├─ Corrections vulns critiques
├─ Roadmap 3 ans       ├─ Audit RGPD          ├─ Phishing #1 et #2
├─ Modèles politiques  ├─ Rapports            ├─ Formation dev (1j)
│                      │                      ├─ Politiques de base
└─ 3-6k€               └─ 10-16k€             └─ 5-9k€
```

**Jalon critique :** Vulnérabilités critiques corrigées Q3 2026

---

## 🎓 Formation (Startup)

**Approche :** Pas de certifications référent en 2026 (hors budget startup).
**Alternative :** S'appuyer sur l'expertise des prestataires pour conseil.

**Formation équipe dev :**
- Atelier secure coding OWASP (1j, 6-8 personnes) : 1 500 € - 2 500 €
- Formation par prestataire pentest (inclus dans mission)

**Montée en compétence :** Si croissance future (50+ employés), envisager certifications référent

---

## 🔍 Sélection Prestataires Pentest

### Critères Obligatoires

✅ **Au moins 1 certification parmi :** OSWE / GWEB / eWPTX
✅ **Références fintech/finance**
✅ **Méthodologie OWASP** (Top 10, ASVS)
✅ **Rapport détaillé** (technique + exec, CVSS, PoC)

### Bonus

⭐ Qualification **PASSI ANSSI**
⭐ Support post-audit (3-6 mois)
⭐ Restitution orale équipe technique

### Prestataires Recommandés (Notre Contexte)

| Prestataire | Certifications | PASSI | TJM | Coût 5j |
|-------------|----------------|-------|-----|---------|
| **SysDream** | OSWE, OSCP, GWEB, eWPTX | ✅ | 950-1 200 € | 4 750 € - 6 000 € |
| **Wavestone** | OSWE, OSCP, GWEB | ✅ | 1 000-1 500 € | 5 000 € - 7 500 € |
| **Vaadata** | OSWE, OSCP, eWPTX | ❌ | 600-900 € | 1 200 € - 6 500 € |
| **Connect3S** | OSWE, OSCP, GWEB | ❌ | 700-950 € | 3 500 € - 5 000 € |

---

## 📈 KPI Cibles 2026

### Techniques
- 🔴 **Vulns critiques** : 100% corrigées < 30 jours
- 🟠 **Vulns majeures** : 100% corrigées < 90 jours
- ✅ **Couverture audits** : 100% applications critiques

### Organisationnels
- 🎣 **Taux clics phishing** : < 10%
- 🎓 **Formation dev** : 100% développeurs formés OWASP
- 📜 **Conformité RGPD** : ≥ 90%
- 🏆 **Certification ISO 27001** : Obtenue Q4 2026

### Budgétaires
- 💰 **Écart budget** : ±10% du prévisionnel

## 📝 Livrables Attendus 2026

### Q1-Q3 : Gouvernance
- [ ] Politique Sécurité SI (PSSI)
- [ ] Charte d'utilisation SI
- [ ] Politique mots de passe (conformité ANSSI)
- [ ] Politique télétravail / nomadisme
- [ ] Charte utilisation LLM
- [ ] Procédure gestion incidents

### Q3-Q4 : ISO 27001
- [ ] Déclaration d'Applicabilité (SoA)
- [ ] 14 procédures obligatoires ISO 27001:2022
- [ ] Registre des risques ISO
- [ ] Plan traitement risques
- [ ] Politique SMSI

### Continue : Pilotage
- [ ] Registre des actifs (MAJ trimestrielle)
- [ ] Matrice des risques cyber (MAJ annuelle)
- [ ] Registre traitements RGPD (MAJ continue)
- [ ] Tableau de bord KPI (mensuel)
- [ ] Rapport sécurité Direction (trimestriel)

---

## ⚠️ Points d'Attention

### Ce Projet N'EST PAS
- ❌ Exécution technique (pentest, config firewall, etc.)
- ❌ Opérations SOC/CERT
- ❌ Administration infrastructure
- ❌ Développement logiciel

### Ce Projet EST
- ✅ **Pilotage** et coordination sécurité
- ✅ **Sélection** et suivi prestataires
- ✅ **Rédaction** politiques et procédures
- ✅ **Reporting** direction et suivi KPI
- ✅ **Formation** et sensibilisation

---

## 🚀 Prochaines Étapes (Décembre 2025)

1. **Présenter roadmap à la Direction**
   - Document : `Pilotage_Securite_2026.md`
   - Focus : Budget 139 700 €, ISO 27001 Q4 2026

2. **Valider budget 2026**
   - Détails par poste dans section 5 du document principal

3. **Identifier consultants ISO 27001**
   - Voir `annexes/A_Selection_Prestataires.md` section audits org.

4. **Préparer appels d'offres Q1**
   - Audits org., AD, infra
   - Cahiers des charges à rédiger

---

**Version :** 1.0 - Décembre 2025
**Prochaine révision :** Trimestrielle (fin Q1 2026)
