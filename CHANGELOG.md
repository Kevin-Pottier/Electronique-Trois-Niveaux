# Historique des versions

## v1.5.2 — 15 septembre 2026
Comblement d'une dette de structure, et métadonnées de citation remises à jour.

**Les quatre chapitres insérés en v1.2--v1.4 n'avaient pas leur encadré
« À retenir » de fin de section « Les Bases ».** Trente-sept chapitres sur
quarante et un referment cette première section par un récapitulatif numéroté
avant de passer à l'Approfondissement. Les chapitres **7 (Instrumentation et
Mesures)**, **16 (La Simulation avec LTspice)**, **22 (Les Oscillateurs)** et
**23 (L'Amplification de Puissance)** en étaient dépourvus : l'encadré avait
été oublié au moment de leur insertion. Ils ont bien reçu, chacun, six points
tirés exclusivement du contenu de leur propre section « Les Bases » :

- ch. 7 — l'instrument répond à une question et une seule, l'ordre de réglage
  de l'oscilloscope, la trace qui défile, l'erreur de charge
  $\Delta V/V = R_{th}/(R_{th}+R_V)$, résolution / justesse / fidélité, et le
  chiffre sans incertitude ;
- ch. 16 — ce que résout un simulateur, la netlist comme forme véritable du
  circuit, les quatre analyses, la linéarisation de `.ac`, les quatre pièges
  (dont le préfixe `M` qui vaut *milli*), et « prédire avant de lancer » ;
- ch. 22 — l'oscillateur sans entrée, les deux familles, la boucle $A$–$\beta$,
  la double condition $A\beta = 1$ sur le module et la phase, le spectre du
  carré, et la durée de démarrage ;
- ch. 23 — concevoir à partir de la chaleur, le bilan
  $P_{\text{alim}} = P_{\text{charge}} + P_{\text{dissipée}}$, les rendements
  par classe, le coût du repos en classe A, le pire cas thermique à
  $\hat{V} = 2V_{CC}/\pi$, et le radiateur sous-évalué de moitié.

Les quarante et un chapitres ont désormais la même architecture interne.

**`CITATION.cff` était resté en version 1.0 du 21 juillet**, cinq versions en
arrière : toute citation produite depuis GitHub désignait la v1.0. Le fichier
est remis à jour et complété (résumé, mots-clés, langue, dépôt, licence). Sa
structure est également corrigée : le champ `type` de premier niveau
n'accepte que `software` ou `dataset` en CFF 1.2.0, si bien que l'ancien
`type: book` était invalide. Le livre est maintenant déclaré dans un bloc
`preferred-citation` de type `book`, qui est la forme prévue pour cela.

Aucune figure, aucun exercice, aucune formule n'a été modifié. Pagination
691 → 693 pages (les quatre encadrés ajoutés) ; 180 figures et 1148 renvois
numérotés inchangés.

## v1.5.1 — 15 septembre 2026
Correction d'une figure. La figure 11.1 (« Le phaseur tournant », chapitre 11)
contredisait le texte qui la précède immédiatement.

Le texte définit la grandeur sinusoïdale par sa **partie réelle** :
$u(t) = \hat{U}\cos(\omega t + \varphi_u) = \mathrm{Re}[\underline{U}e^{j\omega t}]$,
c'est-à-dire la projection du phaseur sur l'axe **horizontal**. La figure, elle,
reportait la **hauteur** de la pointe du vecteur par un trait horizontal, et la
courbe déroulée était tracée comme un `sin` : c'est la partie **imaginaire**. La
légende annonçait pourtant « la projection sur l'axe réel ».

Avec les valeurs du dessin ($\hat{U} = 1{,}4$ et $\varphi_u = 35°$), les deux
lectures donnaient deux valeurs différentes au même instant :

| | $u(0)$ |
|---|---|
| texte : $\hat{U}\cos 35°$ | **1,147** |
| courbe tracée : $1{,}4\sin 35°$ | **0,803** |

L'écart est exactement le déphasage de 90° entre sinus et cosinus. Un étudiant
qui applique la figure repart avec $u(t) = \hat{U}\sin(\omega t + \varphi_u)$ et
décale sa référence de phase d'un quart de période --- invisible tant qu'on ne
fait que des rapports d'amplitudes, gênant dès qu'il y a une condition initiale
ou une comparaison de phase entre deux signaux du circuit.

Le défaut était structurel, pas typographique : la construction « cercle à
gauche, sinusoïde déroulée à droite » reporte nécessairement une *hauteur*,
puisque l'ordonnée de la courbe est verticale. Remplacer `sin` par `cos` aurait
rendu le trait de liaison faux. La figure est donc redessinée :

- le vecteur est projeté sur l'axe réel par un trait pointillé **vertical** ;
- la projection est matérialisée par un segment épais sur l'axe réel, marqué
  d'un trait de congruence et étiqueté $u(0)$ ;
- cette **même longueur** est reportée en ordonnée à l'origine des temps, avec
  le même trait de congruence et la même étiquette $u(0)$ ;
- la courbe devient un cosinus, conforme au texte ;
- les axes du plan complexe sont désormais nommés $\Re$ et $\Im$, l'angle
  $\varphi_u$ est repéré, et une flèche indique le sens de rotation $\omega$.

La légende précise que le vecteur est dessiné à l'instant $t = 0$, et énonce
explicitement le point qui posait problème : c'est la longueur, et non la
hauteur, que l'on reporte en ordonnée.

Pagination inchangée à 691 pages. Le placement des flottants du chapitre 11
bouge de quelques lignes (la légende est plus longue) : la figure passe de la
page 177 à la page 178. Les 180 figures et les 1148 renvois numérotés du texte
sont identiques à ceux de la v1.5.

## v1.5 — 15 septembre 2026
Clôture du cycle de corrections ouvert en v1.4.1. Cette version ne contient
aucun contenu neuf : elle consolide la revue des 180 figures (lisibilité puis
justesse), le remaniement de l'index, et corrige un défaut de numérotation
qui touchait la majorité des exercices.

**Les exercices sont désormais numérotés automatiquement.** Les 250 énoncés
portaient un numéro écrit en dur dans le source. L'insertion des quatre
chapitres des versions v1.2 à v1.4 --- Instrumentation, LTspice, Oscillateurs,
Amplification de puissance --- a décalé les chapitres suivants sans toucher à
ces numéros. Le résultat :

- **201 exercices sur 250 portaient un numéro faux**, avec un décalage de 1, 2
  ou 4 selon leur position par rapport aux insertions. Le chapitre 32
  (Protocoles de communication) contenait des exercices numérotés 28.1 à 28.6 ;
  le chapitre 41, des exercices 37.x.
- **24 numéros étaient en double** : chaque chapitre ajouté avait pris les
  numéros que l'ancien chapitre conservait. Deux exercices différents
  s'appelaient « Exercice 20.3 », deux autres « Exercice 7.1 ».

Un compteur LaTeX lié au chapitre remplace la numérotation manuelle, et les
dix-sept renvois du texte et des légendes de figures deviennent symboliques
(`\ref`). Le problème ne peut plus se reproduire : insérer un chapitre
renumérote tout automatiquement, et un renvoi cassé devient visible à la
compilation au lieu de passer inaperçu.

Aucun énoncé, aucune solution, aucune figure n'a été modifié --- seuls les
numéros changent. Pagination inchangée à 691 pages ; 180 figures et 1623
références croisées inchangées.

## v1.4.4 — 15 septembre 2026
Fin de la passe de justesse : les 110 figures restantes (chapitres 1 à 16 et
22 à 34). Avec les 70 déjà relues en v1.4.2 et v1.4.3, les 180 figures du
livre ont maintenant été vérifiées pour ce qu'elles affirment, et non
seulement pour leur lisibilité.

Cent six sont justes. Beaucoup le sont au calcul près : les $-3$~dB du
passe-bande (13.4) tombent exactement aux fréquences qui donnent
$\Delta f = f_0/Q$ ; le maximum de dissipation de la classe B (23.1) vaut
$0{,}405$, soit très précisément la puissance utile au même point ; les
échantillons du repliement (31.1) valent identiquement ceux de l'alias ; la
dichotomie du SAR (31.3) converge bien sur 10100 ; l'arbitrage CAN (32.4)
diverge au septième bit comme annoncé ; le détecteur de séquence « 101 »
(27.1) gère correctement les recouvrements ; les marges de bruit CMOS (24.4)
sont exactes.

Quatre corrections :
- **25.1** — dans le verrou SR à portes NOR croisées, $S$ et $R$ étaient
  intervertis. Avec le câblage tracé, $Q = \mathrm{NOR}(S, \overline{Q})$ :
  poser $S = 1$ donnait $Q = 0$. Le « Set » remettait à zéro et le « Reset »
  mettait à un. Les sorties étaient bien nommées --- le texte les décrit
  correctement --- donc ce sont les entrées qui ont été échangées.
- **10.2** — deux des trois réponses à l'échelon quittaient l'origine avec une
  pente non nulle. La tension aux bornes du condensateur d'un RLC part
  toujours à pente nulle, puisque le courant de bobine est nul à l'instant
  initial. Les deux expressions sont remplacées par les vraies solutions du
  second ordre.
- **12.1** — la valeur moyenne $P$ était tracée à $0{,}61$ quand la moyenne de
  la courbe dessinée vaut $0{,}728$. La figure voisine 4.3, construite sur le
  même principe, était juste.
- **7.2** — le générateur de Thévenin avait son $+$ du côté de la masse et son
  $-$ du côté de la sortie : il délivrait une tension négative.

Un point reste ouvert, et relève d'un choix de convention plutôt que d'une
erreur : la figure 11.1 trace le phaseur tournant projeté
sur l'axe vertical, c'est-à-dire un sinus, alors que le texte qui la précède
immédiatement pose $u(t) = \hat{U}\cos(\omega t + \varphi) =
\Re[\underline{U}e^{j\omega t}]$. Rendre la figure cohérente avec la
convention $\Re$ suppose de dérouler le temps vers le bas plutôt que vers la
droite : c'est une décision de mise en page qui appartient à l'auteur.

Pagination inchangée à 691 pages.

## v1.4.3 — 14 septembre 2026
Suite de la passe de justesse : chapitres 20--21 (AOP, filtres actifs),
35--38 (découpage, magnétiques, asservissement, PID) et 39--41 (CEM, PCB,
intégrité du signal). Quarante et une figures relues pour ce qu'elles
affirment.

Trente-sept sont justes, et plusieurs le sont au calcul près : le maximum de
la cloche de rendement (36.2) tombe exactement là où les pertes fer égalent
les pertes cuivre ; le lieu des racines (38.2) a son point de fusion en
$-0{,}845$, sa traversée de l'axe en $\omega = \sqrt{8}$ et son
$K_{\text{crit}} = 48$, et les trois pôles marqués pour $K = 10$ sont les
racines exactes ; le diagramme des rebonds (41.2) enchaîne ses cinq tensions
sans une erreur ; le Bode de l'AOP (20.5) vérifie $GBW = A_{OL}\,f_{p1}$ et
$f_{-3\text{dB}} = GBW/A_{CL}$ ; la self de mode commun (39.4) a ses points de
polarité du bon côté.

Deux erreurs de fond :
- **20.2** — le fil de contre-réaction traversait le corps de l'AOP et croisait
  le fil de l'entrée non-inverseuse. À la lecture, le retour semblait aboutir
  sur le « + » : un comparateur, pas un amplificateur. Le montage est
  redessiné, $R_2$ passant par le dessus.
- **36.4** — les deux asymptotes de gain étaient tracées une fois et demie trop
  raides ($-60$ et $-30$ au lieu de $-40$ et $-\SI{20}{\decibel\per\dec}$), et
  le point de croisement annoncé à \SI{50}{kHz} était posé \SI{15}{dB} au-dessus
  de la courbe. Les pentes exactes ramènent le croisement précisément sur
  \SI{50}{kHz} : l'intention était juste, seul le tracé était faux.

Deux retouches mineures : la légende de la figure 20.1 annonçait
« $\pm V_{CC}$ » quand le schéma porte $-V_{EE}$ ; l'étiquette $-A_{\max}$ de
la figure 21.1 ne s'alignait pas sur la ligne qu'elle nomme.

Pagination inchangée à 691 pages.

## v1.4.2 — 14 septembre 2026
Passe de justesse sur les figures, chapitres 17 à 19 (diode, BJT, MOSFET) :
29 figures relues non plus pour leur lisibilité mais pour ce qu'elles
affirment. Valeurs numériques, sens des flèches, polarités, cohérence entre
ce que la figure montre et ce que le texte en dit.

Vingt-six sont justes, y compris les plus exposées : le pont de Graetz
(cathode commune en haut, anode commune en bas, les deux diagonales
conduisent), le régulateur Zener (cathode vers le +, KCL au nœud A), le
miroir de courant, l'inverseur CMOS, les deux modèles petit signal. Le réseau
$I_C(V_{CE})$ de la figure 18.4 est cohérent au calcul près : $\beta = 100$ sur
les quatre courbes, droite de charge à $V_{CC} = \SI{10}{V}$ et
$R_C = \SI{1}{k\ohm}$, point de repos exactement à l'intersection.

Trois corrections :
- **17.2** — l'échelle de l'axe plaçait $V_F$ à \SI{1}{V} : la graduation
  « 0,5 » tombait à mi-chemin de $V_F$. Le tableau de la page précédente donne
  \SI{0.7}{V} pour le silicium. Un lecteur qui mesure sur le graphe lisait le
  contraire de ce que dit le texte. La graduation est remise à sa place.
- **17.5** — la flèche du courant était portée par le fil de retour et pointait
  dans le sens inverse de ce retour ; la boucle, de surcroît, ne contenait
  aucune source : le dessin était un court-circuit avec des étiquettes $+$ et
  $-$ posées dessus. La pile est maintenant dessinée, et le courant porté là
  où son sens est univoque : à travers la jonction, de P vers N.
- **17.9** — la valeur moyenne était tracée à 0,69 fois la crête, au-dessus
  du $2/\pi = 0{,}637$ d'un redressement double alternance *idéal* : une
  valeur inatteignable, a fortiori avec la chute des diodes. Elle est ramenée
  à sa valeur exacte, 0,59 fois la crête.

Pagination inchangée à 691 pages.

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
