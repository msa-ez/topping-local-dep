# Unit microservice development toolkits

includes:
- OpenAPI 3.0 API & Mock Generation for Dependency Services
- Mock Server (Microcks)
- API Documentation (Swagger UI)
- Kafka Server and Async API (Microcks)

## Files will be Generated
```
infra
  docker-compose.yml
  api
    openapi.yaml
```

## How to run
```
cd infra
docker-compose up
```

## Reimporting API
Just referesh the all of the services:
```
docker-compose down
docker-compose up
```
or run the importer service only:
```
docker-compose -f start importer
```