{
  "info": {
    "name": "Vzaar API Get Api Users Username",
    "_postman_id": "861e335d-bdd8-425f-8f1a-fd517401e5e3",
    "description": "nnThis API call returns the users public details along with its relevant metadata.nn",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Api",
      "item": [
        {
          "id": "b7db6a58-d448-4de2-a8c0-67119b3794c6",
          "name": "getApiUsersUsername.Format",
          "request": {
            "url": {
              "protocol": "http",
              "host": "vzaar.com",
              "path": [
                "api/users/:username.json"
              ],
              "query": [
                {
                  "key": "username is the vzaar login name for the user. Note: This must be the actual username and not the email address",
                  "value": "%7B%7D",
                  "disabled": false
                }
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
            "description": "nnThis API call returns the users public details along with its relevant metadata.nn"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "24094da7-4e5d-4240-a541-3bf780eb1d97"
            }
          ]
        }
      ]
    }
  ]
}