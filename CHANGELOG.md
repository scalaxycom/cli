# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).
## [0.1.6] - 2026-11-26

### Documentation

- Docs update

## [0.1.5] - 2026-11-26

### Other

- CLI: single-resource commands show empty fields — `data` envelope not unwrapped [task-14cf1265-0eeb-4f55-8477-8ca9336e897a]
- Merge branch 'gramdy/NIM-14cf1265' into 'master'

## [0.1.4] - 2026-11-25

### Other

- Device verification page calls non-existent endpoints; "Deny" silently approves the device [task-eac48979-9941-4ee0-aaea-a8ec4fba3b68]
- Merge branch 'nimbus/NIM-eac48979' into 'master'
- Consent recording and history [task-771ca399-461d-4484-aa85-ceb4d740d906]
- Merge branch 'nimbus/NIM-771ca399' into 'master'
- Openapi drift check
- Openapi drift check
- Merge branch 'nimbus/NIM-771ca399' into 'master'
- Cli: Trivy fs scan in GitLab CI [subtask-3a6fabfe-6fe9-4ec3-a66c-9db39b98cdba]
- Merge branch 'gramdy/NIM-d197112a' into 'master'
- Cli: bump Trivy to 0.76.2 + Renovate auto-update [subtask-cf080dc9-f0f3-4557-ba61-0f78d03fb124]
- Update Trivy to 0.76.2 and automate future Trivy version updates in all GitLab CI repos [task-b7bbf1c8-9e03-4732-9a12-c333087a11be]
- Merge branch 'gramdy/NIM-b7bbf1c8' into 'master'
- [CLI] Authentication status returns not_authenticated after successful OAuth login [dev] [task-c8671216-d350-4da1-8f4c-fc6345042975]
- Merge branch 'gramdy/NIM-c8671216' into 'master'
- [CLI] `scalaxy version --output json|yaml` ignores the output format and prints plain text [task-d7491e04-8103-4b90-935b-4dc6643e8962]
- Merge branch 'gramdy/NIM-d7491e04' into 'master'
- [CLI] README Quickstart shows `scalaxy servers list` without required project context (`--project` / `SCALAXY_PROJECT`) [task-3a0cdefa-63e8-41ae-b545-b0fb70793cc4]
- Merge branch 'gramdy/NIM-3a0cdefa' into 'master'
- [CLI] `scalaxy ssh-keys create` rejects `--name` with "unknown flag: --name" [task-b8b37172-fb06-4eff-ac0e-22aaef7590a7]
- Merge branch 'gramdy/NIM-b8b37172' into 'master'

## [0.1.3] - 2026-07-30

### Other

- Fix duplicated error wrapping and untyped failure in CLI login [subtask-535c3608-92e9-47f5-a168-7597685610d3]
- Regenerate API client, align CLI contract & verify login end to end [subtask-3e768485-17dd-4017-8848-3aca789e0a6e]
- CLI `scalaxy auth login` fails with 404 — device-flow endpoints missing in platform-api [task-9319fe68-95a5-482b-a8b9-adc80e7a97ac]
- Merge branch 'nimbus/NIM-9319fe68' into 'master'
- README update

## [0.1.2] - 2026-07-15

### Other

- Goreleaser fix

## [0.1.1] - 2026-07-15

### Other

- Init
- Go Module Scaffolding & Build Config [task-025e04bc-8025-4e67-b58e-7ce1077addd9]
- Merge branch 'nimbus/NIM-025e04bc' into 'master'
- NIM-5f1423a7 Core Infrastructure — Config, Auth & Credential Store
- Merge branch 'nimbus/NIM-5f1423a7' into 'master'
- Error handler with polymorphic parsing and exit codes [subtask-6a2d0f63-582f-4f31-b5ae-22e8a5158d9d]
- Confirmation prompts and quiet mode [subtask-3b3d6592-2f3e-4647-b7de-03e22a5191f0]
- Polling helper for --wait [subtask-8f5fe348-5c68-4a1c-a89b-cf2fece54836]
- Pagination helper [subtask-38a675e9-a440-44c2-9ad9-fa0af38275f4]
- JSON and YAML formatters [subtask-6f685443-1ac6-4155-ae05-13b0494f7a2c]
- Core Infrastructure — Output, Errors, Prompts & Pagination [task-6f5c893e-98c4-42f6-b0b3-12e3a34518df]
- Merge branch 'nimbus/NIM-6f5c893e' into 'master'
- Export OpenAPI spec and configure oapi-codegen [subtask-241bbb28-6ab8-4eee-89df-8be638eb6dfb]
- Custom HTTP transport with auth injection and debug logging [subtask-b7ffa454-0449-445b-a6cd-21a7ff1a065f]
- Polymorphic error parser wrapper [subtask-44d8a0be-66c5-49a8-b465-d4954534c9cf]
- Generic paginator for client [subtask-07cae1f8-d717-45c6-a088-8b54cbb3de36]
- Merge branch 'nimbus/NIM-1476f0b8' into 'master'
- Auth login — OAuth device flow with session storage [subtask-9eeb6aee-cdcc-48fe-b775-e6ea4ec5acad]
- Auth logout — session removal and server revocation [subtask-d1e532d6-76af-4f05-b6f0-c45dc7276e1c]
- Auth login — OAuth device flow with session storage [subtask-9eeb6aee-cdcc-48fe-b775-e6ea4ec5acad]
- Auth status — identity display for all auth methods [subtask-e7f7f4e5-e00d-49cd-8fe9-673f7f4d34fb]
- Auth token — print raw credential to stdout [subtask-d91e0125-91a0-4be2-aac3-0d5a89d9df6f]
- Auth introspect — API key capabilities display [subtask-5bb4f632-d55c-4e0a-b4bf-2671753b1962]
- Merge branch 'nimbus/NIM-c97afd4e' into 'master'
- Rename
- Config set/get/list commands [subtask-7d743bf5-6861-4891-b59f-40f735675de9]
- Plans list/get with stock status [subtask-5659fab6-ee7d-4406-bc03-1a2554c96982]
- Regions list and operating-systems list commands [subtask-65d7a04a-95da-4281-bf61-07a269dfa3ce]
- Merge branch 'nimbus/NIM-edfc7ad0' into 'master'
- Rename
- Rename
- Project context resolver helper [subtask-91d3363b-ba8b-4e41-9723-72a10562cc67]
- Ssh-keys list/get — SSH key listing and detail [subtask-133b6a19-0826-4337-ad43-b51e65258279]
- Ssh-keys create — from string or file [subtask-07a2e010-40fc-40e7-84f6-1f59d1c115c3]
- Ssh-keys update/delete — label update and key removal [subtask-50c1243d-88b5-4bfd-a73d-11e97b2c8629]
- Servers list with filters and pagination [subtask-a0c0374d-5ac0-41ca-bb14-d6ab50e4c0d7]
- Servers get — detail view [subtask-bc6bbb38-68aa-468b-bd13-0655109b8efb]
- Servers create with --wait support [subtask-a0e65c11-71ba-4e52-bc99-2930936e9108]
- Servers delete with confirmation and --wait [subtask-3e8c0c27-3206-43ba-a705-25486b55f066]
- Servers events — event history display [subtask-f0dba3fd-4cc6-46f7-b49a-5adc33ffe5e6]
- Servers credentials — one-time root credential display [subtask-05c3cdec-ac4b-4741-a535-5be325a6baca]
- Merge branch 'nimbus/NIM-c61b69ce' into 'master'
- Merge branch 'nimbus/NIM-d5c6b70e' into 'master'
- Servers update hostname [subtask-45ae07bc-9992-4350-9667-6493ff91beb3]
- Servers power-on/power-off/reboot with confirmation and --wait [subtask-37d51710-53ee-4275-bafe-497107c11a6a]
- Servers reinstall with data-loss warning and --wait [subtask-fa22ed9b-f870-4d5a-9cc0-ce2c49cfb49e]
- Servers lock/unlock [subtask-04a9aa40-8e3c-4c77-b7d4-2d83bf5f7ad5]
- Servers wait — poll until target status [subtask-9e816723-afc8-4d5e-af64-164e30cd892e]
- Merge branch 'nimbus/NIM-eb956232' into 'master'
- Merge branch 'master' into nimbus/NIM-6e80ea7e
- Structuring and additional tests
- Merge branch 'nimbus/NIM-6e80ea7e' into 'master'
- Account get/update commands [subtask-4d8fc14c-67ff-42f9-939f-6c8d26cc8302]
- Account sessions list/revoke [subtask-24e4b32b-d898-41c3-9778-a8ac06e8135a]
- Merge branch 'nimbus/NIM-5286b9a3' into 'master'
- Projects list/create — org-scoped project creation [subtask-257bbf30-c0e0-46d6-a13f-a85c31f36a02]
- Projects get/update/delete [subtask-db4663b6-242f-469e-be08-e2cc25ccb584]
- Projects switch — set default project context [subtask-503d5c64-2c7c-455c-8d43-e583eb86a0b8]
- Projects members list/add/update/remove [subtask-5a2694cb-1cc7-4714-971e-9824d66b9030]
- Projects org context resolver [subtask-09b09cb4-fe46-4d1d-a319-72f9017d20b9]
- Merge branch 'nimbus/NIM-66f6dde2' into 'master'
- NIM-a448ebf8 scalaxy update — self-update with SHA-256 verification
- NIM-81234298 Async version check with 24h cache
- Async version check with 24h cache [subtask-81234298-17ed-42ae-ab83-f4d1de6d5de8]
- NIM-a448ebf8 scalaxy update — self-update with SHA-256 verification
- NIM-a448ebf8 scalaxy update — self-update with SHA-256 verification
- NIM-a448ebf8 scalaxy update — self-update with SHA-256 verification
- NIM-a448ebf8 scalaxy update — self-update with SHA-256 verification
- Merge branch 'nimbus/NIM-a9e691d6' into 'master'
- Unit tests for all internal/ packages (80%+ coverage) [subtask-3388dd4a-b100-403a-8a9f-a56721e0450b]
- Command unit tests with mock HTTP [subtask-9512dd0f-9f35-449b-bc02-7b49eb38d118]
- Integration tests with go-vcr cassettes and E2E binary tests [subtask-d2220994-8727-4837-ba3a-7fc887990d47]
- CI pipeline — lint, test, build, release, binary size check [subtask-299f88f0-39e3-4069-8601-7f93cf8fe657]
- Testing Infrastructure & CI Pipeline [task-c0b32df6-2576-4ee9-a3e5-0a164a7a8fd8]
- Merge branch 'nimbus/NIM-c0b32df6' into 'master'
- CLI repo .gitlab-ci.yml skeleton: stages, rules, lint/test/build, Go cache [subtask-35d3003c-1b65-470f-96a4-535fa1faf74e]
- .goreleaser.yaml release.github block + checksums + changelog config [subtask-5240adc1-716e-4a0e-9a59-fa2b25109ef3]
- Author distribution-facing README.md in CLI repo [subtask-b6ba005a-7e52-4811-ad61-b8b190a26524]
- GitLab CI masked+protected variables + GitHub distribution repo setup guide [subtask-ab4e0335-f079-4142-a97c-92a54155ccbf]
- Idempotent release job: goreleaser publish with retry + asset backfill [subtask-2cc3c2e1-13f1-4f33-9716-ae1210ff2af1]
- CHANGELOG.md scaffold + cliff.toml + Makefile changelog/release targets [subtask-1e287144-065e-4c30-b719-0afa6dfb5b80]
- Doc-sync job: selective README/CHANGELOG/LICENCE push + source-leak guard [subtask-c1011113-e6b3-48ce-ae57-24f64699ea8f]
- Update .gitlab-ci.yml file
- Update .gitlab-ci.yml file
- Update .gitlab-ci.yml file
- Update .gitlab-ci.yml file
- Update .gitlab-ci.yml file
- Update .gitlab-ci.yml file
- Update .gitlab-ci.yml file
- Merge branch 'nimbus/NIM-a97b835e' into 'master'

---
*Generated by [git-cliff](https://git-cliff.org)*
