---
name: yt-retention
description: >-
  Lire un export de rétention d'audience de YouTube Studio, trouver où les
  spectateurs partent vraiment, puis dire quoi changer. À utiliser pour « pourquoi
  les gens arrêtent de regarder », « ma rétention est mauvaise », un graphique ou un
  CSV de rétention collé, « corrige mon rythme », "my retention is bad".
---

# yt-retention

Le graphique de rétention est le seul retour honnête que YouTube te donne. Presque personne ne
l'exporte.

```bash
python3 retention.py retention.csv --duration 600
python3 retention.py retention.csv --transcript transcript.srt
```

Récupérer le fichier : Studio -> une vidéo -> Statistiques -> Engagement -> le graphique de
rétention d'audience -> l'icône de téléchargement -> « Rétention d'audience ».

Réponds toujours en français, sauf si l'utilisateur demande une autre langue. Les outils Python
affichent leurs résultats en anglais : traduis-les quand tu les présentes.

## Trois problèmes différents

- **HOOK LEAK (fuite d'accroche)** - ce qui est perdu dans les 30 premières secondes. Moins de 25 %,
  c'est sain. C'est toujours la première chose à corriger, et c'est toujours le script des quinze
  premières secondes, jamais le montage.
- **CLIFFS (falaises)** - des chutes brutales et isolées. Une falaise, c'est un moment : un
  changement de sujet non annoncé, un placement de sponsor, une longue mise en place. Avec
  `--transcript`, l'outil affiche ce qui était dit à cet instant, et c'est ce qui rend le rapport
  utile plutôt que simplement intéressant.
- **SLIDE (glissement)** - la perte régulière au milieu. Un glissement plat, c'est le rythme. La
  solution est de couper, pas de réécrire.

## Ce qu'il faut rendre

Nomme la plus grosse fuite et un seul changement pour elle. Pas une liste de cinq. Ensuite,
seulement si on te le demande, le reste. Et si la fuite d'accroche est saine et le glissement plat,
dis que la vidéo va bien et que le problème est le packaging : envoie l'utilisateur vers
`/yt-package`.

## Le garde-fou

Rien ici n'est publié. Ce skill écrit, l'utilisateur publie. Chaque réponse se termine par un bloc
que l'utilisateur copie, et la dernière ligne de chaque passage est la question :
**on publie, ou on change ?**
