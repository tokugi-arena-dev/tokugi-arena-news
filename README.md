# TOKUGI ARENA News

Public, bilingual announcement data for TOKUGI ARENA. This repository does not contain game source code, player data, Steam keys or authentication credentials.

The game reads `news.json` over HTTPS. Updating this file does not require a new game build.

## Updating announcements

- Keep `schema_version` at `1`.
- Each article needs a unique lowercase `id`, positive integer `revision`, ISO date `YYYY-MM-DD`, and English title/body. Japanese text is supported alongside English.
- Increase `revision` when changing an existing announcement so players can see it as unread again.
- Text is plain text; use `\n` for line breaks. HTML and scripts are not interpreted.
- `url` is optional and must use HTTPS. External links only open when a player clicks the clearly labelled button.
- Maximum: 32 articles, 128 KiB total. To withdraw all announcements, use an empty `articles` array.

お知らせ本文だけを更新するときは `news.json` を編集します。既存記事の更新時は `revision` も増やしてください。ゲーム本体や個人情報、認証情報はこのリポジトリに置かないでください。
