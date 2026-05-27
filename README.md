# Project Name

Projet fictif créé dans le but d’apprendre et pratiquer Git et GitHub.

Ce projet sert principalement à :

- comprendre Git
- apprendre GitHub
- pratiquer le versionnement
- apprendre à collaborer
- comprendre l’organisation d’un projet web

---

# Qu’est-ce que Git ?

Git est un système de versionnement.

Il permet de :

- sauvegarder les différentes versions d’un projet
- suivre les modifications du code
- revenir à une ancienne version
- travailler en équipe sans perdre le travail

Git fonctionne localement sur votre ordinateur.

---

# Qu’est-ce que GitHub ?

GitHub est une plateforme en ligne utilisée pour héberger des projets Git.

GitHub permet :

- de stocker les projets en ligne
- collaborer avec d’autres développeurs
- partager son code
- contribuer à des projets open source
- gérer des branches et pull requests

Git = outil de versionnement  
GitHub = plateforme de collaboration

---

# Initialiser Git dans un projet

Créer un projet :

```bash
mkdir project-name
cd project-name
```

Initialiser Git :

```bash
git init
```

Cette commande crée un dossier caché :

```bash
.git
```

Ce dossier contient :

- l’historique du projet
- les commits
- les branches
- la configuration Git

---

# Vérifier l’état du projet

```bash
git status
```

Cette commande permet de voir :

- les fichiers modifiés
- les fichiers suivis
- les fichiers non suivis

---

# Ajouter des fichiers

Ajouter un fichier spécifique :

```bash
git add index.html
```

Ajouter tous les fichiers :

```bash
git add .
```

---

# Les commits

Créer un commit :

```bash
git commit -m "Ajout du header"
```

Un commit est une sauvegarde intelligente du projet.

Chaque commit possède :

- un identifiant unique
- une date
- un auteur
- un historique

---

# Voir l’historique des commits

```bash
git log
```

---

# Connecter le projet à GitHub

Créer un repository sur GitHub puis connecter le projet :

```bash
git remote add origin https://github.com/username/project-name.git
```

---

# Envoyer le projet sur GitHub

```bash
git push origin main
```

Cette commande envoie le projet local vers GitHub.

---

# Récupérer les modifications

```bash
git pull origin main
```

Cette commande récupère les nouvelles modifications depuis GitHub.

---

# Cloner un projet

Copier un projet GitHub sur son ordinateur :

```bash
git clone https://github.com/username/project-name.git
```

Entrer dans le dossier :

```bash
cd project-name
```

---

# Les branches

Les branches permettent de travailler sur plusieurs fonctionnalités sans casser le projet principal.

Voir les branches :

```bash
git branch
```

Créer une branche :

```bash
git branch feature/navbar
```

Changer de branche :

```bash
git checkout feature/navbar
```

Créer et changer directement :

```bash
git checkout -b feature/navbar
```

---

# Workflow Git simple

## 1. Modifier le projet

Modifier les fichiers du projet.

---

## 2. Vérifier les changements

```bash
git status
```

---

## 3. Ajouter les fichiers

```bash
git add .
```

---

## 4. Créer un commit

```bash
git commit -m "Ajout de la navbar"
```

---

## 5. Envoyer les modifications

```bash
git push origin main
```

---

# Contribution au projet

## Étape 1 — Fork du projet

Créer une copie du repository depuis GitHub avec le bouton :

```text
Fork
```

---

## Étape 2 — Cloner le fork

```bash
git clone https://github.com/votre-username/project-name.git
```

---

## Étape 3 — Créer une branche

```bash
git checkout -b feature/new-feature
```

---

## Étape 4 — Modifier le projet

Ajouter ou modifier le code.

---

## Étape 5 — Commit

```bash
git add .
git commit -m "Ajout de la nouvelle fonctionnalité"
```

---

## Étape 6 — Push

```bash
git push origin feature/new-feature
```

---

## Étape 7 — Pull Request

Depuis GitHub :

- ouvrir le repository
- cliquer sur :
  
```text
Compare & Pull Request
```

- envoyer la demande de fusion

---

# Bonnes pratiques Git

- Faire des commits clairs
- Utiliser des branches
- Faire des commits réguliers
- Pull avant de push
- Éviter les commits vagues

Bon exemple :

```bash
git commit -m "Ajout du système responsive"
```

Mauvais exemple :

```bash
git commit -m "update"
```

---

# Structure du projet

```bash
project/
│
├── index.html
├── style.css
├── script.js
├── assets/
│   ├── images/
│   └── icons/
│
└── README.md
```

---

# Variables CSS

Le projet utilise des variables CSS afin de garder un design cohérent et facilement modifiable.

Les variables sont déclarées dans :

```css
:root
```

---

# Déclaration des variables

```css
:root {
  /* COLORS */
  --primary-color: #0d00ff;
  --background-color: #f5f5f5;
  --text-color: #333333;

  /* FONTS */
  --main-font: Arial, sans-serif;
  --title-size: 32px;
  --text-size: 16px;
  --small-size: 14px;

  /* SPACING */
  --spacing-sm: 10px;
  --spacing-md: 20px;
  --spacing-lg: 40px;

  /* BORDER */
  --border-radius: 10px;

  /* SHADOW */
  --box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);

  /* TRANSITION */
  --transition: 0.3s ease;
}
```

---

# Fonctionnement des variables CSS

Les variables CSS sont utilisées avec :

```css
var(--nom-variable)
```

Exemple :

```css
button {
  background: var(--primary-color);
}
```

---

# Explication des variables

## COLORS

| Variable | Description |
|---|---|
| `--primary-color` | Couleur principale |
| `--background-color` | Couleur de fond |
| `--text-color` | Couleur du texte |

---

## FONTS

| Variable | Description |
|---|---|
| `--main-font` | Police principale |
| `--title-size` | Taille des titres |
| `--text-size` | Taille normale |
| `--small-size` | Petite taille |

---

## SPACING

| Variable | Description |
|---|---|
| `--spacing-sm` | Petit espace |
| `--spacing-md` | Moyen espace |
| `--spacing-lg` | Grand espace |

---

## BORDER

| Variable | Description |
|---|---|
| `--border-radius` | Arrondi des angles |

---

## SHADOW

| Variable | Description |
|---|---|
| `--box-shadow` | Ombre principale |

---

## TRANSITION

| Variable | Description |
|---|---|
| `--transition` | Transition globale |

---

# Exemple d’utilisation

```css
body {
  background: var(--background-color);
  color: var(--text-color);
  font-family: var(--main-font);
}

button {
  background: var(--primary-color);
  padding: var(--spacing-sm) var(--spacing-md);
  border-radius: var(--border-radius);
  box-shadow: var(--box-shadow);
  transition: var(--transition);
}
```

---

# Conclusion

Ce projet est un environnement d’apprentissage destiné à :

- pratiquer Git et GitHub
- apprendre le travail collaboratif
- comprendre l’organisation d’un projet web
- découvrir les bonnes pratiques de développement
- apprendre les variables CSS
