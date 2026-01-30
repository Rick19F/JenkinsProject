# Jenkins Project

This project sets up a Jenkins server using Docker.

## Prerequisites

- Docker
- Docker Compose

## Setup

1. Copy `env.example` to `.env`:

   ```bash
   cp env.example .env
   ```

2. Configure the environment variables in `.env` as needed.

## Usage

Start the Jenkins server:

```bash
docker-compose up -d
```

Stop the Jenkins server:

```bash
docker-compose down
```

View logs:

```bash
docker-compose logs -f
```

## Access

Jenkins will be available at `http://localhost:8080`

## Initial Admin Password

The initial admin password can be found in the Jenkins container:

```bash
docker exec -it jenkins cat /var/jenkins_home/secrets/initialAdminPassword
```
