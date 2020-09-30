# Sandboxes

Various development setups for creating a sandbox in Node.js, Docker, or Codesandbox.

<br>

## Requirements

These development setups require one of the following to be able to run.

* **Node.js** _(Native)_

  Terminal with node version 12 or newer.

  ```bash
  node -v
  ```

  [Download Node.js](https://nodejs.org/en/download/)

* **Docker** _(Container)_

  Terminal with docker version 19 or newer.

  ```bash
  docker -v
  ```

  [Download Docker](https://docs.docker.com/engine/install/)

* **Codesandbox** _(Online)_

  Signed in with Github or Google account.

  [Codesanbox.io](https://codesandbox.io/signin)

<br>

## Setups

### HTML

This is a setup with primarily HTML development in mind. It uses Snowpack to allow Hot Module Replacement (HMR) to get live reloading in the browser.

#### Node.js

```bash
# Change directory to html directory.
cd path/to/sandboxes/html

# Installs the development setup dependencies.
npm ci

# Starts the development server.
npm start
```

#### Docker

```bash
# Change directory to html directory.
cd path/to/sandboxes/html

# Create the docker image.
docker build -t "sandboxes/html" "."

# Create the docker container.
docker run --name "sandboxes-html" -v "$PWD/src:/usr/sandbox/html/src" -p "80:80" --rm -td "sandboxes/html"

# Connect to the docker container.
docker exec -it "sandboxes-html" /bin/bash

# Starts the development server (within the docker container).
npm start
```

#### Codesandbox

[Create sandbox](https://githubbox.com/johanwestling/sandboxes/tree/master/html)
