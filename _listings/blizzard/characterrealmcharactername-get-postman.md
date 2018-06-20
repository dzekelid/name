{
  "info": {
    "name": "World of Warcraft Get Character Realm Charactername",
    "_postman_id": "85390abe-6554-4f31-947d-703b03b28452",
    "description": "Fetches a single character at a time through an HTTP GET request to a URL describing the character profile resource. By default, a basic dataset will be returned and with each request and zero or more additional fields can be retrieved. The core dataset returned includes the character's realm, name, level, last modified timestamp, thumbnail, race id, achievement points value, gender id and class id.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Character",
      "item": [
        {
          "id": "7bc059ae-78fc-431f-bb8f-78b39dfbe963",
          "name": "getCharacterRealmCharactername",
          "request": {
            "url": {
              "protocol": "http",
              "host": "us.battle.net",
              "path": [
                "api",
                "wow",
                "character/:realm/:characterName"
              ],
              "query": [
                {
                  "key": "fields",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "characterName",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "realm",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Fetches a single character at a time through an HTTP GET request to a URL describing the character profile resource. By default, a basic dataset will be returned and with each request and zero or more additional fields can be retrieved. The core dataset returned includes the character's realm, name, level, last modified timestamp, thumbnail, race id, achievement points value, gender id and class id."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6e7c884d-9447-4734-a58c-2db3edcce0b7"
            }
          ]
        }
      ]
    }
  ]
}