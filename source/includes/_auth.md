# Authentication

## Login

> To request a user's authorization token, use this code:

```shell
curl --data "mobile_app[email]=you@example.com&mobile_app[password]=savekittens"
https://{server_name}/api/v2/session/create
```
> The above command returns JSON structured like this:

```json
  {
    "results":{
      "id":64651,
      "username":"someguy",
      "twitter":null,
      "location":null,
      "bio":null,
      "image":"https://lb-community-staging.s3.amazonaws.com/uploads/user/avatar/medium_pinkModule.png",
      "member_since":"Member since June 2015",
      "spree_api_key":"abc123",
      "projects":[]
    },
    "meta":{
      "version":2.0,
      "criteria":{
        "method":"POST",
        "endpoint":"/api/v2/session/create",
        "params":[
          {
            "name":"email",
            "value":"e@ma.il"
          }
        ]
      },
      "success":true,
      "errors":null
    }
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

## Login with Facebook

`POST http://{server}/api/v2/session/fb`

```shell
curl https://{server_name}/api/v2/session/fb
```

> Expects the following minimum payload:

```json
  {
    "first_name": "Peter",
    "last_name": "Pan",
    "email": "e2@ma.il",
    "access_token": {
      "userID": "2"
    }
  }
```

## Log out

```shell
curl --data "token=savekittens"
https://{server_name}/api/v2/session/destroy
```
> The above command always returns 204 no content status

### HTTP Request

`POST http://{server}/api/v2/session/destroy`

### Form Data

Parameter | Description
--------- | -----------
token | `mobile_auth_token`
