# WIP claude vs copilot equivalents

- How do I see my session ID?
    - /status

- How to I name a session?
    - /rename

- How do I resume a session?
    - /resume, then pick the session
    - claude --resume "os161.v1"
    - If, in a given directory, you have had an non-empty session, `claude --continue` resumes the session based on the starting directory. This can be confirmed by the session name appearing in the upper right corner of the prompt line.



- How do I install an MCP server?


- Where is the CLI documentation, the stuff you see in `claude --help`?



- Where is the official vetted list of MCP Servers?


- How do I login?

```bash
claude auth login        # Log in (opens browser OAuth)
claude auth status       # Check auth state + subscriptionType/rateLimitTier
claude auth logout       # Log out
```
