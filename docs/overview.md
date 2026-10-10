# Overview

Hermes WordPress Skills is a pack of [Hermes Agent](https://hermes-agent.nousresearch.com/) skills
for building, maintaining and shipping WordPress sites from the terminal, driven by an AI agent.

The pack targets the **local-first** workflow: build on **Local by Flywheel**, manage everything
with **WP-CLI**, and deploy to a remote server by script rather than by hand.

## The five skills

| Skill | What it does |
|-------|--------------|
| `local-flywheel-setup` | Install/configure Local by Flywheel, create the first site |
| `wordpress-site-management` | Create, list, configure, delete local sites |
| `wp-cli-automation` | Updates (core/plugins/themes), DB export/import, plugin install |
| `wordpress-backup-restore` | Full backups and restores (files + database) |
| `wordpress-deployment` | Remote deploy (FTP/SFTP, SSH/rsync) + URL search-replace |

## How a skill is shaped

Each skill ships a `SKILL.md` (agent instructions), a `scripts/` folder (the working automation),
and `references/` (docs). Drop the folder into `~/.hermes/skills/` and Hermes can invoke it.

> This repository is the **showcase**: it documents behaviour and shows real-looking commands and
> outputs. The executable source is the paid product.
