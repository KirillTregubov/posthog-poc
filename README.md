[PostHog repo self-hosting README](https://github.com/PostHog/posthog?tab=readme-ov-file#self-hosting-the-open-source-hobby-deploy-advanced)
- States it scales to approximately 100k events per month

[GitHub Deploy Script](https://raw.githubusercontent.com/posthog/posthog/HEAD/bin/deploy-hobby) or in repo at [deploy-hobby.sh](./deploy-hobby.sh)
- Needs to run in a Linux environment with at least 4 vCPU, 16GB of RAM, 30GB of disk space
- Uses `docker-ce`, specifically `docker-compose`
- Uses [Clickhouse](https://clickhouse.com/), Postgres and Redis as databases, which the script sets up in the container
- Uses Kafka for event streaming, which the script sets up in the container
- Uses Caddy for reverse proxy