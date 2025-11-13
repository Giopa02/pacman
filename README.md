# 🟡 Pac-Man – Jeu en JavaScript, HTML & CSS  

👾 Une version moderne du célèbre **Pac-Man**, développée en **JavaScript**, **HTML** et **CSS**.  
Ce projet recrée le jeu culte directement dans le navigateur, avec des fantômes, des super pac-gommes et un système de score.  

---

## 📝 Description du jeu  

Le joueur incarne Pac-Man, un personnage jaune évoluant dans un labyrinthe rempli de pac-gommes.  
Le but est simple : **manger toutes les pac-gommes sans se faire attraper par les fantômes**.  

Le labyrinthe est généré à partir d’un tableau numérique (`layout`) représentant chaque case :  
- `0` → Pac-gomme (à manger)  
- `1` → Mur (obstacle)  
- `2` → Zone des fantômes (ils y apparaissent)  
- `3` → Super pac-gomme (rend Pac-Man invincible temporairement)  
- `4` → Espace vide  

Pac-Man peut se déplacer dans toutes les directions et accumule des points en mangeant les pac-gommes.  
Lorsqu’il attrape une **super pac-gomme**, les fantômes deviennent **effrayés** pendant un court instant, et il peut alors les “manger” pour marquer plus de points.  

---

## 🧠 Logique du jeu  

### Création du plateau  
Le plateau de jeu est construit dynamiquement à partir du tableau `layout`.  
Chaque valeur numérique correspond à un type de case : mur, pac-gomme, zone vide, etc.  
Chaque case est ajoutée dans la grille HTML sous forme de `<div>`, ce qui permet d’appliquer des classes CSS pour l’affichage visuel.  

### Déplacement de Pac-Man  
Pac-Man démarre à une position précise sur la grille (`pacmanCurrentIndex = 490`).  
Ses déplacements sont gérés par les touches fléchées.  
À chaque mouvement, le script vérifie :  
- si Pac-Man ne rencontre pas un mur,  
- s’il mange une pac-gomme ou une super pac-gomme,  
- et s’il entre en collision avec un fantôme.  

### Gestion des fantômes  
Les fantômes (Blinky, Pinky, Inky, Clyde) sont créés à l’aide d’une classe `Ghost`.  
Chacun possède :  
- un nom,  
- une position de départ,  
- une vitesse de déplacement,  
- et un état (`isScared`) lorsqu’ils deviennent vulnérables.  

Chaque fantôme se déplace de façon **semi-aléatoire** en choisissant une direction parmi quatre (haut, bas, gauche, droite).  
Si un fantôme est **effrayé** et qu’il entre en contact avec Pac-Man, il retourne à sa position de départ et Pac-Man gagne des points supplémentaires.  

### Gestion du score  
Le score augmente à chaque pac-gomme ou super pac-gomme mangée.  
Lorsqu’un fantôme effrayé est attrapé, Pac-Man gagne **+100 points**.  
Le score total est affiché en direct à l’écran.  

---

## 🏆 Conditions de victoire et de défaite  

- **Victoire 🎉** : Pac-Man gagne lorsque toutes les pac-gommes du labyrinthe ont été mangées (score total = 274).  
- **Défaite 💀** : Si un fantôme non effrayé attrape Pac-Man, la partie s’arrête et un message “Game Over” s’affiche.  

---

## 🧰 Technologies utilisées  

- **HTML5** → structure de la page et grille du jeu  
- **CSS3** → style visuel du labyrinthe, couleurs et animations  
- **JavaScript (ES6)** → logique principale du jeu, déplacements, collisions, gestion des fantômes et du score  

---

## 🌟 Améliorations possibles  

- 🎵 Ajouter des effets sonores (déplacement, victoire, défaite)  
- 🧭 Rendre les fantômes plus intelligents avec une IA de poursuite  
- 💾 Sauvegarder le meilleur score dans le navigateur  
- 📱 Adapter le jeu aux écrans mobiles  
- 🕹️ Créer un menu d’accueil et un écran de fin plus immersifs  

---

## 👩🏽‍💻 Auteur  

Développé par **Giordana** – Étudiante en **BTS SIO** option **développement web** 💻  

✨ Ce projet a été réalisé pour s’entraîner à la **logique algorithmique**, aux **boucles**, à la **manipulation du DOM** et à la **programmation orientée objet** en JavaScript.  

---

## 💬 Remerciements  

Merci d’avoir testé cette version de **Pac-Man** 🙏  
N’hésite pas à proposer des suggestions ou des améliorations pour enrichir le projet 🚀  
