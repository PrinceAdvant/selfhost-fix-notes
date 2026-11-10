# Railway alternatives when usage billing becomes unpredictable

Railway is pleasant to use. Teams start looking elsewhere when usage-based bills swing month to month.

## Options

- Another hosted PaaS with fixed plans. Easy migration, similar experience, still per service pricing.
- A VPS with plain Docker Compose. Cheapest, but you write your own deploy scripts.
- A self-hosted PaaS on a VPS. Git deploys, previews and databases with a flat server bill.

## Migration notes

- Export environment variables first; they are the part people forget.
- Dump databases with `pg_dump` and restore before switching DNS.
- Lower DNS TTL a day before the cutover.

I wrote about picking a [Railway alternative](https://peon.sh/blogs/railway-alternative) in more depth. [Peon](https://peon.sh/) is one of the self-hosted options.
