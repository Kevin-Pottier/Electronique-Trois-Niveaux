# Historique des versions

## v1.4.1 — 11 septembre 2026
Passe de correction, sans ajout de contenu.

**Figures.** Revue des 180 figures, rendues en image et contrôlées une à une :
49 défauts de lisibilité corrigés. L'essentiel relève du placement — repère
traversé par une courbe ou un fil, libellés superposés, texte débordant de son
cadre, flèche de renvoi partant à l'intérieur du texte qu'elle commente. Là où
un repère ne pouvait pas tenir près de sa courbe sans la toucher, il a été
remplacé par une légende dans une zone libre du tracé (15.5, 37.3, 40.2)
plutôt que déplacé à un endroit ambigu.

Trois corrections portent sur le fond et non sur la forme :
- **14.5** — le diagramme de Nyquist ne passait pas par l'origine : le repère
  « ω→∞ » ne désignait rien et contredisait la légende. La boucle intérieure
  est rétablie, le tracé rejoint l'origine, et le point −1 reste visiblement
  à l'extérieur.
- **33.3** — les deux légendes du dark silicon étaient interverties : « éteint »
  en blanc sur case claire, « actif » en noir sur case noire. Les deux étaient
  illisibles.
- **9.6** — le cycle d'hystérésis ne passait pas par les points $B_r$ et $H_c$
  qu'il prétendait repérer ; la boucle est reconstruite pour y passer.

**Index.** 388 → 359 entrées, sans perte d'information : ce sont des doublons
et des redondances qui disparaissent.

Le défaut principal était structurel. Pour plusieurs notions, une famille
hiérarchique et des entrées à plat coexistaient : « convertisseur ▸ buck »
voisinait avec « convertisseur abaisseur (buck) », « transistor ▸ bipolaire »
avec « transistor bipolaire (BJT) ». Le lecteur trouvait la même chose à deux
endroits, avec des renvois de pages différents. Les entrées à plat ont été
rattachées à leur famille — convertisseurs, filtres, puissance, bruit,
résonance, redressement, et les sous-entrées des composants.

Quinze autres doublons venaient de la forme : le même concept sous deux
tournures (« loi d'Ohm » et « Ohm, loi d' » ; idem Thévenin, Millman,
Barkhausen), ou au singulier et au pluriel. Les termes portant un nom propre
sont désormais indexés sous ce nom, là où le lecteur le cherche.

Enfin, quinze entrées étaient des titres de section recopiés — « ce que l'on
mesure, et avec quoi », « déclenchement, ou pourquoi la trace danse »,
« fan-out et charge capacitive ». Elles ont été supprimées, ou remplacées par
le terme que le lecteur chercherait réellement (« déclenchement (trigger) »,
« pince ampèremétrique », « profondeur mémoire »).

Pagination inchangée à 691 pages. Le texte, les 1623 références croisées et
les 250 exercices sont identiques à la v1.4.

## v1.4 — 10 septembre 2026
Ajout du chapitre 16, **La Simulation avec LTspice**, en fin de partie IV :
ce qu'un simulateur calcule réellement et ce qu'il ne calcule pas, la netlist
comme forme véritable du circuit, les quatre analyses, un filtre RC de bout en
bout, les pièges de la première soirée dont le préfixe `M` qui vaut milli ;
les sources et ce que chaque analyse y lit, le pas de calcul et le défaut
qu'il efface, balayages et Monte-Carlo, l'échec de convergence comme signal de
sur-idéalisation ; le modèle comme véritable objet de la simulation, ce que la
simulation ne montrera jamais, la vérification d'une marge de stabilité, et la
discipline de contrôle. 12 pages, 6 exercices corrigés, 4 questions, 2 figures.
Les chapitres 16 à 40 deviennent 17 à 41.

Le chapitre est placé après les filtres et non en partie I : la simulation ne
prend son sens qu'avec l'analyse fréquentielle. Il est construit autour des
notions — directives, modèles, convergence, lecture critique — et non autour
des menus, pour survivre aux changements de version. PSpice partage le moteur
et la syntaxe : seule l'interface diffère.

691 pages, 41 chapitres, 250 exercices corrigés, 690 entrées d'index.

## v1.3 — 10 septembre 2026
Ajout du chapitre 22, **L'Amplification de Puissance**, en fin de partie V :
le bilan énergétique des classes A, B, AB et D ; le pire cas thermique, qui
survient aux deux tiers de l'amplitude et non à pleine puissance ; la
distorsion de croisement et le multiplicateur de V_BE ; le dimensionnement du
radiateur par la chaîne des résistances thermiques ; l'aire de sécurité et le
second claquage ; la classe D et ses compromis ; ce qu'une charge réelle fait
subir à l'étage. 12 pages, 6 exercices corrigés, 4 questions, 3 figures,
toutes les valeurs vérifiées par le calcul. Les chapitres 22 à 39 deviennent
23 à 40.

Le chapitre 17 traitait déjà les classes A, B et AB comme façons de polariser
un transistor. Celui-ci part de là pour traiter ce qui manquait : la
dissipation, sa valeur maximale, et le chemin de la chaleur.

**Les 35 symboles de masse de l'ouvrage ne s'imprimaient pas**, et ce depuis
l'origine. Le préambule chargeait `circuits.ee.IEC` avant circuitikz ; cette
bibliothèque redéfinit le nœud `ground` et ne trace rien. Elle n'était
utilisée nulle part : elle est retirée, et les 35 figures sont réparées.

679 pages, 40 chapitres, 244 exercices corrigés, 672 entrées d'index.

## v1.2 — 9 septembre 2026
Ajout du chapitre 7, **Instrumentation et Mesures**, en fin de partie I :
l'oscilloscope et son déclenchement, l'effet de charge chiffré par Thévenin,
la sonde 10× et sa compensation, bande passante et temps de montée,
échantillonnage et repliement, le piège de la masse reliée à la terre, la
mesure quatre fils, le plancher de bruit thermique, étalonnage et
traçabilité. 14 pages, 6 exercices corrigés, 4 questions de compréhension,
toutes les valeurs vérifiées par le calcul. Les chapitres 7 à 38 deviennent
8 à 39.

Le livre traitait le branchement du multimètre au fil des grandeurs mais
n'expliquait nulle part l'oscilloscope — onze mentions, aucune section.

Passe typographique et de fond menée dans le même cycle :
- **421 caractères manquaient à l'impression depuis la v1.0.** siunitx compose
  ses unités en mode mathématique, où un `°` ou un accent tapé littéralement
  n'existe pas : LaTeX les jetait en silence. Le livre imprimait « 25 C » et
  « dB/dcade ». Corrigé par les macros idoines et deux unités françaises
  déclarées ;
- césure française activée sans babel — les motifs sont déjà dans le format
  pdflatex, inutile de charger un paquet qui casserait CircuiTikZ ;
- 47 débordements de ligne ramenés à zéro, dont deux tiers venaient d'une
  règle méconnue : TeX ne coupe jamais le premier mot d'un paragraphe, et
  chaque cellule `p{}` en ouvre un ;
- les 172 figures reprennent leur place dans le texte (`[!ht]`) ;
- index resserré de 995 à 653 entrées par retrait des recopies de titres ;
- en-tête agrandi pour les six titres de chapitre tenant sur deux lignes.

Le journal de compilation est vierge : 0 erreur, 0 avertissement, 0
débordement, 0 caractère perdu.

667 pages, 39 chapitres, 238 exercices corrigés, 653 entrées d'index.

## v1.1.1 — 9 septembre 2026
Ajout du chapitre 20, **Les Oscillateurs** (Barkhausen, pont de Wien,
relaxation 555, Colpitts, quartz, bruit de phase), en fin de partie V :
16 pages, 6 exercices corrigés, 4 questions de compréhension, toutes les
valeurs vérifiées par le calcul. Les chapitres 20 à 37 deviennent 21 à 38.

Préalable rendu nécessaire par cette insertion : les 951 renvois croisés,
jusque-là écrits en dur, sont convertis en références LaTeX symboliques
(49 `\label` sur les chapitres, annexes et parties). Un chapitre peut
désormais être inséré, déplacé ou renuméroté sans reprendre un seul renvoi.

Corrigé au passage : un renvoi erroné au chapitre des alimentations à
découpage, qui pointait le chapitre Laplace là où le sujet — l'EMI — relève
du chapitre CEM. Débordements de ligne ramenés de 47 à 24 par
`\emergencystretch`.

Passe typographique dans la foulée : césure française activée sans babel (les
motifs sont déjà dans le format pdflatex, inutile de charger un paquet qui
casserait CircuiTikZ), 47 débordements de ligne ramenés à zéro, index resserré
de 995 à 623 entrées par retrait des recopies mécaniques de titres.

653 pages, 232 exercices corrigés, 623 entrées d'index.

## v1.01 — 28 août 2026
Publication du dépôt : licence CC BY-NC-SA, README public, guide de
contribution, fichier de citation, présent changelog. Renommage du projet
en « L'Électronique en trois niveaux » et ajout de l'affiliation ESEO.
Aucune modification du manuscrit — c'est pourquoi cette version ne figure
pas au tableau « Historique des versions » de l'ouvrage, qui ne suit que
le texte.

## v1.0 — 21 juillet 2026
Index complet (956 entrées, 629 clés), typographie française (3 199 espaces
insécables), orthographe vérifiée. Version de référence.

## v0.9 — juillet 2026
Index semé programmatiquement (titres + dictionnaire curaté).

## v0.75 — juillet 2026
Appareil éditorial : page de garde, licence, avant-propos, guide de lecture,
table des figures, pages de partie, annexes, bibliographie commentée,
glossaire, lexique français–anglais.

## v0.5 — juillet 2026
Relecture technique intégrale : trois passes par chapitre, tous les exercices
vérifiés par le calcul, une soixantaine de figures créées ou refaites.

## v0.1 — 15 juin 2026
Rédaction initiale des 37 chapitres.
