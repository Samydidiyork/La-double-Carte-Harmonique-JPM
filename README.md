# La double Carte Harmonique JPM

**Une méthode de composition par double grille harmonique**

> *"Une carte harmonique par voix, des notes pivots pour les relier, des mouvements contraires pour les libérer."*

**Auteur : Jean-Pierre Mallet (JPM)**
**© 2026 Jean-Pierre Mallet — Licence Apache 2.0**

---

## Qu'est-ce que La double Carte Harmonique ?

La double Carte Harmonique JPM est une méthode originale de composition musicale qui utilise deux grilles harmoniques simultanées pour guider l'écriture du contrepoint, de l'accompagnement et de la polyphonie.

Le principe : placer une progression d'accords au-dessus de chaque note d'une mélodie (portée 1), puis construire une seconde progression dans une tonalité différente (portée 2). La relation entre les deux cartes révèle instantanément les notes pivots, les zones de tension et les possibilités mélodiques pour la voix de contrepoint.

```
Portée 1 — Mélodie :      C ——— F ——— G7 ——— C
                           ↕       ↕      ↕       ↕
Portée 2 — Contrepoint :  A ——— D ——— E7 ——— A
```

Cette méthode est universellement applicable : contrepoint, accompagnement, polyphonie à N voix, musique modale, musique tonale.

---

## Pourquoi ce logiciel n'existe pas encore

Les logiciels actuels (MuseScore, Sibelius, Dorico) proposent de la notation musicale mais aucun n'offre une double grille harmonique interactive comme outil de composition guidée. La double Carte Harmonique JPM comble ce vide.

---

## Modules à développer

| Module | Description |
|---|---|
| **Double carte interactive** | Choisir deux gammes, générer automatiquement les progressions cadentielles |
| **Analyse des relations** | Notes pivots en vert, tensions en orange, frottements chromatiques en rouge |
| **Assistant contrepoint** | Suggérer des notes candidates pour la portée 2 selon les règles contrapuntiques |
| **Improvisation guidée** | Entrer un motif germinatif (2-3 notes), proposer des dérives dans le cadre de la double carte |
| **Coloration harmonique** | Tonique en rouge, tierce en vert, autres notes en neutre — code visuel sur les portées et la tablature |
| **Glisser-déposer** | Placer et déplacer les notes directement sur les portées à la souris ou au doigt |
| **Tablature chiffrée** | Affichage des numéros de cases sur les 6 cordes, avec convention 0 = corde à vide |
| **Roue du cycle des quintes** | Visualisation interactive pour choisir les tonalités des deux cartes et leurs relations |
| **Substitution par silence** | Quand une voix atteint la quarte, remplacer la note par un silence (respiration mélodique) |
| **Export** | MIDI, MusicXML, PDF |

---

## Les règles de la méthode

### Ce qu'on construit
- Mouvements contraires entre les voix (indépendance)
- Mouvements parallèles en tierces et sixtes (couleur)
- Notes de passage (fluidité)
- Notes pivots communes aux deux cartes (ancrage harmonique)

### Ce qu'on évite
- Quintes parallèles
- Octaves parallèles
- Croisements de voix
- Sauts augmentés ou diminués non préparés
- Unisson par mouvement direct non préparé

### Code visuel — Coloration des notes

| Couleur | Fonction | Rôle |
|---------|----------|------|
| 🔴 Rouge | Tonique (fondamentale) | Ancrage tonal — note structurelle principale |
| 🟢 Vert | Tierce (3e min ou maj) | Caractère majeur ou mineur de l'accord |
| ⚪ Neutre | Autres notes | Septième, sixte, notes de passage |

Ce code s'applique simultanément sur les deux portées et sur la tablature guitare.

### Règle de substitution par silence à la quarte

Lorsqu'une voix atteint l'intervalle de **quarte juste** (5 demi-tons) par rapport à la tonique, la note est substituée par un **silence** :

- La quarte crée une tension suspendue difficile à résoudre sans préparation
- Le silence à cet endroit libère l'espace mélodique et donne une **respiration naturelle** à la phrase
- Cette règle s'applique voix par voix, indépendamment de l'autre carte

```
Exemple en Do majeur :
Do Ré Mi Fa → Do Ré Mi 𝄽 (silence à Fa = quarte)
```

### Les relations entre tonalités
- **Tierce mineure** — proche, clair-obscur
- **Quinte** — très lié, notes communes abondantes
- **Quarte** — grave et posé
- **Seconde** — tension moderne
- **Triton** — maximum de tension, couleur jazz

---

## Stack technologique suggérée

- **Notation musicale** : [VexFlow](https://www.vexflow.com/) ou [OSMD](https://opensheetmusicdisplay.github.io/)
- **Audio** : Web Audio API, Tone.js
- **Interface** : React ou Vue.js
- **Export MIDI** : JZZ.js ou midi-writer-js
- **Export MusicXML** : musicxml-interfaces

---

## Comment contribuer

1. Forkez ce dépôt
2. Créez une branche pour votre fonctionnalité (`git checkout -b feature/nom-du-module`)
3. Committez vos changements
4. Ouvrez une Pull Request

Toute contribution — développeurs, musiciens, théoriciens — est la bienvenue.

---

## Référence obligatoire

Tout projet dérivé doit mentionner :

> **"La double Carte Harmonique JPM — Jean-Pierre Mallet, 2026"**

---

## Licence

```
Copyright 2026 Jean-Pierre Mallet

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```

---

*"La carte n'est pas une cage — c'est le courant du fleuve."*
*— Jean-Pierre Mallet, 2026*
