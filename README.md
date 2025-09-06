# Monitoring

---

# Purpose

Monitoring stack for my home server.

# High Level Design

* Applications are containerized and deployed using Docker Compose.
* Bind mounts are used to persist data, not docker volumes.

# Technologies

* [Node exporter](https://github.com/prometheus/node_exporter)
* [cAdvisor](https://github.com/google/cadvisor)
* [Prometheus](https://prometheus.io/)
* [Grafana](https://grafana.com/)

# Setup

1. Copy environment template and set secrets
   - `cp template.env.bash .env.bash`
   - Edit `.env.bash` and set appropriate values.
2. Start the stack
   - `source .env.bash`
   - `docker compose -f compose/docker-compose.yml up -d`

Note: The `.env.bash` file is git-ignored and used by docker-compose to inject secrets.
 