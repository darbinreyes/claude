<<<<<<< Updated upstream
=======
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

## Jokes Already Told

Track jokes told via Telegram so they are not repeated.

<!-- Add one bullet per joke: - [brief description] -->
- programmers prefer dark mode (light attracts bugs)
- scarecrow won an award (outstanding in his field)
- photon at hotel (traveling light)
- atoms make up everything
- Schrödinger's cat walks into a bar (and doesn't)
- two atoms walking, one lost an electron (I'm positive!)
- neutron walks into a bar (no charge)
- Heisenberg speeding, cop asks speed (I know exactly where I am — Uncertainty Principle)
- Einstein developed a theory about space (and it was about time too)
- physicists at sporting events (the wave)
- physicist's favorite food (fission chips)
- reading a book about helium (couldn't put it down)
- hamburger less energy than steak (ground state)
- one magnetic field to the other (I find you very attractive)
- physics teacher broke up with biology teacher (no chemistry)
- Higgs boson walks into a church (without me, how do you have mass?)
- two neutrinos walk through a bar
- new theory on inertia (not gaining momentum)
- old physicists never die (just lose their momentum)
- quantum physicist crossed the road (to get to the other side... probably)

## Gitignored

- `.claude/settings.local.json` — machine-specific permission grants; do not commit
>>>>>>> Stashed changes
