# Contribuer au projet

Merci de l'intérêt que vous portez à ce workflow ! 

## Processus
1. Forkez le dépôt.
2. Créez votre branche de fonctionnalité (`git checkout -b feature/NouvelleFonctionnalite`).
3. Commitez vos changements (`git commit -m 'Ajout de la nouvelle fonctionnalité'`).
4. Poussez vers la branche (`git push origin feature/NouvelleFonctionnalite`).
5. Ouvrez une Pull Request.

## 🚨 Checklist d'export sécurisé d'un workflow n8n
Si vous soumettez une modification du `workflow.json`, vous **devez** vérifier ceci avant de commiter :
- [ ] Le workflow est inactif (`active: false`).
- [ ] Aucun bloc `credentials` ou `webhookId` n'est présent.
- [ ] Aucun token ou clé d'API n'est visible dans les URLs des nœuds HTTP Request.
- [ ] Aucune donnée personnelle (téléphones, emails, identifiants de chats) n'est en dur.
- [ ] Le bloc `meta` racine est vidé.
- [ ] Les identifiants liés à votre instance (ID de feuille, UUID locaux) sont remplacés par des placeholders.

Veuillez consulter le [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) pour les règles de bonne conduite.
