# FAQ

## Compte et connexion

### J'ai oublié mon mot de passe, comment le réinitialiser ?
Il n'y a pas de réinitialisation par e-mail : demandez à un administrateur. Il définira un mot de passe temporaire, et l'application vous demandera d'en choisir un nouveau à votre prochaine connexion.

### Pourquoi je ne peux pas changer mon mot de passe moi-même ?
C'est un choix volontaire pour un outil interne : le mot de passe ne se change qu'à la création du compte ou après une réinitialisation par un administrateur. Cela évite les circuits de récupération par e-mail sur un outil fermé.

### Je ne vois pas certaines pages dans le menu (Livraisons, Réceptions…).
Votre rôle ne vous y donne pas accès. Voyez [Rôles et permissions](Roles-et-permissions) ; si vous pensez qu'il vous manque un accès, adressez-vous à un administrateur.

## Scan

### La douchette ne semble pas réagir.
Vérifiez que vous êtes bien sur la page de scan : le champ s'y auto-focalise en permanence. Même si le focus a été perdu (clic ailleurs), l'application intercepte les rafales de la douchette — scannez simplement à nouveau. Si rien ne se passe, vérifiez le branchement de la douchette : elle doit se comporter comme un clavier.

### Le scan à la caméra ne démarre pas.
Le mode caméra nécessite une connexion sécurisée (HTTPS) et l'autorisation d'accéder à la caméra dans le navigateur. Vérifiez l'invite d'autorisation, ou repassez en mode douchette.

### J'ai scanné deux fois la même caisse par erreur.
Rien de grave : un même code relu dans la foulée est ignoré automatiquement. Et si une caisse a réellement été rattachée par erreur, le bouton **Annuler** sur sa ligne la remet en « attendu » dans son arrivage.

### Le scan est refusé avec « déjà reçu ».
La caisse a déjà été scannée dans une autre réception — le message indique laquelle, quand, et par qui. Si c'est un cas exceptionnel légitime, un manager peut valider le re-scan pour les caisses de l'ancien flux.

### Le scan est refusé avec « SSCC inconnu ».
Le code n'apparaît dans aucun arrivage ni aucune livraison. Vérifiez que l'arrivage correspondant a bien été importé ; utilisez la [Recherche SSCC](Recherche-SSCC) pour investiguer.

## Imports et exports

### Mon fichier CSV est refusé à l'import.
Rien n'est créé en cas d'erreur : le message liste les lignes fautives avec leur numéro. Corrigez le fichier (colonnes attendues, lignes incomplètes) et déposez-le à nouveau. Les fichiers avec séparateur point-virgule ou virgule sont acceptés.

### Le fichier CSV exporté s'ouvre mal dans Excel.
Normalement non : les exports sont prévus pour s'ouvrir directement dans Excel en français (séparateur point-virgule, encodage adapté). Si un fichier s'affiche mal, ouvrez-le via un double-clic plutôt que par un import manuel.

### L'écran n'affiche pas toutes les caisses / tous les sachets.
Sur les très gros volumes, l'écran se limite aux lignes les plus récentes pour rester rapide. Les **exports contiennent toujours l'intégralité des données**.

## Comptage et corrections

### J'ai validé une clôture trop tôt.
Les livraisons et réceptions clôturées sont **rouvrables** : bouton Rouvrir sur la fiche.

### J'ai fait une erreur de comptage.
Chaque ligne a un bouton **Annuler** qui défait le dernier mouvement. Pour corriger en bloc, la calculatrice en mode « remplacer » permet de saisir directement le bon total.

### Une caisse annoncée n'arrivera jamais, que faire ?
Un manager ou un administrateur peut la **solder** depuis la fiche de l'arrivage, avec un motif. Elle sort alors du « restant déporté ». L'opération est réversible tant que la caisse n'a pas été reçue.

## Horaires et congés

### Mes journées apparaissent pré-remplies avec un badge « à valider ». C'est compté ?
Non : le pré-remplissage vient de votre horaire type et n'est **pas compté tant que vous n'avez pas validé le jour**. Pensez à valider chaque journée réellement travaillée.

### Ma demande de congé est approuvée, mais je ne vois rien sur mes horaires.
L'absence est créée automatiquement à l'approbation et apparaît en badge sur les jours concernés. Vérifiez que vous regardez le bon mois ; sinon, adressez-vous à votre manager.

### Mon solde d'heures sup ne bouge pas d'un mois sur l'autre.
Le report n'est pas automatique : c'est un manager ou un administrateur qui décide de **reporter** les heures supplémentaires d'un mois. Tant que le mois n'est pas reporté, ses heures sup restent affichées sur ce mois seulement.

## Divers

### Où vont les données de l'outil Préparation de commandes ?
Nulle part : le fichier est traité entièrement dans votre navigateur, rien n'est envoyé au serveur ni conservé. Voir [Préparation de commandes](Preparation-de-commandes).

### Qui peut voir ce que j'ai fait dans l'application ?
Les administrateurs disposent d'un [journal d'activité](Administration) qui trace toutes les actions (scans, comptages, validations, connexions…). C'est ce qui permet de reconstituer une réception en cas de litige.
