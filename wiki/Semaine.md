# Semaine

**Accès : logistique, manager, administrateur.**

## À quoi ça sert

L'écran **Semaine** (menu OPS) annonce ce qu'il faudra préparer dans les trois semaines à venir, **jour de préparation par jour de préparation** : nombre de commandes, nombre d'articles, répartition par type de viande et détail des pièces. Il lit les commandes Shopify **en lecture seule** : il ne peut rien modifier dans la boutique, et aucun nom ni adresse de client n'est affiché ni stocké.

Chaque dimanche soir, un **récapitulatif par mail** reprend les mêmes chiffres pour les destinataires choisis. Une version allégée, le **mail Chrono**, annonce au transporteur le nombre de colis par jour.

## Quelles commandes sont comptées

- Seules les commandes en mode de livraison **« Shipping »** : les retraits sur place ne se préparent pas en carton.
- La date de livraison est lue dans le tag posé sur chaque commande, par exemple « Livraison 3 septembre 2026 ». Les variantes d'écriture sont acceptées (accents, majuscules, « 1er », zéro devant).
  - Un tag **illisible** n'est pas deviné : il est signalé dans l'encart orange « tags de livraison à corriger dans Shopify ».
  - Une commande qui porte **deux dates** (l'ancien tag resté après un report) est comptée à la plus tardive, et signalée pour qu'on retire l'ancien tag.
- Une box générée **sans ses lignes d'articles** (seule la ligne « Box M » existe, le contenu n'étant écrit que dans le détail de la box) est comptée avec sa composition, reprise de ce détail. Dès qu'une pièce à 0 € figure sur la commande, c'est elle qui compte : une box modifiée dans Shopify, dont les pièces ont été remplacées, n'est jamais complétée avec ses pièces d'origine.

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
  - l'**estimation** : le prévu majoré, pour couvrir les nouveaux abonnés et les commandes hors abonnement ;
  - le **réel** constaté à ce jour.

La majoration dépend de l'éloignement :

| Semaine | Lundi → mercredi | Jeudi | Vendredi |
|---|---|---|---|
| La semaine prochaine (celle qu'annonce le mail du dimanche) | aucune | **+10 %** | **+15 %** |
| Les suivantes | **+20 %** | **+20 %** | **+20 %** |

Un jour sans majoration n'affiche que son prévu. L'écran et le mail donnent toujours les mêmes chiffres pour la même semaine.

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
- **jour Chrono** : le jour d'envoi du mail Chrono, réglable à part (même heure) ;
- **nombre de semaines** annoncées par le mail complet (1 à 3) ;
- **destinataires** : ajout, désactivation temporaire, suppression, et pour chacun le **modèle** reçu — **Complet** ou **Chrono** ;
- **Envoyer le complet** / **Envoyer le chrono** pour un envoi immédiat d'un modèle (un bouton n'apparaît que si le modèle a au moins un destinataire actif) ;
- l'**historique** des envois, réussis comme échoués, avec le modèle envoyé.

Le mail suit la même règle que l'écran : une ligne par jour de préparation, avec les livraisons servies rappelées dessous. Il part toujours d'une lecture fraîche de Shopify. Sa première semaine est celle qui s'ouvre le lundi suivant : elle compte déjà les renouvellements annoncés, et seuls son jeudi et son vendredi sont majorés. Il ne contient **aucune donnée client** — ni nom, ni adresse, ni numéro de commande. Le détail commande par commande se regarde dans FeroceWork.

### Le mail Chrono

Pour le transporteur, une version réduite aux deux premières colonnes :

- **deux semaines** : **S**, celle qui s'ouvre au lundi suivant l'envoi, et **S+1** — quel que soit le jour d'envoi réglé ;
- pour chaque jour de préparation, les livraisons servies (France, BELUX) et **un seul nombre** : les commandes à expédier ;
- **pas d'articles** ni de types de viande ;
- les jours encore en train de se remplir (jeudi et vendredi de S, tous les jours de S+1) donnent l'**estimation**, marquée d'un astérisque.

Le complet et le Chrono partent chacun à leur jour et sont suivis séparément : l'envoi de l'un n'empêche pas l'autre de partir la même semaine.
