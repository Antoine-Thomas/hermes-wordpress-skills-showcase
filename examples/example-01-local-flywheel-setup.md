# Example 01 — Provision a local WordPress site

## Command

```bash
hermes run local-flywheel-setup --site-name "demo-site" --php-version "8.2"
```

## Output (truncated)

```text
✓ Local by Flywheel environment detected
✓ WordPress 6.6 installed
✓ Admin user created
✓ Site reachable at http://demo-site.local
```

## Before / After

- **Before**: empty Local by Flywheel install, no site.
- **After**: a running local WordPress with admin user, ready for theme work.
- **Time saved**: manual Local site creation + WP install ≈ 10 min → automated ≈ 40 s.
