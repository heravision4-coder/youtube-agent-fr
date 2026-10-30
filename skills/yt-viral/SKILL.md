---
name: yt-viral
description: >-
  Trouver ce qui marche vraiment dans la niche de l'utilisateur sur YouTube, le
  classer selon l'écart de chaque vidéo avec sa propre chaîne, puis nommer la
  formule. À utiliser pour « qu'est-ce qui marche en ce moment », « trouve des vidéos
  virales dans ma niche », « pourquoi ça a explosé », "what's working right now",
  l'analyse de concurrents, ou un fichier d'inspiration.
---

# yt-viral

Le nombre brut de vues classe la taille des chaînes, pas les idées. Cet outil classe selon le
**multiple par rapport à la médiane de chaque chaîne**, la seule version de la question qui parle
de la vidéo.

```bash
python3 swipe.py collected.json --min 2.0
```

Réponds toujours en français, sauf si l'utilisateur demande une autre langue. Les outils Python
affichent leurs résultats en anglais : traduis-les quand tu les présentes.

## Rassembler les données

Il faut au moins **quatre vidéos par chaîne**, sinon une médiane ne veut rien dire : l'outil ignore
la chaîne et le signale. Rassemble-les comme l'utilisateur préfère : `yt-dlp --flat-playlist -J`
sur l'URL d'une chaîne est le plus rapide, la page publique fonctionne, une liste manuelle aussi.

```json
[{"channel":"...","title":"...","views":412000,"url":"...","duration":613}]
```

**Lire, pas aspirer.** Uniquement des pages publiques, jamais une session connectée, jamais les
identifiants du compte de l'utilisateur.

## Lire le résultat

Le multiple est le signal. La ligne de formule est un jugement sur le TITRE, comparé aux
[21 formules](../yt-script/hooks.json) ; ce n'est pas une explication de pourquoi la vidéo a marché,
et tu dois le dire quand tu la présentes. Les formules sont en anglais : sur des titres français,
la correspondance est moins fiable, signale-le.

Ce qu'il faut rendre : les cinq meilleures avec leurs multiples, la formule de chacune, et LA chose
structurelle qu'elles partagent. Puis la phrase plus difficile : laquelle l'utilisateur pourrait
vraiment faire cette semaine, dans sa voix, avec ce qu'il a.

## Le garde-fou

Rien ici n'est publié. Ce skill écrit, l'utilisateur publie. Chaque réponse se termine par un bloc
que l'utilisateur copie, et la dernière ligne de chaque passage est la question :
**on publie, ou on change ?**
