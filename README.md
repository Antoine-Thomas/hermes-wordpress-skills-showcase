# Hermes WordPress Skills Showcase

**Security-reviewed · Available on Agensi.io**

A curated pack of [Hermes Agent](https://hermes-agent.nousresearch.com/) skills that automate
WordPress development with **Local by Flywheel** and **WP-CLI**: local site provisioning,
plugin/theme/core updates, full file+database backup and restore, and deployment to a remote
server with URL search-replace. Each skill is a documented, self-contained unit that drops into
`~/.hermes/skills/`.

This repository is a **showcase only** — it demonstrates the workflow, commands and outputs.
The full, working source (Python scripts + WP-CLI automation) ships with the commercial version.

---

## What's included in the full version

- **local-flywheel-setup** — install/configure Local by Flywheel and create a first WordPress site
  (`install_local.py`, `configure_local.py`, `create_site.py`, `list_sites.py`, `manage_site.py`)
- **wordpress-site-management** — create, list, configure and delete local sites
  (`create_site.py`, `list_sites.py`, `delete_site.py`, `configure_site.py`)
- **wp-cli-automation** — updates, plugins, themes, DB export/import
  (`update_plugins.py`, `update_themes.py`, `update_core.py`, `export_db.py`, `import_db.py`, `install_plugins.py`)
- **wordpress-backup-restore** — full site backups and restores
  (`backup_site.py`, `restore_site.py`, `list_backups.py`)
- **wordpress-deployment** — remote deploy + URL migration
  (`deploy_ftp.py`, `deploy_ssh.py`, `sync_database.py`, `search_replace.py`)
- Every `SKILL.md` reference document, templates, and the WP-CLI integration layer

## Live preview

**Create a local site**

```bash
$ hermes run local-flywheel-setup --site-name "demo-site" --php-version "8.2"
✓ Local by Flywheel environment detected
✓ WordPress 6.6 installed
✓ Admin user created
✓ Site reachable at http://demo-site.local
```

**Update every plugin on a site**

```bash
$ hermes run wp-cli-automation --action update-plugins --site "my-wp-site"
✓ 14 plugins checked
✓ 5 updated, 9 already current, 0 errors
```

**Back up, then deploy**

```bash
$ hermes run wordpress-backup-restore --action backup --site "my-wp-site" --compress
✓ Archive: backups/my-wp-site-20261010.tar.gz  (files + database)

$ hermes run wordpress-deployment --target ssh --host "user@server.com" --remote-path "/var/www/html"
✓ Files synced (rsync)
✓ Database migrated
✓ URL search-replace applied  (local → production)
✓ Site live
```

See [`Examples/`](Examples/) for the full before/after write-ups.

## Requirements

- [Hermes Agent](https://hermes-agent.nousresearch.com/) installed
- [Local by Flywheel](https://localwp.com/) installed
- [WP-CLI](https://make.wordpress.org/cli/handbook/) available on `PATH`
- Python 3.8+
- Git
- Optional: `lftp` (FTP deploy), `rsync` + `ssh` (SSH deploy)

## Buy the full version on Agensi

**https://www.agensi.io/@thomas-leroyer**

## About the author

Thomas Leroyer — searching.murphy@gmail.com

## License

Copyright (c) 2026 Thomas Leroyer. All rights reserved.

This repository is a showcase only. The code, scripts, and skill files presented here are
proprietary and may not be copied, modified, distributed, sublicensed, or used commercially
without explicit written permission from the author. See [`LICENSE`](LICENSE).

To purchase a commercial license: https://www.agensi.io/@thomas-leroyer

---

**Keywords**: Hermes Agent skills, WordPress automation, WP-CLI, Local by Flywheel, backup restore,
site deployment, AI agent workflow.
