## scalaxy servers wait

Wait for a server to reach a target status

```
scalaxy servers wait <server-id> [flags]
```

### Options

```
  -h, --help            help for wait
      --status string   Target status to wait for (required)
      --timeout int     Timeout in seconds (0 = indefinite) (default 300)
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

* [scalaxy servers](./scalaxy_servers.md)	 - Manage servers

