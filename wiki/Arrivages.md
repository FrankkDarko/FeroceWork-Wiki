# Arrivages

**Accès : logistique, manager, administrateur.**

## À quoi ça sert

Un **arrivage** enregistre un lot de caisses **annoncées** mais pas encore arrivées physiquement — typiquement du stock encore en entrepôt déporté ou en transit. L'arrivage constitue un « réservoir » de caisses connues de l'application : le jour où les palettes arrivent, chaque caisse scannée en [réception](Receptions) est automatiquement reconnue et rattachée à son arrivage d'origine.

Un arrivage ne se « compte » pas : il se **vide** au fil des réceptions.

## Créer un arrivage

1. Depuis la liste des arrivages, cliquez sur **Nouvel arrivage**.
2. Renseignez une **référence** (obligatoire), et si vous le souhaitez un fournisseur et une date.
3. Déposez le **fichier des colis** (obligatoire) : c'est lui qui contient les codes SSCC des caisses annoncées, avec pour chacune l'éleveur, l'article, le lot et la quantité. Un fichier de lignes détaillées peut être ajouté en complément, mais il est facultatif.
4. Validez : les caisses sont créées avec le statut **Attendu (déporté)**.

> 💡 Si certains codes SSCC du fichier sont déjà connus de l'application (doublon d'import, ou historique d'un ancien flux), ils sont ignorés et un message vous l'indique clairement sur la page de l'arrivage. Rien n'est créé en double.

## Suivre un arrivage

La liste des arrivages raisonne en **caisses** : annoncées, reçues, soldées, et surtout **« restant déporté »** — ce qui est encore attendu. Une pastille verte « Tout reçu » apparaît quand il ne reste rien.

La fiche d'un arrivage affiche :

- quatre compteurs : caisses annoncées / reçues / soldées / restant déporté ;
- le tableau des colis : code SSCC, éleveur, article, lot, quantité, **statut**, et un lien direct vers la réception où la caisse a été scannée.

Le tableau est paginé (les gros arrivages dépassent couramment le millier de caisses), avec une recherche libre et des filtres par statut ; vos filtres sont conservés quand vous changez de page.

## Les statuts d'une caisse

| Statut | Signification |
|---|---|
| **Attendu (déporté)** | Annoncée, pas encore scannée nulle part. |
| **Reçu** | Scannée dans une réception ; la réception de rattachement est indiquée. |
| **Transféré** | Caisse issue de l'ancien flux, rattachée après coup à une réception. |
| **Soldé** | Sortie du circuit sur décision d'un manager (voir ci-dessous). |

## Solder une caisse (manager / admin)

Quand une caisse annoncée n'arrivera jamais (casse, erreur d'annonce, litige fournisseur…), un manager ou un administrateur peut la **solder** :

1. Sur la ligne de la caisse, cliquez sur **Solder**.
2. Saisissez un **motif** (obligatoire, 3 caractères minimum).
3. La caisse sort du « restant déporté » et n'est plus attendue.

Le motif et l'auteur du solde restent affichés sous le statut, et l'action est inscrite au [journal d'activité](Administration). Tant que la caisse n'a pas été reçue entre-temps, le solde est **réversible** : un bouton Annuler la remet en « attendu ».
