# Scorecard Dashboard

A [Grafana](https://grafana.com/) dashboard that visualizes community scorecard (CSC) data: scorecards planned and conducted, participants and indicators, criteria raised, waste-management activities, and data-quality metrics. It reads directly from the CSC web platform's PostgreSQL database and signs users in via the platform's OAuth.

For a guide to reading and using the dashboard itself, see the [User Manual](docs/USER_MANUAL.md).

## Stack

- Grafana OSS 10.1.4 (see [Dockerfile](Dockerfile)), packaged as a Docker image with a custom favicon/logo
- PostgreSQL datasource, provisioned from [grafana/provisioning/datasources/default.yml](grafana/provisioning/datasources/default.yml)
- Dashboard JSON provisioned from [grafana/provisioning/dashboards/dashboard.json](grafana/provisioning/dashboards/dashboard.json) (also used as Grafana's home dashboard)
- Community panel plugin: [alexandra-trackmap-panel](grafana/plugins/alexandra-trackmap-panel) (geospatial map), plus `yesoreyeram-boomtheme-panel`
- Sign-in via generic OAuth against the DCSC web platform

## Getting started

1. Copy the env template and fill in your values:
   ```sh
   cp app.example.env app.env
   ```
2. In `app.env`, set at minimum:
   - `GF_SERVER_ROOT_URL` – the public URL the dashboard will be served from
   - `GF_AUTH_GENERIC_OAUTH_CLIENT_ID` / `GF_AUTH_GENERIC_OAUTH_CLIENT_SECRET` – OAuth app credentials from the DCSC web platform
   - `GF_AUTH_GENERIC_OAUTH_AUTH_URL` / `_TOKEN_URL` / `_API_URL` – the DCSC web platform's OAuth endpoints
   - `GF_SECURITY_ADMIN_USER` / `GF_SECURITY_ADMIN_PASSWORD` – change the defaults before deploying
3. Point [grafana/provisioning/datasources/default.yml](grafana/provisioning/datasources/default.yml) at your PostgreSQL instance (host, database, user, password).
4. Build and run:
   ```sh
   docker compose up --build
   ```
5. Open http://localhost:8000 (or the host/port you've mapped) and sign in with **Sign in with DCSC WEB**, or as the admin user configured in `app.env`.

## Project layout

```
Dockerfile                                Builds the Grafana image, installs branding and plugins
docker-compose.yml                        Local/dev run configuration
app.example.env / app.env                 Grafana environment config (app.env is gitignored)
grafana/grafana.ini                       Base Grafana configuration
grafana/provisioning/datasources/         Datasource provisioning (PostgreSQL)
grafana/provisioning/dashboards/          Dashboard provisioning + dashboard.json (the actual dashboard)
grafana/plugins/                          Vendored/community panel plugins
docs/USER_MANUAL.md                       End-user guide to the dashboard
img/                                      Favicon and logo assets
```

## Editing the dashboard

The dashboard is provisioned as JSON ([grafana/provisioning/dashboards/dashboard.json](grafana/provisioning/dashboards/dashboard.json)), so it is managed as code. Make changes in the running Grafana UI, then export the updated dashboard JSON (Dashboard settings → JSON Model) and commit it back to this file.
