---
name: yt-plan
description: >-
  Planifier une semaine ou un mois de vidéos YouTube - quoi publier, quand et dans
  quel ordre, à la mesure du temps réel du créateur. À utiliser pour « planifie ma
  semaine », « calendrier de contenu », « qu'est-ce que je publie », « je ne sais
  pas quoi faire ensuite », "plan my week".
---

# yt-plan

Un planning qui ne tient pas dans la semaine est une liste de regrets. Pose deux questions avant
d'écrire quoi que ce soit : **combien d'heures as-tu vraiment**, et **qu'est-ce qui est déjà à
moitié fait**.

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

## La forme d'une semaine

- **Une vidéo phare.** La vidéo pour laquelle la semaine existe. Elle reçoit le plus de temps et
  sort le jour que les statistiques de la chaîne désignent comme le meilleur : demande-le, ne
  suppose pas que c'est le mardi.
- **Une vidéo légère.** Construite à partir de quelque chose qui existe : un extrait, une réaction,
  une suite au commentaire qui a reçu le plus de réponses la semaine dernière.
- **Des Shorts tirés de la vidéo phare.** Trois, découpés dans la vidéo longue, pas écrits à part.
  `/yt-shorts` les trouve.

Trois publications sur une semaine de sept jours, pas sept. Un planning qui publie tous les jours
n'est pas un planning que quiconque reconnaît, et ce sont les jours vides qui permettent aux jours
pleins de survivre à une mauvaise semaine.

## Ce qu'il faut rendre

Un tableau : jour, format, titre provisoire, la phrase qu'il promet, et ce qui existe déjà pour lui.
Puis la ligne honnête en bas : combien d'heures ça coûte, et quoi abandonner en premier si la
semaine tourne mal.

## Le garde-fou

Rien ici n'est publié. Ce skill écrit, l'utilisateur publie. Chaque réponse se termine par un bloc
que l'utilisateur copie, et la dernière ligne de chaque passage est la question :
**on publie, ou on change ?**
