# Caddy - Docker Compose

This repository contains a Caddy server on docker with docker compose. This can
be used in development and production. This repository is specifically meant for
the Errors Party website and intranet.

## Getting Started

1. Clone the repository on your machine/server.

```sh
git clone https://github.com/ErrorsParty/dc-caddy /srv/ep-caddy
```

2. Navigate into the directory.

```sh
cd /srv/ep-caddy
```

3. Create a docker network for the proxy (frontend) if you haven't already.

```sh
docker network create proxy
```

4. Copy the environment example file.

```sh
cp .env.example .env
```

5. Modify the environment file to your needs.

6. Start the docker compose project.

```sh
docker compose up -d
```

## Trust Root CA

When used in development mode it uses a self signed certificate, this will cause
most browsers to show a warning (which you can skip through).

If you wish to disable this warning only for the Errors Party staging CA you can
trust the CA in your browser.

https://www.techrepublic.com/article/how-to-add-a-trusted-certificate-authority-certificate-to-chrome-and-firefox/
