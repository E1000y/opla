# opla-front

Opla.ai Frontend using Node es7 react and redux.


## Getting started

### Prerequisites

First of all, make sure you have [Node 8.x](https://nodejs.org/en/download/) and
[Yarn](https://yarnpkg.com/en/docs/install) installed.

This project requires a backend application to start. At the moment, you have to
install this [backend application](https://github.com/Opla/backend) by yourself.
In the following, we assume this backend application runs locally and is
available at: `127.0.0.1:8081`.

### Installation

1. Install the (dev) dependencies:

    ```
    $ yarn install
    ```

2. Run the configuration tool:

   ```
   $ bin/opla init
   ```

3. Start the dev environment:

    ```
    $ yarn dev
    ```

This application should be available at: http://127.0.0.1:8080/.

## Docker Image

By default, on docker run, the app will run opla/bin init to try to connect to the backend and register a new app. Please populate `OPLA_API_DOMAIN` and `OPLA_FRONT_CLIENT_NAME` env variables for the frontend to be able to register the backend app properly.

### Configuration
You have 2 options: 
    1. pass ENV variables to override config properties one by one. See Dockerfile `ENV` statement for available environment variables.
    2. override `default.json` by mounting your own `/src/config/config.json` file. You can create such a file for a specific backend instance, by running `bin/opla init` locally, provided that you can connect to that backend.

### Helm charts
Helm charts get published at https://opla.github.io/front
You can fetch charts this way : 
```
helm repo add https://opla.github.io/front
helm repo update
helm fetch opla-front/opla-front
```

## Contributing

Please, see the [CONTRIBUTING.md](../CONTRIBUTING.md) file.


## Contributor Code of Conduct

Please note that this project is released with a [Contributor Code of
Conduct](http://contributor-covenant.org/). By participating in this project you
agree to abide by its terms. See [CODE_OF_CONDUCT.md](../CODE_OF_CONDUCT.md) file.


## License

opla-front is released under the GPL v2.0+ License. See the bundled
[LICENSE](../LICENSE) file for details.
