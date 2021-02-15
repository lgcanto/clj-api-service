# Running Code Analysis
- After all containers are up, attach shell to the `clf-api-service_backend` container and execute:
```bash
sonar-scanner
```

- Go to http://localhost:9000/dashboard?id=clj-api-service-backend to see the quality report