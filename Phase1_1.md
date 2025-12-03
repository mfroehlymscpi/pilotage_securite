Version template type à compléter

## 1. Lister les applications concernées

| Application | Type | Domaine(s) | Stack technique | Criticité | Hébergement | Notes |
|------------|------|------------|----------------|-----------|-------------|-------|
| Monujo Client | Web app | app.monujo.com | VueJS | 🔴 Critique | | Interface client principale |
| Monujo Admin | Web app | admin.monujo.com | VueJS | 🔴 Critique | | Backoffice gestion |
| API SCPI | API REST | api.monujo.com | Symfony | 🔴 Critique | | Agrégation données SCPI |
| Backend Symfony | Backend | | Symfony | 🔴 Critique | | Logique métier |
| Mobile Capacitor | App mobile | | Capacitor + VueJS | 🟠 Majeur | | Application mobile hybride |
| ...                    | ...                   | ...              | ...                     | ...                 | ...          | ...         |
| | | | | | | |

---

## 2. Lister les données sensibles manipulées

| Type de donnée | Catégorie RGPD | Volume estimé | Durée conservation | Mesures protection actuelles | Criticité |
|----------------|----------------|---------------|-------------------|----------------------------|-----------|
| Données clients (nom, prénom, email, téléphone) | Données personnelles | | | | 🔴 Critique |
| Données financières SCPI | Données sensibles | | | | 🔴 Critique |
| Transactions ISR | Données financières | | | | 🔴 Critique |
| Documents justificatifs (RIB, pièces d'identité) | Données sensibles | | | | 🔴 Critique |
| Données d'authentification (mots de passe, tokens) | Données sensibles | | | | 🔴 Critique |
| Logs utilisateurs | Données personnelles | | | | 🟠 Majeur |
| ...                    | ...                   | ...              | ...                     | ...                 | ...          | ...         |
| | | | | | |

---

## 3. Lister les environnements

| Environnement | URL/Accès | Infrastructure | Accès (qui ?) | Données utilisées | Niveau sécurité | Notes |
|---------------|-----------|----------------|---------------|-------------------|-----------------|-------|
| Production | | | | Données réelles | 🔴 Critique | Environnement live |
| Staging/Préprod | | | | Données anonymisées ? | 🟠 Majeur | Tests pré-déploiement |
| CI/CD (GitHub Actions, etc.) | | | | | 🟠 Majeur | Pipeline déploiement |
| Environnements dev locaux | | Postes développeurs | Équipe dev | Données test | 🟡 Modéré | Postes individuels |
| Télétravail | | VPN ? | Équipe complète | Variable | 🟠 Majeur | Accès distant |
| ...                    | ...                   | ...              | ...                     | ...                 | ...          | ...         |
| | | | | | | |

---

## 4. Lister les services tiers/SaaS

| Service                | Catégorie             | Fournisseur      | Usage                   | Données partagées   | Niveau accès | Contrat/DPA | Criticité   |
|------------------------|-----------------------|------------------|-------------------------|---------------------|--------------|-------------|-------------|
| Google Workspace       | Email, Drive          | Google           | Communication, stockage |                     |              |             | 🟠 Majeur   |
| GitHub                 | Code source           | Microsoft        | Versioning, CI/CD       | Code source complet |              |             | 🔴 Critique |
| Dashlane               | Gestion mots de passe | Dashlane         | Secrets management      | Credentials         |              |             | 🔴 Critique |
| Datakeen               | Données SCPI          | Datakeen         | Agrégation SCPI         | Données SCPI        |              |             | 🔴 Critique |
| SMS Provider           | Notifications         |                  | Envoi SMS               | Numéros téléphone   |              |             | 🟡 Modéré   |
| LLM (ChatGPT/Claude ?) | IA générative         | OpenAI/Anthropic | Développement, support  | Code, données ?     |              |             | 🟠 Majeur   |
| ...                    | ...                   | ...              | ...                     | ...                 | ...          | ...         | ...         |
|                        |                       |                  |                         |                     |              |             |             |

---

## 5. Déterminer le périmètre exact de l'analyse ISO 27005

### Périmètre proposé (à valider)

**Applications incluses :**
- [ ] Monujo Client (VueJS)
- [ ] Monujo Admin (VueJS)
- [ ] API SCPI (Symfony)
- [ ] Backend Symfony
- [ ] Mobile Capacitor
- [ ] ... (À compléter exhaustivement)

**Infrastructures incluses :**
- [ ] Environnement de production
- [ ] Environnement de staging
- [ ] ~~Pipeline CI/CD~~ On en a pas vraiment
- [ ] Environnements de développement
- [ ] Réseaux des locaux
- [ ] Accès télétravail/VPN
- [ ] ... (À compléter exhaustivement)

**Services tiers inclus :**
- [ ] GitHub (code source, CI/CD)
- [ ] Dashlane (gestion secrets)
- [ ] Datakeen (agrégation SCPI)
- [ ] Google Workspace
- [ ] SMS Provider
- [ ] Services LLM utilisés
- [ ] ... (À compléter exhaustivement)

**Données sensibles incluses :**
- [ ] Données clients (identité, contact)
- [ ] Données financières SCPI
- [ ] Transactions ISR
- [ ] Documents justificatifs
- [ ] Credentials et tokens
- [ ] ... (À compléter exhaustivement)

**Exclusions (si applicable) :**
-

---

### Synthèse du périmètre (à fournir aux prestataires)

> **Périmètre de l'analyse de risques ISO 27005 :**
>
> L'analyse couvrira l'ensemble de la plateforme MeilleureSCPI.com incluant :
> - Applications web et mobile (VueJS, Symfony, Capacitor)
> - API REST d'agrégation de données SCPI
> - Environnements de production, staging, développement et CI/CD
> - Services tiers critiques (GitHub, Dashlane, Datakeen, Google Workspace, LLM)
> - Données personnelles et financières des clients (conformité RGPD)
> - Infrastructure de télétravail et accès distants
>
> **Secteur :** Fintech / Conseil en investissement SCPI
> **Réglementation :** RGPD, exigences secteur financier
> **Objectif :** Gouvernance sécurité, préparation ISO 27001