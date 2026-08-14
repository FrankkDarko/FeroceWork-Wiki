# Préparation de commandes

**Accès : logistique, manager, administrateur.**

## À quoi ça sert

Transformer l'export des commandes de la boutique en ligne en deux documents de terrain prêts à imprimer :

- le **listing** — la préparation commande par commande ;
- le **picking** — les totaux par article, rangés par famille de produits, pour sortir la marchandise en un seul passage.

## Confidentialité : tout reste dans votre navigateur

Particularité de cet outil : le fichier de commandes est **traité entièrement en local**, dans votre navigateur. Rien n'est envoyé au serveur, rien n'est enregistré en base. Fermez l'onglet, il ne reste aucune trace.

## Utilisation

1. **Déposez le fichier** d'export des commandes (glisser-déposer).
2. La **date de livraison** se pré-remplit automatiquement à partir du nom du fichier ; vous pouvez la modifier ou la laisser vide (elle figure alors simplement en moins sur les documents).
3. L'analyse est immédiate. Si le fichier n'a pas le bon format, un message explicite liste les colonnes attendues.
4. La page affiche une **synthèse** : nombre de commandes, de lignes, d'articles distincts, total de produits, puis un récapitulatif par **famille** (bœuf, porc, poulet, agneau, poisson, épicerie, autre) avec quantités et pourcentages.
5. Deux boutons ouvrent chacun un **aperçu PDF** dans une fenêtre : vous pouvez vérifier le document, puis **Télécharger** ou **Imprimer** directement.

## Bon à savoir

- Le classement par famille se fait d'après le libellé des articles. Un article que l'application ne sait pas classer tombe volontairement dans **« autre »** — c'est fait exprès, pour qu'il saute aux yeux pendant la préparation plutôt que d'être rangé au mauvais endroit.
- Les articles « pack à composer » et les **Box** sont ignorés dans le picking : leur contenu réel figure déjà en lignes séparées dans l'export, il n'est donc compté qu'une fois.
- Les quantités d'un même article sont additionnées toutes commandes confondues dans le picking.
- Les familles vides sont masquées à l'écran mais conservées dans le PDF, pour que la mise en page reste identique d'une semaine à l'autre.
- Les éventuels avertissements d'analyse (lignes ambiguës, valeurs inattendues) sont listés sous les boutons, sans bloquer la génération.
