# Réceptions

**Accès : logistique, manager, administrateur.**

## À quoi ça sert

Une **réception** enregistre ce qui arrive **réellement**, un jour donné, sans qu'on ait besoin de savoir à l'avance de quel [arrivage](Arrivages) viennent les palettes. C'est le pendant terrain de l'arrivage : l'arrivage annonce, la réception constate.

Une réception est créée **vide** et se remplit uniquement au scan. Le scan est **global** : vous scannez une caisse, l'application la retrouve toute seule dans l'ensemble des arrivages et la rattache automatiquement.

## Créer une réception

1. Depuis la liste des réceptions, cliquez sur **Nouvelle réception**.
2. Le formulaire est minimal : une **référence** pré-remplie avec la date du jour, et une note libre de provenance (facultative).
3. Cliquez sur **Créer et passer au scan** — vous êtes prêt à scanner.

## Scanner les caisses

Posez-vous devant la palette et scannez chaque caisse (code SSCC) à la douchette. Le champ de scan garde le focus en permanence et le reprend après chaque action : vous pouvez enchaîner sans toucher ni clavier ni souris. Vous pouvez aussi saisir un code à la main.

Selon la caisse scannée, l'application réagit différemment :

| Cas | Réaction |
|---|---|
| Caisse d'un arrivage, jamais reçue | ✅ Rattachement automatique, bandeau vert de confirmation. |
| Caisse de l'ancien flux, jamais scannée | ✅ **Transfert automatique**, signalé par une pastille « Transféré » avec la référence d'origine. |
| Caisse déjà scannée dans une **autre** réception | ⛔ Refus « déjà reçu », avec la réception, la date et l'opérateur concernés. |
| Caisse déjà scannée dans **cette** réception | ℹ️ Rien à faire : elle n'est pas recomptée. |
| Caisse de l'ancien flux déjà pointée à l'époque | ⛔ Refus, sauf **validation explicite d'un manager** dans une fenêtre de confirmation. |
| Caisse « mixte » (plusieurs articles) ou quantité inhabituellement élevée | ⚠️ Fenêtre de confirmation article par article, avec possibilité de corriger la quantité réellement comptée. |
| Code SSCC inconnu | ⛔ Refus, message explicite. |

Chaque scan se confirme **au son et à la couleur**, sans avoir à lire l'écran :

| Signal | Signification |
|---|---|
| 🟢 Bip aigu + flash vert | La caisse est prise en compte. |
| 🟠 Deux notes + flash orange | Une action est demandée : la fenêtre de confirmation s'ouvre. |
| 🔴 Bip grave + flash rouge | La caisse n'est **pas** prise en compte (inconnue, déjà reçue dans une **autre** réception, erreur) : mettez-la de côté ou rescannez-la. |
| 🔵 Deux petits « tic » + flash bleu léger | Rien à faire : la caisse est déjà comptée dans **cette** réception, ou vient d'être scannée à l'instant. |

Sur téléphone, chaque cas vibre aussi différemment.

> 💡 Un même code relu dans la foulée (moins d'une seconde) n'est compté qu'une fois, avec le message « Déjà scanné à l'instant ». Le champ de scan reste actif pendant l'envoi d'une caisse : il se vide dès la lecture et accepte aussitôt la suivante. Les caisses lues pendant un envoi partent dans l'ordre, et un compteur « N scans en attente d'envoi » s'affiche sous le champ tant qu'il en reste : la douchette peut aller plus vite que le réseau, rien ne se perd.

### Quand le wifi coupe (chambre froide)

Continuez à scanner. À l'ouverture de la réception, le téléphone a chargé la liste des caisses attendues : si le serveur ne répond plus, chaque caisse est jugée **sur le téléphone**, avec les mêmes règles et les mêmes signaux (bip, couleur, fenêtre de confirmation pour un colis mixte ou une quantité à vérifier).

- Un bandeau orange **« Hors ligne — N scans gardés sur le téléphone »** indique combien de caisses attendent d'être envoyées.
- Les scans sont gardés même si la page se recharge ou si le téléphone s'éteint.
- Au retour du réseau, ils partent **tout seuls**, avec leur heure réelle, et un message confirme l'envoi. Ils partent même si vous avez quitté l'écran de la réception, tant que vous êtes connecté avec le même compte.
- Cas rare : si un collègue a reçu la même caisse dans une **autre** réception pendant la coupure, un message « Scan hors ligne refusé » nomme la caisse à vérifier.

> ⚠️ Si la session a expiré pendant la coupure, le bandeau le dit : reconnectez-vous avec **le même compte**, les scans partiront ensuite.

## Suivre la réception

La fiche affiche en continu :

- trois compteurs : **caisses reçues**, **pièces**, et transferts de l'ancien flux ;
- le tableau **« Contenu reçu »**, agrégé par éleveur × article × lot ;
- la liste des caisses scannées, chacune avec son **origine cliquable** (l'arrivage ou la livraison d'où elle vient), l'heure du scan et l'opérateur.

## Corriger une erreur

Chaque caisse reçue porte un bouton **Annuler** tant que la réception est ouverte. L'annulation retire exactement la quantité qui avait été comptée (même corrigée à la main), détache la caisse et la remet en « attendu » dans son arrivage. L'opération est tracée au journal d'activité.

## Clôturer

En fin de réception, cliquez sur **Clôturer** (confirmation demandée). Une réception clôturée passe en lecture seule : plus aucun scan ni annulation n'est accepté. Elle reste **rouvrable** en cas de besoin.

## Exports

Trois formats sont disponibles depuis la fiche :

- **CSV** — une ligne par caisse × article, avec le SSCC, la provenance, le type d'origine (arrivage ou transfert), la date de scan et le nom de l'opérateur : c'est la pièce de traçabilité de référence.
- **Excel** — le contenu reçu, mis en forme et prêt à imprimer.
- **PDF** — avec un panneau d'options : regrouper par produit, trier par éleveur et/ou par lot. Vos options sont mémorisées pour la prochaine fois.

Les exports contiennent toujours **toutes** les caisses, même quand l'écran n'affiche que les plus récentes.
