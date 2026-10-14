# pixel-pantry

> Le garde-manger à pixels de mon blog : captures, illustrations et memes conservés au frais, servis
> tièdes via CDN.

Rien à installer, rien à construire. On dépose des images, GitHub les stocke, jsDelivr les livre.

## Ce qu'il y a dans les placards

```
images/
├── covers/       visuels de couverture d'articles
├── posts/        un sous-dossier par article : posts/mon-super-article/
├── screenshots/  captures d'écran, interfaces, terminal
└── misc/         avatars, logos, icônes, le reste du bocal
```

## Se servir

Une image déposée dans `images/covers/hello.png` est aussitôt disponible.

**Par le CDN jsDelivr**, recommandé : rapide, mis en cache, pensé pour ça.

```
https://cdn.jsdelivr.net/gh/Simon256px/pixel-pantry@main/images/covers/hello.png
```

**Directement depuis GitHub**, pratique pour tester mais pas fait pour du trafic.

```
https://raw.githubusercontent.com/Simon256px/pixel-pantry/main/images/covers/hello.png
```

Dans un article en Markdown :

```markdown
![Une image bien fraîche](https://cdn.jsdelivr.net/gh/Simon256px/pixel-pantry@main/images/covers/hello.png)
```

jsDelivr garde les fichiers en cache longtemps. Si tu remplaces une image sous le même nom,
l'ancienne peut traîner quelques heures. Le plus simple : ne jamais écraser, créer un nouveau nom
(`hello-v2.png`), ou épingler un tag ou un commit à la place de `@main`.

## Ranger des images

```bash
git add images/ && git commit -m "add: visuels article X" && git push
```

Ou par glisser-déposer depuis l'interface web de GitHub, si les mains sont pleines.

## Règles de la cuisine

- **Noms en kebab-case**, sans accents ni espaces : `capture-terminal-dnf.png`, pas
  `Capture Écran 2.PNG`.
- **On compresse avant de ranger.** Une capture de blog dépasse rarement 300 Ko ;
  [Squoosh](https://squoosh.app) fait le travail en dix secondes.
- **Le bon format** : `.webp` par défaut, `.png` si la transparence ou un texte net est indispensable,
  `.jpg` pour les photos, `.svg` pour les logos et schémas.
- **Pas de vidéos ni de gros fichiers.** GitHub râle au-delà de 50 Mo et refuse à 100 Mo.
- **Rien de sensible dans une capture** : jetons, e-mails, adresses internes. Une fois poussé, c'est
  dans l'historique git pour toujours.

## Contribuer

Une image cassée, un lien mort, une coquille ? Voir [CONTRIBUTING.md](CONTRIBUTING.md).

## Soutenir

Si le blog te plaît, tu peux me soutenir sur [ko-fi.com/simon256px](https://ko-fi.com/simon256px).

## Licence

Distribué sous [licence MIT](LICENSE).
