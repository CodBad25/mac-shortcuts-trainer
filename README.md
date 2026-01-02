# Mac Shortcuts Trainer

[![GitHub Pages](https://img.shields.io/badge/demo-live-brightgreen)](https://codbad25.github.io/mac-shortcuts-trainer/)

Application web PWA interactive pour apprendre et maîtriser les raccourcis clavier macOS avec gamification.

**[Essayer l'app](https://codbad25.github.io/mac-shortcuts-trainer/)**

## Fonctionnalités

### Mode Flashcards
- **Répétition espacée** : Les raccourcis difficiles reviennent plus souvent
- **3 modes** :
  - Nouveaux : Apprendre de nouveaux raccourcis
  - Révision : Revoir les raccourcis à réviser
  - Tous : Pratiquer l'ensemble

### Mode Quiz
- **Saisie clavier interactive** : Tapez réellement le raccourci pour valider
- **3 niveaux** :
  - Rapide : 10 questions
  - Standard : 20 questions
  - Marathon : 50 questions

### Système de Gamification
- **XP et Niveaux** : Gagnez de l'expérience à chaque bonne réponse
- **Streaks** : Bonus pour les séries de bonnes réponses
- **8 Badges** à débloquer :
  - Premiers pas (10 raccourcis appris)
  - Apprenti rapide (5 streak)
  - Dévoué (Niveau 5)
  - Maître (50% maîtrisés)
  - Expert (Tous maîtrisés)
  - Roi du Streak (10 streak)
  - Niveau 10
  - Quiz Parfait (100% sur un quiz)

### Bibliothèque
- **75+ raccourcis** organisés par catégorie
- Indicateur de maîtrise pour chaque raccourci
- Filtrage par catégorie
- Système de favoris (étoile)

### Recherche
- **Recherche par action** : Trouvez un raccourci en décrivant ce que vous voulez faire
- **Traducteur Windows → Mac** : Convertissez vos raccourcis Windows en équivalent Mac
- **Contribution** : Proposez de nouveaux raccourcis à ajouter

### Paramètres
- **Thème sombre** : Mode clair/sombre
- **Sons de feedback** : Retour audio pour succès/erreur
- **Filtre par difficulté** : Facile, Moyen, Difficile
- **Favoris en premier** : Priorisez vos raccourcis favoris

### PWA (Progressive Web App)
- Installable sur mobile et desktop
- Fonctionne hors ligne
- Icône sur l'écran d'accueil

### Défi quotidien
- **5 raccourcis par jour** à maîtriser
- Compte à rebours jusqu'à minuit
- **+50 XP bonus** à la complétion
- Renouvellement automatique chaque jour

### Statistiques avancées
- Sessions totales, score moyen, meilleur streak
- Jours actifs de pratique
- **Graphique de maîtrise par catégorie**

### Clavier visuel interactif
- Affichage des touches à presser en temps réel
- Les touches attendues sont surlignées
- Feedback visuel lors de la frappe

### Animations
- **Confettis** lors des succès (quiz ≥80%, défi complété)
- Animations fluides et récompensantes

## Catégories de raccourcis

| Catégorie | Exemples |
|-----------|----------|
| **Système** | Copier, Coller, Annuler, Enregistrer |
| **Finder** | Nouveau dossier, Aperçu rapide, Corbeille |
| **Captures** | Écran complet, Zone, Fenêtre |
| **Navigation** | Spotlight, Mission Control, Bureaux virtuels |
| **Texte** | Gras, Italique, Navigation curseur |
| **Fenêtres** | Plein écran, Onglets, Masquer |
| **Navigateur** | Actualiser, Zoom, Favoris |
| **Productivité** | Préférences, Emoji, Dictée |

## Raccourcis essentiels inclus

### Les plus utiles
| Action | Raccourci |
|--------|-----------|
| Copier | `⌘ + C` |
| Coller | `⌘ + V` |
| Annuler | `⌘ + Z` |
| Spotlight | `⌘ + Espace` |
| Capture zone | `⌘ + ⇧ + 4` |
| Basculer apps | `⌘ + Tab` |
| Fermer fenêtre | `⌘ + W` |
| Quitter app | `⌘ + Q` |
| Nouveau dossier | `⌘ + ⇧ + N` |
| Ouvrir Documents | `⌘ + ⇧ + O` |

## Installation

### Option 1 : En ligne (recommandé)
Visitez [codbad25.github.io/mac-shortcuts-trainer](https://codbad25.github.io/mac-shortcuts-trainer/)

### Option 2 : PWA
1. Ouvrez l'app dans Chrome/Safari
2. Cliquez sur "Installer" dans la bannière ou le menu du navigateur
3. L'app sera disponible comme une application native

### Option 3 : Local
```bash
git clone https://github.com/CodBad25/mac-shortcuts-trainer.git
open mac-shortcuts-trainer/index.html
```

## Technologies

- HTML5 (single-file application)
- CSS3 (Variables CSS, Flexbox, Grid, Animations, Dark mode)
- JavaScript vanilla (ES6+)
- Web Audio API (sons de feedback)
- Service Worker (cache offline)
- LocalStorage (sauvegarde de progression)

## Stockage des données

La progression est sauvegardée localement dans le navigateur (LocalStorage) :
- XP et niveau
- Raccourcis maîtrisés
- Badges débloqués
- Historique de répétition espacée

## Responsive

L'application s'adapte à toutes les tailles d'écran :
- Desktop
- Tablette
- Mobile

## Légende des symboles

| Symbole | Touche |
|---------|--------|
| ⌘ | Command |
| ⌃ | Control |
| ⌥ | Option/Alt |
| ⇧ | Shift |
| ⌫ | Backspace |
| ↵ | Enter |
| ↑↓←→ | Flèches |

---

Créé le 2 janvier 2026
