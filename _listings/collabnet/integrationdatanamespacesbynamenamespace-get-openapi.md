---
swagger: "2.0"
x-collection-name: CollabNet
x-complete: 0
info:
  title: CollabNet TeamForge API Documentation Gets namespace info by name
  version: 1.0.0
  description: Gets namespace info by name.
basePath: /ctfrest/foundation/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /users/by-username/{username}/preferences:
    patch:
      summary: Sets preferences by user name
      description: Sets preferences by user name.
      operationId: setPreferences
      x-api-path-slug: usersbyusernameusernamepreferences-patch
      parameters:
      - in: body
        name: body
        description: Preferences
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: username
        description: Username
      responses:
        200:
          description: OK
      tags:
      - Sets
      - Preferences
      - By
      - User
      - Name
  /users/by-username/{username}/groups/{groupid}:
    put:
      summary: Add user to a user group by user name
      description: Add user to a user group by user name.
      operationId: addUserToGroupByUsername
      x-api-path-slug: usersbyusernameusernamegroupsgroupid-put
      parameters:
      - in: path
        name: groupid
        description: Group id
      - in: path
        name: username
        description: Username
      responses:
        200:
          description: OK
      tags:
      - User
      - To
      - User
      - Group
      - By
      - User
      - Name
  /integrationdata/namespaces/by-name/{namespace}:
    get:
      summary: Gets namespace info by name
      description: Gets namespace info by name.
      operationId: getNamespaceByName
      x-api-path-slug: integrationdatanamespacesbynamenamespace-get
      parameters:
      - in: path
        name: namespace
        description: Namespace name
      responses:
        200:
          description: OK
      tags:
      - Namespace
      - Info
      - By
      - Name
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---