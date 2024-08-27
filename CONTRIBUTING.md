# Contributing guide

## Bugs and feature requests

Both bugs and feature requests can be filed in the Github issue tracker, as well as general questions and feedback.

Bug reports are of course welcome, especially those reported with [short, self-contained, correct examples](http://sscce.org/).

## Development

### Quick start

You'll need Python>=3.12 to build the backend and Node>=20 to build the frontend. Then, you can install dependencies and run the dashboard with:
```sh
make install
make build-frontend
make serve-dashboard
```

### Backend

Install backend dependencies with
```sh
make install
```

You can run the API server with
```sh
make serve-api
```

When dependencies are changed in `pyproject.toml` the lockfiles should be updated via [`pip-compile`](https://github.com/jazzband/pip-tools):
```sh
make pip-compile
```

### Frontend

Install frontend dependencies with
```sh
npm install
```
in the `frontend` directory.

Run the frontend in dev mode (for hot-reloading) with
```sh
npm run dev
```
in the `frontend` directory


Then, to use the frontend
```sh
make build-frontend
make serve-dashboard
```

### Documentation

To build the docs:
```sh
make build-doc
```

Then, you can access the local build via:
```sh
open doc/_build/html/index.html
```