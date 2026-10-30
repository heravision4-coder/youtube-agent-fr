# Agent YouTube en français

Version française des skills Claude Code de [Jakeschincariol/youtube-agent-skill](https://github.com/Jakeschincariol/youtube-agent-skill)
(licence MIT, voir `LICENSE`), traduite depuis le commit `a2feb21`.

Les fichiers `SKILL.md` sont traduits et demandent à Claude de répondre en français. Les outils
Python et `hooks.json` sont inchangés : ils restent en anglais, et leurs scores sont moins fiables
sur du texte français (voir les avertissements dans `yt-script` et `yt-edit`).

## Installation

```bash
cp -r skills/yt-* ~/.claude/skills/
```

Commandes : `/yt-script`, `/yt-package`, `/yt-edit`, `/yt-retention`, `/yt-viral`, `/yt-seo`,
`/yt-shorts`, `/yt-chapters`, `/yt-comment`, `/yt-plan`, `/yt-audit`.
