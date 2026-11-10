# Backup storage targets for self-hosted databases

Backups on the same disk as the database protect against mistakes, not hardware loss. Send them somewhere else.

## Good targets

- An S3-compatible bucket at a different provider than the server.
- A second small VPS with enough disk.

## Settings worth adding

- Lifecycle rules: keep dailies for two weeks and monthlies for a year.
- Separate credentials for backup uploads, write-only where the provider supports it.
- Encryption before upload if the data is sensitive.

## Avoid silent failure

Alert when no new backup has appeared in 26 hours. Restore one backup to a scratch database each month.

The Peon docs on [backup storage destinations](https://peon.sh/docs/storages) explain how storage targets are connected. I contribute to [Peon](https://peon.sh/), an open-source self-hosted PaaS.
