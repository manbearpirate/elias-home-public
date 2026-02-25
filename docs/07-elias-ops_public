## What Elias Is
- A Raspberry Pi-based home services box
- Runs Docker + Portainer (container management UI)
- Can run Plex (media server)
- Reads media from a NAS (Movies/TV shares)
- Monitored by a separate device (“Tobias”) running Uptime Kuma + Netdata

---

## High-Level Architecture
- **Elias**: primary services host (Docker)
- **NAS**: stores media (Movies/TV/Music shares)
- **Tobias**: monitoring + alerting (Uptime Kuma + Netdata)
- **Clients**: TV/Roku, phones, web browsers

---

## Daily Health Check (1 minute)
1) Confirm Elias is reachable (SSH or web UI)
2) Confirm Portainer is reachable
3) Confirm monitoring dashboard shows green
4) (Optional) Confirm NAS is reachable

---

## Docker Operations (Elias)

### List containers
```bash
docker ps -a
