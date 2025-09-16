# Statistics for Strava

Reference: [Statistics for Strava Docs](https://statistics-for-strava-docs.robiningelbrecht.be/#/getting-started/installation)


## Preparation

You need to start by setting up a API in Strava at [strava.com/settings/api](https://www.strava.com/settings/api).

- Copy the `Client ID` and `Client Secret`, you'll need these during the installation.
- Make sure the `Website` and `Authorization Callback Domain` are set to the url you will host your app on. Something like `192.168.1.235`.
- Make sure to add an `App Icon`. You can find this setting at the bottom of the API settings page. 


## Setup

Create the necessary directories.

```bash
cd ~
mkdir server/statistics-for-strava
cd server/statistics-for-strava
```

Create the [`docker-compose.yml`](docker-compose.yml) file.

Create the [`.env`](.env) file. Fill in the Strava API data. Do not change the `STRAVA_REFRESH_TOKEN` variable. 

Note: Every time you change the `.env` file, you need to recreate (for example; docker compose up -d) your container for the changes to take effect (restarting does not update the `.env`). 

Create the [`config/config.yml`](config/config.yml) file. Most of the defaults are OK, however some required data must be added:

- Add `appUrl`. Should be something like `http://192.168.X.XXX:XXXX/`.
- Add birthday in `birthday`.
- Add your weights over time in `weightHistory`.


To run the application run the following command:

```bash
docker compose up -d
```

The docker container is now running; navigate to http://homeserver:8080/ to access the app.

On the first start up you must authorize the app on the Strava API. Following this procedure will give you the `STRAVA_REFRESH_TOKEN`. Input this into the `config.yml` file and restart the container.

You can npw import the data and access the app.


## Import and build statistics

Once you have successfully authenticated with Strava, you can import your data and build the html files, after which you can view your statistics.

```bash
docker compose exec app bin/console app:strava:import-data
docker compose exec app bin/console app:strava:build-files
```

Importing will take some time on the first run to avoid Strava API rate limits.


## Scheduling

To schedule the updates and build commands you can use the host system crontab.

```bash
crontab -e
```

Then add the following. This will run the import and build scripts every day at 04:00.

```
0 4 * * * cd ~/server/statistics-for-strava && docker compose exec --user josep app bin/console app:strava:import-data && docker compose exec --user josep app bin/console app:strava:build-files
```
