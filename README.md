# Docker Network Isolation Lab

Shows that containers on different Docker networks cannot reach each other.

- web1 -> frontend only
- web2 -> frontend + backend (the bridge)
- db   -> backend only

Run: docker compose up -d
Test: docker compose exec web1 ping -c 2 db   (fails)
      docker compose exec web2 ping -c 2 db   (works)
