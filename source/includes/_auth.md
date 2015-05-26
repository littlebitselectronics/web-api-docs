# Authentication

> To request a user's authorization token, use this code:

```shell
curl --data "mobile_app[email]=you@example.com&mobile_app[password]=savekittens"
https://{server_name}/api/v2/session/create
```
> The above command returns JSON structured like this:

```json
  {
    "id": 54786,
    "username": "someperson001",
    "first_name": null,
    "last_name": null,
    "avatar": "https://lb-community-staging.s3.amazonaws.com/uploads/user/avatar/blueModule.png",
    "mobile_auth_token": "aaaaaaaaaaaaaaaaaaaaaaaaa"
  }
```

> To authorize, use this code:


```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here"
  -H "MobileAppAuth: {mobile_auth_token}"
```

### Testing on Staging Servers

While testing on Staging servers (stg1,stg2, pre-live, etc.) most requests are protected via HTTP Basic Auth. Therefore each HTTP Request must be prefaced with username/password like:

`username:password@stg1.littlebits.cc`

or

`username:password@pre-live.littlebits.cc`


### HTTP Request

`POST http://{server}/api/v2/session/create`

### Form Data

Parameter | Description
--------- | -----------
mobile_app[email] | End user's email address
mobile_app[password] | End users' password


The API uses keys to grant access. A users mobile authentication token is returned in response to successful email and password authentication.

The API expects mobile authentication token to be included in subseqeunt API requests in a header that looks like the following:

`MobileAppAuth: meowmeowmeow`

<aside class="notice">
You must replace `meowmeowmeow` with the users mobile_auth_token.
</aside>
