# Core Concepts

## How Claude Code Works - <https://code.claude.com/docs/en/how-claude-code-works>

- LSP requires plugin + binary per language.

- For parallel work, use git worktree , `! claude --worktree`

- `--resume <NOTHING>` != `--continue`

    - `--resume <NOTHING>` // Opens the session picker at startup.

    - `--continue` resumes the most recent conversation in the current
      directory, fails with "No conversation found to continue" if you never
      started a non-empty session with claude in that current directory.

- message history != context, entire message history is saved.

- session scoped permissions always need to be re-approved.

- `claude mcp add gitnexus -- gitnexus mcp` // The stuff after — is NOT a
  comment, it's an argument. Like `git difftool -- foo.c`

- `claude --resume “os161.v1” --fork-session` // When you want to try a
  different approach without affecting the original session.

- Like `--resume`, `--fork-session` does not inherit permissions, you must
  re-approve them.

- DON'T start same session in 2 terminals - Nothing corrupts, but the
  conversation becomes jumbled. - For parallel work from the same starting
  point, use `--fork-session`.

- <https://code.claude.com/docs/en/statusline.md>

- `/compact` with a focus e.g. `/compact focus on the API changes`

## CLAUDE.md details

- <https://code.claude.com/docs/en/memory>

## claude does NOT read AGENTS.md files, use @ imports from CLAUDE.md

- <https://code.claude.com/docs/en/memory#agents-md>


## SKILL.md

- <https://code.claude.com/docs/en/skills#frontmatter-reference>

## Why it's called `SKILL.md`

- It's a convention that Claude Code adopted. The idea is that the
filename is always `SKILL.md` and the *directory name* carries the semantic
meaning (`conventional-commits/SKILL.md`, `security-review/SKILL.md`, etc.).

This way:

- Tooling can discover skills by scanning for `SKILL.md` files without knowing
  domain-specific filenames.

- The skill is portable/shareable — you can drop the whole
  `conventional-commits/` folder into any project's `.claude/skills/` and it
  just works.

- It mirrors how `CLAUDE.md` is always named `CLAUDE.md` regardless of what's in
  it.

## Stay safe with checkpoints and permissions

- Checkpoints:

    - Session scoped file edit undoing, git not required, but is session scoped
      and only aplies to file changes.

    - 2x tap \ESC , or `/undo`.

- Permissions:
    - Control what claude can do without asking.
    - \SHIFT + \TAB to cycle permission modes.
        - Default: ask for file edits and commands.
        - Auto-edit: Ask only for commands.
        - Plan: read only mode. Create a plan.
        - Auto: not available yet, research preview.
    - Allow specific commands in settings.json, see: <https://code.claude.com/docs/en/permissions>

## Work effectively with Claude Code


### Ask

- `/init` // Create CLAUDE.md for a project

- `/agents` // Browse or create agents, some agents are "built-in" = always available.

- `/doctor` // Diagnose problems with your claude installation.


### It's a conv

- Use natural language.

- Iterate.

- Interupt and steer, type + \ENTER at any time.

- Be specific upfront = less steering.

- Provide verification conditions, test case I/O examples. For visual work,
  paste screen shots, ask to compare.

- For complex, start with, exploration/research, use plan mode. Review and
  refine plans. Two phase approach is much better.

- Delegate using conversation like with a competent colleage.

## Explore the Context Window <https://code.claude.com/docs/en/context-window>

