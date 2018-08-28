swagger: "2.0"
x-collection-name: Google Glass
x-complete: 1
info:
  title: Google Mirror
  description: interacts-with-glass-users-via-the-timeline-
  contact:
    name: Google
    url: https://google.com
  version: v1
host: www.googleapis.com
basePath: /mirror/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /accounts/{userToken}/{accountType}/{accountName}:
    post:
      summary: Insert Account
      description: Inserts a new account for a user
      operationId: mirror.accounts.insert
      x-api-path-slug: accountsusertokenaccounttypeaccountname-post
      parameters:
      - in: path
        name: accountName
        description: The name of the account to be passed to the Android Account Manager
      - in: path
        name: accountType
        description: Account type to be passed to Android Account Manager
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: userToken
        description: The ID for the user
      responses:
        200:
          description: OK
      tags:
      - Account