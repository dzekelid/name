{
  "info": {
    "name": "Bitbucket Add Users Username Hooks",
    "_postman_id": "15ab1b83-5542-49f0-923c-8e25d3ab085a",
    "description": "Creates a new webhook on the specified user account.\n\nAccount-level webhooks are fired for events from all repositories\nbelonging to that account.\n\nNote that one can only register webhooks on one's own account, not that\nof others.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "users",
      "item": [
        {
          "id": "9975c668-e9d8-4105-b39a-d8276d9fcb60",
          "name": "postUsersUsernameHooks",
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
            "method": "POST",
            "body": {
              "mode": "raw"
            },
            "description": "Creates a new webhook on the specified user account"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "b54da542-26c0-45df-8ef7-506e9af81644"
            }
          ]
        }
      ]
    }
  ]
}