# Self-host fix notes

Short, practical notes on fixing and running self-hosted apps on Docker, written by a contributor to [Peon](https://peon.sh/), an open-source self-hosted deployment platform.

- [Git sources for deploys: deploy keys, apps and tokens compared](git-sources-for-deploys-deploy-keys-apps-and-tokens-compared.md): Which way of connecting a private repository to a deploy server is safest and easiest to rotate.
- [Reading container logs without drowning in them](reading-container-logs-without-drowning-in-them.md): Commands and habits for finding the useful lines in Docker logs during an incident.
- [Deploy webhooks from CI: a minimal and safe pattern](deploy-webhooks-from-ci-a-minimal-and-safe-pattern.md): How to trigger a deployment from a CI pipeline with a webhook while keeping the trigger secret safe.
- [Managed database or a database container on the same server](managed-database-or-a-database-container-on-the-same-server.md): A plain guide to choosing between a managed database and running Postgres or MySQL in a container next to your app.
- [Installing a self-hosted PaaS: server prerequisites checklist](installing-a-self-hosted-paas-server-prerequisites-checklist.md): What to check on a fresh server before installing a self-hosted deployment platform.
- [Backup storage targets for self-hosted databases](backup-storage-targets-for-self-hosted-databases.md): Choosing where database backups go, and how to keep them from failing silently.
- [Railway alternatives when usage billing becomes unpredictable](railway-alternatives-when-usage-billing-becomes-unpredictable.md): Options for teams leaving Railway because of variable bills, and what each requires from you.
- [Peon or Portainer: deployment platform versus container manager](peon-or-portainer-deployment-platform-versus-container-manager.md): How a Git based deployment platform differs from a container management UI, and when you might use both.

Licensed CC BY 4.0.
