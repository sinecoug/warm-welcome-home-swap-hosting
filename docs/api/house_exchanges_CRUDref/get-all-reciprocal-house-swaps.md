# Get a list of a host's reciprocal house swaps

Get a list of all the reciprocal house exchanges for a specific host.

## URL

```shell

{GET}{server_url}/house-exchanges/{user_id}?type-of-exchange=reciprocal
```

## Parameters

None

## Request headers

None

## Request body

None

## Return body

The following example shows the response for the host whose `user_id` is 1. It shows the details of the host's only reciprocal house exchange

```js
[
    {
      "user_id": 1,
      "arrival-date": "2024-09-05T13:00",
      "departure-date": "2024-09-13T12:00", 
      "guest-names": "Sarah and John",
      "last-name-primary": "Jones",
      "number-of-guests": "3",
      "type-of-exchange": "Reciprocal",  
      "id": 2
    }
  ]
```

**Note** You can use a similar request to find a specific value for a property. These include `arrival-date`,`departure-date`,`last-name-primary`, `number-of-guests`, `guest-names`, and `id`. In the GET request URL, replace the parameter after the question mark. Then change the value after the equal sign.

## Return status

| Status value | Return status | Description |
| ------------- | ----------- | ----------- |
| 200 | Success | Requested data returned successfully |
| 404 | Error | The requested resource does not exist |
| ECONNREFUSED | N/A | Service is offline. Start the service and try again. |