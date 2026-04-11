# WIP claude vs copilot equivalents

- How do I see my session ID?
    - /status
    - /session is not a claude command.

- How to I name a session?
    - /rename

- How do I resume a session?
    - /resume, then pick the session
    - claude --resume "os161.v1"
    - If, in a given directory, you have had an non-empty session, `claude
      --continue` resumes the session based on the starting directory. This can
      be confirmed by the session name appearing in the upper right corner of
      the prompt line in case you have named the session.



## H MCP server?

- claude:
    - `! claude mcp --help`
    - `! claude mcp add` installs
    - `! claude mcp remove` uninstalls
    - `/mcp`  opens installed mcps, can disable or reconnect

- copilot:
    - `/mcp [show|add|edit|delete|disable|enable ... Manage MCP server configuration`

## Updating the CLI

- claude `! claude update`
- copilot: `/update`




## Where is the CLI documentation, the stuff you see in `claude --help`?



## Where is the official vetted list of MCP Servers?


# How do I login?


- claude:
    - /login
    - ! claude auth login

- copilot:
    - /login
    - claude login


# FOO

LSP requires plugin + binary per language

parallel work, use git worktree , claude —worktree


—resume <NOTHING> != —continue

message history != context, entire message history is saved

session scoped permissions always need to be re-approved.

 claude mcp add gitnexus -- gitnexus mcp // the stuff after — is NOT a comment, is an arg. like git difftool — foo.c

claude —resume “os161.v1” —fork-session // when you want to try a different approach without affecting the original session.

like —resume, fork session don’t inherit permissions, you must re-approve them.

DONT start same session in 2 terminals - Nothing corrupts, but the conversation becomes jumbled. - For parallel work from the same starting point, use --fork-session


<https://code.claude.com/docs/en/statusline.md>


/compact with a focus (like /compact focus on the API changes

## CLAUDE.md details

<https://code.claude.com/docs/en/memory>

## claude does NOT read AGENTS.md files

<https://code.claude.com/docs/en/memory#agents-md>


## SKILL.md

<https://code.claude.com/docs/en/skills#frontmatter-reference>

On why it's called `SKILL.md`: It's a convention from the that Claude Code
adopted. The idea is that the filename is always `SKILL.md` and the *directory
name* carries the semantic meaning (`conventional-commits/SKILL.md`,
`security-review/SKILL.md`, etc.).

This way:

- Tooling can discover skills by scanning for `SKILL.md` files without knowing
  domain-specific filenames

- The skill is portable/shareable — you can drop the whole `conventional-commits/` folder into any project's `.claude/skills/` and it just works

- It mirrors how `CLAUDE.md` is always named `CLAUDE.md` regardless of what's in it

## Stay safe with checkpoints and permissions

- Sheckpoints:
    - Session scoped file edit undoing, git not required, but is session scoped and only aplies to file changes.
    - 2x tap <ESC> , or /undo

- Permissions:
    - Control what claude can do without asking.
    - <SHIFT> + <TAB> to cycle permission modes.
        - Default: ask for file edits and commands.
        - Auto-edit: Ask only for commands.
        - Plan: read only mode. Create a plan.
        - Auto: not available yet, research preview.
    - Allow specific commands in settings.json, see: https://code.claude.com/docs/en/permissions

## Work effectively with Claude Code