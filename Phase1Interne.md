# ✅ **TODO — Phase 1 : Avant le choix du prestataire**

*(À réaliser en interne)*

---

# 1) Définir le besoin et le périmètre

### 🎯 Objectif : formaliser ce qu’on veut sécuriser et pourquoi.

#### ✔ Actions à réaliser

* [ ] Lister les applications concernées
  (Monujo client, Monujo admin, API SCPI, backend Symfony, mobile Capacitor…)
* [ ] Lister les données sensibles manipulées
  (données clients, SCPI, transactions ISR, documents justificatifs…)
* [ ] Lister les environnements
  (prod, staging, CI/CD, postes dev, télétravail…)
* [ ] Lister les services tiers/SaaS
  (Google, GitHub, Dashlane, Datakeen, SMS provider, LLM…)
* [ ] Déterminer le périmètre exact de l’analyse ISO 27005
  → “Ce périmètre sera fourni aux prestataires lors de la demande de devis.”

[Tableau type à compléter](Phase1_1.md)

#### ⏱️ Durée : 0,5 à 1 jour

---

# 2) Créer la liste des exigences / cahier des charges

### 🎯 Objectif : formaliser clairement ce qu’on attend du prestataire.

#### ✔ Actions à réaliser

* [ ] Écrire un **cahier des charges synthétique** incluant :
    * [ ] Analyse complète **ISO 27005**
    * [ ] Registre des actifs
    * [ ] Catalogue des menaces
    * [ ] Liste des vulnérabilités
    * [ ] Scénarios de risques
    * [ ] Matrice probabilité × impact
    * [ ] Plan de traitement (priorisé)
    * [ ] Recommandations ISO 27002
    * [ ] Feuille de route 12 mois
    * [ ] Restitution orale
* [ ] Ajouter contrainte : **pas d'exécution technique** (gouvernance uniquement)
* [ ] Ajouter contrainte : **analyse tenant compte de notre secteur (fintech / SCPI)**
* [ ] Ajouter contrainte : **prise en compte LLM / API / SaaS**

---

# 3) Identifier et comparer les prestataires

### 🎯 Objectif : obtenir 3 à 5 prestataires qualifiés.

#### ✔ Actions à réaliser

* [ ] Construire une **liste de prestataires potentiels** (voir ci-dessous)
* [ ] Vérifier leurs compétences
    * [ ] Expérience ISO 27005 / 27001
    * [ ] Références fintech / SaaS
    * [ ] Certifications (CISSP, ISO Lead Auditor, OSCP…)
* [ ] Leur envoyer un **email type** (voir plus bas)
* [ ] Récupérer devis + méthode proposée
* [ ] Comparer selon une grille simple :
    * [ ] Prix
    * [ ] Méthodologie
    * [ ] Délais
    * [ ] Pertinence secteur
    * [ ] Clarté des livrables
    * [ ] Relation humaine / disponibilité

#### ⏱️ Durée : 2 à 4 jours

---

# 4) Sélection & contractualisation

### 🎯 Objectif : choisir, finaliser, encadrer juridiquement.

#### ✔ Actions à réaliser

* [ ] Organiser un call court avec les 2 meilleurs prestataires
* [ ] Poser les questions critiques :
    * Quels livrables exacts ?
    * Quel niveau de détail dans la matrice ?
    * Prise en compte CI/CD / LLM ?
    * Expérience dans les applications web Vue/Symfony ?
* [ ] Choisir le prestataire
* [ ] Obtenir un devis + planning ferme
* [ ] Transmettre au dirigeant pour validation
* [ ] Signature (bons de commande, CGV, NDA)

#### ⏱️ Durée : 1 à 3 jours

---

# 🎯 **Liste de prestataires potentiels (à adapter)**

*(Tu pourras étoffer selon budget/localisation)*

* **OZINT (France)** – Risk analysis, ISO 27005, audit orga
* **Advens** – Prestataire sécurité majeur France
* **XMCO** – Audit, pentest, gouvernance
* **Synacktiv** – (plus technique / pentest mais très réputés)
* **Wavestone** – Gros cabinet (peut être cher)
* **CyberSecura** – PME spécialisée ISO 27001/27005
* **Digitemis** – Analyse de risques, audits, RGPD
* **Nomios** – SecOps + gouvernance
* **Orange Cyberdefense** – Gros acteur (coût élevé)

(+ à compléter avec prestataires locaux)

---

# 📧 **Email type à envoyer aux prestataires**

Voici un modèle court, clair et pro :

---

**Objet : Demande de devis – Analyse de risques ISO 27005**

Bonjour,

Nous recherchons un prestataire pour réaliser une **analyse de risques conforme ISO 27005** dans le cadre du renforcement de notre gouvernance sécurité.

Notre périmètre inclut notamment :

* Applications web (VueJS / Symfony)
* Backend d’agrégation SCPI
* Services SaaS / API externes
* Données sensibles (clients, SCPI, transactions)
* CI/CD et environnements de développement
* Usage de LLM et automatisations internes

**Livrables attendus :**

* Registre complet des actifs
* Menaces, vulnérabilités, scénarios
* Matrice des risques (probabilité × impact)
* Plan de traitement priorisé
* Recommandations (ISO 27002)
* Restitution orale + rapport final

Merci de nous transmettre :

* Votre méthodologie
* Vos délais
* Vos livrables
* Un devis estimatif
* Vos références dans le secteur SaaS ou fintech

Bien cordialement,
[Mathieu – MeilleureSCPI.com]

---

# 🧩 **Tu veux que je t’en fasse une version Markdown prête à copier-coller ?**
