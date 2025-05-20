To run setup with Docker Compose and then execute tests using the k6 container, follow these steps:

1. Start All Services with Docker Compose
From your project root (where docker-compose.yml is now located), run:

docker-compose up -d

This will start all services (influxdb, grafana, chronograf, k6, and typescript-starter) in the background.

2. Run k6 Load Test Using Docker
To execute your k6 test script, run:

docker-compose run --rm k6 run /scripts/1-smoke-test.js



This command will use the k6 service to run the test script located at stress-test.js inside the container.

You can view Grafana dashboards at: http://localhost:3000/
To stop all services, use:

docker-compose down

