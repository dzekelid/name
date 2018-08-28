{
  "info": {
    "name": "Bitbucket Get Users Username Hooks",
    "_postman_id": "82777abf-9bbe-4e88-9330-a75665516db1",
    "description": "Returns a paginated list of webhooks installed on this user account.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "users",
      "item": [
        {
          "id": "5f1b068f-2eb0-4251-9ede-be818051a0c1",
          "name": "getUsersUsernameHooks",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "users/:username/hooks"
              ],
              "variable": [
                {
                  "id": "username",
                  "value": "username",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns a paginated list of webhooks installed on this user account"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "8d3882a4-7462-4d9e-b2c8-11181b53e058"
            }
          ]
        }
      ]
    }
  ]
}