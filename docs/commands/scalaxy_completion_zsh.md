## scalaxy completion zsh

Generate the zsh autocompletion script

### Synopsis

Generate the zsh autocompletion script for scalaxy.

To load completions in your current shell session:

	source <(scalaxy completion zsh)

To load completions for every new session, add the script to a directory
in your $fpath, for example:

	scalaxy completion zsh > "${fpath[1]}/_scalaxy"

You may need to start a new shell for this setup to take effect.


```
scalaxy completion zsh
```

### Options

```
  -h, --help   help for zsh
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

