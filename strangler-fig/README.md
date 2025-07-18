# Strangler Fig pattern

```mermaid
flowchart TD
  A[Client] --> B[Load Balancer]
  B --> C{Page in New Site?}
  C -- Yes --> D[NextJS]
  C -- No --> E[Legacy Site]
```

This can be tested by launching the app

```sh
docker compose up
http://localhost:8080
http://localhost:8080/hello # <- nextjs
http://localhost:8080/legacy.php # <- legacy php code
```
