## scalaxy ssh-keys create

Create an SSH key in a project

```
scalaxy ssh-keys create [flags]
```

### Examples

```
  scalaxy ssh-keys create --name my-key --public-key-file ~/.ssh/id_ed25519.pub
```

### Options

```
  -h, --help                     help for create
      --name string              Name for the SSH key (required)
      --public-key string        SSH public key string
      --public-key-file string   Path to SSH public key file
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

* [scalaxy ssh-keys](./scalaxy_ssh-keys.md)	 - Manage SSH keys

