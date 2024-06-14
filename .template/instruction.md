#### Local Microservice Development Dependencies use mock servers to conduct tests even when the target service is not running.

#### The advantages of using mock servers for testing are as follows:

#### 1. Independence: Tests can be conducted independently without being affected by the state of other services or systems.

#### 2. Speed: Responses are received faster than actual API calls, improving test speed.

#### 3. Cost Reduction: Costs associated with external API calls are reduced.

#### 4. Stability: Tests are not affected by the instability or downtime of external services.

#### 5. Support for Early Development Stages: Tests can be conducted even in the early stages of development when the actual API is not yet ready.

#### Local Microservice Development Dependencies use the Given-When-Then pattern to structure test code consistently and clearly. The setup can be done as follows:

### How to Create Test Codes

#### 1. In the modeling stage, create a Policy or Command sticker and attach it to an Aggregate sticker.

#### 2. To create Examples for the Given-When-Then pattern, set Relations as Event - Policy or Command - Event.

#### 3. Click 'Examples' on the Policy or Command sticker panel and create examples according to the Given-When-Then pattern.

### How to run
```
cd <microservice> // The microservice where the test code is created
cd infra
docker-compose up
```

### Includes:
  - OpenAPI 3.0 API & Mock Generation for Dependency Services
  - Mock Server (Microcks)
  - API Documentation (Swagger UI)
  - Kafka Server and Async API (Microcks)

### Files will be Generated
```
infra
  docker-compose.yml
  api
    openapi.yaml
```

### Reimporting API
Just referesh the all of the services:
```
docker-compose down
docker-compose up
```
or run the importer service only:
```
docker-compose -f start importer
```
