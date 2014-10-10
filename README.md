# Postcodes.io [![Build Status](https://travis-ci.org/ideal-postcodes/postcodes.io.png)](https://travis-ci.org/ideal-postcodes/postcodes.io)

Free Postcode API server using the Office for National Statistics' postcode directory.

Documentation can be found at [postcodes.io](http://postcodes.io)

## Requirements

Please make sure you have the following available:

- Node (>= v0.10) [(Instructions)](http://nodejs.org/)
- Postgres with PostGIS extension [(Instructions)](http://postgis.net/install)

## Install & Download Data & Run

**Download and install**

```bash
$ git clone https://github.com/ideal-postcodes/postcodes.io.git

& cd postcodes.io/ && npm install
```

**Configure Postgres and Seed Database**

Postcodes.io is packaged with a script to setup and download the ONS Postcode Directory. To run this, navigate into the repository directory and run,

```
$ npm run setup
```

This script will prompt you for Postgres superuser credentials. This privilege is required to create a new user, database, extensions and then to load the data. For the security conscious, you can find out how this works by [reading our installation notes](http://postcodes.io/docs#Install-notes) and [the script itself](/bin/setup.sh). Other install methods are available but require a bit of extra work.

You can change the Postgres username/password yourself but you will need to update 'config/config.js' with the relevant credentials.

The import process takes around 10 minutes to complete.

**Run it**

```
node server.js // Default environment is development
```

## Contributions

Contributions are welcome. 

## Testing

```
npm test
```

## License 

MIT