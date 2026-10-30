---
name: yt-chapters
description: >-
  Écrire les chapitres d'une vidéo YouTube à partir d'une transcription, validés
  selon les règles de YouTube pour qu'ils s'affichent vraiment. À utiliser pour
  « ajoute des chapitres », « horodatages », « découpe cette vidéo en sections »,
  "add chapters", "timestamps".
---

# yt-chapters

```bash
python3 chapters.py transcript.srt --target 8
```

Réponds toujours en français, sauf si l'utilisateur demande une autre langue. Les outils Python
affichent leurs résultats en anglais : traduis-les quand tu les présentes.

## Les règles, qui ne sont pas optionnelles

Une liste de chapitres qui enfreint l'une d'elles ne devient pas des chapitres, sans aucun
avertissement : le bloc reste dans la description sans rien faire.

- La première entrée doit être **00:00**.
- Il en faut **au moins trois**.
- Chacun doit durer **au moins 10 secondes**.

L'outil vérifie les trois et signale une liste invalide au lieu de te laisser la coller.

## Renomme chaque ligne

`chapters.py` trouve bien les LIMITES : il note les pauses réellement marquées selon le changement
de vocabulaire de part et d'autre. Les titres qu'il produit sont les mots du sujet, et ce n'est
qu'un brouillon. Un chapitre appelé « Thumbnails Titles Packaging » est un bouche-trou. Réécris
chacun comme la promesse de sa section, dans la voix de l'utilisateur, en trois à cinq mots.

Les chapitres servent aussi de diagnostic de rétention : si une section ne peut pas être nommée en
cinq mots, c'est deux sections, ou c'est du remplissage.

## Le garde-fou

Rien ici n'est publié. Ce skill écrit, l'utilisateur publie. Chaque réponse se termine par un bloc
que l'utilisateur copie, et la dernière ligne de chaque passage est la question :
**on publie, ou on change ?**
