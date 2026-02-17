---
tags:
    - hp
    - personal
---

# Spring 26 Projects
List of projects (coding)

## Homelab!

### Ideas:
- YAML for configs 
    - maybe a config repo?
    - All open ports & why 
    - basic IDS
    - SSH usage logging 
- DB for logins 
    - central auth service - maybe even do cookies?
    - admin vs. user views - configure plex server
    - To-do list / tasks db 
- Central Service inventory - knows what's running, where, etc.
    - /health endpoint for each server!
        - maybe runs through rpi or smth
    - heartbeat system - machines report uptimes and stuff
    - YAML to describe what should be active, server flags when this ain't true
    - expose systemd status across-machines
    - Log aggregator
    - Inbound Connections Log - ASN 
    - API contract validation
- Network Usage visualizer / tracker 
    - Basic CI/CD for services?
    - auto-update OS 
- Site
    - live status page public
    - live dashboard private 
    - what's running page
- ML stuff  
    - monitor network / cpu usage for upticks
    - log clustering
    - ML to supress repetitive logs

- Opentelemetry - traces metrics, logs, etc. across services! 
    - trace requests across everything

- Secure Authentication!
    - Hashicorp Vault - Secret Management, encryption, credentials
    - Authentik - self-hosted SSO and stuff!
    - Tailscale? - apparently can secure access to ssh, postgres, etc.

- Orchestration & Jobs!
    - Nomad - grown-up Systemd
    - Or roll my own systemd service replacer!
    - Docker - keeps stuff separate

- Security!
    - wazuh - SIEM + HIDS

Raspberry Pi - Central Monitor
- firewall!
- Runs central service inventory
- Prometheus - Metrics Collection 
- Grafana - Logs visualization & graphing
- Loki - Log aggregation & indexing

https://chatgpt.com/share/69863765-159c-800c-97ca-df2db5d86c61


## Website
Sync w/ obsidian!
- now page [about now](https://nownownow.com/about)
- public/ folder 
- certain pages use md 
- online cv 

database
- last song
- todos 
- anything else 

dashboard - admin! 
- current servers online
- current services online 
- enable-able public dashboard elements

misc. 
- recommend a book
- recommend a song
- recent song 
- my fav languages 
- blog page - pulls from public/blog
- public page
- how it works? button for certain things

