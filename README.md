# Flask Weather — CI/CD Lab

A Flask weather app packaged with Docker and delivered through a Jenkins pipeline, with Ansible for post-deploy configuration.

Built as a hands-on DevOps training project (Orange Digital Center / personal practice).

## What this shows

- Application containerization with **Docker**
- CI/CD with **Jenkins** (checkout → build image → push registry → Ansible)
- Configuration automation with **Ansible**
- Simple Flask + OpenWeather API workflow

## Pipeline flow

```text
Git checkout → Docker build → Docker Hub push → Ansible playbook
```

## Key files

- `app.py` — Flask application
- `Dockerfile` — container image
- `Jenkinsfile` — CI/CD pipeline
- `playbook.yaml` / `ansible.cfg` / `hosts` — Ansible deployment config

## Run locally

```bash
docker build -t flask-weather .
docker run --rm -p 5000:5000 flask-weather
```

> Configure API keys and credentials in your own environment — do not commit secrets.
