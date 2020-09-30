# CSS

This is the development setup focused primarily on CSS development. It uses Snowpack to allow Hot Module Replacement (HMR) to get live reloading in the browser.

<br>

## Node.js

Follow these procedures to install the development setup directly in your local machine.

```bash
# Change directory to css directory.
cd path/to/sandboxes/css

# Installs the development setup dependencies.
npm ci

# Starts the development server.
npm start
```

## Docker

Follow these procedures to install the development setup in a Docker container running in your local machine.

```bash
# Change directory to css directory.
cd path/to/sandboxes/css

# Create the docker image.
docker build -t "sandboxes/css" "."

# Create the docker container.
docker stop "sandboxes-css"; docker run --name "sandboxes-css" -v "$PWD/src:/usr/sandbox/css/src" -p "3002:3002" --rm -td "sandboxes/css"

# Connect to the docker container & start the development server.
docker exec -it "sandboxes-css" /bin/bash -c "npm start"
```

## Codesandbox

Use Codesanbox in cases where you need a online version of the development setup.

[Create sandbox](https://githubbox.com/johanwestling/sandboxes/tree/master/css)

<br>
