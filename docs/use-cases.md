# Use cases

## 1. Freelance / agency site builds

Spin up a fresh local WordPress per client project, configure theme + plugins, then push to the
client's server with a scripted URL migration. Repeatable and reviewable — no "it worked on my
machine" drift between projects.

```bash
hermes run local-flywheel-setup --site-name "client-acme" --php-version "8.2"
hermes run wordpress-deployment --target ssh --host "deploy@acme.com" --remote-path "/var/www"
```

## 2. Maintenance on a live site

Weekly upkeep without logging into wp-admin: update core/plugins/themes, take a backup first so any
bad update is one command away from being rolled back.

```bash
hermes run wordpress-backup-restore --action backup --site "my-wp-site"
hermes run wp-cli-automation --action update-plugins --site "my-wp-site"
```

## 3. Staging → production promotion

Keep a Local build as staging, back it up, then deploy the same artefact to production with the
database and URLs rewritten in one pass — the backup doubling as the rollback point.

```bash
hermes run wordpress-backup-restore --action backup --site "staging" --compress
hermes run wordpress-deployment --target ssh --host "user@prod.com" --remote-path "/var/www/html"
```
