# Semaine

**Accès : logistique, manager, administrateur.**

## À quoi ça sert

L'écran **Semaine** (menu OPS) annonce ce qu'il faudra préparer dans les trois semaines à venir, **jour de préparation par jour de préparation** : nombre de commandes, nombre d'articles, répartition par type de viande et détail des pièces. Il lit les commandes Shopify **en lecture seule** : il ne peut rien modifier dans la boutique, et aucun nom ni adresse de client n'est affiché ni stocké.

Chaque dimanche soir, un **récapitulatif par mail** reprend les mêmes chiffres pour les destinataires choisis.

## Quelles commandes sont comptées

- Seules les commandes en mode de livraison **« Shipping »** : les retraits sur place ne se préparent pas en carton.
- La date de livraison est lue dans le tag posé sur chaque commande, par exemple « Livraison 3 septembre 2026 ». Les variantes d'écriture sont acceptées (accents, majuscules, « 1er », zéro devant).
  - Un tag **illisible** n'est pas deviné : il est signalé dans l'encart orange « tags de livraison à corriger dans Shopify ».
  - Une commande qui porte **deux dates** (l'ancien tag resté après un report) est comptée à la plus tardive, et signalée pour qu'on retire l'ancien tag.
- Une box générée **sans ses lignes d'articles** (seule la ligne « Box M » existe, le contenu n'étant écrit que dans le détail de la box) est comptée avec sa composition, reprise de ce détail.

## Lire une ligne

**Chaque ligne est un jour de préparation** : le jour où l'on monte les cartons. Elle réunit tout ce qui part ce jour-là :

- les commandes **France** (et Monaco) livrées **le lendemain** ;
- les commandes **BELUX** (Belgique, Luxembourg) livrées **le surlendemain** : le transport prend un jour de plus.

Rien ne part le week-end : un départ qui tomberait un samedi ou un dimanche **recule au vendredi**. Le vendredi réunit donc les livraisons France du samedi au lundi et les livraisons BELUX du dimanche au mardi.

Sous le nom du jour, les livraisons servies sont rappelées en petit, une par date et par destination — « livr. samedi 3 oct. · 196 cdes », « BELUX livr. mardi 6 oct. · 1 cde » — pour recouper avec Shopify. Un jour de semaine **sans rien à préparer** apparaît grisé.

> 💡 Les semaines sont bornées par le jour de préparation : une livraison du lundi appartient à la semaine du vendredi où on la monte. Le total d'une semaine dit donc ce qu'on prépare cette semaine-là ; il ne se recoupe pas exactement avec Shopify filtré par date de livraison.

## Semaine en cours et semaines à venir

- **Semaine en cours** : les commandes sont posées, on affiche le **réel**, sans majoration.
- **Semaines suivantes** : elles se remplissent encore. Un abonnement ne crée sa commande que quelques jours avant la livraison, donc trois nombres sont donnés :
  - le **prévu** : les commandes déjà passées **plus** les renouvellements d'abonnement annoncés ;
  - l'**estimation +20 %** : le prévu majoré, pour couvrir les nouveaux abonnés et les commandes hors abonnement ;
  - le **réel** constaté à ce jour.

Un renouvellement est rangé, lui aussi, sur son jour de préparation. Un abonné dont la commande est déjà passée n'est jamais compté deux fois. Les abonnements en pause sont écartés.

> 💡 Le bas de l'écran indique combien d'abonnements ont été relevés et sur quelle fenêtre de commandes : on sait toujours sur quoi repose le chiffre.

## Le détail d'une journée

Cliquer sur une ligne l'ouvre :

- la répartition par type (bœuf, porc, poulet, agneau, poisson, épicerie…), avec les mêmes catégories que le picking ;
- le **détail des pièces** : produit par produit, la quantité à sortir, groupée par type. Sur une semaine à venir, la part venant des renouvellements annoncés est précisée (« dont 4 abo. ») ;
- la liste des commandes du jour, avec leur nombre d'articles ; une pastille BELUX marque les commandes belges et luxembourgeoises, et le survol d'une commande donne son jour de livraison.

Les Box et le « Supplément découpe » ne sont pas comptés : ce ne sont pas des morceaux à sortir.

## Fraîcheur des chiffres

Shopify est lu **une fois par jour**, le matin, par la tâche planifiée — avant l'arrivée de l'équipe. Cette lecture sert ensuite toute la journée à **tous les utilisateurs** : la page s'ouvre tout de suite.

La date et l'heure de la lecture sont affichées **en tête de page**. Le bouton **Forcer la recharge** relit Shopify sur-le-champ (une trentaine de secondes) — pour voir une commande ou un tag posé depuis le matin. La nouvelle lecture sert alors à tout le monde.

## Le récapitulatif du dimanche

Dans le panneau en bas de page :

- **jour et heure d'envoi** (dimanche 20 h par défaut) ;
- **nombre de semaines** annoncées par le mail (1 à 3) ;
- **destinataires** : ajout, désactivation temporaire, suppression ;
- **Envoyer maintenant** pour un envoi immédiat ;
- l'**historique** des envois, réussis comme échoués.

Le mail suit la même règle que l'écran : une ligne par jour de préparation, avec les livraisons servies rappelées dessous. Il part toujours d'une lecture fraîche de Shopify. Sa première semaine est celle qui s'ouvre le lendemain : elle n'est pas majorée, mais elle compte déjà les renouvellements annoncés. Il ne contient **aucune donnée client** — ni nom, ni adresse, ni numéro de commande. Le détail commande par commande se regarde dans FeroceWork.
