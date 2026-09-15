# Contribuer

## Signaler une erreur

Ouvrez une **issue** avec : la **page**, la **citation exacte** du passage, et
ce qui vous semble faux (valeur, unité, raisonnement, schéma, typographie).
Les erreurs de calcul sont prioritaires : toutes les valeurs du livre sont
censées être vérifiées — si l'une résiste à votre vérification, c'est
précisément celle qu'il faut signaler.

## Proposer une amélioration

Les pull requests sont bienvenues, en respectant les conventions du livre :

- structure en **trois niveaux** (Bases / Approfondissement / Niveau Ingénieur) ;
- encadrés existants uniquement. Trois sont structurels, un par section :
  `bases`, `approfondissement`, `ingenieur`. Six s'emploient au fil du texte :
  `formule`, `intuition`, `analogie`, `attention`, `pratique`, `retenir` ;
- **toute valeur numérique nouvelle doit être vérifiable par le calcul** ;
- figures en CircuiTikZ/TikZ, dans le style des figures existantes ;
- typographie française (espaces insécables devant `: ; ! ?`, guillemets
  « français ») ;
- compilation sans erreur : `pdflatex` + `makeindex` + `pdflatex` ×2 (voir le
  [README](README.md), et l'avertissement sur `makeindex` si vous compilez
  dans un répertoire séparé).

## Renvois et numérotation

**Aucun numéro ne s'écrit à la main.** Chapitres, sections, figures, tableaux
et exercices sont numérotés par LaTeX et cités par `\ref`. Cette règle n'est
pas cosmétique : insérer un chapitre au milieu du livre décale tout ce qui
suit, et un numéro écrit en dur ne bouge pas. Le manuscrit a perdu 201 numéros
d'exercices de cette façon.

- un exercice s'ouvre par `\exo\label{exo:...}`, jamais par
  « `\textbf{Exercice 12.3}` » ;
- un tableau reçoit une légende `\captionof{table}{...}` placée juste après
  le `\begin{center}` qui l'entoure — il apparaît alors dans la *Liste des
  tableaux*. Les tableaux des encadrés « Résumé du chapitre » font exception :
  ils ne sont pas numérotés ;
- pour renvoyer à un élément, `\ref{...}` et rien d'autre. Un renvoi cassé
  devient visible à la compilation, un numéro faux ne se voit jamais.

## Licence des contributions

En proposant une contribution, vous acceptez qu'elle soit diffusée sous la
licence du livre, **CC BY-NC-SA 4.0**.
