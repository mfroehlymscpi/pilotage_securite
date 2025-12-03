# Graph de vecteurs d'attaque identifié manuellement

```json
{
  "Humains": {
    "EchangesVerbaux": [
      "Appels avec prestataires",
      "Echanges impromptus (machine à café)",
      "Exposition visuelle des écrans dans les espaces de coworking"
    ],
    "ErreursHumaines": [
      "Divulgation involontaire d'informations",
      "Manipulation incorrecte de documents ou données"
    ],
    "IngenierieSociale": [
      "Phishing",
      "Spear phishing",
      "Imposture téléphonique",
      "Demande d’accès frauduleuse"
    ]
  },

  "Physiques": {
    "Locaux": [
      "Domicile des employés (télétravail)",
      "Bureaux distants (Marseille, Paris, Strasbourg, Madagascar)",
      "Espaces de coworking ou open-space"
    ],
    "DocumentsPapier": [
      "Accès non autorisé aux documents dans les locaux",
      "Interception lors du transport (ex: La Poste)"
    ]
  },

  "Materiel": {
    "TerminauxInternes": {
      "Laptop_PC_Smartphone": [
        "Accès réseau non sécurisé (Wi-Fi public, mauvais chiffrement)",
        "Accès physique temporaire non contrôlé",
        "Perte ou vol du matériel (accès persistant)"
      ]
    },
    "Serveurs": [
      "Compromission de l’hébergeur",
      "Accès réseau non autorisé"
    ],
    "TerminauxClients": [
      "Attaque via nos applications exécutées sur les postes utilisateurs"
    ]
  },

  "LogicielsEtCode": {
    "CodeApplicatif": [
      "Vulnérabilités dans le code (VueJS, Symfony)",
      "Mauvaise validation des entrées",
      "Endpoints API insuffisamment protégés"
    ],
    "Dependances": [
      "Librairies npm vulnérables",
      "Bundles Symfony",
      "Frameworks front/back"
    ],
    "LogicielsLaptop": [
      "Plugins IDE (PhpStorm, VSCode)",
      "Packages système (apt)",
      "Extensions navigateur"
    ]
  },
  "ServicesEtReseaux": {
    "APIExternes": [
      "APIs des sociétés de gestion",
      "Services email (SMTP, API)"
    ],
    "ExtensionsNavigateur": [
      "Outils de développement",
      "Outils SEO",
      "Extensions non vérifiées"
    ],
    "SaaS": [
      "Service de paye",
      "LLM (ChatGPT, OpenAI API, Claude, Gemini)",
      "Gestionnaire de mots de passe (Dashlane)",
      "Google Workspace / GCP",
      "npm",
      "GitHub",
      "Docker Hub",
      "Fournisseur SMS",
      "Datakeen (KYC / extraction documentaires)",
      "Online.net / Scaleway",
      "Cloudflare",
      "Lucidchart"
    ]
  },
  "Donnees": {
    "Documents": [
      "Documents papier contenant des informations sensibles",
      "Notes personnelles",
      "Documents imprimés non détruits"
    ],
    "DonneesApplicatives": [
      "Exfiltration via endpoints API",
      "Fuites dans les logs ou traces",
      "Dump de base de données non sécurisé"
    ],
    "DonneesLLM": [
      "Fuite de données personnelles ou confidentielles",
      "Attaques par prompt injection",
      "Exfiltration via plugins ou serveurs MCP"
    ]
  }
}
```