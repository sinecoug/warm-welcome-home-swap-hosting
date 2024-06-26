# Tutorial: Add a new host to the service

 In this tutorial, you will see how easy it is to add a new host. Be sure to [set up](before-you-start-tutorials.md) your system first.

Expect this tutorial to take about 15 minutes to complete.

## Before you start

First, confirm that your local service is running in a command window. Use the following:

    ```shell
    
         cd <your-github-workspace>/warm-welcome-home-swap-hosting/api
        # Run the service and monitor its database file for updates
        json-server -w warm-welcome-home-swap-hosting-db-source.json

    ```

## Start the Postman app

1. Open the Postman app on your desktop.
1. In the Postman app, create a new request and enter the values below.
    * **METHOD**: POST
    * **URL**: `{server_url}/hosts`
    * **Headers**:
        * `Content-Type: application/json`
    * **Request body**:
        The table below lists the required properties for each host.

    | Property name | Type | Description |
    | ------------- | ----------- | ----------- |
    | `last_name` | String | Host’s last name |
    | `first_name` | String | Host’s first name|
    | `email` | String |Host’s email address |

1. In the Request body, enter the JSON script for the properties as shown below.

   ```js

    {
      "last_name": "Rochester",
      "first_name": "Edward",
      "email": "ed.rochester@example.com"
    }

   ```

1. In the Postman app, make the request by choosing **Send**. The Response body should look like the output below. Note that the content should be the same as you entered in the **Request body**. Also, the response should now include the new host's unique `id`.

```js

    {
    "last_name": "Rochester",
    "first_name": "Edward",
    "email": "ed.rochester@example.com",
    "id": 5
    } 
   ```

## Next steps

Congrats on adding your first host! Let's [add your first guest](tutorial-add-new-guest.md).

After doing this tutorial in Postman, you might like to repeat it in your favorite programming language. To do this, adapt the values from the tutorial to the properties and arguments that the language uses to make REST API calls.

## Related topics

[Hosts resource](../api/users.md)
