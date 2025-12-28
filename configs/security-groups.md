# Security Groups (summary)

## Proxy Server SG
- Inbound: SSH (22) from your IP (or Anywhere for lab)
- Outbound: Allow all (default)

## Application Server SG
- Inbound: SSH (22) allowed from Proxy Server (recommended)
- Outbound: Allow all (default) so it can reach NAT + DB over peering (tighten in prod)

## Database Server SG
- Inbound: SSH (22) from Application Server / Proxy (lab)
- Inbound: DB port from Application Server (recommended; add the specific DB port you use)
- Outbound: Allow all (default)
