# Installing a self-hosted PaaS: server prerequisites checklist

A clean install saves hours later. Check these first:

- A supported OS, ideally a current Ubuntu or Debian LTS.
- At least 2 GB RAM for the platform plus a small app; builds are the memory peak.
- Ports 80 and 443 open in both the server firewall and any cloud firewall.
- A DNS record for the dashboard pointing at the server.
- Swap configured on small servers so builds do not get OOM killed.
- Time sync enabled (`timedatectl`), since TLS and tokens depend on correct clocks.

```
free -h
df -h /
sudo ss -tlnp | grep -E ':80|:443'
timedatectl
```

Anything already listening on 80 or 443, such as an old Nginx, will conflict with the platform proxy.

The [Peon installation guide](https://peon.sh/docs/installation) has the install command and supported systems. [Peon](https://peon.sh/) is open source and self-hosted.
