# Verdaccio docker compose set up

This is a simple docker compose set up for [Verdaccio](http://www.verdaccio.org/).

## Usage

1. Clone this repository

2. Create a `.env` file (and change the UID and GID to your own)

```bash
cp .env.sample .env
```

3. Run `docker-compose up -d`

4. You use Verdaccio globally by setting the NPM environment variable to localhost:4873

```bash
export NPM_CONFIG_REGISTRY=http://localhost:4873
```

You can use Verdaccio globally only if it's running with the following command:

```bash
type nc > /dev/null && nc -w1 -z localhost 4873 && export NPM_CONFIG_REGISTRY=http://localhost:4873
```
