# Docker Ofelia acme.sh

#### This runs a cron schedule within a docker container to renew ssl certificates generated by https://acme.sh

## Setup:

1. Copy the [crontab-sample](crontab-sample) to `crontab`
1. If you already have existing acme.<span>sh certs, place the files in the following file structure
```
acme.sh
|
|__ certs
|	|
|	|__ example.com (dir)
|	|
|	|__ mysite.com (dir)
|
|__ configs
	|
	|__ ca (dir)
	|
	|__ account.conf (file)
	|
	|__ http.header (file)
```

## Run:

```bash
docker-compose up -d
docker-compose logs
```

## Generate a new wildcard cert:

```bash
./scripts/new-cert.sh --help
```

## Manually run acme.sh commands:

```bash
./scripts/shell.sh
```
