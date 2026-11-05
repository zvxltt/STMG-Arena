# STMG Arena

Application web de révision de la **Première STMG** façon jeu vidéo : 16 leçons, 80 missions sur le rap, les jeux vidéo, le Real Madrid et le FC Porto, de l'XP et des rangs (Fer → Radiant).

Toute l'app tient dans un seul fichier, `index.html` (HTML, CSS et JavaScript, images incluses). Pas de framework ni de serveur.

**En ligne :** https://zvxltt.github.io/STMG-Arena/

## Fonctionnalités

- **Cours** : SGN, Management, Droit et Économie (définitions, formules, pièges).
- **Missions** : calculs, QCM, tableaux à compléter, classements, textes à trous, graphiques à analyser et rédactions. 5 missions par leçon, jouées l'une après l'autre ; les 5 sont nécessaires pour valider la leçon.
- **Correction automatique** dans le navigateur : chiffres, choix et tableaux corrigés exactement ; rédactions notées avec une grille de mots-clés du cours. Le corrigé s'affiche une fois la réponse validée.
- **Pré-contrôles** : un vrai sujet type contrôle par leçon (16 au total), avec des documents à lire et analyser (textes, tableaux, graphiques), noté sur 20, avec chrono facultatif. Thèmes : rap, jeux vidéo, Real Madrid, FC Porto, équipe de France.
- **XP et rangs** : l'XP se gagne avec les bonnes réponses (premier essai) et en validant une leçon. Animation en anneau autour de l'emblème du rang à chaque gain, avec promotion (passable). 9 rangs avec emblèmes dessinés en SVG.
- **Arène** : historique des missions jouées, avec note et copie corrigée.
- **Scanner** : photo du cours → lecture du texte sur l'appareil (Tesseract.js, chargé depuis jsDelivr) → la bonne leçon.
- **Sauvegarde automatique** : XP, missions, pré-contrôles, brouillons et dernière page ouverte sont enregistrés à chaque action (localStorage + copie dans IndexedDB). Un code de transfert (onglet Rangs) permet de changer d'appareil.
- **Installable** : `manifest.webmanifest` et icônes pour l'ajouter à l'écran d'accueil (plein écran, comme une appli).
- **Animations** : écran de chargement, transitions entre les pages, apparition des cartes en cascade, révélation de la note.
- **Comme une vraie app** : en-tête et barre d'onglets fixes, seul le contenu défile ; zoom désactivé ; champs adaptés au tactile.

## Modifier l'app

Ouvre `index.html` sur GitHub, clique sur le crayon, modifie, puis « Commit changes ». GitHub Pages met le site à jour en une ou deux minutes.
