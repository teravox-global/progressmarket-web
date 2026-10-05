# CODEX_INDEX — progressmarket-web

Updated: 2026-10-05
Repository: https://github.com/teravox-global/progressmarket-web
Default branch: main
Purpose: Progress Market web/landing repository; exact production mapping is not established by current server inventory.

## Start here in every new development chat
1. Read this index first.
2. No root README.md was present in the main-branch root listing at this snapshot. No root AGENTS.md was present in the main-branch root listing.
3. Read the project docs below and check their current contents/branch before following old snapshots.
4. Read the current “Аудит (сервера и сервисы) TeraVox_Infrastructure_Access_Map_2026-10-05(1).md” from the IT Department project/Library for server, service, network, access and incident details. It is the shared infrastructure source of truth; do not copy secret values into this repository.
5. Before edits/deploy: confirm active branch, clean/dirty state, target environment, current host/container health and latest verified_at in the global map. Never reset a dirty checkout or deploy to a host inferred only from this repository name.

## Source documents
docs/LEAD_REFERRAL_V1.md; docs/MARKET_V1_1_DEPLOY.md

## Runtime / infrastructure pointer
The clone is on Agent Hub. A public hostname/runtime mapping is not confirmed; do not deploy based on repository name alone.
The global infrastructure map records SSH aliases, Docker access, databases, private networks, credential file references, known outages, and which secondary access path is currently missing. Secrets are stored on target servers or in the approved secret manager; this index must never contain private keys, tokens, passwords, or .env contents.

## Change record required for infrastructure work
When a task adds or changes a server, service, container, database, network, domain, credential, ACL, or deploy path:
- update this CODEX_INDEX.md and the global TeraVox infrastructure map in the same task/PR;
- record purpose, owner, runtime status/version, ports and exposure, dependencies/network, database name/role, primary and backup access, secret reference (path/name only), expiry/rotation, backup/restore reference, verification time and unresolved incident;
- if either access path is missing, mark NEEDS_ACCESS and create an IT Department dispatcher task before deployment;
- add expiry reminders to the dispatcher; never claim automatic expiry monitoring unless a live watcher is verified.

## Build, tests and deploy
Determine the actual commands from current package manifests, Makefile/pyproject, CI workflows and deployment docs. Do not infer production commands from this index. Record verified commands and results here after checking them in the current branch.
