# homeserver

Home server documentation and configuration files


## Initial setup and requirements

1. Install Ubuntu Server

2. Set up directory structure (see below)

3. Set up [Docker](https://docs.docker.com/engine/install/ubuntu/) and [Docker Compose](https://docs.docker.com/compose/install/linux/#install-using-the-repository)

4. Set up desired services


## Directory structure

```
/home/josep/
├── server/
│   ├── audiobookshelf
│   ├── jellyseerr
│   ├── immich
│   ├── paperless
│   └── ...
└── data/
    ├── audiobooks
    ├── movies
    └── tv
```

The `server` folder contains all the configuration and metadata files for each service. The `data` folder contains the actual media (videos, audios, etc.)
