# Semaine

**Accès : logistique, manager, administrateur.**

## À quoi ça sert

L'écran **Semaine** (menu OPS) annonce ce qu'il faudra préparer dans les trois semaines à venir, jour par jour : nombre de commandes, nombre d'articles, répartition par type de viande et détail des pièces. Il lit les commandes Shopify **en lecture seule** : il ne peut rien modifier dans la boutique, et aucun nom ni adresse de client n'est affiché ni stocké.

Chaque dimanche soir, un **récapitulatif par mail** reprend les mêmes chiffres pour les destinataires choisis.

## D'où vient la date de livraison

La date est lue dans le tag posé sur chaque commande Shopify, par exemple « Livraison 3 septembre 2026 ». Les variantes d'écriture sont acceptées (accents, majuscules, « 1er », zéro devant).

- Un tag **illisible** n'est pas deviné : il est signalé dans l'encart orange « tags de livraison à corriger dans Shopify ».
- Une commande qui porte **deux dates** (l'ancien tag resté après un report) est comptée à la plus tardive, et signalée pour qu'on retire l'ancien tag.

## Lire une ligne

Chaque ligne correspond à un jour de livraison, mais c'est le **jour de préparation** qui est écrit en gros : c'est le jour où l'on monte les cartons.

- Une commande **France** (et Monaco) se prépare **la veille** de la livraison.
- Une commande **BELUX** (Belgique, Luxembourg) se prépare **l'avant-veille** : le transport prend un jour de plus. Sa part est indiquée sur la ligne (« BELUX mardi 15 sept. · 3 cdes »), et les commandes concernées portent une pastille BELUX dans le détail.
- Rien ne part le week-end : un départ qui tomberait un samedi ou un dimanche **recule au vendredi**. Une livraison du lundi se prépare donc le vendredi précédent.

Le jour de livraison reste indiqué en petit sous le jour de préparation, pour recouper avec Shopify. Un jour de semaine **sans rien à préparer** apparaît grisé. Les livraisons du samedi, du dimanche et du lundi, préparées le vendredi, n'apparaissent que lorsqu'il y a des commandes ; celle du lundi est alors marquée « sem. préc. », puisque son vendredi est celui de la semaine d'avant.

## Semaine en cours et semaines à venir

- **Semaine en cours** : les commandes sont posées, on affiche le **réel**, sans majoration.
- **Semaines suivantes** : elles se remplissent encore. Un abonnement ne crée sa commande que quelques jours avant la livraison, donc trois nombres sont donnés :
  - le **prévu** : les commandes déjà passées **plus** les renouvellements d'abonnement annoncés ;
  - l'**estimation +20 %** : le prévu majoré, pour couvrir les nouveaux abonnés et les commandes hors abonnement ;
  - le **réel** constaté à ce jour.

Un abonné dont la commande est déjà passée n'est jamais compté deux fois. Les abonnements en pause sont écartés.

> 💡 Le bas de l'écran indique combien d'abonnements ont été relevés et sur quelle fenêtre de commandes : on sait toujours sur quoi repose le chiffre.

## Le détail d'une journée

Cliquer sur une ligne l'ouvre :

- la répartition par type (bœuf, porc, poulet, agneau, poisson, épicerie…), avec les mêmes catégories que le picking ;
- le **détail des pièces** : produit par produit, la quantité à sortir, groupée par type. Sur une semaine à venir, la part venant des renouvellements annoncés est précisée (« dont 4 abo. ») ;
- la liste des commandes du jour, avec leur nombre d'articles.

Les Box et le « Supplément découpe » ne sont pas comptés : ce ne sont pas des morceaux à sortir.

## Fraîcheur des chiffres

Les chiffres sont gardés **cinq minutes** pour que l'écran s'ouvre vite (la lecture complète de Shopify prend une dizaine de secondes). L'heure de lecture est affichée ; le bouton **Actualiser** force une relecture immédiate.

## Le récapitulatif du dimanche

Dans le panneau en bas de page :

- **jour et heure d'envoi** (dimanche 20 h par défaut) ;
- **nombre de semaines** annoncées par le mail (1 à 3) ;
- **destinataires** : ajout, désactivation temporaire, suppression ;
- **Envoyer maintenant** pour un envoi immédiat ;
- l'**historique** des envois, réussis comme échoués.

Le mail part toujours d'une lecture fraîche de Shopify. Sa première semaine est celle qui s'ouvre le lendemain : elle n'est pas majorée, mais elle compte déjà les renouvellements annoncés. Il ne contient **aucune donnée client** — ni nom, ni adresse, ni numéro de commande. Le détail commande par commande se regarde dans FeroceWork.
