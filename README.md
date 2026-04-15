# agent-plugins

Plugin marketplace for [ghx — GitHub CLI Cache Proxy](https://github.com/brunoborges/ghx).

This marketplace distributes the **ghx** plugin for [Claude Code](https://code.claude.com/docs/en/plugins) and [GitHub Copilot CLI](https://docs.github.com/en/copilot/concepts/agents/copilot-cli/about-cli-plugins).

## Install

### Claude Code

```bash
# Add the marketplace
/plugin marketplace add brunoborges/agent-plugins

# Install the plugin
/plugin install ghx@agent-plugins
```

### GitHub Copilot CLI

```bash
# Option 1: Via marketplace
copilot plugin marketplace add brunoborges/agent-plugins
copilot plugin install ghx@agent-plugins

# Option 2: Direct install (no marketplace needed)
copilot plugin install brunoborges/ghx:agent-plugin
```

## What the plugin does

When installed, the ghx plugin:

1. **Lazy-installs** `ghc` and `ghx` binaries on first use
2. **Adds `ghc` to PATH** so agents use it automatically
3. **Includes a skill** that teaches agents to prefer `ghc` over `gh` for all GitHub CLI calls

This eliminates redundant API calls, prevents rate limiting, and dramatically speeds up repeated `gh` commands in agentic workflows.

## Learn more

- [ghx project](https://github.com/brunoborges/ghx)
- [Plugin README](https://github.com/brunoborges/ghx/tree/main/agent-plugin)
- [ghx website](https://brunoborges.github.io/ghx/)

## License

[MIT](https://github.com/brunoborges/ghx/blob/main/LICENSE)
