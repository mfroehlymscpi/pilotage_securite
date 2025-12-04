# Workflow habituel

## Documentation : 

* [ISO prioritaires](IsoPrioritaires.md)
* [Lsite des ISO officiels pertinents](IsoPertinents.md)
* [Exemple ISO 27005](Demo27005.md)
* [📞 Contacts & Ressources](Phase2_Contacts.md)

--- 

### ✅ **Workflow ISO 27005 — Version Résumée (+ durées)**
1. **Cadrage du périmètre**
   *Définir ce qui est inclus dans l’analyse.*
   **Durée : 0,5 à 1 jour**

2. **Inventaire des actifs**
   *Lister ce qui doit être protégé (humains, données, apps, serveurs, SaaS…).*
   **Durée : 1 à 3 jours**

3. **Identification des menaces**
   *Ce qui peut attaquer les actifs.*
   **Durée : 0,5 à 2 jours**

4. **Identification des vulnérabilités**
   *Faiblesses existantes permettant une attaque.*
   **Durée : 1 à 2 jours**

5. **Construction des scénarios de risques**
   *Actif + Menace + Vulnérabilité → Scénario.*
   **Durée : 1 à 2 jours**

6. **Évaluation des risques**
   *Probabilité × Impact → Criticité.*
   **Durée : 0,5 à 1 jour**

7. **Plan de traitement des risques**
   *Mesures prioritaires, quick wins → actions long terme.*
   **Durée : 1 à 2 jours**

8. **Alignement ISO 27002**
   *Traduction en mesures de sécurité techniques et organisationnelles.*
   **Durée : 1 jour**

9. **Rapport final + restitution**
   *Document ISO 27005 complet + recommandations.*
   **Durée : 1 jour**

---
### ⏱️ **Durée totale estimée : 6 à 13 jours**
(typique pour une PME / fintech de votre taille)

---

Si tu veux, je peux t’en générer une **version ultra-courte** style bullet points pour la direction.


Voici **un workflow professionnel, clair et complet**, correspondant à **la vraie manière** dont une mission ISO 27005 est réalisée dans une PME / fintech / SaaS.
Tu peux l’utiliser tel quel pour ton dossier *Pilotage Sécurité* ou pour briefer un prestataire.

Je te détaille :

* les **pré-requis** (avant ISO 27005)
* le **workflow ISO 27005** (la mission elle-même)
* ce qu’on fait **après ISO 27005**
* la manière dont ça s’intègre dans ISO 27001 / 27002

C’est la version sérieuse, utilisée par les prestataires cybersécurité.

---

# 🟦 **1. Étapes AVANT l’analyse ISO 27005**

(*préparation / cadrage / collecte d’informations*)

### **1.1. Définition du périmètre**

* Quels systèmes ? (Monujo, admin, API SCPI, back Symfony, CI/CD…)
* Quelles données ? (clients, utilisateurs, SCPI, financiers, RGPD…)
* Quels environnements ? (prod, staging, local dev, mobile Capacitor)
* Quels prestataires ? (hébergeur, société de gestion, SaaS…)
* Quels employés concernés ?

### **1.2. Description de l’entreprise**

* Activité (fintech / data / agrégation SCPI)
* Processus métier (investissement, conseil, data, dashboards…)
* Organigramme sécurité (Rôle référent, CTO, devs…)

### **1.3. Collecte documentaire**

* Architecture technique
* Diagrammes (API, flux, bases de données)
* Politiques internes existantes
* Procédures (accès, onboarding, télétravail…)
* Inventaire SaaS (Google, GitHub, Dashlane, etc.)
* Inventaire CI/CD (GitHub Actions, tests, déploiements…)

### **1.4. Interviews clés**

* CTO / Dev lead
* Développeurs
* Data
* Ops / Infra
* DPO

👉 *Objectif : comprendre la réalité opérationnelle.*

---

# 🟦 **2. Workflow ISO 27005 (la mission elle-même)**

C’est **la méthode officielle**, que tous les prestataires suivent.

---

## **Étape 1 — Identification des actifs**

Catégories ISO typiques :

* Ressources humaines
* Machines & équipements
* Applications (Monujo, Admin, API SCPI…)
* Données (clients, beneficiaries, transactions ISR…)
* Services externes (SaaS, APIs, prestataires)
* Processus métier
* Environnements cloud
* CI/CD, containers

👉 *Livrable : Registre complet des actifs.*

---

## **Étape 2 — Identification des menaces**

Menaces ISO + spécifiques fintech / SCPI :

* Menaces humaines (erreur, ingénierie sociale, insider…)
* Menaces techniques (faille applicative, supply-chain npm, API…)
* Menaces physiques (vol laptop, coworking…)
* Menaces cloud / SaaS
* Menaces réseau (MITM, DNS poisoning…)
* Menaces LLM (prompt injection, fuite de données)
* Menaces données (exfiltration, mauvaise configuration)

👉 *Livrable : Catalogue des menaces.*

---

## **Étape 3 — Identification des vulnérabilités**

Exemples :

* Absence de MFA
* Dépendances non mises à jour (npm, composer)
* Manque de segmentation
* Absence de scan SAST / SCA
* Journaux sensibles
* CI/CD non sécurisée
* Manque de politique télétravail
* Absence de classification des données
* Mauvaise configuration SaaS (Google, GitHub…)

👉 *Livrable : Registre des vulnérabilités.*

---

## **Étape 4 — Construction des scénarios de risques**

Formule ISO :

> **Actif + Menace + Vulnérabilité = Scénario de risque**

Exemple :

**Laptop employé + Vol + Absence de chiffrement disque → fuite de données client.**

👉 *Livrable : Scénarios de risques clarifiés, avec exemples.*

---

## **Étape 5 — Évaluation du risque (probabilité × impact)**

Échelle classique :

* Probabilité : 1 → 5
* Impact : 1 → 5
* Criticité = PxI

Catégories :

* faible
* modéré
* élevé
* critique
* inacceptable

👉 *Livrable : Matrice des risques.*

---

## **Étape 6 — Proposition de traitements des risques**

4 options ISO :

* **Réduire** (mettre une mesure)
* **Transférer** (assurance, prestataire externe)
* **Éviter** (arrêter le service)
* **Accepter** (si faible risque)

👉 *Livrable : Plan de traitement des risques.*

---

## **Étape 7 — Alignement des mesures avec ISO 27002**

ISO 27002 propose **93 mesures de sécurité**.

Exemples utiles pour vous :

* MFA sur tous les systèmes
* Chiffrement disque laptop
* Sauvegardes automatiques
* Rotation des accès / droits minimaux
* Sécurité CI/CD (SAST, SCA, secrets)
* Sécurité Cloud (IAM, logs, alerting)
* Sécurité LLM
* Politiques de confidentialité
* Contrôle des prestataires (vendor management)
* Sensibilisation sécurité

👉 *Livrable : Plan de mesures ISO 27002 adaptés à votre contexte.*

---

## **Étape 8 — Rapport final ISO 27005**

Contenu typique :

* Contexte & périmètre
* Méthodologie ISO 27005
* Liste des actifs
* Liste des menaces
* Liste des vulnérabilités
* Scénarios
* Matrice complète
* Plan de traitement
* Priorisation (quick wins, mois 1, mois 6, mois 12)

👉 *Livrable : **Document officiel**, exploitable dans le dossier “Pilotage Sécurité”.*

---

# 🟦 **3. Étapes APRÈS ISO 27005 (ce qu’on fait ensuite)**

### **3.1. Intégration dans un cadre ISO 27001 light (PME)**

* Politique sécurité interne
* Procédure accès
* Procédure télétravail
* Procédure sauvegarde
* Procédure CI/CD
* Politique LLM
* Gestion des prestataires
* Journalisation / monitoring
* Incident Response

👉 *C’est la partie gouvernance.*

---

### **3.2. Priorisation des actions**

Toute la roadmap sécurité sort directement du rapport 27005.

Exemples :

* MFA obligatoire (mois 1)
* Chiffrement laptop + rotation clés (mois 1–3)
* SAST + SCA CI/CD (mois 2–4)
* Mise à jour dépendances (continu)
* Audit de sécurité applicatif (annuel)
* Politique LLM (mois 1)
* Formation anti-phishing (mois 3)
* …

---

### **3.3. Mise en place des audits réguliers**

* Pentest annuel (avec prestataire OSCP / OSWE / eWPTX)
* Audit infra (tous les 12–18 mois)
* Audit RGPD (annuel)
* Tests d’ingénierie sociale (phishing, etc.)

---

### **3.4. Mise en place d’un cycle d’amélioration continue**

ISO 27001 impose le **PDCA (Plan → Do → Check → Act)** :

1. **Plan** → Analyse 27005 + mesures 27002
2. **Do** → Mise à en place
3. **Check** → Audit interne + pentest
4. **Act** → Améliorations, correctifs, roadmap

👉 *C’est ce qui transforme votre sécurité en un vrai système solide.*

---

# 🟩 **4. Résumé simple du workflow**

```
Préparation
   ↓
Analyse ISO 27005
   ↓
Matrice des risques
   ↓
Plan de traitement
   ↓
Mesures ISO 27002
   ↓
Gouvernance ISO 27001 light
   ↓
Audits annuels
   ↓
Cycle d’amélioration continue
```

---

# 🟦 Si tu veux, je peux maintenant te produire :

* **Le schéma (diagramme)** du workflow
* Une **version “prête à présenter à ton patron”**
* Le **cahier des charges type** à envoyer aux prestataires
* La **checklist ISO 27005 complète**
* Une **version PDF** complète

Tu veux lequel ?
