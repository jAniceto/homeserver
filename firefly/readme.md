# Firefly III

## Set up

Create the following 3 files:

- [`docker-compose.yml`](docker-compose.yml)
- [`.env`](.env)
- [`.db.env`](.db.env)


Run the following command in the directory where both docker-compose.yml and all configuration files are present.

```bash
docker compose -f docker-compose.yml up -d --pull=always
```

You can follow the progress of the installation by running this command:

```bash
docker compose -f docker-compose.yml logs -f
```

You can now visit Firefly III at `http://localhost` or `http://docker-ip:port`.