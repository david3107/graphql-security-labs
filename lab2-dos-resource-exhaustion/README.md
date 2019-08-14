# GraphQL Resource Exhaustion


The application uses GraphQL to retrieve Users and Posts for the DefDev new blog. 

> Run the application 

```sh
docker build . -t graphql/dos && docker run -ti -p 5000:5000 graphql/dos
```

Great now the app is running. Browse to `http://0.0.0.0:5000/` 

## Discovery 

The application does not implement a frontend but runs GraphQL on the backend to retrieve data from a Sqlite database. The database is structured as followed:

Users 

| uuid  |     username    |
|----------|:-------------:|
| 1 |  jhon |
| 2 |    jimcarry   |
    

Posts

| uuid  |     title    |    body    | author_id |
|----------|:-------------:|:-------------:|:-------------:|
| 1 |  jhon |... TEXT ... |1 |
| 2 |    jimcarry   | ... TEXT ... | 2 |
| 3 |    jimcarry   |... TEXT ... | 1 |


Each posts can only be written from one User and each User can write more than one posts. 

 



