# Bible de l'Électronique

Ouvrage de référence multi-niveaux en électronique, du composant physique au système complet.
Rédigé en LaTeX, compilé avec `pdflatex` (CircuiTikZ pour les schémas).

## Public et philosophie

Double lectorat : accessible aux débutants **et** de qualité référence pour ingénieurs/chercheurs.
Chaque chapitre est structuré en trois niveaux :

- 🟢 **Bases** — intuitif, sans Maxwell/ARQS
- 🟡 **Approfondissement** — modèle d'ingénierie
- 🔴 **Niveau Ingénieur** — modèle physique avec limites réelles

Principes : pas d'affirmation sans justification, hypothèses explicites, causalité physique
traçable de bout en bout, liens inter-chapitres systématiques.

## État d'avancement

**Phase V0.1** (production de contenu) — **terminée** : 37 chapitres, 9 parties, 536 pages.

| Partie | Chapitres | Sujet | État |
|--------|-----------|-------|------|
| I    | 1–6   | Fondamentaux              | ✅ |
| II   | 7–9   | Composants passifs        | ✅ |
| III  | 10–12 | Régime sinusoïdal         | ✅ |
| IV   | 13–14 | Fonctions de transfert    | ✅ |
| V    | 15–19 | Semi-conducteurs          | ✅ |
| VI   | 20–29 | Électronique numérique    | ✅ |
| VII  | 30–32 | Alimentations             | ✅ |
| VIII | 33–34 | Asservissement            | ✅ |
| IX   | 35–37 | CEM / PCB                 | ✅ |

**Phase V0.5** (peer-review, visuels, homogénéisation) — en cours : francisation ✅ · ch.1 ✅ · ch.2 ✅ · ch.3 ✅ · ch.4 ✅ · ch.5 ✅ · ch.6 ✅ · ch.7 ✅ · ch.8 ✅ · ch.9 ✅ · ch.10 ✅ · ch.11 ✅ · ch.12 ✅ · ch.13 ✅ · ch.14 ✅ · ch.15 ✅ · ch.16 ✅ · ch.17 ✅ · ch.18 ✅ · ch.19 ✅ · ch.20 ✅ · ch.21 ✅ · ch.22 ✅ · ch.23 ✅ · ch.24 ✅ · ch.25 ✅ · ch.26 ✅ · ch.27 ✅ · ch.28 ✅ · ch.29 ✅ · ch.30 ✅ · ch.31 ✅ · ch.32 ✅
**Ne pas mélanger V0.1 et V0.5.**

## Compilation

```bash
pdflatex Bible_Elec.tex
pdflatex Bible_Elec.tex   # 2e passe (sommaire)
pdflatex Bible_Elec.tex   # 3e passe (références stables)
```

## Conventions éditoriales (rappel)

- Environnements colorés : `bases`, `approfondissement`, `ingenieur`, `formule`, `intuition`,
  `attention`, `pratique`, `retenir`.
- Résumés en 3 tableaux par niveau en fin de chapitre.
- 6 exercices/chapitre (2 débutant, 2 intermédiaire, 2 ingénieur) + 4 questions de compréhension.
- Schémas CircuiTikZ `american` : courants intégrés sur les fils (`i=`), labels non superposés,
  tracés orthogonaux, masse commune fermée.

## Workflow par chapitre

1. Rédaction d'un fichier `ChapitreNN.tex` autonome
2. Compilation + vérification visuelle (PDF)
3. Relecture (peer review)
4. Corrections ciblées → « Bon à Tirer »
5. Merge dans `Bible_Elec.tex`
6. Commit git
