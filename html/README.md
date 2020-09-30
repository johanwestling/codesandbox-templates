# HTML

This is the development setup focused primarily on HTML development. It uses Snowpack to allow Hot Module Replacement (HMR) to get live reloading in the browser.

<br>

## Node.js

Follow these procedures to install the development setup directly in your local machine.

```bash
# Change directory to html directory.
cd path/to/sandboxes/html

# Installs the development setup dependencies.
npm ci

# Starts the development server.
npm start
```

## Docker

Follow these procedures to install the development setup in a Docker container running in your local machine.

```bash
# Change directory to html directory.
cd path/to/sandboxes/html

# Create the docker image.
docker build -t "sandboxes/html" "."

# Create the docker container.
docker run --name "sandboxes-html" -v "$PWD/src:/usr/sandbox/html/src" -p "80:8080" --rm -td "sandboxes/html"

# Connect to the docker container.
docker exec -it "sandboxes-html" /bin/bash

# Starts the development server (within the docker container).
npm start
```

## Codesandbox

Use Codesanbox in cases where you need a online version of the development setup.

[Create sandbox](https://githubbox.com/johanwestling/sandboxes/tree/master/html)

<br>
