# open5e

[![Build Status](https://travis-ci.org/eepMoody/open5e.svg?branch=master)](https://travis-ci.org/eepMoody/open5e)

An SRD and open-source material reference site for 5th edition D&amp;D

## Contributing

Open5e is a community project driven by a small number of volunteers in their spare time. We welcome any and all contributions! Please join our Discord to help out: https://discord.gg/9RNE2rY or check out the issue board if you'd like to see what's being worked on!

# Starting the Server

The Django API uses Django REST Framework for its browsability and ease of use when developing CRUD endpoints.

## Server Quickstart

The server runs in a docker container. You'll need to first install docker on your system, then getting it running is extremely simple:

starting from root `/open5e` directory:

``` bash
export OPEN_5E_ROOT=`pwd` #set the /server folder as the root of the Python project
export DJANGO_SECRET='@pt#ouh)@!c+2eh(!aj_vtc=s7t$uk-l1!ry3^fcercz%si01@' # this should be a nukable test key that you're manually replacing at startup time for production
docker-compose up
```

You will want to leave the server terminal running while you launch the UI in a separate termainal so you can observe requests.


# Building the UI layer

Open5e uses the Nuxt framework for Vue.js, which takes care of a lot of the architectural work for the frontend layer while allowing a large amount of flexibility.

## Build Setup

From /open5e

``` bash
cd ui
# install dependencies
$ npm install # Or yarn install

# serve with hot reload at localhost:3000
$ npm run dev
```

Other build options:
```
# build for production and launch server
$ npm run build
$ npm start

# generate static project
$ npm run generate
```

For detailed explanation on how things work, checkout the [Nuxt.js docs](https://github.com/nuxt/nuxt.js).
