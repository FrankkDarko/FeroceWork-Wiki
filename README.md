# FeroceWork

> **L'application interne qui fiabilise les réceptions de marchandises et simplifie la gestion d'équipe, du scan des colis au suivi des horaires.**

---

## 🎯 Le projet

FeroceWork est une application web interne développée pour les équipes logistiques et administratives de l'entreprise. Elle est née d'un constat simple : vérifier une livraison à la main, en comparant les produits reçus avec un listing papier ou un tableur, c'est long, source d'erreurs, et sans traçabilité.

L'application remplace ce processus par un flux entièrement numérique : les marchandises annoncées sont importées dans l'outil, les colis sont scannés à leur arrivée (douchette ou caméra), les écarts sont détectés automatiquement, et des rapports propres (CSV, Excel, PDF) sont générés en fin de réception. Chaque action est tracée : on sait toujours qui a fait quoi, et quand.

Au fil du temps, FeroceWork s'est enrichi d'un volet RH complet : saisie des horaires, calcul automatique des heures supplémentaires, demandes de congés avec circuit de validation, et gestion des absences.

## ✨ Fonctionnalités principales

### Logistique
- **Arrivages** — enregistrement des lots de caisses annoncées (stock déporté), qui deviennent scannables le jour où les palettes arrivent physiquement.
- **Réceptions** — constat de ce qui arrive réellement : scan global des caisses (codes SSCC), rattachement automatique à leur arrivage d'origine, détection des doublons et des codes inconnus.
- **Livraisons** — vérification d'une livraison annoncée : import du fichier attendu, comptage par scan ou saisie manuelle (boutons +1/−1, calculatrice intégrée), validation ligne par ligne, clôture avec rapport d'écarts.
- **Recherche SSCC** — un scan suffit pour répondre à « où est ce carton ? » : statut, parcours complet et contenu détaillé de n'importe quelle caisse.
- **Incomplets** — suivi des sachets incomplets constatés en réception, de leur mise en stock jusqu'à leur rattachement à une commande.
- **Préparation de commandes** — transformation d'un export de commandes en documents de terrain imprimables (listing de préparation et picking par famille de produits), avec traitement 100 % local dans le navigateur.
- **Exports** — CSV, Excel et PDF sur les livraisons et réceptions, avec options de mise en page (regroupement, tri) mémorisées par utilisateur.

### RH et équipe
- **Horaires** — saisie des heures jour par jour, horaire type pré-rempli, calcul automatique de la cible mensuelle, des heures supplémentaires et du solde reporté.
- **Congés et absences** — demandes de congé (journée, demi-journée ou période) avec circuit d'approbation par les managers, et impact automatique sur le calcul des heures.
- **Exports RH** — récapitulatifs mensuels par salarié en PDF et Excel.

### Administration
- **4 rôles** (utilisateur, logistique, manager, administrateur) avec permissions granulaires, appliquées côté serveur.
- **Gestion des comptes** — création par l'administrateur, mot de passe temporaire avec changement obligatoire à la première connexion.
- **Journal d'activité** — audit complet et filtrable de toutes les actions de l'application.

## 🛠️ Stack technique

| Domaine | Technologie |
|---|---|
| Framework | Next.js (App Router) + React |
| Langage | TypeScript |
| Interface | Tailwind CSS |
| Authentification | Auth.js (sessions, mots de passe hachés) |
| Base de données | PostgreSQL (Neon) via Drizzle ORM |
| Scan | Douchette HID + caméra (bibliothèque ZXing) |
| Exports | ExcelJS (Excel) · React-PDF (PDF) · CSV natif |
| Hébergement | Vercel |

## 🔒 Code source

Le code source de FeroceWork est **privé** : il s'agit d'un outil interne, propriété de l'entreprise. Ce dépôt public sert uniquement de vitrine et de documentation fonctionnelle — il ne contient aucun code applicatif ni aucune donnée d'exploitation.

## 📚 Documentation

Le fonctionnement complet de l'application, fonctionnalité par fonctionnalité et du point de vue de l'utilisateur, est documenté dans le **[wiki du projet](../../wiki)** :

- [Prise en main](../../wiki/Prise-en-main) — guide de démarrage pour un nouvel utilisateur
- [Rôles et permissions](../../wiki/Roles-et-permissions)
- Les pages détaillées de chaque fonctionnalité (arrivages, réceptions, livraisons, horaires, congés…)
- [FAQ](../../wiki/FAQ)
