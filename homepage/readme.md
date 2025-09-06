# Set up Homepage

Reference: [Docker Installation](https://gethomepage.dev/installation/docker/)

Set up directory for configuration file, for instance, in your `/home` directory:

```bash
cd ~
mkdir -p server/homepage/config
```

Create a `docker-compose.yml` file:

```bash
cd server/homepage
nano docker-compose.yml
```

Start Docker container:

```bash
docker compose up -d
```

Going to `http://hostname:3000`, you should see your homepage.