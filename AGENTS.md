# AI Agent Instructions

## Overview

Nandi Social (MIT): Social Manager, its workflows and its policy. It prepares social posts in a browser the user watches; a person publishes. See [README.md](README.md).

Inside the Nandi workspace, the workspace `AGENTS.md` adds the general standards. This file is the stand-alone minimum for contributors.

## Core Rules (CRITICAL)

- **A person publishes.** Never make the agent click Post, Publish, Share, Send, Reply or Tweet, or press Enter to send. It calls `browser_hand_over` instead. Never automate likes, follows, connection requests, messages, reposts or comments on others' posts.
- `policies/social-posting.md` applies only to `agent:social-manager` (the installer refuses pack policies for other agents). Change it only to refuse more.
- An agent's `skill.md` body stays at **900 words or fewer**.
- Its `capabilities` must match the registry entry in `nandi-registry` **exactly**: `tools` = `allowed-tools`, `network` = the `network.allow` hosts, `pilots` = the `pilots` ids, `requires_approval` = `requires_approval`.
- Every tool that writes files or runs commands **requires approval** (writes to My notes are the user's one decision in Nandi).
- **No `model:`** in a pack. Pack agents use the user's default model.
- **Releases:** bump `version` in `.nandi/manifest.yaml`, tag `v<version>`, then update and sign the entries in `nandi-registry`.
- No unsolicited commits, and never force-push. Use Conventional Commits.

## Check

`NANDI_PACK_DIR=<this folder> cargo test --lib local_pack_checkout_installs -- --ignored` in `nandi/src-tauri` validates the pack as an install does; `python tools/build_index.py --check` in `nandi-registry` checks the registry entry.

## Licence

MIT (see `LICENSE`).
