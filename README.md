# Elastic Search Docker


## Usage
* Copy the [env.example](env.example) file to .env and set values. `cp env.example .env && vim .env`
* Start docker `./bin/dev/start`

Based off of your values in the .env file the [start](./bin/dev/start) script will either start
an HTTPS secured version of es and kibana or an HTTP unsecured version.

The [docker-compose.yml](docker-compose.yml) file is a just a symlink to [insecure.yml](insecure.yml) so you can
delete it, if you have a conflicting file, and everything will still work.
