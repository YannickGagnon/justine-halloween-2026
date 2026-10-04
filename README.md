# Justine — Halloween 2026

Page statique pour présenter le costume de Justine. On l’ouvre depuis un code QR, sur un téléphone. Il n’y a pas d’étape de compilation : les fichiers `index.html` et `styles.css` sont servis tels quels.

Le nom du personnage n’est pas encore choisi. Partout dans la page, il est écrit **« le personnage »**. Remplacez cette expression par le vrai nom quand vous l’avez.

## Adresse à mettre dans le QR code

https://yannickgagnon.github.io/justine-halloween-2026/

Encodez cette adresse telle quelle. Elle fonctionne une fois GitHub Pages activé (voir plus bas).

## Modifier les textes

Tout le texte visible est dans `index.html`. Les passages à remplacer sont marqués par un commentaire `<!-- TEXTE -->`.

À changer :

- la petite ligne au-dessus du titre, le titre, et le sous-titre ;
- le paragraphe d’introduction ;
- les trois blocs (« le personnage », le costume, le mot de Justine) ;
- le titre et la légende sous chaque vidéo.

Les guillemets français « » font partie du texte. Vous pouvez les garder autour du nom.

`styles.css` règle seulement la mise en page et les couleurs. Inutile d’y toucher pour changer les mots.

## Changer les vidéos

Les vidéos ne sont pas dans ce dépôt, et il ne faut pas y ajouter de fichiers vidéo. Elles restent hébergées ailleurs (YouTube). La page n’affiche qu’un lecteur.

Dans `index.html`, chaque lecteur a une adresse de cette forme :

```text
https://www.youtube-nocookie.com/embed/ID_VIDEO_01
```

Les identifiants provisoires sont `ID_VIDEO_01`, `ID_VIDEO_02` et `ID_VIDEO_03`. Remplacez chacun par l’identifiant réel, aux deux endroits où il apparaît pour cette vidéo : dans l’adresse du lecteur, et dans la petite étiquette sous la légende.

Pour trouver l’identifiant :

- adresse longue `https://www.youtube.com/watch?v=abcdefghijk` → `abcdefghijk` ;
- lien court `https://youtu.be/abcdefghijk` → la même suite, après la barre oblique.

Il y a trois lecteurs. Pour n’en garder que deux, supprimez un bloc `<figure>…</figure>` entier.

## Mettre le site en ligne

GitHub Pages n’a pas pu être activé depuis l’environnement qui a préparé cette page (le jeton n’a pas le droit d’administration sur le dépôt). Le propriétaire du dépôt fait ce réglage une fois :

1. Ouvrir [Settings → Pages](https://github.com/YannickGagnon/justine-halloween-2026/settings/pages).
2. Sous **Build and deployment**, menu **Source** : **Deploy from a branch**.
3. Branche : **main**. Dossier : **/ (root)**.
4. Cliquer **Save**.

Après une ou deux minutes, la page répond à l’adresse du QR code. Chaque mise à jour poussée sur `main` republie le site.

Le fichier `.nojekyll` demande à GitHub de publier les fichiers directement, sans les faire passer par Jekyll.
