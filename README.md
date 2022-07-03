# influxdb2-docker-monitoring

A way to monitor the docker containers running on localhost.

## Installation

- Run `cp .env.example .env`
- Fill the first part of the values
- Run `docker-compose up`
- Connect with your user and password from your `.env` to your server on `http://your-server:8086`
- Navigate to `Load data` > `Telegraf` > `Docker Monitoring` > `Setup Instructions` and click `GENERATE NEW API TOKEN`. Copy the value to your `.env`, in front of the `TELEGRAF_INFLUXDB_TOKEN` key
- Fill the `DOCKER_GID` value in your `.env` with the value printed by `stat -c '%g' /var/run/docker.sock` on your host machine
- Run `docker-compose down` and `docker-compose up` to reload the environment variables
- You should be able to contemplate graphs in `Dashboards` > `Docker` at `http://your-server:8086`.
