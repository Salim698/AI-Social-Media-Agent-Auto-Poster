# Liste des Nœuds et Modules

Le système complet s'appuie sur des nœuds n8n pour la logique et des modules Make pour la publication.

## 1. Nœuds n8n (Orchestrateur)

| Nom du Nœud | Type de Nœud | Fonction |
|---|---|---|
| ⏱️ Schedule Trigger | `n8n-nodes-base.scheduleTrigger` | Lance le workflow à intervalles réguliers |
| 💡 Piocher une Idée | `n8n-nodes-base.supabase` | Requête de sélection |
| 🧠 Lire Profil Supabase | `n8n-nodes-base.supabase` | Requête de sélection |
| 📚 Lire Historique Supabase | `n8n-nodes-base.supabase` | Requête de sélection |
| ✍️ Construire Prompt | `n8n-nodes-base.code` | Formatage JS |
| 🤖 Gemini API | `n8n-nodes-base.httpRequest` | Requête HTTP Externe |
| 🔍 Parser Réponse | `n8n-nodes-base.code` | Nettoyage JSON |
| 📤 Make Webhook | `n8n-nodes-base.httpRequest` | Envoi du payload vers Make |
| Enregistrer le Post | `n8n-nodes-base.supabase` | Requête d'insertion |
| Update a row | `n8n-nodes-base.supabase` | Requête de mise à jour |
| ✅ Telegram Confirmer | `n8n-nodes-base.telegram` | Notification |

*Total n8n : 11 nœuds*

## 2. Modules Make (Relais de publication)

| Nom du Module | Application | Fonction |
|---|---|---|
| Custom Webhook | `Webhooks` | Écoute et reçoit le texte généré par n8n instantanément |
| Create a Post | `Facebook Pages` | Publie le contenu sur la page Facebook configurée |

*Total Make : 2 modules*
