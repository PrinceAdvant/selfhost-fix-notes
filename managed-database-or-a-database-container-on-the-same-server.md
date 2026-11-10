# Managed database or a database container on the same server

## Container on the same server

Pros: no extra bill, lowest latency, full control of versions and extensions.
Cons: you own backups, upgrades and disk monitoring.

## Managed database

Pros: automated backups, point in time recovery, failover options.
Cons: a separate monthly cost that often exceeds the app server, and limited extensions.

## How I decide

- Prototype or internal tool: container, with nightly dumps to object storage.
- Paying customers and a small team: container is still fine if backups are tested monthly.
- Strict uptime or compliance needs: managed.

The key word is tested. A backup you have never restored is a guess.

The Peon docs on [databases in Peon](https://peon.sh/docs/databases) show how one-click Postgres, MySQL and Redis are set up with backups. I work on [Peon](https://peon.sh/).
