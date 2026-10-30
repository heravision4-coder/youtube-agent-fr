---
name: yt-script
description: >-
  Écrire le script d'une vidéo YouTube à partir d'une idée brute - des accroches
  tirées de 21 formules et notées, puis le script parlé complet avec les temps
  forts de rétention marqués. À utiliser dès que l'utilisateur veut un script, une
  accroche, une phrase d'ouverture, « qu'est-ce que je dis », « écris ma prochaine
  vidéo », "write my next video", ou s'apprête à tourner sans avoir ses quinze
  premières secondes.
---

# yt-script

Une idée transformée en script que les gens regardent jusqu'au bout.

Deux outils vivent dans ce dossier et ils fonctionnent tous les deux. Utilise-les. N'évalue pas
l'accroche à l'œil.

```bash
python3 hookscore.py hooks.txt              # classer tes accroches
python3 hookscore.py --hook "une phrase"    # noter une seule accroche
```

Réponds toujours en français, sauf si l'utilisateur demande une autre langue. Les outils Python
affichent leurs résultats en anglais : traduis-les quand tu les présentes.

Attention : `hookscore.py` et `hooks.json` reconnaissent des tournures anglaises. Une accroche en
français risque d'être sous-notée (surtout CURIOSITY, ADDRESS et le nom de la formule). Note aussi
une traduction anglaise fidèle de chaque accroche, et présente les deux scores en disant lequel
est le plus fiable.

## Avant d'écrire

1. Lis `~/.claude/youtube/voice.md` s'il existe. C'est le profil de voix de l'utilisateur : sa façon
   de parler face caméra, les mots qu'il n'emploie jamais, à qui il s'adresse, ce qu'il refuse
   d'affirmer. S'il n'existe pas, demande **trois de ses propres vidéos**, lis-les ou transcris-les,
   déduis-en sa voix et écris le fichier. Un script dans la mauvaise voix est pire que pas de
   script, parce qu'il faut le lire à voix haute.
2. N'invente jamais un chiffre, un résultat ou une source. Si un chiffre renforcerait le propos et
   que tu ne l'as pas, demande-le ou écris la phrase sans lui.

## La structure

**Les 15 premières secondes, c'est tout le travail.** Elles font trois choses, sinon la vidéo fuit :
confirmer le clic que le titre a promis, ouvrir une question que le spectateur ne peut pas refermer,
et prouver que la récompense existe.

1. **L'accroche.** Écris-en CINQ à partir des [21 formules](hooks.json), passe-les dans
   `hookscore.py`, garde les deux meilleures et montre-les toutes les deux à l'utilisateur avec
   leurs scores. Ne rends jamais une seule accroche.
2. **Le virage** (0:15-0:45). Dis ce que la vidéo va faire, en une phrase, et commence à le faire.
   Pas d'intro de chaîne, pas de « avant de commencer », pas d'appel à s'abonner. C'est la première
   cause de la chute à 0:30.
3. **Le corps.** Une idée par temps. Indique pour chaque temps ce qui est À L'ÉCRAN, pas seulement
   ce qui est dit : une tête qui parle sans rien à regarder, c'est un podcast.
4. **La récompense.** Livre ce que l'accroche a promis, explicitement, et dis que tu le livres :
   « voilà le prompt, il est dans la description ».
5. **La conclusion.** Une seule demande. Pas trois.

## Ce qu'il faut rendre

- les deux meilleures accroches avec leurs tableaux de scores
- le script, temps par temps, avec `[À L'ÉCRAN : ...]` sur chaque temps
- la durée estimée à 150 mots par minute (le français parlé est plutôt autour de 150-170)
- une ligne qui nomme la formule utilisée par l'accroche gagnante et pourquoi elle convient à
  cette idée

## Le garde-fou

Rien ici n'est publié. Ce skill écrit, l'utilisateur publie. Chaque réponse se termine par un bloc
que l'utilisateur copie, et la dernière ligne de chaque passage est la question :
**on publie, ou on change ?**
