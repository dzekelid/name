{
  "info": {
    "name": "Bitbucket Get Users Username",
    "_postman_id": "2858be20-d7f4-4171-b325-372463979aa3",
    "description": "Gets the public information associated with a user account.\n\nIf the user's profile is private, `location`, `website` and\n`created_on` elements are omitted.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "users",
      "item": [
        {
          "id": "eb41b2c5-ad0a-44f3-a5d2-970291efe55c",
          "name": "getUsersUsername",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.bitbucket.org",
              "path": [
                "2.0",
                "users/:username"
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
            "description": "Gets the public information associated with a user account"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a8f3fb22-85c4-4808-9b67-c604f4899f7b"
            }
          ]
        }
      ]
    }
  ]
}