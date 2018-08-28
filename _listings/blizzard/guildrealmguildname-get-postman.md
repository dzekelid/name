{
  "info": {
    "name": "World of Warcraft Get Guild Realm Guildname",
    "_postman_id": "dce03f23-06c1-4f9b-9e62-68ec8b306aef",
    "description": "Fetches a single guild at a time through an HTTP GET request to a url describing the guild profile resource. By default, a basic dataset will be returned and with each request and zero or more additional fields can be retrieved. The core dataset returned includes the guild's name, level, faction and achievement points.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Character",
      "item": [
        {
          "id": "717f5333-600c-4dfa-8fc3-a94fb5f5250a",
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
              "id": "19145f87-42a0-45a5-b636-3e13069314f8"
            }
          ]
        }
      ]
    },
    {
      "name": "Guild",
      "item": [
        {
          "id": "87667a85-3e60-4bba-8e28-4af0b89ffbc8",
          "name": "getGuildRealmGuildname",
          "request": {
            "url": {
              "protocol": "http",
              "host": "us.battle.net",
              "path": [
                "api",
                "wow",
                "guild/:realm/:guildName"
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
                  "id": "guildName",
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
            "description": "Fetches a single guild at a time through an HTTP GET request to a url describing the guild profile resource. By default, a basic dataset will be returned and with each request and zero or more additional fields can be retrieved. The core dataset returned includes the guild's name, level, faction and achievement points."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bd219018-10de-4237-8609-f210bb8fedb0"
            }
          ]
        }
      ]
    }
  ]
}