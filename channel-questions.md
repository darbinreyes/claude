# Channel Q&A

## Does /exit stop Telegram responses?

Yes — `/exit` ends the Claude Code session, which shuts down the Telegram channel plugin. No more messages will be processed until you restart.

To re-enable, restart with the channels flag:

```bash
claude --channels plugin:telegram@claude-plugins-official
```

Your access config (`allowFrom`, `dmPolicy`) is already saved in `~/.claude/channels/telegram/access.json`, so no re-pairing needed — it picks up where it left off.

---

## What happens if you start more than one session with `--channels`?

Running two sessions simultaneously with the same bot token causes problems:

- Both sessions poll the same bot token via `getUpdates`
- Telegram delivers each incoming message to **only one** poller — whichever claims it first
- Messages are split unpredictably between the two sessions
- Both sessions could reply, potentially sending duplicate responses

The safe approach is **one session at a time** with channels enabled. Exit the current session before starting a new one.
