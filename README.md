
# infra_landing_page

A lightweight, Dockerized landing page built with Vite, React, and Tailwind CSS.  
CI/CD is powered by GitHub Actions and Ansible, targeting a self-hosted environment with Traefik for routing.

## Features

- ⚡ Fast build using Vite
- 🎨 Styled with Tailwind CSS
- 🐳 Dockerized for consistent deployment
- 🔁 GitHub Actions + Ansible for automated CI/CD
- 🌐 Hosted at [landing.sevensteves.com](https://landing.sevensteves.com)

## Development

To start the development server:

```bash
cd web
npm install
npm run dev
````

## Build & Run with Docker

```bash
docker build -t infra_landing_page web
docker run -p 8080:3000 infra_landing_page
```

## Deployment

* Docker image is built and pushed via GitHub Actions
* Deployed with Ansible to `sjl-dwork-01.home`
* Configured for HTTPS access through Traefik
