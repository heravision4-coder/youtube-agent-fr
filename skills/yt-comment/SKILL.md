---
name: yt-comment
description: >-
  Rédiger des réponses aux commentaires YouTube dans la voix du créateur, triées
  selon celles qui méritent une réponse. À utiliser pour « réponds à mes
  commentaires », « gère la section commentaires », « quelqu'un a demandé X »,
  "reply to my comments", ou un fil de commentaires collé.
---

# yt-comment

La section commentaires est une surface de rétention, pas une corvée. Ce sont les réponses des
premières heures qui décident si un fil devient une conversation que d'autres lisent.

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

## Trier d'abord, toujours

Range ce que colle l'utilisateur en quatre piles et dis combien il y en a dans chacune avant
d'écrire quoi que ce soit :

1. **Questions** - réponds-y. Ce sont les sujets de la prochaine vidéo, alors note celles qui
   reviennent.
2. **Corrections** - s'ils ont raison, dis-le simplement et remercie-les. Ne conteste jamais un
   fait que tu ne peux pas vérifier.
3. **Compliments** - réponds à quelques-uns, brièvement, avec un détail précis tiré de leur
   commentaire. Un mur de « merci ! » identiques a l'air automatique, parce qu'il l'est.
4. **Provocations** - ne réponds pas. Dis-le et passe à la suite. N'écris jamais de répartie, même
   méritée.

## Écrire la réponse

- Moins de 30 mots. Une longue réponse dans un fil, c'est un article de blog que personne n'a
  demandé.
- Réponds à la vraie question dès la première phrase.
- Une question en retour, seulement si elle est sincère.
- Pas d'emoji, sauf si l'utilisateur en met dans ses propres réponses. Vérifie son fichier de voix.
- Ne promets jamais une vidéo qu'il n'a pas accepté de faire.

## Le cœur et l'épingle

Dis quel commentaire épingler, UN seul, et pourquoi. Épingle la question que le plus de gens se
posent aussi, pas le commentaire le plus gentil. Mets des cœurs généreusement : ça ne coûte rien et
ça se voit.

## Le garde-fou

Rien ici n'est publié. Ce skill écrit, l'utilisateur publie. Chaque réponse se termine par un bloc
que l'utilisateur copie, et la dernière ligne de chaque passage est la question :
**on publie, ou on change ?**
