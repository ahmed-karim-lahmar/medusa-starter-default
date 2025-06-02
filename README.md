# Medusa Starter

### Prerequisites

- Linux or WSL with Ubuntu installed for Windows
- Node.js v20+ with yarn (use nvm)
- Docker with Docker Compose

### Project Setup

```
- Clone the repo

1- Postgres db:
- cp .env.template .env
- Add POSTGRES_USER and POSTGRES_PASSWORD in .env
- docker compose up -d

2- Backend:
- cd backend && yarn install
- cp .env.template .env
- Change username and password in DATABASE_URL
- npx medusa db:migrate
- yarn seed
- npx medusa user -e <email_addr> -p <password>
- yarn dev
- Navigate to localhost:9000/app and login
- Copy the publishable api key from settings > publishable api keys

3- Frontend:
- Open a new terminal at the root of the project
- cd frontend
- cp .env.local.template .env.local
- paste the api key in NEXT_PUBLIC_MEDUSA_PUBLISHABLE_KEY
- yarn install
- yarn dev
- Navigate to localhost:8000
```
