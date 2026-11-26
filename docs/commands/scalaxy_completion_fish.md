## scalaxy completion fish

Generate the fish autocompletion script

### Synopsis

Generate the fish autocompletion script for scalaxy.

To load completions in your current shell session:

	scalaxy completion fish | source

To load completions for every new session, add the script to your
fish completions directory, for example:

	scalaxy completion fish > ~/.config/fish/completions/scalaxy.fish


```
scalaxy completion fish
```

### Options

```
  -h, --help   help for fish
```

### Options inherited from parent commands

```
      --api-key string   API key for authentication
      --debug            Enable debug mode
      --no-color         Disable colored output
      --org string       Organization context override
  -o, --output string    Output format: table, json, yaml (default "table")
      --project string   Project context override
  -q, --quiet            Suppress non-essential output
  -y, --yes              Skip confirmation prompts
```

### SEE ALSO

* [scalaxy completion](./scalaxy_completion.md)	 - Generate shell autocompletion scripts

