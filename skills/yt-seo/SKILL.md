---
name: yt-seo
description: >-
  Écrire la description, les tags et le texte orienté recherche d'une vidéo
  YouTube, visant la requête qu'une vraie personne tape. À utiliser pour « écris ma
  description », « tags », « SEO », « aide cette vidéo à être trouvée », « personne
  ne trouve ma vidéo », "write my description".
---

# yt-seo

La recherche est un levier plus petit que le packaging, et plus grand qu'on ne le croit pour les
vidéos intemporelles. Pour une vidéo destinée au fil des abonnés, dis-le et mets plutôt l'effort
sur `/yt-package`.

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

## La description

- **Les deux premières lignes sont les seules que tout le monde lit.** Elles s'affichent avant
  « ...plus » et servent d'extrait dans la recherche. Dis ce que la vidéo leur apporte, avec les
  mots qu'ils auraient tapés.
- Ensuite le lien ou la ressource, s'il y en a une, pour qu'elle soit visible sans dérouler.
- Ensuite les chapitres (`/yt-chapters` les écrit).
- Ensuite la version longue : ce qui est couvert, pour qui, ce que la vidéo suppose déjà connu.

## Les tags, honnêtement

Les tags sont un signal faible, et YouTube l'a dit. Sers-t'en pour lever les ambiguïtés :
orthographes, noms d'outils, abréviations que les gens tapent vraiment. Et arrête-toi là. Quinze,
c'est largement assez. Un mur de tags n'est pas une stratégie, et ajouter des tags sans rapport est
contraire aux conditions d'utilisation.

## Le test des requêtes

Avant de rendre quoi que ce soit, écris les trois requêtes de recherche que cette vidéo devrait
gagner, et vérifie que le titre et les deux premières lignes de la description contiennent les mots
de ces requêtes. Si ce n'est pas le cas, le problème vient du titre, pas de la description.

## Le garde-fou

Rien ici n'est publié. Ce skill écrit, l'utilisateur publie. Chaque réponse se termine par un bloc
que l'utilisateur copie, et la dernière ligne de chaque passage est la question :
**on publie, ou on change ?**
