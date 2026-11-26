## scalaxy servers create

Deploy a new server

```
scalaxy servers create [flags]
```

### Options

```
  -h, --help                  help for create
      --hostname string       Hostname for the server
      --os string             Operating system slug to install
      --plan string           Plan slug to deploy
      --region string         Region slug to deploy in
      --ssh-key stringArray   SSH key ID to install (repeatable)
      --timeout int           Timeout in seconds for --wait (default 600)
      --wait                  Wait for the server to become active
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

