# Recherche SSCC

**Accès : logistique, manager, administrateur. Outil en lecture seule — aucune donnée n'est modifiée.**

## À quoi ça sert

Répondre en un scan à la question de terrain la plus fréquente : **« cette caisse, elle en est où ? »**

La recherche interroge la totalité des caisses connues de l'application, tous flux confondus : [arrivages](Arrivages), [livraisons](Livraisons) historiques et [réceptions](Receptions).

## Utilisation

Un seul champ, actif dès l'ouverture de la page. Scannez le code SSCC à la douchette ou tapez-le à la main. Après chaque recherche, le champ reprend le focus : vous pouvez enchaîner les cartons sans toucher à rien.

## Ce que vous obtenez

Le résultat s'affiche en trois blocs :

1. **Le statut global**, dans un bandeau coloré : attendu / reçu / transféré / soldé.
2. **Le parcours de la caisse** :
   - le document d'origine (arrivage ou livraison), avec lien direct et date d'import ;
   - puis, selon le cas : la réception de rattachement avec date, heure et opérateur ; ou le motif de solde avec son auteur ; ou la mention « scanné sur place » pour l'ancien flux ; ou, à défaut, « pas encore reçu — en stock déporté ou en transit ».
3. **Le contenu de la caisse** : un article par ligne (désignation, code, éleveur, lot, quantité) avec le statut de chacun — pratique pour les caisses mixtes partiellement reçues.

Un code absent de toute la base donne un message net : « SSCC inconnu, n'apparaît dans aucun arrivage ni aucune livraison ».

> 💡 Les codes à 20 chiffres (avec préfixe technique d'étiquette) sont automatiquement ramenés au SSCC à 18 chiffres : scannez l'étiquette telle quelle, l'application s'occupe du reste.
