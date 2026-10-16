# Politique de Sécurité

## Signaler une vulnérabilité ou une fuite de clé
Si vous trouvez une donnée sensible (clé API, token, identifiant privé) laissée par erreur dans le code, **n'ouvrez pas d'Issue publique**.
Veuillez contacter directement l'auteur ou soumettre une PR immédiate supprimant la donnée concernée.

## Bonnes pratiques
- Utilisez toujours le fichier `.env` pour vos environnements locaux.
- N'exportez jamais un workflow n8n avec ses `credentials`.
