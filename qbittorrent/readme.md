# Set up qbittorrent

Reference: [Docker Hub qbittorrent](https://hub.docker.com/r/linuxserver/qbittorrent)

Set up directories.

```bash
cd ~
mkdir -p server/bittorrent/appdata
mkdir downloads
```

Create a `docker-compose.yml` file with the following contents.

```bash
cd server/qbittorrent
nano docker-compose.yaml
```

Then while in the same folder as the `docker-compose.yml` run:

```bash
docker compose up -d
```

The web UI is available at `http://homeserver:8080`.