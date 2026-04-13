# claude vs copilot equivalents

## How do I see my session ID?

- claude:
    - `/status`
        - \TAB to cycle between: status, config (=settings),
        usage (e.g. current session), stats (e.g. all time tokens)

- copilot:
    - `/session info` is not a claude slash command.
        - sub-commands `[info| checkpoints [n]|files|plan|rename [name]]`

## How to I name a session?

- claude:
    - `/rename`
    - Note: named sessions have name appearing in the upper right corner of the
      prompt line.

- copilot:
    - `/rename`
    - Note: with no name argument given, auto generates a name.

## How do I resume a session?

- claude:
    - `/resume`
        - opens session picker

    - `claude --resume "os161.v1"`
        - resume given name or session ID.
        - with no arg, opens the session picker at startup.

    - If, in a given directory, you have had an non-empty session,
    `claude --continue` resumes the session based on the starting directory. This
    can be confirmed by the session name appearing in the upper right corner of the
    prompt line in case you have named the session.

- copilot:
    - `/resume`
        - opens session picker, same as claude.
        - optional arg: session ID.

    - `copilot --resume=[session-ID]`
        - session name not accepted, only GUID ID. Claude accepts name.
        - with no arg, opens the session picker at startup, same as claude.

## MCP server?

- claude:
    - `! claude mcp --help`
    - `! claude mcp add` installs
    - `! claude mcp remove` uninstalls
    - `/mcp`  opens installed mcps, can disable or reconnect, nothing else.

- copilot:
    - `/mcp [show|add|edit|delete|disable|enable ... Manage MCP server configuration`

## How do I update the CLI to the latest version?

- claude:
    - `! claude update`, there is no slash command.

- copilot:
    - `/update`

## Where is the CLI documentation, the stuff you see in `--help`?

- claude:
    - <https://code.claude.com/docs/en/cli-reference>

- copilot:
    - <https://docs.github.com/en/copilot/reference/copilot-cli-reference/cli-command-reference>

## Where is the official vetted list of MCP Servers?

- claude:
    - Note: `/mcp` shows the mcp servers. There seems to be a dintiction between
    servers that appear in the list only after a `! claude update` and those added
    by `! claude mcp add`.

    - Note: Connectors and MCPs in some contexts means the same thing, the term connectors is generally used when working with a claude GUI.

    - <https://code.claude.com/docs/en/mcp>

    - `/reload-plugins` refreshes MCPs without having to exit the claude terminal.

- copilot:
    - Since the MCP protocol is standard, I expect only a difference in how you
    add/remove MCPs.
    - <https://github.com/mcp> ?

## How do I login?

- claude:
    - `/login`
    - `! claude auth login`

- copilot:
    - `/login`
    - `claude login`
