# 🥫 pixel-pantry

> Le garde-manger à pixels de mon blog. Captures, illustrations et memes conservés au frais, servis tièdes via CDN.

Rien à installer, rien à builder. On dépose des images, GitHub les stocke, jsDelivr les livre.

## 🧊 Ce qu'il y a dans les placards

```
images/
├── covers/       # visuels de couverture d'articles
├── posts/        # un sous-dossier par article : posts/mon-super-article/
├── screenshots/  # captures d'écran, UI, terminal
└── misc/         # avatars, logos, icônes, le reste du bocal
```

## 🍽️ Comment se servir

Une image déposée dans `images/covers/hello.png` est immédiatement disponible :

**Via le CDN jsDelivr** (recommandé : rapide, caché, pensé pour ça)

```
https://cdn.jsdelivr.net/gh/Simon256px/pixel-pantry@main/images/covers/hello.png
```

**Via GitHub en direct** (pratique pour tester, pas fait pour du trafic)

```
https://raw.githubusercontent.com/Simon256px/pixel-pantry/main/images/covers/hello.png
```

En Markdown, dans un article :

```markdown
![Une image bien fraîche](https://cdn.jsdelivr.net/gh/Simon256px/pixel-pantry@main/images/covers/hello.png)
```

> 💡 jsDelivr met les fichiers en cache agressivement. Si tu remplaces une image par une autre **sous le même nom**, l'ancienne peut traîner quelques heures. Le plus simple : ne jamais écraser, toujours créer un nouveau nom (`hello-v2.png`), ou épingler un tag/commit à la place de `@main`.

## 🧑‍🍳 Règles de la cuisine

- **Noms en kebab-case**, sans accents ni espaces : `capture-terminal-dnf.png`, pas `Capture Écran 2.PNG`.
- **On compresse avant de ranger.** Une capture d'écran de blog dépasse rarement 300 Ko. [Squoosh](https://squoosh.app) fait le travail en dix secondes.
- **Le bon format** : `.webp` par défaut, `.png` si transparence ou texte net indispensable, `.jpg` pour les photos, `.svg` pour les logos et schémas.
- **Pas de vidéos, pas de gros fichiers.** GitHub râle au-delà de 50 Mo et refuse à 100 Mo. Ce placard est fait pour des images, pas pour un déménagement.
- **Rien de sensible dans une capture** : tokens, e-mails, URLs internes. Une fois poussé, c'est dans l'historique git pour toujours.

## 📦 Ajouter des images

```bash
git add images/ && git commit -m "add: visuels article X" && git push
```

Ou par glisser-déposer depuis l'interface web GitHub, si les mains sont pleines.

## 📄 Licence

Les images de ce dépôt sont ma production personnelle — tous droits réservés, sauf mention contraire dans le dossier concerné. Le dépôt est public pour être servi par un CDN, pas pour être vidé.
