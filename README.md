# STMG Arena

Application web de révision de la **Première STMG** façon jeu vidéo : 16 leçons, 80 missions sur le rap, les jeux vidéo, le Real Madrid et le FC Porto, de l'XP et des rangs (Fer → Radiant).

Tout est en **HTML, CSS et JavaScript**, sans framework ni serveur : il suffit d'ouvrir `index.html`.

## Fonctionnalités

- **Cours** : SGN, Management, Droit et Économie (définitions, formules, pièges).
- **Missions** : calculs, QCM, tableaux à compléter, classements, textes à trous, graphiques à analyser et rédactions. 3 missions principales par leçon + 2 bonus.
- **Correction automatique** dans le navigateur : chiffres, choix et tableaux corrigés exactement ; rédactions notées avec une grille de mots-clés du cours. Le corrigé s'affiche une fois la réponse validée.
- **XP et rangs** : l'XP se gagne uniquement avec les bonnes réponses (premier essai) et en validant une leçon. Animation à chaque gain (passable).
- **Arène** : historique des missions jouées, avec note et copie corrigée.
- **Scanner** : prends en photo ton cours, le texte est lu sur l'appareil (Tesseract.js, fourni dans `vendor/`) et l'app t'envoie vers la bonne leçon.
- **Mobile** : barre d'onglets en bas, tableaux défilants, champs adaptés au tactile.

La progression est enregistrée dans le navigateur (localStorage).

## Mettre en ligne avec GitHub Pages

1. Crée un dépôt sur GitHub et envoie tout le contenu de ce dossier (avec `index.html` à la racine).
2. Dans le dépôt : **Settings → Pages → Build and deployment → Source : Deploy from a branch**, branche `main`, dossier `/ (root)`.
3. Après une minute, l'app est en ligne à l'adresse `https://<ton-pseudo>.github.io/<nom-du-depot>/`.

Pour tester sur ton ordinateur, ouvre `index.html`. Le scanner photo a besoin d'un petit serveur local (par exemple `python3 -m http.server` dans ce dossier, puis http://localhost:8000).

## Structure

```
index.html          page principale
css/style.css       styles (thème sombre, version téléphone)
js/data.js          contenu : leçons et missions
js/app.js           logique : navigation, correction, XP, rangs, scanner
img/                visuels (générés avec Higgsfield)
vendor/tesseract/   moteur de lecture de texte (Tesseract.js 5.1.1, licence Apache 2.0)
ocr/fra-data.wasm   données de langue française pour Tesseract (fichier .traineddata compressé)
```

## Ajouter une mission

Dans `js/data.js`, chaque leçon a une liste `M.<id>` de missions. Une mission contient un thème (`t: 'rap' | 'jeu' | 'foot'`), un titre, un contexte, l'XP, un corrigé et des parties : `N` (calcul), `Q` (QCM), `C` (classement), `T` (tableau), `H` (texte à trous), `R` (rédaction) et `G` (graphique). Ajoute `b:1` pour une mission bonus.

Les chiffres des exercices sont inventés pour l'entraînement.
