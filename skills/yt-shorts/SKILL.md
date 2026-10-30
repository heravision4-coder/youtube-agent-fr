---
name: yt-shorts
description: >-
  Trouver les Shorts cachés dans une vidéo longue et les écrire, en s'appuyant sur
  la transcription pour choisir des moments autonomes. À utiliser pour « découpe ça
  en shorts », « fais des extraits », « recycle cette vidéo », « qu'est-ce que je
  coupe », "cut this into shorts".
---

# yt-shorts

Un Short tiré d'une vidéo longue n'est pas un extrait du meilleur moment. C'est un moment qui
**tient debout sans la vidéo autour**, ce qui est un ensemble bien plus petit.

Réponds toujours en français, sauf si l'utilisateur demande une autre langue. Les outils Python
affichent leurs résultats en anglais : traduis-les quand tu les présentes.

## Choisir

Lis la transcription et trouve des passages de 20 à 55 secondes où les trois conditions sont
vraies :

1. Il commence sur une pensée complète. Si la première phrase a besoin de la minute précédente, ce
   n'est pas un Short.
2. Il contient un virage : une affirmation, puis quelque chose qui la complique ou la prouve.
3. Il se termine sur une vraie phrase, pas sur une phrase qui s'éteint.

Classe les candidats et montre à l'utilisateur les cinq meilleurs avec leurs timecodes et leur
première phrase, pour qu'il puisse en écarter un sans lire toute la transcription.

## Écrire chacun

- **Une NOUVELLE première phrase.** Celle de la vidéo longue suppose un contexte que ce spectateur
  n'a pas. Écris la remplaçante et passe-la dans `../yt-script/hookscore.py` (voir l'avertissement
  sur le français dans `yt-script`).
- **Un texte à l'écran pour les deux premières secondes**, avec des mots différents de la phrase
  parlée.
- **Un point de boucle** : ce que la dernière phrase prépare pour que la première y réponde.
- Une note de cadrage vertical : ce qui est coupé d'une image 16:9 et si ça compte.

## Le garde-fou

Rien ici n'est publié. Ce skill écrit, l'utilisateur publie. Chaque réponse se termine par un bloc
que l'utilisateur copie, et la dernière ligne de chaque passage est la question :
**on publie, ou on change ?**
