# claude vs copilot equivalents

## How do I see my session ID?

- claude:
    - `/status`

- copilot:
    - `/session` is not a claude slash command.

## How to I name a session?

- claude:
    - `/rename`

- copilot:
    - `/rename`

## How do I resume a session?

- `/resume`, then pick the session

- `claude --resume "os161.v1"`

- If, in a given directory, you have had an non-empty session,
`claude --continue` resumes the session based on the starting directory. This
can be confirmed by the session name appearing in the upper right corner of the
prompt line in case you have named the session.

## MCP server?

- claude:
    - `! claude mcp --help`
    - `! claude mcp add` installs
    - `! claude mcp remove` uninstalls
    - `/mcp`  opens installed mcps, can disable or reconnect, nothing else.

- copilot:
    - `/mcp [show|add|edit|delete|disable|enable ... Manage MCP server configuration`

## Updating the CLI

- claude `! claude update`, there is no slash command.
- copilot: `/update`

## Where is the CLI documentation, the stuff you see in `claude --help`?

<https://code.claude.com/docs/en/cli-reference>

## Where is the official vetted list of MCP Servers?

- Note: `/mcp` shows the mcp servers. There seems to be a dintiction between
  servers that appear in the list only after a `! claude update` and those added
  by `! claude mcp add`.

- Note: Connectors and MCPs in some contexts means the same thing, the term connectors is generally used when working with a claude GUI.

<https://code.claude.com/docs/en/mcp>

- `/reload-plugins` refreshes MCPs without having to exit the claude terminal.

## How do I login?

- claude:
    - `/login`
    - `! claude auth login`

- copilot:
    - `/login`
    - `claude login`
