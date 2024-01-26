# splunk-with-addon-builder

Splunk instance using Docker with Splunk Add-on Builder pre installed

## Pre-installed Splunk Apps

- [Splunk Add-on Builder v4.1.4](https://splunkbase.splunk.com/app/2962/release/4.1.4/download)
- [Splunk Common Information Model (CIM)](https://splunkbase.splunk.com/app/1621/release/5.3.1/download)

## Setup

1. Copy `.env.example` to `.env`.
2. Edit the Splunkbase credentials and Splunk WebUI password in `.env`.
3. Add Splunk Developer license in `license` folder. Rename the file to `splunk.license`.
4. Start the server by running `docker-compose up -d`. Wait about 5 minutes for the server to come up.
5. Access the webui on <http://localhost:8000>. Login with username `admin` and password configured in `.env` file.

When you're done with the instance, run `docker-compose down` to stop the instance. All Splunk changes will be saved.

## Clean up

Run command `docker-compose down -v` to delete the containers and volumes.
