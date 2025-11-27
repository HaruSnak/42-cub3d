<img src="readme/cub3d.png" alt="cub3d" width="900"/>

<div align="center">

# Cub3D
### A 3D Raycasting Game Project at 42 School Using MiniLibX

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]
[![License][license-shield]][license-url]

</div>

---

## 🇬🇧 English

<details>
<summary><b>📖 Click to expand/collapse English version</b></summary>

### 📖 About

**Cub3D** is a compulsory project for 42 School students. It consists of creating a 3D graphical representation of a maze from a first-person perspective using ray-casting principles, similar to classic games like Wolfenstein 3D. The player navigates through the maze using keyboard and mouse controls.

This project teaches:
- 3D graphics programming with raycasting and MiniLibX
- Map parsing and validation from .cub files
- Raycasting algorithm implementation (DDA)
- Texture mapping for walls based on orientation
- Floor and ceiling color rendering
- Player movement, rotation, and collision detection
- Event handling and smooth window management

### 🧠 Skills Learned

By completing the Cub3D project, students develop essential skills in C programming and 3D game development:

- **Raycasting implementation**: Understanding and implementing the DDA algorithm for 3D projection from 2D maps.
- **MiniLibX usage**: Initializing windows, handling events, drawing pixels, and loading textures with MiniLibX.
- **Map parsing**: Reading and validating .cub files with textures, colors, and map layout.
- **3D rendering**: Projecting 2D maps into 3D views with correct perspective and distances.
- **Texture application**: Applying different wall textures based on North, South, East, West orientations.
- **Color management**: Setting floor and ceiling colors via RGB values.
- **Player controls**: Implementing WASD movement, arrow key rotation, mouse rotation, and ESC quit.
- **Collision detection**: Preventing movement through walls for realistic navigation.
- **Bonus features**: Adding minimap, mouse rotation, and other enhancements.
- **Error handling**: Robust validation of map files with clear error messages.
- **Code organization**: Modular functions adhering to 42 norms.

## Approach
This project was challenging to manage as a team. Similar to other projects like Minishell, I started development alone, which complicated task distribution, leading to implementing most of the project autonomously.

**Parsing: The Technical Challenge**  
I structured development around rigorous parsing as an essential prerequisite for a robust test suite. Specific complexities included:
- Handling variable map sizes and positions in .cub files
- Validating empty spaces (only allowed when surrounded by walls)
- Ensuring closed maps and single player position

**Development Pipeline**  
Once parsing was finalized:
- Graphical Assets: Selected external resources, modified in Photoshop for optimal rendering.
- Raycasting Integration: Teammate (tmoel1) joined to "finalize" the algorithm, implement movements (WASD) + collisions.

![game](readme/game.gif)

**Additional Features (BONUS):**
- Added an interactive minimap
- Integrated mouse control for rotation

**Quality Validation**  
To ensure robustness:
- Developed an exhaustive test suite with varied maps
- Systematically verified parser edge cases

### **Features**

**Raycasting with DDA algorithm:** *Projects 3D view from 2D map using digital differential analysis.*  

**Directional wall textures:** *Different textures for North, South, East, West walls.*  

**Floor and ceiling colors:** *RGB color settings for ground and sky.*  

**Player controls:** *WASD movement, arrow rotation, mouse rotation, ESC quit.*  

**Collision detection:** *Walls block movement.*  

**Minimap (bonus):** *2D overview with player position.*  

### **Features to be added:**

**Doors and animated sprites:** *Interactive elements for enhanced gameplay.*  

**Improved textures and lighting:** *Better visual effects.*  

### 📋 Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Compilation](#compilation)
- [Function Reference](#function-reference)
- [Credits](#credits)

<a name="features"></a>

### ✨ Features

- **Complete 3D raycasting engine** with textured walls and colored floors/ceilings
- **Map validation** ensuring closed maps, valid paths, and required elements
- **Player movement and rotation** with keyboard and mouse controls
- **Collision detection** preventing invalid movements
- **Bonus minimap** showing 2D overview
- **Mouse rotation** for smooth viewpoint control
- **Strict C compliance** with 42 School norming standards

<a name="installation"></a>

### 🚀 Installation

```bash
# Clone the repository
git clone https://github.com/HaruSnak/42-cub3d
cd 42-cub3d
```

<a name="usage"></a>

### 💻 Usage

Compile and run the game with a map file:

```bash
make
./cub3D maps/map1.cub
```

Controls:
- **WASD**: Move forward/backward/left/right
- **Arrow keys**: Rotate left/right
- **Mouse**: Rotate viewpoint
- **ESC**: Quit the game

<a name="project-structure"></a>

### 📂 Project Structure

```
42-cub3d/
├── Makefile                    # Build script
├── cub3d.h                     # Main header file
├── cub3d.c                     # Main game entry point
├── LICENSE                     # License file
├── README.md                   # This file
├── README-Template.md          # Template for README
├── assets/                     # Game textures
│   ├── textures/
│   └── ui/
├── includes/
│   ├── cub3d.h
│   └── libft/                  # Custom library
├── maps/                       # Map files (.cub)
├── minilibx-linux/             # MiniLibX library
├── readme/                     # README assets
└── srcs/                       # Source files
    ├── bonus/
    ├── errors/
    ├── game/
    ├── parsing/
    ├── player/
    ├── raycasting/
    ├── texturing/
    └── ui/
```

<a name="compilation"></a>

### 🔧 Compilation

Compile the project using the Makefile:

```bash
make          # Compile the game
make bonus    # Compile with bonus features
make clean    # Remove object files
make fclean   # Remove executable and object files
make re       # Recompile everything
```

<a name="function-reference"></a>

### 📚 Function Reference

#### Main Functions
- [`main`](srcs/cub3d.c) - Game initialization and loop
- [`ft_parse_base`](srcs/parsing/parsing.c) - Map parsing and validation
- [`cast_rays`](srcs/raycasting/raycasting_draw.c) - Raycasting rendering
- [`key_press`](srcs/player/keys.c) - Input handling

#### Key Features
- **DDA Algorithm**: Core raycasting for wall detection
- **Texture Mapping**: Applies XPM textures to walls
- **Minimap Rendering**: Draws 2D overview in bonus
- **Mouse Rotation**: Adjusts player angle via mouse movement

### 👨‍🎓 Note
<p align="left">
    <img src="readme/115.png" alt="115/100" width="216" height="164">
</p>

<a name="credits"></a>

### 📖 Credits

- **42 School Norm**: [Official C Coding Standard](https://cdn.intra.42.fr/pdf/pdf/960/norme.en.pdf)
- **Raycasting Tutorial**: [Lode Vandevenne](https://lodev.org/cgtutor/raycasting.html)
- **MiniLibX Documentation**: [Harm-Smits Guide](https://harm-smits.github.io/42docs/libs/minilibx/getting_started.html)

### 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

</details>

---

## 🇫🇷 Français

<details>
<summary><b>📖 Cliquez pour développer/réduire la version française</b></summary>

### 📖 À propos

**Cub3D** est un projet obligatoire pour les étudiants de l'école 42. Il s'agit de créer une représentation graphique 3D d'un labyrinthe en vue subjective en utilisant les principes du ray-casting, similaire aux jeux classiques comme Wolfenstein 3D. Le joueur navigue dans le labyrinthe en utilisant les contrôles clavier et souris.

Ce projet enseigne :
- La programmation graphique 3D avec raycasting et MiniLibX
- Le parsing et la validation de cartes depuis des fichiers .cub
- L'implémentation de l'algorithme de raycasting (DDA)
- Le mappage de textures pour les murs selon l'orientation
- Le rendu des couleurs du sol et du plafond
- Le mouvement, la rotation du joueur et la détection de collisions
- La gestion des événements et la gestion fluide des fenêtres

### 🧠 Compétences acquises

En complétant le projet Cub3D, les étudiants développent des compétences essentielles en programmation C et développement de jeux 3D :

- **Implémentation du raycasting** : Comprendre et implémenter l'algorithme DDA pour la projection 3D depuis des cartes 2D.
- **Utilisation de MiniLibX** : Initialiser des fenêtres, gérer les événements, dessiner des pixels et charger des textures avec MiniLibX.
- **Parsing de cartes** : Lire et valider des fichiers .cub avec textures, couleurs et disposition de carte.
- **Rendu 3D** : Projeter des cartes 2D en vues 3D avec perspective et distances correctes.
- **Application de textures** : Appliquer différentes textures de murs selon les orientations Nord, Sud, Est, Ouest.
- **Gestion des couleurs** : Définir les couleurs du sol et du plafond via des valeurs RGB.
- **Contrôles du joueur** : Implémenter le mouvement WASD, la rotation avec les flèches, la rotation souris et la sortie ESC.
- **Détection de collisions** : Empêcher le mouvement à travers les murs pour une navigation réaliste.
- **Fonctionnalités bonus** : Ajouter une minimap, rotation souris et autres améliorations.
- **Gestion d'erreurs** : Validation robuste des fichiers de carte avec des messages d'erreur clairs.
- **Organisation du code** : Fonctions modulaires respectant les normes 42.

## Approche
Ce projet s'est avéré particulièrement difficile à gérer en équipe. Comme pour d'autres projets comme Minishell, j'ai commencé le développement seul, ce qui a compliqué la distribution des tâches, me conduisant à implémenter la majorité du projet de manière autonome.

**Parsing : Le défi technique**  
J'ai structuré le développement autour d'un parsing rigoureux, essentiel pour établir une suite de tests robuste. Les complexités spécifiques incluaient :
- Gestion des tailles de cartes variables et positions dans les fichiers .cub
- Validation des espaces vides (seulement autorisés lorsqu'entourés de murs)
- Assurance de cartes fermées et position de joueur unique

**Pipeline de développement**  
Une fois le parsing finalisé :
- Ressources graphiques : Sélection de ressources externes, modifiées dans Photoshop pour un rendu optimal.
- Intégration du raycasting : Le coéquipier (tmoel1) a rejoint pour finaliser l'algorithme, implémenter les mouvements (WASD) + collisions.

![game](readme/game.gif)

**Fonctionnalités supplémentaires (BONUS) :**
- Ajout d'une minimap interactive
- Intégration du contrôle souris pour la rotation

**Validation de qualité**  
Pour assurer la robustesse :
- Développement d'une suite de tests exhaustive avec diverses cartes
- Vérification systématique des cas limites du parser

### **Fonctionnalités**

**Raycasting avec algorithme DDA :** *Projette la vue 3D depuis la carte 2D en utilisant l'analyse différentielle numérique.*  

**Textures de murs directionnelles :** *Textures différentes pour les murs Nord, Sud, Est, Ouest.*  

**Couleurs du sol et plafond :** *Paramètres de couleur RGB pour le sol et le ciel.*  

**Contrôles du joueur :** *Mouvement WASD, rotation flèches, rotation souris, sortie ESC.*  

**Détection de collisions :** *Les murs bloquent le mouvement.*  

**Minimap (bonus) :** *Aperçu 2D avec position du joueur.*  

### **Fonctionnalités à ajouter :**

**Portes et sprites animés :** *Éléments interactifs pour un gameplay amélioré.*  

**Textures et éclairage améliorés :** *Meilleurs effets visuels.*  

### 📋 Table des matières

- [Caractéristiques](#caractéristiques)
- [Installation](#installation-1)
- [Utilisation](#utilisation)
- [Structure du projet](#structure-du-projet)
- [Compilation](#compilation-1)
- [Référence des fonctions](#référence-des-fonctions)
- [Crédits](#crédits-1)

<a name="caractéristiques"></a>

### ✨ Caractéristiques

- **Moteur de raycasting 3D complet** avec murs texturés et sols/plafonds colorés
- **Validation de carte** assurant des cartes fermées, chemins valides et éléments requis
- **Mouvement et rotation du joueur** avec contrôles clavier et souris
- **Détection de collisions** empêchant les mouvements invalides
- **Minimap bonus** montrant l'aperçu 2D
- **Rotation souris** pour un contrôle fluide du point de vue
- **Conformité stricte C** avec les normes de l'école 42

<a name="installation-1"></a>

### 🚀 Installation

```bash
# Cloner le dépôt
git clone https://github.com/HaruSnak/42-cub3d
cd 42-cub3d
```

<a name="utilisation"></a>

### 💻 Utilisation

Compilez et lancez le jeu avec un fichier de carte :

```bash
make
./cub3D maps/map1.cub
```

Contrôles :
- **WASD** : Avancer/reculer/gauche/droite
- **Flèches** : Rotation gauche/droite
- **Souris** : Rotation du point de vue
- **ESC** : Quitter le jeu

<a name="structure-du-projet"></a>

### 📂 Structure du projet

```
42-cub3d/
├── Makefile                    # Script de build
├── cub3d.h                     # Fichier d'en-tête principal
├── cub3d.c                     # Point d'entrée principal du jeu
├── LICENSE                     # Fichier de licence
├── README.md                   # Ce fichier
├── README-Template.md          # Template pour README
├── assets/                     # Textures du jeu
│   ├── textures/
│   └── ui/
├── includes/
│   ├── cub3d.h
│   └── libft/                  # Bibliothèque personnalisée
├── maps/                       # Fichiers de carte (.cub)
├── minilibx-linux/             # Bibliothèque MiniLibX
├── readme/                     # Ressources README
└── srcs/                       # Fichiers sources
    ├── bonus/
    ├── errors/
    ├── game/
    ├── parsing/
    ├── player/
    ├── raycasting/
    ├── texturing/
    └── ui/
```

<a name="compilation-1"></a>

### 🔧 Compilation

Compilez le projet en utilisant le Makefile :

```bash
make          # Compiler le jeu
make bonus    # Compiler avec fonctionnalités bonus
make clean    # Supprimer les fichiers objets
make fclean   # Supprimer l'exécutable et les fichiers objets
make re       # Recompiler tout
```

<a name="référence-des-fonctions"></a>

### 📚 Référence des fonctions

#### Fonctions principales
- [`main`](srcs/cub3d.c) - Initialisation et boucle du jeu
- [`ft_parse_base`](srcs/parsing/parsing.c) - Parsing et validation de la carte
- [`cast_rays`](srcs/raycasting/raycasting_draw.c) - Rendu par raycasting
- [`key_press`](srcs/player/keys.c) - Gestion des entrées

#### Fonctionnalités clés
- **Algorithme DDA** : Raycasting de base pour la détection des murs
- **Mappage de textures** : Applique des textures XPM aux murs
- **Rendu de minimap** : Dessine l'aperçu 2D en bonus
- **Rotation souris** : Ajuste l'angle du joueur via le mouvement souris

### 👨‍🎓 Note
<p align="left">
    <img src="readme/115.png" alt="115/100" width="216" height="164">
</p>

<a name="crédits-1"></a>

### 📖 Crédits

- **Norme 42** : [Standard C officiel](https://cdn.intra.42.fr/pdf/pdf/960/norme.en.pdf)
- **Tutoriel Raycasting** : [Lode Vandevenne](https://lodev.org/cgtutor/raycasting.html)
- **Documentation MiniLibX** : [Guide Harm-Smits](https://harm-smits.github.io/42docs/libs/minilibx/getting_started.html)

### 📄 Licence

Ce projet est sous licence **MIT** - voir le fichier [LICENSE](LICENSE) pour plus de détails.

</details>

---

[contributors-shield]: https://img.shields.io/github/contributors/HaruSnak/42-cub3d.svg?style=for-the-badge
[contributors-url]: https://github.com/HaruSnak/42-cub3d/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/HaruSnak/42-cub3d.svg?style=for-the-badge
[forks-url]: https://github.com/HaruSnak/42-cub3d/network/members
[stars-shield]: https://img.shields.io/github/stars/HaruSnak/42-cub3d.svg?style=for-the-badge
[stars-url]: https://github.com/HaruSnak/42-cub3d/stargazers
[issues-shield]: https://img.shields.io/github/issues/HaruSnak/42-cub3d.svg?style=for-the-badge
[issues-url]: https://github.com/HaruSnak/42-cub3d/issues
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://www.linkedin.com/in/shany-moreno-5a863b2aa
[license-shield]: https://img.shields.io/github/license/HaruSnak/42-cub3d.svg?style=for-the-badge
[license-url]: https://github.com/HaruSnak/42-cub3d/blob/master/LICENSE
