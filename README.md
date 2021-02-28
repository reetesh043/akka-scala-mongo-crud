## akka-scala-mongo-crud
CRUD  application to show how to use akka-http and akka-stream with mongo in scala

### Run Application
Start the mongodb docker container
```
docker-compose up -d
```

Compile the code using below command
```
sbt compile
```

Run the application
```
sbt run
```

### Request
Create an employee

```
curl --location --request POST 'http://localhost:8081/api/employee/create' \
--header 'Content-Type: application/json' \
--data-raw '{
"name":"reetesh",
"dateOfBirth":"1998-01-03"
}'
```

Get employees data

```
curl --location --request GET 'http://localhost:8081/api/employee/search'
```