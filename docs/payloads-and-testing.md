# Format des Données & Tests

## Webhook Make (Envoi)
Le nœud HTTP "Make Webhook" envoie ce payload `multipart/form-data` (ou `application/x-www-form-urlencoded` selon n8n) vers Make :

```json
{
  "post": "Texte du post généré par l'IA...",
  "platforms[0]": "facebook"
}
