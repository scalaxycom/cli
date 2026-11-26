## scalaxy completion bash

Generate the bash autocompletion script

### Synopsis

Generate the bash autocompletion script for scalaxy.

To load completions in your current shell session:

	source <(scalaxy completion bash)

To load completions for every new session, add the script to your
bash completion directory, for example:

	scalaxy completion bash > /etc/bash_completion.d/scalaxy


```
scalaxy completion bash
```

### Options

```
  -h, --help   help for bash
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

