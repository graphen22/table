# Table périodique des femmes de science — mise en ligne

Ce dossier est le site complet. Il ne dépend d'aucun serveur : il suffit de
déposer son contenu à la racine d'un dépôt GitHub et d'activer GitHub Pages.

## Contenu

    index.html           la page entière (structure, styles, textes des fiches)
    img/vignettes/       les 118 vignettes de 200 px, pour les cases de la table
    img/grandes/         les 118 images de 900 px, pour les fiches
    audio/               les 118 enregistrements
    data/contenu.json    les textes extraits des fichiers Word (référence)
    .nojekyll            empêche GitHub de retraiter le dossier

Le numéro du fichier est la clé : `img/vignettes/042.jpg`,
`img/grandes/042.jpg` et `audio/042.mp3` sont tous la case 42.

Ce dossier est fabriqué par `outils/tout_reconstruire.py` : ne le modifiez pas
à la main, vos changements seraient écrasés à la reconstruction suivante.

## Mise en ligne, première fois

1. Sur github.com, créez un dépôt public, par exemple `table-femmes-science`.
2. Bouton **Add file › Upload files**, glissez le contenu de ce dossier
   (les fichiers et les deux sous-dossiers), puis **Commit changes**.
   Au-delà de 100 fichiers d'un coup, faites-le en deux ou trois fois.
3. Onglet **Settings › Pages**. Sous *Source*, choisissez **Deploy from a branch**,
   branche `main`, dossier `/ (root)`. **Save**.
4. Au bout d'une à deux minutes, le site est à
   `https://VOTRECOMPTE.github.io/table-femmes-science/`.

## Mise à jour

Remplacez les fichiers concernés dans le dépôt (même procédure d'upload, GitHub
écrase les fichiers de même nom). Le site se régénère tout seul.

Pour tout changement de la page elle-même — nouveaux textes, nouvelle mise en
page — c'est `index.html` qu'il faut remplacer : il est reconstruit à partir du
tableau de correspondance et des fichiers Word.

## Adresse personnalisée

GitHub Pages accepte un nom de domaine à vous : *Settings › Pages › Custom
domain*. Il faut posséder le domaine et ajouter un enregistrement DNS chez le
bureau d'enregistrement.

## Limites de GitHub Pages

- 1 Go pour le site publié — largement suffisant : 118 audios de 3 minutes en
  qualité parole pèsent environ 250 Mo.
- 100 Mo par fichier, jamais atteint ici.
- 100 Go de trafic par mois.
- Le dépôt doit être public pour que Pages soit gratuit ; les fichiers sont donc
  visibles de tous, ce qui vaut la peine d'être vérifié pour les noms d'élèves.
