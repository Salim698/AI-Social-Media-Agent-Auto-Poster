# Limitations & Roadmap

Voici les problèmes identifiés et axes d'améliorations (ouverts pour de futures Pull Requests).

| ID | Sujet | Label | Description |
|---|---|---|---|
| 1 | **Crash si table `idees_posts` vide** | `bug` | Actuellement, si le nœud "Piocher une Idée" ne renvoie rien, le nœud "Construire Prompt" plante car il attend `idee_id`. Il manque une branche `IF`. |
| 2 | **Gestion d'erreur HTTP silencieuse** | `bug`, `help wanted` | Si Make ou Gemini tombe, le workflow s'arrête net. Il faudrait un nœud *Error Trigger* pour notifier Telegram d'un échec. |
| 3 | **Format d'envoi Make** | `refactor` | Le nœud Make utilise des paramètres Body formattés. Le transfert JSON pur serait plus propre. |
| 4 | **Suppression de variables système cloud** | `good first issue` | Vérifier la compatibilité des variables `$env` sur n8n Cloud vs Auto-hébergé. |
