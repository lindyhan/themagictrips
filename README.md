<h2>Table of Contents</h2>

- [Prerequisites](#prerequisites)
- [Quickstart](#quickstart)
  - [Medusa](#medusa)
  - [Storefront](#storefront)


## Prerequisites

- Node >= 20
- Yarn >= 3.5
- Docker and Docker Compose
- Stripe account (for payments)

## Quickstart

```bash
git clone git@github.com:Agilo/fashion-starter.git
```

### Medusa

```bash
cd medusa

# Create the .env file
cp .env.template .env

# Install dependencies
yarn

# Spin up the database and Redis
docker-compose up -d

# Build the project
yarn build

# Run the migrations
yarn medusa db:migrate

# Seed the database
yarn seed

# Create an user
yarn medusa user -e "admin@medusa.local" -p "supersecret"

# Start the development server
yarn dev
```

At this point, you should be able to access the Medusa admin at http://localhost:9000/app with the credentials you just created. After logging in, you should go to http://localhost:9000/app/settings/publishable-api-keys, copy the publishable key, and paste it into the `NEXT_PUBLIC_MEDUSA_PUBLISHABLE_KEY` env variable in the `storefront/.env.local` file.

### Storefront

```bash
cd storefront

# Create the .env.local file
cp .env.template .env.local

# Install dependencies
yarn

# Start the development server
yarn dev
```

You should now be able to access the storefront at http://localhost:8000.

<a href="https://agilo.com" target="_blank">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github.com/user-attachments/assets/a4429448-a08a-4f5a-8195-2cea1416ca87">
    <img src="https://github.com/user-attachments/assets/772994f8-32c6-4b27-832f-2660f833fd78">
  </picture>
</a>
