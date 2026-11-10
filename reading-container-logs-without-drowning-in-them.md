# Reading container logs without drowning in them

During an incident, scrolling `docker logs` from the top wastes time. These habits help.

```
docker logs --since 15m --tail 200 app
docker logs -f app 2>&1 | grep -iE "error|fatal|panic"
docker inspect --format '{{.State.ExitCode}} {{.State.OOMKilled}}' app
```

- Start with `--since` matching when the alert fired.
- Check the exit code and the OOM flag before reading anything else. Exit 137 with OOMKilled true is a memory limit, not a bug in the last commit.
- Log in a structured format (JSON lines) so you can filter by field later.
- Set log rotation (`max-size`, `max-file`) so logs never fill the disk.

A browser-based terminal into the container is handy for quick checks when you are away from your laptop. The Peon docs on [logs and web terminal](https://peon.sh/docs/logs-and-terminal) describe that setup. I work on [Peon](https://peon.sh/).
