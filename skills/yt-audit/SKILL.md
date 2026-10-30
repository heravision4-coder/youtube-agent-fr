---
name: yt-audit
description: >-
  Auditer une chaîne YouTube de bout en bout - packaging, régularité, les quinze
  premières secondes, et ce qu'il faut corriger en premier. À utiliser pour « audite
  ma chaîne », « pourquoi ma chaîne ne grandit pas », « analyse mes vidéos », "audit my
  channel", ou une URL de chaîne collée.
---

# yt-audit

Un audit qui liste vingt problèmes est une façon d'éviter celui qui compte. Celui-ci se termine
sur UNE seule correction.

Réponds toujours en français, sauf si l'utilisateur demande une autre langue. Les outils Python
affichent leurs résultats en anglais : traduis-les quand tu les présentes.

## Avant d'écrire

1. Lis `~/.claude/youtube/voice.md` s'il existe. C'est le profil de voix de l'utilisateur : sa façon
   de parler face caméra, les mots qu'il n'emploie jamais, à qui il s'adresse, ce qu'il refuse
   d'affirmer. S'il n'existe pas, demande **trois de ses propres vidéos**, lis-les ou transcris-les,
   déduis-en sa voix et écris le fichier. Un script dans la mauvaise voix est pire que pas de
   script, parce qu'il faut le lire à voix haute.
2. N'invente jamais un chiffre, un résultat ou une source. Si un chiffre renforcerait le propos et
   que tu ne l'as pas, demande-le ou écris la phrase sans lui.

## Quoi regarder, dans cet ordre

1. **Les dix derniers titres, comme un ensemble.** Lis-les en liste, comme les montre la page de la
   chaîne. Promettent-ils des choses différentes ? Passe-les dans `../yt-package/title.py`. Une
   chaîne dont tous les titres ont la même forme a un problème de format, pas de titre.
2. **Les miniatures, à la taille du fil.** Réduis-les. Qu'est-ce qui reste lisible ? Si trois sont
   illisibles à cette taille, c'est ça la correction et rien d'autre ne compte encore.
3. **Les quinze premières secondes des trois vidéos les plus récentes.** Transcris-les et note-les
   avec `../yt-script/hookscore.py`. C'est là que la plupart des chaînes perdent.
4. **Le rythme de publication.** Pas la fréquence : la RÉGULARITÉ. Six vidéos en une semaine puis
   rien pendant un mois, c'est pire qu'une tous les quinze jours pour toujours.
5. **La forme de la rétention**, s'ils peuvent l'exporter. `/yt-retention`.

## Ce qu'il faut rendre

- La correction la plus importante, nommée, avec ce qu'il faut faire cette semaine.
- Trois choses qui marchent déjà, pour qu'ils ne les cassent pas. Sois précis : « ton énergie est
  bonne » n'est pas une observation.
- Ce qu'il ne faut PAS faire tout de suite, et pourquoi.

N'ouvre jamais un audit par des compliments que tu ne penses pas, et ne le termine jamais par une
liste de vingt choses.

## Le garde-fou

Rien ici n'est publié. Ce skill écrit, l'utilisateur publie. Chaque réponse se termine par un bloc
que l'utilisateur copie, et la dernière ligne de chaque passage est la question :
**on publie, ou on change ?**
