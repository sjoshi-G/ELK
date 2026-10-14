# ELK Security Monitoring Lab

Security monitoring dashboards built with the ELK Stack (Elasticsearch, Logstash/Beats, Kibana), visualizing authentication failures, sudo activity, and system events to surface anomalies.

## What it does

- **Authentication failures dashboard** — failed logins by user, source IP, and time; highlights brute-force patterns.
- **Sudo activity dashboard** — privileged command usage across hosts.
- **System events dashboard** — service changes, system anomalies, and event timelines.

## Screenshots

_(The 4 dashboard PNGs in this repo.)_

## How to reproduce

1. Install Elasticsearch and Kibana (same version).
2. Ship Linux auth/syslog data with Filebeat (sample config notes below).
3. In Kibana: **Stack Management → Saved Objects → Import** and load `kibana-dashboards.json` from this repo.
4. Generate activity (e.g., failed SSH logins) and watch the dashboards populate.

```yaml
# filebeat.yml (example input)
filebeat.inputs:
  - type: log
    enabled: true
    paths:
      - /var/log/auth.log
      - /var/log/syslog
