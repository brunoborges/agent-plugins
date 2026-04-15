# agent-plugins

Plugin marketplace for [ghcd — GitHub CLI Cache Proxy](https://github.com/brunoborges/ghcd).

This marketplace distributes the **ghcd** plugin for [Claude Code](https://code.claude.com/docs/en/plugins) and [GitHub Copilot CLI](https://docs.github.com/en/copilot/concepts/agents/copilot-cli/about-cli-plugins).

## Install

### Claude Code

```bash
# Add the marketplace
/plugin marketplace add brunoborges/agent-plugins

# Install the plugin
/plugin install ghcd@agent-plugins
```

### GitHub Copilot CLI

```bash
# Option 1: Via marketplace
copilot plugin marketplace add brunoborges/agent-plugins
copilot plugin install ghcd@agent-plugins

# Option 2: Direct install (no marketplace needed)
copilot plugin install brunoborges/ghcd:agent-plugin
```

## What the plugin does

When installed, the ghcd plugin:

1. **Lazy-installs** `ghc` and `ghcd` binaries on first use
2. **Adds `ghc` to PATH** so agents use it automatically
3. **Includes a skill** that teaches agents to prefer `ghc` over `gh` for all GitHub CLI calls

This eliminates redundant API calls, prevents rate limiting, and dramatically speeds up repeated `gh` commands in agentic workflows.

## Learn more

- [ghcd project](https://github.com/brunoborges/ghcd)
- [Plugin README](https://github.com/brunoborges/ghcd/tree/main/agent-plugin)
- [ghcd website](https://brunoborges.github.io/ghcd/)

## License

[MIT](https://github.com/brunoborges/ghcd/blob/main/LICENSE)
