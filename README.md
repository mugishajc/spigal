# spigal

A Spring Boot REST service backed by MongoDB, managing student records with embedded documents.

## Data model

`Student` document:

- `firstname`, `lastname`, unique `email`
- `gender` (enum)
- `address` (embedded document: country, city, postcode)
- `favouriteSubjects` (list of strings)
- `totalSpentInBooks` (BigDecimal)
- `created` (timestamp)

## Stack

- Java 17, Spring Boot, Spring Data MongoDB, Lombok
- MongoDB and Mongo Express via Docker Compose

## Running

Start MongoDB and Mongo Express:

```bash
cd spigal
docker compose up -d
```

Mongo Express is then at `http://localhost:8081`. Start the app:

```bash
./mvnw spring-boot:run
```

Connection settings live in `src/main/resources/application.properties`.
