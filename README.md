# Elastic Search Docker
Quickly spin up a secure (HTTPS) or insecure (HTTP) instance of elasticsearch and kibana


## Usage
* Copy the [env.example](env.example) file to .env and set values. `cp env.example .env && vim .env`
* Start docker `./bin/dev/start`

Based off of your values in the .env file the [start](./bin/dev/start) script will either start
an HTTPS secured version of es and kibana or an HTTP insecured version.

The [docker-compose.yml](docker-compose.yml) file is a just a symlink to [insecure.yml](insecure.yml) so you can
delete it, if you have a conflicting file, and everything will still work.

### Other Scripts
* `./bin/dev/stop` will stop the docker containers
* `./bin/dev/clean` will remove any docker artfacts (run if you are switching between secure and insecure)
* The [es_functions](./bin/dev/es/es_functions) script has bash functions to call elasticsearch API endpoints from in a docker container
* The [kibana_functions](./bin/dev/kibana/kibana_functions) script has bash functions to call kibana endpoints from in a docker container
