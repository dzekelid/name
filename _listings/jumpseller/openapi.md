---
swagger: "2.0"
x-collection-name: Jumpseller
x-complete: 1
info:
  title: Jumpseller
  description: explore-all-our-endpoints-with-your-own-set-of-of-access-tokens--all-changes-affect-your-production-jumpseller-store-
  version: "1"
host: api.jumpseller.com
basePath: /v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /settings/{name}.json:
    get:
      summary: Get Settings Name
      description: ""
      operationId: getSettingsName.json
      x-api-path-slug: settingsname-json-get
      parameters:
      - in: path
        name: name
        description: Name of the Store Setting
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Settings
      - Name
      - Json
    put:
      summary: Put Settings Name
      description: ""
      operationId: putSettingsName.json
      x-api-path-slug: settingsname-json-put
      parameters:
      - in: body
        name: body
        description: Store Setting parameters to change
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: name
        description: Name of the Store Setting
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Settings
      - Name
      - Json
---