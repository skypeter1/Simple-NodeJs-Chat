## Simple Websocket Chat App

A simple chat app using Node.js, Express, and Socket.IO.

### Prerequisites

- Node.js 20+
- npm
- Docker (for container targets)
- Make

### Run locally (Node)

```bash
make build
make run-app
```

Or without Make:

```bash
npm install
npm start
```

Open http://localhost:8080/

### Makefile targets

| Target | Description |
| --- | --- |
| `make` / `make default` | Show image/app info |
| `make env-info` | Print application/image variables |
| `make test` | Install deps and smoke-check imports |
| `make build` | Install npm dependencies |
| `make run-app` | Run the app with Node on port 8080 |
| `make build-image` | Build the Docker image |
| `make run-local-image` | Build and run the app in Docker on port 8080 |
| `make shell` | Build the image and open a shell inside it |
| `make stop` | Stop/remove the local container |
| `make clean` | Stop container, remove image, delete `node_modules` |

### Run with Docker

```bash
make run-local-image
```

Open http://localhost:8080/

Stop the container with:

```bash
make stop
```

Open an interactive shell in the image:

```bash
make shell
```

### Deploy to Cloud Foundry

You'll need the CF CLI installed.

```bash
cf login -a <endpoint> -u <user> -o <org> -s <space>
cf push -f manifest.yml
```
