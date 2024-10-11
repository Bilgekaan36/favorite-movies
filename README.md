# Payload 3.0 Movies Example

This repo showcases Payload 3.0, its support for Postgres (as well as MongoDB), its asset management system and admin dashboard, as well as simple deployment to Vercel.

### Quick Start

### Local Development

#### Create the local development environment file.

```bash
cp .env.example .env.development.local
```

#### Run the script start database script, which uses docker to spin up Postgres.

```bash
./start-database.sh
```

#### Create a payload secret, perhaps using `openssl rand -base64 32` and set that value in the .env.development.local file.

Get a [TMBD API key](https://www.themoviedb.org/settings/api) and add it to the .env.development.local file. You will need an account on TMDB. It's all free.

#### Install the dependencies.

```bash
pnpm i
```

#### Create the database migration file.

```bash
pnpm run payload migrate:create initial
```

#### Run the migration to create the database tables.

```bash
pnpm run payload migrate
```

#### Start up the development server.

```bash
pnpm dev
```
