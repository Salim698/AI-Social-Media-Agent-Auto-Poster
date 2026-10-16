# Guide d'Installation

## 1. Prérequis
- Une instance n8n fonctionnelle.
- Un compte Supabase avec les tables configurées (voir `database-schema.md`).
- Une clé API Google Gemini (Google AI Studio).
- Un compte Make (Integromat) configuré pour poster sur Facebook.
- Un bot Telegram fonctionnel.

## 2. Variables d'Environnement
Dans l'environnement de votre n8n (fichier `.env` de votre Docker, par exemple), ajoutez :
```env
MAKE_WEBHOOK_URL="[https://hook.eu1.make.com/xxx](https://hook.eu1.make.com/xxx)"
GEMINI_API_KEY="xxx"
TELEGRAM_CHAT_ID="xxx"
