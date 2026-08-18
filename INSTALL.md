# How to install

## Claude Code

### Install

```bash
claude plugin marketplace add chpl/i-have-adhd-and-aphantasia
claude plugin install i-have-adhd@i-have-adhd
```

Type `/i-have-adhd`.

### Verify

```bash
claude plugin list
```

### Update

```bash
claude plugin marketplace update i-have-adhd
```

### Uninstall

```bash
claude plugin uninstall i-have-adhd
claude plugin marketplace remove i-have-adhd
```

Or keep it installed and turn it off: `claude plugin disable i-have-adhd`.

### Always-on (optional)

A `SessionStart` hook loads the full ruleset at the start of every session, no `/i-have-adhd` needed:

```bash
touch ~/.claude/.i-have-adhd-always
```

Back to on-demand:

```bash
rm ~/.claude/.i-have-adhd-always
```

The hook only fires when the flag file exists, so installing the plugin changes nothing by itself. Honors `$CLAUDE_CONFIG_DIR` if you've moved your config dir. "stop adhd mode" still turns it off for the current session.
