# JavaScript

This is the development setup focused primarily on JavaScript development. It uses Snowpack to allow Hot Module Replacement (HMR) to get live reloading in the browser.

<br>

## Node.js

Follow these procedures to install the development setup directly in your local machine.

```bash
# Change directory to javascript directory.
cd path/to/sandboxes/javascript

# Installs the development setup dependencies.
npm ci

# Starts the development server.
npm start
```

## Docker

Follow these procedures to install the development setup in a Docker container running in your local machine.

```bash
# Change directory to javascript directory.
cd path/to/sandboxes/javascript

# Create the docker image.
docker build -t "sandboxes/javascript" "."

# Create the docker container.
docker stop "sandboxes-javascript"; docker run --name "sandboxes-javascript" -v "$PWD/src:/usr/sandbox/javascript/src" -p "3003:3003" --rm -td "sandboxes/javascript"

# Connect to the docker container & start the development server.
docker exec -it "sandboxes-javascript" /bin/bash -c "npm start"
```

## Codesandbox

Use Codesanbox in cases where you need a online version of the development setup.

[Create sandbox](https://githubbox.com/johanwestling/sandboxes/tree/master/javascript)

<br>
