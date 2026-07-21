# Bible de l'Électronique

**Du débutant absolu à l'ingénieur confirmé** — un livre libre de 644 pages,
écrit en français, du courant électrique au circuit imprimé.

> « Un bébé doit pouvoir comprendre les bases, un ingénieur doit pouvoir s'y
> référer comme source de qualité. »

## Le principe : trois livres en un

Chaque chapitre est écrit trois fois, à trois altitudes :

1. **Les Bases** — aucune connaissance préalable supposée ;
2. **Approfondissement** — les modèles, les calculs, les montages classiques ;
3. **Niveau Ingénieur** — les limites, les compromis et les pièges réels.

On peut le lire comme trois livres emboîtés, et y revenir à mesure que l'on
grandit.

## Contenu

37 chapitres en 9 parties : Fondamentaux · Composants passifs · Régime
sinusoïdal · Fonctions de transfert et filtres · Semi-conducteurs ·
Électronique numérique · Alimentations · Asservissement · CEM et conception
de cartes. Plus : annexes (séries E, constantes, notations), bibliographie
commentée, glossaire, lexique français–anglais, index.

En chiffres : **644 pages** · **300 exercices corrigés** · **175 schémas et
figures** (CircuiTikZ/TikZ) · **956 entrées d'index** · toutes les valeurs
numériques vérifiées par le calcul.

## Obtenir le livre

- **PDF prêt à lire** : voir les [Releases](../../releases) (v1.0) ;
- **Compiler soi-même** (TeX Live complet requis) :

```bash
pdflatex Bible_Elec.tex
makeindex Bible_Elec.idx
pdflatex Bible_Elec.tex
pdflatex Bible_Elec.tex
```

## Signaler une erreur, contribuer

Une valeur douteuse, une coquille, un schéma perfectible ? Ouvrez une
[issue](../../issues) avec la page et la citation exacte — chaque erreur
signalée rend la version suivante meilleure. Voir
[CONTRIBUTING.md](CONTRIBUTING.md).

## Licence

[CC BY-NC-SA 4.0](LICENSE.md) : libre de partager et d'adapter, pas de vente,
contributions repartagées sous la même licence.

## Auteur

**Kévin Pottier** — ingénieur en électronique, enseignant en école
d'ingénieurs. Contact : `kevin.pottier@eseo.fr`.

Ce livre a été écrit avec l'aide substantielle d'une intelligence artificielle
(Claude, d'Anthropic), sous la direction et la vérification systématique de
l'auteur — la démarche est détaillée dans l'avant-propos.
