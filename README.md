# Portfolio Guillaume Morvan

Site statique du portfolio de Guillaume Morvan, publié avec GitHub Pages. Le projet conserve deux interfaces distinctes, une pour desktop et une pour mobile.

## Structure

- `index.html` choisit la version à afficher selon la largeur de la fenêtre et transmet les paramètres de l’URL.
- `desktop.html` contient l’interface desktop, ses styles et son JavaScript.
- `mobile.html` contient l’interface mobile, ses styles et son JavaScript.
- `pages/` contient les planches utilisées par la version desktop.
- `pages-mobile/` contient les planches, légendes et textes des projets mobiles.
- `Vignettes/` contient les images de présentation des projets.
- `apropos/` contient les planches de la section « À propos » desktop.
- `parcours-mobile/` contient les textes et images de la section « Parcours » mobile.
- `contact-mobile/` contient les éléments de la section « Contact » mobile.
- `cover.jpg` et `cover-mobile.jpg` sont les couvertures des deux versions.
- `portfolio-guillaume-morvan.pdf` est la version PDF du portfolio.
- `back-up-index.html` est une ancienne sauvegarde et n’est pas utilisée par l’accueil actuel.

Le site n’utilise ni framework ni étape de compilation : le HTML, le CSS et le JavaScript sont directement servis par le navigateur.

## Prévisualisation locale

Depuis la racine du dépôt, lancer un serveur HTTP :

```powershell
python -m http.server 8000
```

Puis ouvrir :

```text
http://localhost:8000/
```

La page d’accueil redirige vers `desktop.html` au-dessus de 700 px et vers `mobile.html` à 700 px ou moins. Les deux versions peuvent aussi être testées directement :

```text
http://localhost:8000/desktop.html
http://localhost:8000/mobile.html
```

Arrêter le serveur avec `Ctrl+C`.

Il est important d’utiliser un serveur HTTP plutôt que d’ouvrir les fichiers avec le protocole `file://`, car la version mobile charge plusieurs fichiers texte avec `fetch()`.
