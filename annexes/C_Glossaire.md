# Annexe C : Glossaire Technique

*Annexe du document [Pilotage Sécurité 2026](../Pilotage_Securite_2026.md)*

---

## Sommaire

- [A](#a) | [B](#b) | [C](#c) | [D](#d) | [E](#e) | [F](#f) | [G](#g) | [H](#h) | [I](#i) | [K](#k) | [L](#l) | [M](#m) | [N](#n) | [O](#o) | [P](#p) | [R](#r) | [S](#s) | [T](#t) | [V](#v) | [W](#w) | [X](#x) | [Z](#z)

---

## A

### Active Directory (AD)
Annuaire Microsoft pour gestion centralisée des identités, authentification et autorisations dans un réseau Windows. Cible privilégiée des attaquants (élévation privilèges, mouvement latéral).

### ANSSI
Agence Nationale de la Sécurité des Systèmes d'Information. Autorité nationale française en matière de cybersécurité. Publie guides de bonnes pratiques et qualifie prestataires (PASSI, PRIS).

### AppSec (Application Security)
Ensemble des pratiques de sécurisation des applications : secure coding, tests sécurité (SAST/DAST), pentest applicatif, revue code.

### API (Application Programming Interface)
Interface permettant communication entre applications. Les API REST/GraphQL sont des cibles d'attaque (injection, authentification faible, rate limiting absent).

### ASVS (Application Security Verification Standard)
Référentiel OWASP définissant 3 niveaux de sécurité applicative (Level 1: Opportuniste, Level 2: Standard, Level 3: Critique).

---

## B

### Bug Bounty
Programme rémunérant chercheurs sécurité qui découvrent vulnérabilités. Modèle "pay-per-result" (paiement uniquement si vulnérabilité valide).

### BYOD (Bring Your Own Device)
Utilisation d'appareils personnels (smartphone, laptop) à des fins professionnelles. Nécessite politique sécurité spécifique (MDM, séparation données).

---

## C

### CEH (Certified Ethical Hacker)
Certification pentest d'EC-Council. Reconnaissance moyenne, moins exigeante qu'OSCP/OSWE.

### CI/CD (Continuous Integration / Continuous Deployment)
Pipeline automatisé de build, test et déploiement code. Sécuriser CI/CD essentiel (injection malware, compromission supply chain).

### CIPP/E (Certified Information Privacy Professional / Europe)
Certification IAPP sur protection données et RGPD. Essentielle pour DPO et référents RGPD.

### CISM (Certified Information Security Manager)
Certification ISACA sur management et gouvernance sécurité. Idéale pour rôle pilotage/coordination.

### CISSP (Certified Information Systems Security Professional)
Certification (ISC)² vision 360° sécurité SI (8 domaines). Reconnue internationalement, exigeante (5 ans expérience requis).

### CSSLP (Certified Secure Software Lifecycle Professional)
Certification (ISC)² sur sécurisation cycle développement logiciel (secure coding, AppSec).

### CVE (Common Vulnerabilities and Exposures)
Base de données publique des vulnérabilités identifiées. Chaque vulnérabilité = identifiant unique (ex: CVE-2024-1234).

### CVSS (Common Vulnerability Scoring System)
Système notation gravité vulnérabilités (0-10). Score ≥ 9.0 = Critique, 7.0-8.9 = Élevé, 4.0-6.9 = Moyen, < 4.0 = Faible.

---

## D

### DAST (Dynamic Application Security Testing)
Analyse sécurité applicative en boîte noire (sans accès code source), en simulant attaques. Complémentaire SAST.

### DevSecOps
Intégration sécurité dans processus DevOps. Automatisation tests sécurité dans CI/CD, "shift left" (sécurité dès conception).

### DLP (Data Loss Prevention)
Solutions prévention fuite données : monitoring, chiffrement, contrôle exfiltration.

### DPO (Data Protection Officer / Délégué Protection Données)
Responsable conformité RGPD dans l'entreprise. Obligatoire pour organismes publics et traitement grande échelle données sensibles.

---

## E

### eWPTX (eLearnSecurity Web Application Penetration Tester eXtreme)
Certification pentest web avancée (eLearnSecurity / INE Security). Très technique, reconnue.

---

## F

### Firewall (Pare-feu)
Équipement filtrant trafic réseau selon règles (IP source/destination, ports, protocoles). Essentiel sécurité périmètre.

---

## G

### Golden Ticket
Technique attaque Active Directory : compromission compte KRBTGT permettant création tickets Kerberos arbitraires (accès total domaine).

### GPEN (GIAC Penetration Tester)
Certification pentest GIAC/SANS. Reconnaissance correcte, moins spécialisée qu'OSCP.

### GWEB (GIAC Web Application Penetration Tester)
Certification GIAC/SANS spécialisée pentest web. Très technique, équivalent OSWE.

---

## H

### Hardening
Durcissement sécurité système : désactivation services inutiles, mises à jour, configuration sécurisée, principe moindre privilège.

---

## I

### IAM (Identity and Access Management)
Gestion identités et accès : authentification, autorisation, SSO, MFA, provisioning/deprovisioning comptes.

### ISO 27001
Norme internationale système management sécurité information (SMSI). Certification reconnue garantissant gouvernance sécurité.

### ISO 27002
Recueil bonnes pratiques sécurité information (114 mesures). Complément ISO 27001.

### ISO 27701
Extension ISO 27001 sur protection données personnelles et RGPD.

---

## K

### Kerberoasting
Technique attaque Active Directory : extraction hash mots de passe comptes service (SPN) pour craquage offline.

### KPI (Key Performance Indicator)
Indicateur performance clé. Pour sécurité : nb vulnérabilités critiques, délai remédiation, taux couverture audits, incidents, etc.

---

## L

### LLM (Large Language Model)
Modèle IA génératif (ChatGPT, Claude, etc.). Risques : prompt injection, fuite données, génération contenu malveillant. Nécessite charte usage.

---

## M

### MFA (Multi-Factor Authentication / Authentification Multi-Facteurs)
Authentification combinant plusieurs facteurs : connaissance (mdp), possession (token, smartphone), inhérence (biométrie).

### MITM (Man-In-The-Middle)
Attaque interception communication entre 2 parties pour écoute/modification données.

---

## N

### NDA (Non-Disclosure Agreement / Accord Confidentialité)
Contrat confidentialité signé avec prestataires accédant informations sensibles.

### NIST
National Institute of Standards and Technology (USA). Publie frameworks sécurité reconnus (NIST CSF, guides techniques).

---

## O

### OSCP (Offensive Security Certified Professional)
Certification pentest référence Offensive Security. Pratique (24h exam), très reconnue.

### OSEP (Offensive Security Experienced Penetration Tester)
Certification pentest avancée Offensive Security (évasion défenses, Red Team).

### OSWE (Offensive Security Web Expert)
Certification pentest web experte Offensive Security. Très technique, reference AppSec.

### OWASP (Open Web Application Security Project)
Organisation à but non-lucratif, référence sécurité applicative web. Publie OWASP Top 10, ASVS, guides secure coding.

### OWASP Top 10
Liste 10 vulnérabilités web critiques les plus courantes : injection, authentification cassée, XSS, CSRF, mauvaise config, etc.

---

## P

### PASSI (Prestataire Audit Sécurité Systèmes Information)
Qualification ANSSI attestant compétences prestataire audit SSI. Obligatoire pour audits OIV (Opérateurs Importance Vitale).

### PCA/PRA (Plan Continuité/Reprise Activité)
Procédures permettant poursuite activité critique (PCA) et reprise après incident majeur (PRA).

### Pentest (Test Intrusion / Penetration Testing)
Simulation attaque informatique par experts sécurité pour identifier vulnérabilités exploitables. Méthodes : black box, grey box, white box.

### Phishing (Hameçonnage)
Technique social engineering : email/SMS frauduleux incitant victime à divulguer infos sensibles ou cliquer lien malveillant.

### PIA (Privacy Impact Assessment / Analyse Impact Vie Privée)
Étude impacts traitement données personnelles sur vie privée. Obligatoire RGPD pour traitements à risque élevé.

### PoC (Proof of Concept)
Preuve exploitabilité vulnérabilité. Dans rapport pentest, démontre réalité menace.

### PRIS (Prestataire Réponse Incidents Sécurité)
Qualification ANSSI pour prestataires SOC/CERT/gestion incidents.

### PSSI (Politique Sécurité Systèmes Information)
Document cadre définissant orientations sécurité entreprise, rôles, règles, objectifs.

---

## R

### Red Team
Simulation attaque réaliste par équipe offensive testant défenses globales entreprise (technique + organisationnel + physique).

### RGPD (Règlement Général Protection Données)
Règlement européen 2016/679 sur protection données personnelles. Sanctions jusqu'à 20 M€ ou 4% CA mondial.

### ROI (Return On Investment)
Retour investissement. Pour sécurité : économies incidents évités vs coût programme sécurité.

---

## S

### SAST (Static Application Security Testing)
Analyse sécurité code source (boîte blanche) sans exécution. Détecte vulnérabilités dès développement. Complémentaire DAST.

### SBOM (Software Bill of Materials)
Inventaire composants logiciels et dépendances application. Essentiel gestion risque supply chain.

### SCA (Software Composition Analysis)
Analyse dépendances open-source pour détecter vulnérabilités connues (CVE).

### SCPI (Société Civile Placement Immobilier)
Véhicule investissement immobilier. Données SCPI = données financières sensibles.

### Secure Coding
Développement sécurisé : validation entrées, gestion erreurs, principe moindre privilège, protection secrets, etc.

### SIEM (Security Information and Event Management)
Plateforme centralisation et analyse logs sécurité. Corrélation événements, alertes, détection incidents.

### SMB (Server Message Block)
Protocole partage fichiers/imprimantes Windows. Vulnérabilités fréquentes (SMB relay, EternalBlue).

### SMSI (Système Management Sécurité Information)
Ensemble processus gestion sécurité SI selon ISO 27001.

### SOC (Security Operations Center)
Centre opérationnel supervision sécurité 24/7 : monitoring, détection incidents, réponse.

### Social Engineering (Ingénierie Sociale)
Manipulation psychologique pour obtenir informations/accès : phishing, pretexting, tailgating, vishing.

### Supply Chain Attack (Attaque Chaîne Approvisionnement)
Compromission fournisseur/dépendance pour atteindre cible finale. Ex: SolarWinds, Log4Shell.

---

## T

### TIBER-FR
Framework ANSSI tests résilience cyber (Red Team). Basé sur threat intelligence, scénarios validés, prestataires qualifiés.

### TJM (Taux Journalier Moyen)
Tarif journée consultant. Pour pentester : 700-1 200 €/j selon expertise.

---

## V

### VLAN (Virtual LAN)
Segmentation logique réseau. Isole flux métiers critiques (ex: SCPI, production, administration).

### VPN (Virtual Private Network)
Réseau privé virtuel chiffré pour accès distant sécurisé.

### Vulnerability (Vulnérabilité)
Faiblesse système exploitable par attaquant. Classée selon criticité (CVSS), type (OWASP Top 10), impact.

---

## W

### WAF (Web Application Firewall)
Pare-feu applicatif filtrant requêtes HTTP/HTTPS. Protège contre injections SQL, XSS, etc.

### White Box (Boîte Blanche)
Audit avec accès complet : code source, architecture, credentials. Max vulnérabilités détectées.

### WiFi (IEEE 802.11)
Réseau sans-fil. Risques : Evil Twin, capture handshake WPA2, rogue AP.

---

## X

### XSS (Cross-Site Scripting)
Injection code JavaScript malveillant dans application web, exécuté navigateur victime. Types : reflected, stored, DOM-based.

---

## Z

### Zero Trust
Modèle sécurité "ne jamais faire confiance, toujours vérifier". Authentification/autorisation continue, segmentation micro, moindre privilège.

---

## Acronymes Fréquents

| Acronyme | Signification |
|----------|---------------|
| ACL | Access Control List |
| APT | Advanced Persistent Threat |
| CERT | Computer Emergency Response Team |
| CIA | Confidentiality, Integrity, Availability |
| CTI | Cyber Threat Intelligence |
| DMZ | Demilitarized Zone |
| DOS/DDOS | Denial of Service / Distributed DOS |
| GPO | Group Policy Object (AD) |
| IDS/IPS | Intrusion Detection/Prevention System |
| LDAP | Lightweight Directory Access Protocol |
| MDM | Mobile Device Management |
| NTLM | NT LAN Manager |
| OIV | Opérateur Importance Vitale |
| PKI | Public Key Infrastructure |
| SAML | Security Assertion Markup Language |
| SPN | Service Principal Name (AD) |
| SSO | Single Sign-On |
| TLS/SSL | Transport Layer Security / Secure Sockets Layer |
| 2FA | Two-Factor Authentication |

---

## Ressources Complémentaires

**Référentiels ANSSI :**
- [cyber.gouv.fr](https://cyber.gouv.fr) - Guides bonnes pratiques
- [Référentiel PASSI](https://cyber.gouv.fr/publications/referentiel-dexigences-passi)

**OWASP :**
- [owasp.org](https://owasp.org) - OWASP Top 10, ASVS, guides
- [OWASP Top 10 2021](https://owasp.org/Top10/)

**RGPD :**
- [CNIL](https://www.cnil.fr) - Documentation RGPD France
- [EUR-Lex RGPD](https://eur-lex.europa.eu/eli/reg/2016/679/oj) - Texte officiel

**ISO :**
- [ISO 27001:2022](https://www.iso.org/standard/82875.html)
- [ISO 27002:2022](https://www.iso.org/standard/75652.html)
