# n8n AI Social Media Agent

Agent autonome n8n qui génère et publie du contenu sur Facebook via Gemini, Supabase et Make.

[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](CONTRIBUTING.md)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)



*Screenshots :*
![Workflow n8n](images/workflow.png)
![Scénario Make](images/make-scenario.png)



## Fonctionnalités
- **Pilotage Data-Driven** : Base de données Supabase pour stocker les profils, historiques et idées de posts.
- **Génération IA Avancée** : Utilisation de l'API Google Gemini avec un prompt ingénierie complexe pour garantir un ton naturel et éviter le spam.
- **Publication Automatisée** : Connexion à Make (anciennement Buffer) pour bypasser les restrictions de publication d'automatisations Facebook.
- **Monitoring Telegram** : Notifications automatiques pour confirmer les publications.

## Architecture

```mermaid
graph TD
    A[Schedule Trigger <br/> 5-10x / jour] -->|Déclencheur| B(Supabase: Piocher Idée)
    B --> C(Supabase: Lire Profil)
    C --> D(Supabase: Lire Historique)
    D --> E[Code: Construire Prompt]
    E -->|Requête JSON| F((API Gemini))
    F -->|Réponse texte| G[Code: Parser Réponse JSON]
    G -->|Payload| H((Webhook Make / Facebook))
    H --> I(Supabase: Archiver Post)
    I --> J(Supabase: Mettre à jour statut)
    J --> K((Telegram: Confirmation))
