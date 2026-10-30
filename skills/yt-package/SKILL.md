---
name: yt-package
description: >-
  Écrire et vérifier le titre et la miniature d'une vidéo YouTube comme un seul
  ensemble, en contrôlant la troncature, les répétitions et le flou avant
  publication. À utiliser pour « idées de titre », « comment j'appelle ça », « texte
  de miniature », « mon CTR est mauvais », "title ideas", le packaging, ou toute
  demande de renommer ou de repackager une vidéo existante.
---

# yt-package

Le titre et la miniature forment UN ensemble. Les écrire séparément, c'est la raison pour laquelle
la plupart des packagings échouent : la miniature répète le titre, et la moitié de la surface de
clic dit deux fois la même chose.

```bash
python3 title.py --title "..." --thumb "L'IA A TOUT FAIT"
python3 title.py titles.txt            # un par ligne, classés
```

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

## Les règles que l'outil applique, et pourquoi

- **60 caractères**, c'est là que la recherche sur ordinateur coupe ; **40**, c'est le fil
  d'accueil sur mobile. Les deux sont signalés parce qu'ils échouent différemment : une coupe sur
  ordinateur perd la fin, une coupe sur mobile peut perdre le sujet.
- **La miniature ne doit pas répéter le titre.** Des mots différents, la même promesse.
- **Trois mots maximum sur la miniature.** À la taille du fil, un quatrième mot devient une tache
  grise.
- **Un chiffre, un nom ou une date** bat tous les adjectifs disponibles.
- **Deux mots en majuscules, c'est le plafond** avant qu'un titre ressemble à du spam.

Les titres français sont souvent plus longs que leurs équivalents anglais : surveille de près les
limites de 40 et 60 caractères.

## En écrire dix, en garder deux

Génère dix titres, passe-les tous dans `title.py`, montre à l'utilisateur les trois meilleurs avec
leurs scores et le problème précis de chacun. Pour le gagnant, écris le brief de miniature :
l'expression, le cadrage, les trois mots, et ce que le fond doit faire pour garder le contraste à
la taille du fil.

## Le garde-fou

Rien ici n'est publié. Ce skill écrit, l'utilisateur publie. Chaque réponse se termine par un bloc
que l'utilisateur copie, et la dernière ligne de chaque passage est la question :
**on publie, ou on change ?**
