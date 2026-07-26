# Livraisons

**Accès : logistique, manager, administrateur.**

## À quoi ça sert

Une **livraison** sert à vérifier une livraison **annoncée** : on importe le fichier de ce qui est prévu (lignes article × éleveur × lot avec les quantités attendues), puis on compte ce qui arrive réellement — au scan ou à la main. L'application calcule les écarts en continu et produit un rapport final.

> 💡 C'est le flux « tout-en-un » historique de l'application. Pour le circuit en deux temps (annonce d'un côté, constat de l'autre), voyez [Arrivages](Arrivages) et [Réceptions](Receptions).

## Créer une livraison

1. Cliquez sur **Nouvelle livraison**.
2. Renseignez une **référence** (obligatoire), et si besoin le fournisseur et la date prévue.
3. Déposez le **fichier des lignes attendues** (obligatoire) : code article, désignation, éleveur, quantité, et éventuellement lot et référence fournisseur.
4. Un second fichier, celui des **colis (SSCC)**, peut être déposé en même temps ou importé plus tard depuis la fiche.

Si le fichier est mal formé, rien n'est créé : l'application affiche la liste des lignes fautives avec leur numéro, pour corriger le fichier avant de réessayer.

## La fiche livraison

Elle regroupe tout le travail de vérification :

- les **compteurs** : lignes conformes, manquantes, en excédent, incomplets déclarés, lignes validées, progression globale ;
- la zone **caisses SSCC** : scan des colis annoncés ;
- la zone de **comptage** ligne par ligne.

## Compter

### Au scan

Deux modes de scan des codes-barres article : **douchette** (champ auto-focalisé, aucun réglage) ou **caméra** du téléphone. Chaque scan déclenche un bip et une vibration — aigus si tout va bien, graves si le code est hors livraison — et affiche un bandeau avec la désignation et le ratio compté/attendu. Un bouton **Annuler** est disponible immédiatement.

Pour les caisses SSCC : une caisse simple est confirmée automatiquement ; une caisse mixte, un code inconnu ou une quantité inhabituelle ouvrent une fenêtre de confirmation article par article. Une caisse confirmée peut être dé-confirmée.

### À la main

Chaque ligne propose :

- des boutons **+1 / −1** ;
- une **calculatrice** intégrée, en mode « ajouter » ou « remplacer », qui accepte les expressions du type `3×24+2` ;
- la **détection automatique du conditionnement** : si la désignation contient « ×10 », un bouton +10 apparaît tout seul ;
- un bouton **Annuler** qui défait le dernier mouvement de la ligne ;
- une case **Ligne validée** pour marquer la ligne comme terminée ;
- un bouton pour déclarer des [sachets incomplets](Incomplets) sur cette ligne.

Des filtres par éleveur, par lot et une recherche libre permettent de ne voir que ce qu'on est en train de traiter ; on peut aussi masquer les lignes déjà validées. Vos préférences d'affichage sont mémorisées.

Le total d'une ligne ne peut jamais devenir négatif, et chaque mouvement est tracé : annuler ne supprime rien, cela marque simplement le mouvement comme annulé.

## Clôturer

Le bouton **Clôturer** demande confirmation, avec un avertissement explicite si des écarts subsistent. Une livraison clôturée est en lecture seule ; le bouton **Rouvrir** permet de revenir en arrière si nécessaire.

## Exports

Trois formats depuis la fiche :

- **CSV** et **Excel** — une ligne par ligne de livraison : attendu, scanné, manuel, total compté, écart, et un statut en clair (Conforme, Excédent, Manquant, Non compté). Les fichiers s'ouvrent directement dans Excel en français, sans manipulation d'encodage.
- **PDF** — rapport avec statistiques et zone de signatures. Un panneau d'options permet de regrouper par produit (avec sous-totaux) et de trier par éleveur et/ou lot, dans l'ordre de priorité de votre choix ; les options sont mémorisées.

Si la livraison comporte des sachets incomplets, un bandeau propose en plus un export (CSV et PDF) limité aux incomplets de cette livraison.

## Rechercher dans les livraisons

La liste des livraisons offre une recherche sur la référence et le fournisseur, ainsi qu'un filtre de statut (Toutes / En cours / Clôturées). Les filtres sont inscrits dans l'adresse de la page : vous pouvez mettre une vue en favori ou l'envoyer à un collègue.
