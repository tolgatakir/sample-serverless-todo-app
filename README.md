## Usage

You can create, retrieve, update, or delete todos with the following commands:

### Create a Todo

```bash
curl -X POST https://XXXXXXX.execute-api.eu-west-1.amazonaws.com/dev/todos --data '{ "text": "Learn Serverless" }'
```

Example Result:

```bash
{"id":"e585bb70-74ed-11eb-a999-c7c1b4267e55","text":"Learn Serverless","checked":false,"createdAt":1613985067175,"updatedAt":1613985067175}%
```

### List all Todos

```bash
curl https://XXXXXXX.execute-api.eu-west-1.amazonaws.com/dev/todos
```

Example output:

```bash
[{"checked":false,"createdAt":1613985067175,"text":"Learn Serverless","id":"e585bb70-74ed-11eb-a999-c7c1b4267e55","updatedAt":1613985067175}]%
```

### Get one Todo

```bash
# Replace the <id> part with a real id from your todos table
curl https://XXXXXXX.execute-api.eu-west-1.amazonaws.com/dev/todos/<id>
```

Example Result:

```bash
[{"checked":false,"createdAt":1613985067175,"text":"Learn Serverless","id":"e585bb70-74ed-11eb-a999-c7c1b4267e55","updatedAt":1613985067175}]%
```

### Update a Todo

```bash
# Replace the <id> part with a real id from your todos table
curl -X PUT https://XXXXXXX.execute-api.eu-west-1.amazonaws.com/dev/todos/<id> --data '{ "text": "Learn Serverless", "checked": true }'
```

Example Result:

```bash
{"checked":true,"createdAt":1613985067175,"text":"Learn Serverless","id":"e585bb70-74ed-11eb-a999-c7c1b4267e55","updatedAt":1613985228142}%
```

### Delete a Todo

```bash
# Replace the <id> part with a real id from your todos table
curl -X DELETE https://XXXXXXX.execute-api.eu-west-1.amazonaws.com/dev/todos/<id>
```

Example Result:

```bash
{}%
```
