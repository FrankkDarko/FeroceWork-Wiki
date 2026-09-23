# Suivis Chrono

**Accès : logistique, manager, administrateur.**

## À quoi ça sert

Après la génération des étiquettes, Chronopost renvoie un fichier avec le **numéro de suivi** de chaque colis. La page **Suivis Chrono** (menu OPS) reporte ces numéros dans les commandes Shopify : chaque commande passe en **expédiée** et le client reçoit son **mail de suivi**.

C'est le seul écran de FeroceWork qui écrit dans Shopify.

## Confidentialité

Le fichier retour contient les nom, adresse et mail des destinataires. Il est **lu dans votre navigateur** : seuls le numéro de commande, l'identifiant Shopify et le numéro de suivi sont envoyés au serveur.

## Les étapes

### 1. Déposer le fichier

Glissez le fichier retour Chronopost (.txt ou .csv) dans la zone de dépôt, ou cliquez pour le choisir. L'écran annonce combien de numéros de suivi ont été lus, et les lignes écartées avec leur raison (numéro de suivi illisible, identifiant manquant, commande en double dans le fichier).

### 2. Vérifier auprès de Shopify

Le bouton **Vérifier auprès de Shopify** relit chaque commande, **sans rien écrire**, et annonce ce qui se passera :

| État | Ce que ça veut dire |
|---|---|
| **À expédier** | La commande recevra son suivi. |
| **Expédiée sans suivi — le suivi sera remis** | La commande est déjà expédiée mais n'a plus de numéro : il a été retiré à la main dans Shopify. Le numéro du fichier y sera remis. |
| **Suivi déjà posé** | Rien à faire, la commande a déjà son suivi. |
| **Commande introuvable** | L'identifiant du fichier ne correspond à aucune commande. |
| **Le n° ne correspond pas à l'identifiant** | Le numéro et l'identifiant du fichier désignent deux commandes différentes : on ne tranche pas. |
| **Commande annulée** | Rien ne sera écrit. |
| **Colis multiple — à vérifier** | Plusieurs numéros pour une même commande : à traiter à la main. |

Un envoi **annulé** dans Shopify ne compte pas comme un suivi posé : la commande repasse « à expédier ».

### 3. Lancer l'envoi

Relisez l'aperçu, puis cliquez **Envoyer**. C'est définitif : Shopify ne permet pas d'annuler un mail déjà envoyé.

## L'envoi continue sans vous

L'envoi se fait **sur le serveur**. Une fois lancé, vous pouvez **quitter la page, fermer l'onglet ou verrouiller le téléphone** : il continue jusqu'au bout. En revenant sur la page, le lot en cours est affiché en tête avec sa barre d'avancement. S'il s'est terminé pendant votre absence, un message l'annonce — suivis posés, commandes en échec — pendant 24 heures, ou jusqu'à ce que vous le refermiez.

- **Arrêter** interrompt le lot : ce qui est posé reste posé.
- Après cinq échecs d'affilée, le lot **s'arrête de lui-même** — le problème est alors général (droit Shopify, connexion) — et la raison est affichée.
- **Reprendre** relance un lot arrêté ou interrompu : les commandes en échec sont retentées, celles déjà traitées ne sont pas touchées.

Chaque commande est relue juste avant d'écrire : une commande expédiée entre-temps depuis l'admin Shopify est reconnue et n'est pas traitée deux fois. **Relancer le même fichier ne double jamais un suivi.**

Un seul lot peut tourner à la fois.

## Derniers envois

En bas de page, les cinq derniers lots avec leur état (en cours, terminé, arrêté, interrompu), le nombre de suivis posés et d'échecs. **Détail** affiche, commande par commande, le suivi posé ou la raison de l'échec.

Chaque suivi posé est inscrit au [journal d'activité](Administration).
