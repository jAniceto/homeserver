# Jellyfin

Reference: [Jellyfin Container Installation](https://jellyfin.org/docs/general/installation/container)

An open-source alternative to Plex is Jellyfin.

Create persistent storage for configuration and cache data. Create two directories on the host and use bind mounts:

```
/home/josep/
├── server/
│   ├── ...
│   └── jellyfin
|       ├── cache
│       └── config
└── data/
    ├── ...
    └── media
        ├── books
        ├── movies
        └── tv
```

Create a `docker-compose.yml` file with the following contents.

```bash
cd server/jellyfin
nano docker-compose.yml
```

Copy the contents of the [`docker.compose.yml` file](docker-compose.yml).

Then while in the same folder as the `docker-compose.yml` run:

```bash
docker compose up -d
```

Jellyfin will be available at `http://homeserver:8096`.

Note: If the startup wizard does not show, try to clear browser cache.