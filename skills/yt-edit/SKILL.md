---
name: yt-edit
description: >-
  Transformer la transcription d'un enregistrement brut en liste de coupes - blancs,
  tics de langage et reprises, avec les timecodes. À utiliser pour « monte ça »,
  « coupe les blancs », « resserre cette vidéo », « j'ai trop parlé », "edit this",
  ou toute demande de raccourcir des rushes à partir d'une transcription.
---

# yt-edit

Une liste de coupes à partir d'une transcription horodatée. L'outil affiche les coupes.
L'utilisateur les applique.

```bash
python3 deadair.py transcript.srt              # srt, vtt ou json whisper
python3 deadair.py transcript.srt --floor 0.35 --json
```

Pas encore de transcription ? Demande-en une, ou produis-la d'abord : `whisper`, `faster-whisper`,
ou les sous-titres que YouTube génère sur une vidéo non répertoriée fonctionnent tous. Ne devine
jamais les timings.

Réponds toujours en français, sauf si l'utilisateur demande une autre langue. Les outils Python
affichent leurs résultats en anglais : traduis-les quand tu les présentes.

Attention : la détection des tics de langage (FILLER) repose sur des mots anglais (« um », « so
yeah », « basically »). Sur une vidéo en français, elle rate « euh », « du coup », « en fait » :
repère-les toi-même dans la transcription et ajoute-les à la liste.

## Ce que l'outil trouve

- **DEAD** - les silences plus longs que le seuil, coupés au MILIEU pour garder une respiration de
  chaque côté. Couper au ras de la parole, c'est ce qui donne à une prise resserrée un air essoufflé.
- **FILLER** - les segments qui ne contiennent qu'un tic de langage.
- **REPEAT** - une phrase recommencée. Comparée au dernier segment réellement parlé, pas au segment
  précédent littéral, parce que la plupart des reprises ont un « euh » entre les deux essais.

## Ce que l'outil ne fera pas

Il ne touche pas aux médias. Il n'a aucun avis sur les plans de coupe. Une coupe de 40 % dans le
rapport, c'est 40 % de la PAROLE : si la vidéo contient une longue démo silencieuse, ce chiffre est
faux. Compare le rapport aux images avant de te fier à la durée affichée en bas.

## Le garde-fou

Rien ici n'est publié. Ce skill écrit, l'utilisateur publie. Chaque réponse se termine par un bloc
que l'utilisateur copie, et la dernière ligne de chaque passage est la question :
**on publie, ou on change ?**
