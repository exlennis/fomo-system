
### Playground Directory Cleanup Automation

This document details the automated cleanup process configured for the `/Users/ez/Local/playground` directory. Files and directories older than 5 days are automatically removed to maintain a clean working environment and prevent unnecessary disk usage.

## Configured Cleanup Process

The playground directory has been configured with an automatic cleanup system that:

- Runs daily at midnight (00:00)
- Identifies files and directories modified more than 5 days ago
- Permanently removes these items from the system
- Preserves the base playground directory itself

## Technical Implementation

### Crontab Configuration

The cleanup is implemented via the user's crontab with the following entry:

```
0 0 * * * find /Users/ez/Local/playground -mindepth 1 -mtime +5 -delete
```

This breaks down as:
- `0 0 * * *` - Schedule to run at 00:00 (midnight) every day
- `find /Users/ez/Local/playground` - Target the playground directory
- `-mindepth 1` - Only process contents within the directory, not the directory itself
- `-mtime +5` - Match files modified more than 5 days ago
- `-delete` - Permanently remove matching files and directories

### Verifying the Configuration

To check the current crontab configuration:

```bash
crontab -l
```

### Modifying the Configuration

To edit the crontab settings:

```bash
crontab -e
```

Common modifications might include:
- Changing the frequency (e.g., weekly instead of daily)
- Adjusting the age threshold (e.g., 7 days instead of 5)
- Adding exclusions for specific files or directories

## Important Considerations

- **Permanent Deletion**: Files are removed directly without being sent to the Trash/Bin
- **No Recovery**: Deleted files cannot be recovered without external backups
- **No Confirmation**: The process runs silently in the background without user intervention
- **Inclusive Scope**: Both files and directories matching the age criteria are removed
- **No Logging**: The standard configuration does not maintain logs of what was deleted

## Recommendations

- Do not store important files in the playground directory for extended periods
- Back up any files from the playground directory you wish to keep
- Consider adding more sophisticated exclusion rules if needed for specific files

## Troubleshooting

If the cleanup doesn't seem to be working:
1. Verify crontab is active with `crontab -l`
2. Check system logs for any cron-related errors
3. Test the find command manually to ensure it works as expected

