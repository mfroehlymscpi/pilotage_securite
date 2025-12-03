# Pilotage Sécurité - Documentation Projet

**Programme de cybersécurité 2026**
Fintech conseil en investissement SCPI

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

Structurer, piloter et coordonner la cybersécurité de l'entreprise **sans internaliser l'exécution technique**.

**Rôle interne :** Référent sécurité / Chef de projet sécurité
**Mission :** Sélectionner et piloter les prestataires externes (pentest, audits, certifications)

---

## 📄 Document Principal

### [Pilotage_Securite_2026.md](./Pilotage_Securite_2026.md)

Le document de référence contenant :

| Section | Contenu |
|---------|---------|
| **1. Introduction** | Contexte, objectifs, périmètre technique |
| **2. Risques & Enjeux** | Cartographie cyberrisques, impact business |
| **3. Organisation** | Rôles, interlocuteurs internes/externes |
| **4. Roadmap 2026** | Planning trimestriel détaillé (Q1-Q4) |
| **5. Budget** | 139 700 € HT en 2026, 70-80k€/an ensuite |
| **6. Livrables** | Documents à produire (PSSI, politiques, KPI) |
| **7. KPIs** | Indicateurs techniques, org., budgétaires |
| **8. Formation** | Plan de formation référent + équipe dev |

**Usage :** Document à présenter à la Direction pour validation budget/roadmap

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

## 📊 Chiffres Clés 2026

| Indicateur | Valeur |
|------------|--------|
| **Budget total** | 139 700 € HT (≈ 167k€ TTC) |
| **Audits applicatifs** | 18 000 € (pentest VueJS/Symfony/API) |
| **Certification ISO 27001** | 40 000 € (accompagnement + certif) |
| **Formation référent** | 12 700 € (4 certifications) |
| **Audits RGPD** | 18 000 € (initial + suivi) |
| **Sensibilisation phishing** | 5 000 € (3 campagnes/an) |

**Budget récurrent (2027+) :** 70 000 € - 80 000 € HT/an

---

## 🗓️ Roadmap 2026

```
Q1 (Jan-Mars)          Q2 (Avr-Juin)          Q3 (Juil-Sep)          Q4 (Oct-Déc)
│                      │                      │                      │
│ DIAGNOSTIC           │ APPLICATIF & RGPD    │ REMÉDIATION          │ CERTIFICATION
│                      │                      │                      │
├─ Audit org.          ├─ Pentest web/API     ├─ Corrections vulns  ├─ Certification ISO
├─ Audit AD            ├─ Audit RGPD          ├─ Formation dev      ├─ Re-test pentest
├─ Audit infra         ├─ Phishing #1         ├─ Rédaction PSSI     ├─ Bilan annuel
├─ Formation ISO LI    ├─ Formation CISM      ├─ Accompagnement ISO ├─ Formation Lead Auditor
└─ 29 000 €            └─ 41 200 €            └─ 43 500 €           └─ 26 000 €
```

**Jalon critique :** Certification ISO 27001 obtenue Q4 2026

---

## 🎓 Certifications Prioritaires Référent Sécurité

| Certification | Trimestre 2026 | Coût HT | Organisme |
|---------------|----------------|---------|-----------|
| ISO 27001 Lead Implementer | Q1 (Janvier) | 3 000 € | M2i / IB Formation |
| CISM | Q2 (Avril) | 4 200 € | CERTyou / EduGroupe |
| CIPP/E | Q2 (Juin) | 2 000 € | PLB / Prosica |
| ISO 27001 Lead Auditor | Q4 (Octobre) | 3 500 € | PECB / CERTyou |

**TOTAL :** 12 700 € HT / 17 jours

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

---

## 📞 Contacts & Ressources

### Organismes Certificateurs
- **ISACA** (CISM) : [isaca.org](https://www.isaca.org)
- **(ISC)²** (CISSP) : [isc2.org](https://www.isc2.org)
- **PECB** (ISO 27001) : [pecb.com](https://pecb.com)
- **IAPP** (CIPP/E) : [iapp.org](https://iapp.org)

### Autorités & Référentiels
- **ANSSI** (guides sécurité) : [cyber.gouv.fr](https://cyber.gouv.fr)
- **CNIL** (RGPD) : [cnil.fr](https://www.cnil.fr)
- **OWASP** (AppSec) : [owasp.org](https://owasp.org)
- **AFNOR** (ISO 27001 certification) : [certification.afnor.org](https://certification.afnor.org)

### Organismes Formation France
- **EduGroupe** : [edugroupe.com](https://edugroupe.com)
- **CERTyou** : [certyou.com](https://www.certyou.com)
- **SysDream** : [sysdream.com](https://sysdream.com)
- **M2i Formation** : [m2iformation.fr](https://www.m2iformation.fr)

---

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
