# Gitlab Docker

Gitlab Docker setup with Runners and Docker Registry support

## Installation

Create `.env` file and populate it with

```
GITLAB_DOMAIN=gitlab.example.com
GITLAB_EMAIL_FROM=email@example.com
GITLAB_SMTP_PASSWORD=password
```

Check config with

```shell
docker-compose config
```

Generate cert

```shell
sudo letsencrypt certonly -a webroot -w /srv/gitlab/letsencrypt -d gitlab.example.com
```

## Usage

```shell
docker-compose up -d
```

## Update

```shell
docker-compose pull
docker-compose up -d
```
