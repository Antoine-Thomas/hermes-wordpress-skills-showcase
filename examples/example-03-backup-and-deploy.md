# Example 03 — Backup local, then deploy to production

## Commands

```bash
# 1. Full backup (files + database)
hermes run wordpress-backup-restore --action backup --site "my-wp-site" --compress

# 2. Deploy to a remote server over SSH/rsync
hermes run wordpress-deployment --target ssh --host "user@server.com" --remote-path "/var/www/html"
```

## Output (truncated)

```text
✓ Archive: backups/my-wp-site-20261010.tar.gz  (files + database)

✓ Files synced (rsync)
✓ Database migrated
✓ URL search-replace applied  (local → production)
✓ Site live
```

## Before / After

- **Before**: manual export (plugin or mysqldump), SFTP upload, hand-edited SQL to swap URLs.
- **After**: two commands; backup is reversible and URL migration is scripted.
- **Risk reduced**: no forgotten URL swap, no half-uploaded site — the backup is the rollback point.

## Workflow

```mermaid
flowchart LR
  A[Local site] --> B[backup files+DB]
  B --> C[rsync to server]
  C --> D[migrate DB]
  D --> E[search-replace URLs]
  E --> F[Site live]
```
