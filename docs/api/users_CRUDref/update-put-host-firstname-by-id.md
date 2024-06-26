# Update (PUT) a specific host's first name

Change a host's first name using the host's `id`.

## HTTP Method

PUT

## URL

```shell

{server_url}/hosts/{id}
```

## Parameters

| Property name | Type | Description |
| ------------- | ----------- | ----------- |
| `id` | Number | Service-generated unique ID for the host |

## Request headers

| Key | Value |
|---|---|
| Content-Type | application/json |

## Request body

**Important** The request body replaces all the current properties of the host, except the unique IDs. For properties that you do not want to change, you must use their current values in the request body.

```js
    {
      "last_name": "Weimann",
      "first_name": "Nicholas",
      "email": "n.weimann@example.com"      
    }
```

## Return body

The following example shows the response if the `id` parameter value is 4.

```js
[
    {
      "last_name": "Weimann",
      "first_name": "Nicholas",
      "email": "n.weimann@example.com",
      "id": 4
    }
]
```

**Note** You can use a request like this to update a host's `email` and `last_name`. Just replace the parameter in the curly braces {} in the request URL.

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data updated and returned successfully |
| 404 | Error | Specified user record not found |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |
