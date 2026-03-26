# Telegram Channel Setup

Reference: https://code.claude.com/docs/en/channels#telegram

## Prerequisites

- [Bun](https://bun.sh) installed (`bun --version` to check)
- Claude Code v2.1.80 or later, authenticated with a claude.ai account

## Setup Steps

### 0. Create a Telegram bot

Open [BotFather](https://t.me/BotFather) in Telegram and send `/newbot`. Give it a display name and a username ending in `bot`. Copy the token it returns.

### 1. Install the plugin

```
/plugin install telegram@claude-plugins-official
```

If the plugin is not found, refresh the marketplace first:

```
/plugin marketplace update claude-plugins-official
```

Or add it if you haven't before:

```
/plugin marketplace add anthropics/claude-plugins-official
```

Then retry the install. After installing, run `/reload-plugins` to activate the configure command.

### 2. Configure your bot token

```
/telegram:configure <token>
```

Saves the token to `~/.claude/channels/telegram/.env`. Alternatively, set `TELEGRAM_BOT_TOKEN` in your shell environment before launching Claude Code.

### 3. Start Claude Code with the channel enabled

```bash
claude --channels plugin:telegram@claude-plugins-official
```

### 4. Pair your account

Send any message to your bot in Telegram — it replies with a pairing code. Then in Claude Code:

```
/telegram:access pair <code>
```

Lock down access so only your account can send messages:

```
/telegram:access policy allowlist
```
