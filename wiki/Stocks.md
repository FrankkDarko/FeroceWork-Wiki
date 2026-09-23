# Stocks

**Accès : logistique, manager, administrateur.** La configuration du plan est réservée aux managers et administrateurs.

## À quoi ça sert

Le module **Stocks** montre ce qui est rangé en chambre froide, **emplacement par emplacement**. Chaque case se remplit comme un réservoir : un emplacement presque vide se repère d'un coup d'œil.

Le stock se suit par **produit, éleveur et lot**, en **pièces** — la même maille que les cartons.

> ⚠️ Le stock ne bouge **que par ce qui y est saisi**. Les réceptions, annulations de réception et inventaires ne l'alimentent pas : ce qui est affiché correspond à ce qui a été décidé sur place.

## Le plan

- Les **travées** sont désignées par une lettre, les **positions** le long de la travée par un chiffre : « A3 », comme on le dit sur le terrain.
- Les travées le long des murs ont deux niveaux, **sol** et **étage** ; celles du milieu n'ont que le sol.
- La **chambre froide extérieure** apparaît comme un conteneur unique avec son niveau de remplissage global.
- Un emplacement partagé entre plusieurs produits l'annonce clairement ; le détail complet s'affiche au survol.
- Un emplacement sans capacité renseignée n'affiche pas de jauge, plutôt que de faire semblant d'être plein.

## Sur un emplacement

Cliquez sur une case pour l'ouvrir :

- **Ajouter un produit** / **Ajouter une pièce** — une entrée, avec produit, éleveur, lot et nombre de pièces ;
- **Retirer une pièce** — une sortie, avec un motif facultatif (casse, erreur de comptage…) ;
- **Corriger la quantité** — saisissez la quantité réelle : c'est l'**écart** qui est enregistré ;
- **Déplacer vers un autre emplacement** — un transfert ;
- **Annuler ce mouvement** — écrit un mouvement inverse.

Rien n'est jamais écrasé : chaque mouvement est gardé, on peut toujours remonter qui a fait quoi, quand et pourquoi.

## Configurer le plan (managers)

Depuis **Plan** :

- nombre de **travées** et de **positions** par zone, travées à étage ;
- pour chaque emplacement : **capacité** en pièces, **produit dédié**, ou **désactivé** (allée centrale, pilier…) ;
- **Renuméroter** met les codes à jour après un changement de grille.

## Purger le stock (administrateurs)

Le bouton **Purger le stock** remet tous les emplacements à zéro d'un coup, par exemple après des essais ou un import raté. Le plan est conservé (zones, travées, emplacements, capacités, produits dédiés). C'est définitif : il faut recopier le mot **PURGER** pour déclencher, et l'opération est inscrite au [journal d'activité](Administration).
