# Example 02 — Update plugins across a site

## Command

```bash
hermes run wp-cli-automation --action update-plugins --site "my-wp-site"
```

## Output (truncated)

```text
✓ 14 plugins checked
✓ 5 updated, 9 already current, 0 errors
```

## Before / After

- **Before**: logging into wp-admin to update plugins one by one.
- **After**: one command, full update pass, machine-readable result.
- **Time saved**: ~5 min interactive → ~15 s automated.
