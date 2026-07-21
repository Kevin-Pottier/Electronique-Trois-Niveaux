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
- encadrés existants uniquement : formule, intuition, attention, pratique,
  retenir ;
- **toute valeur numérique nouvelle doit être vérifiable par le calcul** ;
- figures en CircuiTikZ/TikZ, dans le style des figures existantes ;
- typographie française (espaces insécables devant `: ; ! ?`, guillemets
  « français ») ;
- compilation sans erreur : `pdflatex` ×2 + `makeindex` + `pdflatex` ×2.

## Licence des contributions

En proposant une contribution, vous acceptez qu'elle soit diffusée sous la
licence du livre, **CC BY-NC-SA 4.0**.
