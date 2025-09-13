# Plex

Reference: [Docker Hub - Plex](https://hub.docker.com/r/linuxserver/plex)

Plex is a media server software. We install the Plex server in our Ubuntu server and can stream our media to the Plex clients that can be installed in yor Android phone, your SmartTV, etc. 

We can start by adding a few more folder for Plex.

```
/home/josep/
├── server/
│   ├── ...
│   └── plex
|       ├── library/
│       └── docker-compose.yml
└── data/
    ├── ...
    └── media/
        ├── transcode/
        ├── movies/
        └── tv/
```

```bash
cd server/plex
nano docker-compose.yml
```

Copy the contents of the [`docker.compose.yml` file](docker-compose.yml).

Then while in the same folder as the `docker-compose.yml` run:

```bash
docker compose up -d
```

Plex will be available at `http://homeserver:32400/web`.
