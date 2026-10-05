# Préparation de commandes

**Accès : logistique, manager, administrateur.**

## À quoi ça sert

Produire, pour un jour de préparation, tout ce qu'il faut pour monter et expédier les cartons :

- le **listing** — la préparation commande par commande ;
- le **picking** — les totaux par article, rangés par famille de produits, pour sortir la marchandise en un seul passage ;
- le **fichier Chronopost** — l'import des étiquettes, avec le poids de chaque colis ;
- les **factures** — une page par commande, à glisser dans le carton.

La page a deux onglets : **Depuis Shopify** (le cas courant) et **Depuis un export CSV** (l'outil d'origine, pour un fichier qu'on a déjà sous la main ou un jour où Shopify ne répond pas).

## Depuis Shopify

### 1. Choisir le jour et charger

Le **jour de préparation** est proposé par défaut : aujourd'hui, ou lundi si l'on ouvre la page un week-end. On peut choisir n'importe quelle date. **Charger les commandes** lit Shopify (une quinzaine de secondes) et reprend les commandes qui se montent ce jour-là, avec la même règle que la page [Semaine](Semaine) :

- la France livrée **le lendemain**, le BELUX livré **le surlendemain** ;
- le vendredi, tout ce qui arrive jusqu'au mardi.

Seules les commandes **non expédiées**, en mode de livraison **« Shipping »**, sont reprises. Celles du jour qui ne le sont pas — déjà expédiées, en attente — sont comptées et annoncées sous le titre, pour expliquer l'écart avec la page Semaine.

### 2. Générer les documents

- **Aperçu Listing** et **Aperçu Picking** ouvrent le PDF dans une fenêtre, d'où on le **télécharge** ou l'**imprime**.
- **Fichier Chronopost** télécharge le fichier d'import des étiquettes. Si un article n'a pas de poids enregistré, le fichier est bloqué et les articles concernés sont listés : leur poids se renseigne dans **Étiquettes Chrono**, puis on recharge la page.
- **Aperçu Factures** relit les factures dans Shopify et produit **un seul PDF, une page par commande**, dans l'ordre du listing.

### Les factures

Elles reprennent la facture Shopify rubrique pour rubrique : adresses, lignes, remises, TVA, total, paiements, note. **Tous les montants viennent de Shopify tels quels**, lignes à 0 € comprises.

- Le **code-barres** du numéro de commande est en tête de page, à scanner au moment de fermer le carton (il encode les chiffres du numéro, sans le « # »).
- Quand la commande porte un tag **« livret … »** (livret huile/suif, livret cuisson…), le livret à glisser dans le carton est rappelé **juste sous la ligne de la box**, sans prix.
- Une facture tient **toujours sur une page** : quand une commande est longue, ses lignes d'articles rétrécissent pour tenir.

**Mise en page des factures** (panneau sous les boutons) : par défaut, les articles suivent l'ordre de la commande. En option, ils sont **séparés par type** comme sur le picking, dans l'ordre de types qu'on choisit, et triés par ordre alphabétique si on le souhaite. La ligne « Box » reste toujours en tête. **Enregistrer pour tout le monde** garde le réglage pour toute l'équipe et les jours suivants. Seul l'ordre change : aucune ligne n'est masquée.

### Commandes divisées : viande et vinaigre de cidre

Une commande qui mêle viande et vinaigre de cidre est **divisée** dans Shopify en deux expéditions : le carton réfrigéré d'un côté, le carton de vinaigre de l'autre.

- Seule la **partie viande** est préparée : le vinaigre n'entre ni dans le listing, ni dans le picking, ni dans le poids Chronopost. Les commandes concernées sont nommées à l'écran.
- Une commande dont il ne reste que le vinaigre à expédier n'est pas reprise.
- Un vinaigre qui voyage dans le même carton que la viande, faute de division, reste dans le carton.
- La facture, elle, garde toutes les lignes de la commande.

La section **Vinaigre de cidre — Colissimo** liste les parties vinaigre à envoyer : par défaut celles du jour choisi, ou d'un clic **toutes celles en attente**, quelle que soit la date du carton viande. Pour chaque commande : le numéro, le destinataire, le jour de livraison de la viande (ou « déjà partie ») et le nombre de cartons. **Copier les numéros** aide à les retrouver dans l'**application Colissimo de Shopify**, où se font leurs étiquettes.

### Box générées sans leurs lignes

Il arrive qu'une commande n'ait que la ligne « Box M », sa composition n'étant écrite que dans le détail de la box (« Le Haché Féroce : x2 »). FeroceWork reprend alors la composition de ce détail — dans le listing, le picking, le fichier Chronopost et la facture (où chaque pièce porte la mention « Composition de la box », à 0 €). Ces commandes sont signalées en orange : **à vérifier au moment de monter le carton**.

### Confidentialité

Les commandes sont lues dans Shopify **à la demande** et ne font que passer : rien n'est stocké en base. Les PDF et le fichier Chronopost sont fabriqués **dans votre navigateur**.

## Depuis un export CSV

1. **Déposez le fichier** d'export des commandes (glisser-déposer).
2. La **date de livraison** se pré-remplit à partir du nom du fichier ; vous pouvez la modifier ou la laisser vide.
3. La page affiche une **synthèse** : nombre de commandes, de lignes, d'articles distincts, total de produits, puis un récapitulatif par **famille**.
4. Deux boutons ouvrent l'**aperçu PDF** du listing et du picking.

Le fichier est **traité entièrement dans votre navigateur** : rien n'est envoyé au serveur, rien n'est enregistré.

## Bon à savoir

- Le classement par famille se fait d'après le libellé des articles. Un article que l'application ne sait pas classer tombe volontairement dans **« autre »**, pour qu'il saute aux yeux pendant la préparation.
- Les **Box** sont ignorées dans le picking : leur contenu figure en lignes séparées, il n'est compté qu'une fois.
- Les quantités d'un même article sont additionnées toutes commandes confondues dans le picking.
- Les familles vides sont masquées à l'écran mais conservées dans le PDF, pour que la mise en page reste identique d'une semaine à l'autre.
