# **Phase 1 : Avant le choix du prestataire**

*(À réaliser en interne)*

---

# 1) Définir le besoin et le périmètre

### 🎯 Objectif : formaliser ce qu’on veut sécuriser et pourquoi.

#### ✔ Actions à réaliser
Élements à compléter dans les tableaux type :
[Tableau type à compléter](Phase1_1.md)

* [ ] Lister les applications concernées
* [ ] Lister les données sensibles manipulées
* [ ] Lister les environnements
* [ ] Lister les services tiers/SaaS
* [ ] Déterminer le périmètre exact de l’analyse ISO 27005 ou autre

#### ⏱️ Durée : 0,5 à 1 jour

---

# 2) Créer la liste des exigences / cahier des charges

### 🎯 Objectif : formaliser clairement ce qu’on attend du prestataire.

#### ✔ Actions à réaliser

* [ ] Compléter et valider le [Cahier des Charges — Accompagnement Sécurité & Analyse des Risques](Phase1_2_cahier_des_charges.md)

---

# 3) Identifier et comparer les prestataires

### 🎯 Objectif : obtenir 3 à 5 prestataires qualifiés.

#### ✔ Actions à réaliser

Aggrémenter la liste des prestataire : 
- Fiche pour le moment trop complexe (à simplifier)
- Essayer d'avoir des informations de contact pertinent
- https://docs.google.com/spreadsheets/d/1e01Ogh2e8VDH63oRNChUTJLMA_LD_du_mVX8sJuLfaU/edit?gid=0#gid=0

#### ⏱️ Durée : 2 à 4 jours

---

# 4) Sélection & contractualisation

### 🎯 Objectif : choisir, finaliser, encadrer juridiquement.

#### Phase 1
* Valider le template de mail et le cahier des charge synthetique
* Transmission préfiltre ChatGPT 
    * Créer un projet ChatGPT avec les information du tableau à compléter (Critères).
    * Créer une conversation ChatGPT pour chaque prestataire dans le quel on mettra le resultat des échanges

#### Phase 2
- Faire un version exhaustive du cahier des charges
- Transmettre aux presta retenu avec lien calendly pour un rdv d'1 heure

### ✔ Actions à réaliser

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
