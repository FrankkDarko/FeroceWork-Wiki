# Étapes à faire de ton côté

Tout le contenu est prêt dans ce dossier (`FeroceWork-Wiki`), déjà cloné et relié au dépôt public `FrankkDarko/FeroceWork-Wiki`. Voici les étapes manuelles, dans l'ordre.

---

## 0. Relire le contenu

Avant toute publication, relis le `README.md` et les pages du dossier `wiki/` pour vérifier qu'aucune information que tu juges sensible n'y figure (rien de nominatif n'a été inclus, mais c'est toi qui as le dernier mot).

---

## 1. Pousser le README vers le dépôt public

Le dossier `wiki/` peut être commité aussi : il sert de sauvegarde versionnée des pages (le wiki GitHub lui-même vit dans un dépôt séparé, voir étape 3). En revanche, ce fichier `ETAPES-A-FAIRE.md` est un pense-bête local — évite de le publier.

```bash
cd C:/Users/louis/Documents/GitHub/FeroceWork-Wiki
```

```bash
git add README.md wiki/
```

```bash
git commit -m "Page de présentation + pages du wiki"
```

```bash
git push origin main
```

Vérifie ensuite sur https://github.com/FrankkDarko/FeroceWork-Wiki que le README s'affiche bien en page d'accueil.

> Une fois tout terminé, tu peux supprimer `ETAPES-A-FAIRE.md` (il n'est pas commité si tu as suivi les commandes ci-dessus).

---

## 2. Activer le wiki et restreindre son édition

Sur GitHub, dans le dépôt **FeroceWork-Wiki** :

1. Va dans **Settings** → onglet **General** → section **Features**.
2. Coche **Wikis** pour activer le wiki.
3. Juste en dessous, coche **Restrict editing to collaborators only** — ainsi, seuls les collaborateurs du dépôt peuvent modifier les pages ; le public peut seulement les lire.

---

## 3. Importer les pages du wiki d'un coup (via git)

Le wiki GitHub est en réalité un **dépôt git séparé** (`FeroceWork-Wiki.wiki.git`). C'est la méthode la plus simple pour importer toutes les pages d'un coup. Attention à une subtilité : ce dépôt n'existe qu'après la création de la **première page via l'interface web**.

1. Sur https://github.com/FrankkDarko/FeroceWork-Wiki, onglet **Wiki** → **Create the first page** → laisse le titre « Home », mets n'importe quel contenu provisoire → **Save page**. (Cette page sera écrasée par notre `Home.md` juste après.)

2. Clone le dépôt du wiki (dans un dossier à part, pas dans FeroceWork-Wiki) :

```bash
cd C:/Users/louis/Documents/GitHub
```

```bash
git clone https://github.com/FrankkDarko/FeroceWork-Wiki.wiki.git
```

3. Copie toutes les pages préparées dans ce clone (écrase le Home provisoire) :

```bash
cp C:/Users/louis/Documents/GitHub/FeroceWork-Wiki/wiki/*.md C:/Users/louis/Documents/GitHub/FeroceWork-Wiki.wiki/
```

4. Commit et push :

```bash
cd C:/Users/louis/Documents/GitHub/FeroceWork-Wiki.wiki
```

```bash
git add -A
```

```bash
git commit -m "Import des pages du wiki"
```

```bash
git push origin master
```

> ⚠️ Le dépôt wiki de GitHub utilise historiquement la branche **`master`** (pas `main`). Si le push est refusé, vérifie le nom de la branche avec `git branch` et pousse vers celle-ci.

5. Recharge l'onglet **Wiki** sur GitHub : toutes les pages doivent apparaître, avec `Home` en sommaire. Clique sur quelques liens du sommaire pour vérifier qu'ils mènent aux bonnes pages (les liens utilisent les noms de fichiers avec tirets, ex. `Prise-en-main`).

---

## 4. Vérifications finales

- [ ] Le README s'affiche correctement sur la page du dépôt public.
- [ ] Les liens de la section « Documentation » du README mènent bien au wiki (`../../wiki` pointe vers l'onglet Wiki du dépôt).
- [ ] Toutes les pages du wiki sont présentes et le sommaire (Home) fonctionne.
- [ ] Dans **Settings → Features**, « Restrict editing to collaborators only » est bien coché.
- [ ] Le dépôt public ne contient ni code source, ni fichier `.env`, ni donnée réelle.

---

## Pour mettre à jour plus tard

- **README** : modifie `README.md` dans `FeroceWork-Wiki`, puis `git add` / `commit` / `push` classique.
- **Wiki** : modifie les pages dans `FeroceWork-Wiki/wiki/` (la sauvegarde versionnée), recopie-les dans `FeroceWork-Wiki.wiki/` et pousse — ou édite directement en ligne via l'onglet Wiki (réservé aux collaborateurs).
