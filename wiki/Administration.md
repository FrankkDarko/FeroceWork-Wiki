# Administration

**Accès : administrateurs uniquement** (sauf mention contraire).

## Gestion des utilisateurs

La page **Utilisateurs** permet de gérer tous les comptes de l'application. Il n'y a pas d'inscription libre : chaque compte est créé à la main par un administrateur.

### Créer un compte

- **Identifiant** : lettres, chiffres, tirets et tirets bas (2 caractères minimum).
- **Mot de passe temporaire** : 8 caractères minimum — un bouton **Auto** génère un mot de passe aléatoire équilibré.
- **Rôle** : utilisateur, logistique, manager ou administrateur (voir [Rôles et permissions](Roles-et-permissions)).

À sa première connexion, la personne est **obligée de choisir son propre mot de passe** avant d'accéder à quoi que ce soit. Le mot de passe temporaire ne sert donc qu'une fois.

### Actions sur un compte existant

- **Réinitialiser le mot de passe** — pour un oubli : l'admin définit un nouveau mot de passe temporaire, et l'utilisateur devra de nouveau en choisir un personnel à sa prochaine connexion.
- **Changer le rôle** — promotion ou rétrogradation, effet immédiat.
- **Activer / désactiver** — un compte désactivé ne peut plus se connecter, sans être supprimé.

### Garde-fous

- Impossible de **désactiver son propre compte**.
- Impossible de **se retirer soi-même le rôle administrateur**.

Ces protections sont appliquées côté serveur : elles tiennent même en dehors de l'interface.

> ℹ️ En dehors de la création et de la réinitialisation par un admin, un utilisateur ne peut pas changer son mot de passe lui-même — c'est un choix volontaire pour un outil interne à petite équipe.

## Journal d'activité

La page **Activité** est l'audit complet de l'application. Chaque action y est enregistrée : qui, quoi, quand, sur quelle cible.

Le journal couvre notamment :

- les connexions (réussies et échouées) ;
- le cycle de vie des livraisons, arrivages et réceptions (création, clôture, réouverture, imports) ;
- chaque scan, chaque mouvement de comptage, chaque annulation — avec le détail exact (quantité, delta, validation manager…) ;
- les soldes de caisses et leurs annulations, avec motif et auteur ;
- la vie des incomplets (création, vente, remise en stock, note, suppression) ;
- l'administration des comptes, des horaires et des congés.

### Filtres

Le journal se filtre par **utilisateur**, **type d'événement** et **période** (par défaut, les 7 derniers jours), avec pagination. Les filtres se conservent en changeant de page.

## Une traçabilité de bout en bout

C'est un principe transverse de FeroceWork : **aucune action ne disparaît**. Annuler un scan ou un comptage ne supprime rien — l'événement est marqué comme annulé et reste consultable. En cas de litige sur une réception, le journal permet de reconstituer précisément ce qui s'est passé.
