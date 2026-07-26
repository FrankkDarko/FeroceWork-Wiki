# Incomplets

**Accès : logistique, manager, administrateur.**

## À quoi ça sert

Les **incomplets** sont les sachets dont le poids ou la quantité est en défaut, constatés au moment de la réception. Plutôt que de les perdre de vue, l'application les suit de leur mise en stock jusqu'à leur écoulement, quand ils sont rattachés à un numéro de commande.

## La page Incomplets

Deux onglets avec compteurs :

- **En stock** — les sachets en attente d'être écoulés ;
- **Vendus** — ceux déjà rattachés à une commande.

Les sachets sont regroupés par produit en sections repliables. Des filtres par produit, éleveur et lot, plus une recherche libre (désignation, code, référence, éleveur, lot, numéro de commande, note) permettent de retrouver rapidement un sachet précis.

## Déclarer un incomplet

Deux chemins :

1. **Depuis une ligne de livraison** — un bouton dédié sur chaque ligne de comptage ouvre la saisie avec le produit, l'éleveur et le lot déjà pré-remplis. Les sachets créés sont rattachés à la livraison d'origine et alimentent son compteur « Incomplets ».
2. **Depuis la page Incomplets** — le bouton **Nouvel incomplet** : recherche du produit, éleveur, lot, nombre de sachets, et **un poids saisi pour chaque sachet** (les poids diffèrent généralement d'un sachet à l'autre ; la virgule est acceptée). Une note libre est possible. Si vous renseignez directement un numéro de commande, les sachets sont créés comme « vendus ».

## Gérer les sachets

Sur chaque sachet :

- **Vendre** — saisissez le numéro de commande : le sachet passe dans l'onglet Vendus.
- **Remettre en stock** — annule une vente faite par erreur.
- **Note** — modifiable directement sur la ligne.
- **Supprimer** — avec confirmation.

Toutes ces actions sont inscrites au [journal d'activité](Administration).

## Exports

Deux formats, **CSV** et **PDF**, contextuels à l'onglet actif (en stock ou vendus). Depuis une fiche livraison, les mêmes exports existent, restreints aux incomplets de cette livraison.

> 💡 Quand l'historique devient très volumineux, l'écran n'affiche que les lignes les plus récentes, mais les exports contiennent toujours l'intégralité des données.
