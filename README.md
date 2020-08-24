# camunda-client-sample

Get started sample to use camunda-client following: https://docs.camunda.org/get-started/quick-start/.

### Setup

```
docker pull camunda/camunda-bpm-platform:latest
docker run -d -p 8080:8080 camunda/camunda-bpm-platform:latest

```

OPEN http://localhost:8080/camunda-welcome/index.html

Credential: `demo/demo`

### Test

```curl
curl -H "Content-Type: application/json" -X POST -d '{"variables": {"amount": {"value":1555,"type":"long"}, "item": {"value":"item-aabc"} } }' http://localhost:8080/engine-rest/process-definition/key/payment-retrieval/start

curl -H "Content-Type: application/json" -X POST -d '{"variables": {"amount": {"value":1555,"type":"long"}, "item": {"value":"item-xyz"} } }' http://localhost:8080/engine-rest/process-definition/key/payment-retrieval/start
```
