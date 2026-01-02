# Documentation - Mac Shortcuts Trainer

## Contexte du projet

**Date de création** : 2 janvier 2026
**Auteur** : Développé avec Claude Code
**Objectif** : Application personnelle pour apprendre et maîtriser les raccourcis clavier macOS via la gamification.

## Stack technique

- **HTML5** : Single-file application (~3500 lignes)
- **CSS3** : Variables CSS, Flexbox, Grid, animations, dark mode
- **JavaScript** : Vanilla ES6+, aucune dépendance externe
- **Stockage** : LocalStorage (progression, paramètres, statistiques)
- **PWA** : Service Worker + Manifest pour installation native

## Architecture

```
mac-shortcuts-trainer/
├── index.html      # Application complète (HTML + CSS + JS)
├── manifest.json   # Configuration PWA
├── sw.js           # Service Worker (cache offline)
├── icon-192.png    # Icône PWA
├── icon-512.png    # Icône PWA grande
├── README.md       # Documentation utilisateur
└── DOCUMENTATION.md # Ce fichier
```

## Fonctionnalités implémentées

### 1. Modes d'apprentissage

#### Flashcards
- Répétition espacée (algorithme SM-2 simplifié)
- 3 modes : Nouveaux, Révision, Tous
- Notation : Difficile / Moyen / Facile
- Progression sauvegardée par raccourci

#### Quiz
- Saisie clavier interactive (vraies touches)
- 3 durées : 10, 20, 50 questions
- Feedback immédiat avec correction
- Clavier visuel montrant les touches attendues

### 2. Gamification

| Élément | Description |
|---------|-------------|
| **XP** | Points d'expérience gagnés à chaque action |
| **Niveaux** | Progression (niveau × 100 XP requis) |
| **Streaks** | Séries de bonnes réponses consécutives |
| **Badges** | 8 badges à débloquer |
| **Défi quotidien** | 5 raccourcis/jour avec bonus +50 XP |

### 3. Bibliothèque

- **75+ raccourcis** organisés en 8 catégories
- Indicateur de maîtrise (0-3)
- Système de favoris
- Filtre par difficulté
- Filtre par catégorie

### 4. Recherche

- Recherche par action/description
- Traducteur Windows → Mac
- Contribution de raccourcis personnalisés

### 5. Statistiques

- Sessions totales
- Score moyen aux quiz
- Meilleur streak
- Jours actifs
- Graphique de maîtrise par catégorie

### 6. UX/UI

- Thème clair/sombre
- Sons de feedback (Web Audio API)
- Animations confettis
- Clavier visuel interactif
- Design responsive (mobile-first)
- PWA installable

## Structure du code JavaScript

```javascript
// Données
const shortcuts = [...];        // 75+ raccourcis
const keyMap = {...};           // Mapping touches clavier

// État principal
let state = {
    xp, level, streak, maxStreak,
    masteredShortcuts, shortcutProgress,
    selectedCategories, currentCards,
    quizQuestions, quizScore, badges
};

// Paramètres
let settings = {
    darkMode, soundEnabled,
    favoritesFirst, difficultyFilter, favorites
};

// Statistiques
let stats = {
    totalSessions, quizScores,
    bestStreak, daysActive
};

// Défi quotidien
let dailyChallenge = {
    date, target, progress, completed, shortcuts
};
```

## Stockage LocalStorage

| Clé | Contenu |
|-----|---------|
| `macShortcutsState` | Progression, XP, niveau, badges |
| `macShortcutsSettings` | Thème, sons, favoris, filtres |
| `macShortcutsStats` | Statistiques avancées |
| `macShortcutsDailyChallenge` | État du défi quotidien |
| `userShortcuts` | Raccourcis ajoutés par l'utilisateur |

## Catégories de raccourcis

1. **Système** - Copier, Coller, Annuler, etc.
2. **Finder** - Navigation fichiers
3. **Captures** - Screenshots
4. **Navigation** - Spotlight, Mission Control
5. **Texte** - Formatage, curseur
6. **Fenêtres** - Gestion des fenêtres
7. **Navigateur** - Safari/Chrome
8. **Productivité** - Préférences, Emoji

## Algorithme de répétition espacée

```javascript
// Notation Facile (3)
progress.level = min(3, level + 1)
progress.nextReview = now + (level × 24h)

// Notation Moyen (2)
progress.nextReview = now + 12h

// Notation Difficile (1)
progress.level = max(0, level - 1)
progress.nextReview = now + 1h

// Maîtrisé si level >= 3
```

## PWA - Service Worker

```javascript
// Stratégie : Cache-first
// Fichiers cachés :
// - index.html
// - manifest.json
// - icon-192.png
// - icon-512.png
```

## Évolutions possibles

### Court terme
- [ ] Raccourcis d'applications spécifiques (VS Code, Figma...)
- [ ] Export PDF cheat sheet
- [ ] Import/Export JSON progression

### Moyen terme
- [ ] Mode survie (endurance)
- [ ] Plus de badges
- [ ] Tutoriel d'accueil

### Long terme
- [ ] Backend pour sync cloud
- [ ] Classement (si multi-utilisateurs)
- [ ] Traductions (EN, ES)

## Déploiement

**URL** : https://codbad25.github.io/mac-shortcuts-trainer/

**Hébergement** : GitHub Pages (branche `main`, dossier `/`)

**Mise à jour** :
```bash
git add -A
git commit -m "Description des changements"
git push
# Déploiement automatique en ~1-2 minutes
```

## Historique des commits

| Date | Description |
|------|-------------|
| 2026-01-02 | Initial commit: PWA avec gamification |
| 2026-01-02 | Update README avec fonctionnalités |
| 2026-01-02 | Ajout confettis, clavier visuel, stats, défi quotidien |

---

*Documentation générée le 2 janvier 2026*
