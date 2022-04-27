# Objectifs

* Permettre de déclarer publiquement à quel compte mastodon correspond son propre compte twitter
* Permettre de trouver à quel compte mastodon correspond un compte twitter particulier
* Permettre de s'abonner automatiquement sur Mastodon à tous ceux auxquels on est abonnés sur twitter


# Problèmes

Le site précédent, bridge.joinmastodon.org, ne fonctionne plus. Twitter aurait révoqué les accès à l'API. Il est probable que Twitter de valide pas une app destinée à faire fuiter les utilisateurs.

Solution : Utiliser une extension Chrome/Firefox qui utilise directement une fenêtre déjà authentifiée.

# Fonctionnement 

Menu de l'extension : 
1. S'identifier sur twitter : demande à ouvrir un onglet twitter et s'y identifier si ce n'est pas déjà le cas
2. S'identifier sur le Fediverse : demande un identifiant fediverse ; si le domaine est reconnu comme un serveur mastodon, proposer de s'y identifier si ce n'est pas déjà le cas
3. Déclarer le lien entre les deux comptes : propose de publier un tweet avec l'identifiant fediverse et un hashtag ; ping un service distant avec le lien vers ce tweet pour l'enregistrer dans une base publique ; propose une coche optionnelle pour effacer immédiatement le tweet ensuite pour ceux qui le veulent
4. Voir / M'abonner aux comptes fediverse auxquels je ne suis pas abonné : liste les abonnements twitter, regarde lesquels ont une correspondance sur le fediverse, vérifie le statut "moved" sur les comptes mastodon, liste les abonnements mastodon, propose la liste de ceux qui manqent et un bouton pour s'y abonner automatiquement
5. Me désabonner des comptes twitter qui ont un équivalent dans le fédiverse : liste les abonnements twitter, regarde lesquels ont une correspondance sur le fediverse, vérifie le statut "moved" sur les comptes mastodon, liste les abonnements mastodon, propose la liste de ceux auxquels on est abonné dans les deux réseaux et un bouton pour s'y désabonner sur twitter

