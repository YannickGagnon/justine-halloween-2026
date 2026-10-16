# Justine — Halloween 2026

Page statique pour présenter le costume de Justine : Jennie, son avatar. On l’ouvre depuis un code QR, sur un téléphone. Il n’y a pas d’étape de compilation : `index.html` est servi tel quel.

La page est un album de polaroïds. On touche une photo, la vidéo s’ouvre en grand.

## Adresse à mettre dans le QR code

https://yannickgagnon.github.io/justine-halloween-2026/

Encodez cette adresse telle quelle.

## Modifier les textes

Tout est dans `index.html`, styles et script compris.

- Le titre et la phrase d’accueil sont dans le bloc `<header>`.
- La légende de chaque photo est dans la liste `clips`, en bas du fichier (champ `label`). Le champ `sticker` est l’autocollant posé sur le coin de la photo.

## Changer les vidéos

Les vidéos sont dans `vids/`, et une image fixe par vidéo dans `vids/posters/`. Chaque entrée de la liste `clips` donne la vidéo (`src`) et son image (`poster`).

Pour ajouter une vidéo : déposez le fichier `.mp4` dans `vids/`, tirez-en une image, puis ajoutez une ligne à `clips`. Pour l’image :

```sh
ffmpeg -ss 2 -i vids/ma-video.mp4 -frames:v 1 -vf scale=540:-2 -q:v 4 vids/posters/ma-video.jpg
```

Gardez les vidéos courtes et légères : la page est souvent ouverte sur un réseau mobile.

## Mise en ligne

GitHub Pages publie la branche `main`, dossier racine. Chaque mise à jour poussée sur `main` republie le site après une ou deux minutes.

Le fichier `.nojekyll` demande à GitHub de publier les fichiers directement, sans les faire passer par Jekyll.
