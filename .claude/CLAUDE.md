# telegram_bot

This project is a reference workspace for running Claude Code with a Telegram channel plugin, allowing Claude to receive and respond to messages via a personal Telegram bot.

## Project Purpose

Use Claude Code interactively from Telegram — send prompts from your phone, get replies back in chat.

## Key Files

- `README.md` — full setup guide (bot creation, plugin install, token config, pairing)
- `channel-questions.md` — Q&A on channel behavior (exit, multiple sessions, access policy)
- `claude-questions.md` — Q&A on Claude Code session commands (status, rename, resume)

## Starting the Channel

```bash
claude --channels plugin:telegram@claude-plugins-official
```

Access config is saved at `~/.claude/channels/telegram/access.json` — no re-pairing needed after restart.

## Gitignored

- `.claude/settings.local.json` — machine-specific permission grants; do not commit
