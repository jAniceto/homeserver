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
    ├── torrents
    │   ├── books
    │   ├── movies
    │   └── tv
    └── media
        ├── books
        ├── movies
        └── tv
```

The `server` folder contains all the configuration and metadata files for each service. The `data` folder contains the actual media (videos, audios, etc.)


## Services 

Overview of several services for a Home Server.


### Dashboard

- [Homepage](https://gethomepage.dev/configs/)
- [Glance](https://github.com/glanceapp/glance)


### Files

- [File Browser](https://github.com/filebrowser/filebrowser) and currently [FileBrowser Quantum](https://github.com/gtsteffaniak/filebrowser)
- [NextCloud](https://nextcloud.com/install/#instructions-server)
- OwnCloud
- [Syncthing](https://syncthing.net/)
- [Samba](https://www.samba.org/)
  [Kopia](https://kopia.io/docs/getting-started/)


### Media libraries and management

- [Calibre](https://calibre-ebook.com/) and [Calibre-Web](https://github.com/janeczku/calibre-web)
- [audiobookshelf](https://www.audiobookshelf.org/)
- [Paperless-ngx](https://docs.paperless-ngx.com/) - Scan, OCR and organize documents
- [Karakeep](https://karakeep.app/) - bookmark anything


### Server and Networking

- [Caddy](https://caddyserver.com/) - Reverse proxy
- [Uptime Kuma](https://uptimekuma.org/) - Server status monitoring


### Documentation and knowledge base

- [Outline](https://www.getoutline.com/)
- [Joplin](https://joplinapp.org) - Note-taking app


### Personal data tracking

- [Statistics for Strava](https://github.com/robiningelbrecht/statistics-for-strava) - Additional stats from your Strava data
- [Firefly III](https://docs.firefly-iii.org/how-to/firefly-iii/installation/docker/) - Personal finance manager 
- [Dawarich](https://dawarich.app/) - Self-hosted alternative to Google Timeline


### Utilities

- [Stirling-PDF](https://github.com/Stirling-Tools/Stirling-PDF)
- [ntfy](https://github.com/binwiederhier/ntfy) - Send push notifications


## Resources

- [MediaStack.Guide](https://mediastack.guide/), [MediaStack.Guide Github](https://github.com/geekau/mediastack)
- [r/SelfHosted Wiki](https://wiki.r-selfhosted.com/)
- [arr Stack example docker-compose](https://gist.github.com/Webreaper/81ecda3ecc45fa61a16dfc90cfc4550d)
- [Awesome *Arr](https://github.com/Ravencentric/awesome-arr)
- [Synology arr guide](https://github.com/MathiasFurenes/synology-arr-guide)
- [Workshop How2Homelab](https://projects.franciscoribeiro.pt/workshops/glua/how2homelab_practical_guide.html)
- [Looking for a minimal-fluff guide to first home server setup for technical people](https://www.reddit.com/r/HomeServer/comments/17vcllp/looking_for_a_minimalfluff_guide_to_first_home/)
- [The complete guide to building your personal self hosted server for streaming and ad-blocking](https://www.reddit.com/r/Piracy/comments/pqsomd/the_complete_guide_to_building_your_personal_self/)
- [Techno TIm](https://technotim.live/)
- [TechHutTV Wiki](https://github.com/TechHutTV/homelab)
- [awesome-selfhosted](https://awesome-selfhosted.net)
