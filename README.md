# Scalaxy CLI

[![Latest Release](https://img.shields.io/github/v/release/scalaxycom/cli?logo=github&label=latest%20release)](https://github.com/scalaxycom/cli/releases/latest)
[![License](https://img.shields.io/github/license/scalaxycom/cli?logo=github)](./LICENCE.md)

## Project Description

The **Scalaxy CLI** is the official command-line interface for [Scalaxy Metal](https://www.scalaxy.com), the bare-metal cloud platform for deploying and managing dedicated physical servers. It wraps the Scalaxy Metal Platform API, letting you provision and delete servers, run power actions, reinstall operating systems, manage SSH and API keys, browse deployment plans, regions, and operating systems, and drive your infrastructure from the terminal or CI/CD pipelines — no web dashboard required. It is distributed as a single, dependency-free static binary.

## Install

The CLI is a single static binary published to [GitHub Releases](https://github.com/scalaxy/cli/releases/latest). Every release ships five platform archives plus a `checksums.txt` file containing the SHA-256 digest of each archive.

Each archive filename embeds the release version, so the snippets below first read `checksums.txt` to discover the exact current filename for your platform, then download and verify that archive. This keeps every command working across releases without you ever editing a version number.

The download and checksum base URL is always:

```
https://github.com/scalaxy/cli/releases/latest/download/
```

### Linux (amd64)

```bash
ARCHIVE=$(curl -sSL https://github.com/scalaxy/cli/releases/latest/download/checksums.txt | grep linux_amd64 | awk '{print $2}')
curl -sSL "https://github.com/scalaxy/cli/releases/latest/download/$ARCHIVE" -o "$ARCHIVE"
curl -sSL https://github.com/scalaxy/cli/releases/latest/download/checksums.txt | grep linux_amd64 | sha256sum -c -
tar -xzf "$ARCHIVE" scalaxy
chmod +x scalaxy
sudo mv scalaxy /usr/local/bin/
```

### Linux (arm64)

```bash
ARCHIVE=$(curl -sSL https://github.com/scalaxy/cli/releases/latest/download/checksums.txt | grep linux_arm64 | awk '{print $2}')
curl -sSL "https://github.com/scalaxy/cli/releases/latest/download/$ARCHIVE" -o "$ARCHIVE"
curl -sSL https://github.com/scalaxy/cli/releases/latest/download/checksums.txt | grep linux_arm64 | sha256sum -c -
tar -xzf "$ARCHIVE" scalaxy
chmod +x scalaxy
sudo mv scalaxy /usr/local/bin/
```

### macOS — Apple Silicon (darwin/arm64)

```bash
ARCHIVE=$(curl -sSL https://github.com/scalaxy/cli/releases/latest/download/checksums.txt | grep darwin_arm64 | awk '{print $2}')
curl -sSL "https://github.com/scalaxy/cli/releases/latest/download/$ARCHIVE" -o "$ARCHIVE"
curl -sSL https://github.com/scalaxy/cli/releases/latest/download/checksums.txt | grep darwin_arm64 | sha256sum -c -
tar -xzf "$ARCHIVE" scalaxy
chmod +x scalaxy
sudo mv scalaxy /usr/local/bin/
```

> On macOS, `sha256sum` is provided by the `coreutils` Homebrew formula (`brew install coreutils`) — or use `shasum -a 256 -c -` in its place.

### macOS — Intel (darwin/amd64)

```bash
ARCHIVE=$(curl -sSL https://github.com/scalaxy/cli/releases/latest/download/checksums.txt | grep darwin_amd64 | awk '{print $2}')
curl -sSL "https://github.com/scalaxy/cli/releases/latest/download/$ARCHIVE" -o "$ARCHIVE"
curl -sSL https://github.com/scalaxy/cli/releases/latest/download/checksums.txt | grep darwin_amd64 | sha256sum -c -
tar -xzf "$ARCHIVE" scalaxy
chmod +x scalaxy
sudo mv scalaxy /usr/local/bin/
```

> On macOS, `sha256sum` is provided by the `coreutils` Homebrew formula (`brew install coreutils`) — or use `shasum -a 256 -c -` in its place.

### Windows (amd64)

PowerShell:

```powershell
$Checksums = (Invoke-WebRequest -Uri "https://github.com/scalaxy/cli/releases/latest/download/checksums.txt" -UseBasicParsing).Content
$Line = ($Checksums -split "`n" | Select-String "windows_amd64")
$Archive = ($Line -split '\s+')[1]
Invoke-WebRequest -Uri "https://github.com/scalaxy/cli/releases/latest/download/$Archive" -OutFile $Archive
# Verify the SHA-256 hash matches the one printed above:
(Get-FileHash $Archive -Algorithm SHA256).Hash.ToLower()
Expand-Archive -Path $Archive -DestinationPath scalaxy-bin
Move-Item scalaxy-bin\scalaxy.exe "$env:LOCALAPPDATA\Microsoft\WindowsApps\scalaxy.exe"
```

### Package managers

- **Homebrew** (future): `brew install scalaxy/tap/scalaxy`
- **Scoop** (future): `scoop install scalaxy`

### Verify the installation

```bash
scalaxy version
```

## Quickstart

```bash
# 1. Authenticate with your Scalaxy account (opens a browser-based login)
scalaxy auth login

# 2. List your servers
scalaxy servers list
```

Common next steps:

```bash
scalaxy servers create --plan <plan> --region <region> --os <os> --hostname my-server
scalaxy servers get <server-id>
scalaxy servers power-on <server-id>
scalaxy auth status
```

## Authentication

The CLI supports three authentication methods. Credentials are resolved in this order: the `--api-key` flag → the `SCALAXY_API_KEY` environment variable → a stored interactive session.

- **Interactive session** — run `scalaxy auth login` to sign in through a browser-based flow. The resulting session token is stored locally in a credentials file with `0600` permissions. Use `scalaxy auth status` to inspect the active identity and `scalaxy auth logout` to revoke it.
- **User token** — a personal API key (`--api-key <key>` or `SCALAXY_API_KEY=<key>`) scoped to your account, with `read_only` or `read_write` access. Manage your keys from the dashboard or via `scalaxy api-keys`.
- **Organization token** — an org-scoped API key (`--api-key <key>` or `SCALAXY_API_KEY=<key>`) with granular `resource:action` permissions and no account context. Pass the target organization with `--org` or `SCALAXY_ORG` when needed.

For the full guide, see the [authentication documentation](https://docs.scalaxy.cloud/cli/auth).

## Supported Platforms

Pre-built static binaries are published for:

| Operating system | Architecture | Archive |
| --- | --- | --- |
| Linux | amd64 | `.tar.gz` |
| Linux | arm64 | `.tar.gz` |
| macOS (Intel) | amd64 | `.tar.gz` |
| macOS (Apple Silicon) | arm64 | `.tar.gz` |
| Windows | amd64 | `.zip` |

Each binary is self-contained with no runtime dependencies.

## Documentation

Full CLI documentation — command reference, configuration, output formats, and examples — is at <https://docs.scalaxy.cloud/cli>.

For contributors and release operators, see [`CONTRIBUTING.md`](./CONTRIBUTING.md) (development + release workflow + ops runbook) and [`docs/ops/release-pipeline.md`](./docs/ops/release-pipeline.md) (release-pipeline prerequisites: GitLab CI variables, GitHub distribution repo setup, token rotation).

## License

Distributed under the terms described in [`LICENCE.md`](./LICENCE.md).
