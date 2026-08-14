# Inventaires

**Accès : logistique, manager, administrateur.**

## À quoi ça sert

Un **inventaire** compte ce qui est **physiquement présent** en stock, carton par carton, à un instant donné. Contrairement à une [réception](Receptions), il ne modifie rien : il **constate**. Vous pouvez compter des caisses déjà reçues, encore attendues, ou même inconnues de l'application — l'inventaire photographie le stock tel qu'il est.

À la fin, un **PDF trié par produit** donne le résultat du comptage, avec sous-totaux par article et total général.

## Créer un inventaire

1. Depuis la liste des inventaires, cliquez sur **Nouvel inventaire**.
2. Le formulaire est minimal : une **référence** pré-remplie avec la date du jour, et une note libre (facultative) — par exemple la zone comptée.
3. Cliquez sur **Créer et passer au comptage** — vous êtes prêt à scanner.

## Compter les cartons

Scannez chaque caisse (code SSCC) à la douchette, ou saisissez le code à la main. Le champ de scan garde le focus en permanence.

**Chaque scan demande une validation** — c'est le principe de l'inventaire, il n'y a jamais de validation automatique :

1. L'application retrouve le carton dans les arrivages et livraisons, et **propose sa valeur supposée** (la quantité annoncée, ou la quantité corrigée à la réception si elle avait été rectifiée).
2. Une fenêtre s'ouvre avec l'article, l'éleveur, le lot et la quantité proposée.
3. Appuyez sur **Entrée** pour valider la quantité proposée (le bouton **Valider** a déjà le focus), ou cliquez sur **Corriger** pour saisir la quantité réellement comptée.

Selon la caisse scannée :

| Cas | Réaction |
|---|---|
| Caisse connue, pas encore comptée dans cet inventaire | ✅ Fenêtre de validation avec la quantité proposée. |
| Caisse « mixte » (plusieurs articles) | ⚠️ Validation article par article, dans la même fenêtre. |
| Caisse **déjà comptée** dans cet inventaire | ⛔ Refus, avec la date et l'opérateur du premier comptage. |
| Code SSCC **inconnu** de l'application | ✏️ La **saisie manuelle** s'ouvre pré-remplie : le carton est compté quand même, marqué « hors base ». |

> 💡 Comme pour les réceptions : un même code relu par erreur dans la foulée est ignoré, et les scans en rafale sont mis en file d'attente — rien ne se perd.

## La saisie manuelle

Le bouton **Saisie manuelle** permet de compter ce qui n'a pas de carton scannable : stock en vrac, étiquette illisible, carton hors base. Le formulaire est le même que pour les [incomplets](Incomplets) : recherche du produit (désignation, code article ou SKU), éleveur, lot et quantité.

Ces comptages sont marqués **« Manuel »** (ou **« Hors base »** si un SSCC inconnu a été scanné) dans la trace et dans les exports — on sait toujours ce qui a été compté à la main.

## Suivre l'inventaire

La fiche affiche en continu :

- trois compteurs : **comptages**, **pièces**, et saisies manuelles ;
- le tableau **« Stock compté »**, agrégé par article × éleveur × lot, avec la part saisie à la main ;
- la **trace des comptages**, chacun avec son SSCC, son type (scan, manuel, hors base), la mention « Corrigé » le cas échéant, l'heure et l'opérateur.

## Corriger une erreur

Chaque comptage porte un bouton **Annuler** tant que l'inventaire est ouvert. L'annulation retire exactement la quantité qui avait été validée et le carton peut être rescanné. L'opération est tracée au journal d'activité.

## Clôturer

En fin de comptage, cliquez sur **Clôturer**. Un inventaire clôturé passe en lecture seule : plus aucun scan ni annulation n'est accepté. Il reste **rouvrable** en cas de besoin.

## Exports

Trois formats sont disponibles depuis la fiche :

- **PDF** — le livrable de l'inventaire : **toujours trié et regroupé par produit**, avec sous-total par article, total général, et une section d'audit listant les saisies manuelles.
- **Excel** — deux feuilles : la synthèse par produit, et la trace complète des comptages.
- **CSV** — une ligne par comptage, avec le SSCC, le type, les corrections, la date et l'opérateur.

Les exports contiennent toujours **tous** les comptages, même quand l'écran n'affiche que les plus récents.
