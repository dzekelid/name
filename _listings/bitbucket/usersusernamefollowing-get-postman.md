{
  "info": {
    "name": "Bitbucket Get Users Username Following",
    "_postman_id": "aa5938c0-bc66-41d3-9aa6-ef7186aa70b6",
    "description": "Returns the list of accounts this user is following.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "users",
      "item": [
        {
          "id": "1becf2f0-f121-4a3b-9a37-4d06b64e2125",
          "name": "getUsersUsernameFollowing",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "users/:username/following"
              ],
              "variable": [
                {
                  "id": "username",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Returns the list of accounts this user is following"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "661bcb55-30be-4c65-b573-4ce50e2257c5"
            }
          ]
        }
      ]
    }
  ]
}