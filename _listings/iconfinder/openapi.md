---
swagger: "2.0"
x-collection-name: Iconfinder
x-complete: 1
info:
  title: Icon Finder
  description: give-your-users-instant-access-to-more-than-300000-icons-
  termsOfService: https://developer.iconfinder.com/api/2.0/terms.html
  version: v2
host: api.iconfinder.com
basePath: /v2/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  GET /v2/users/{username}:
    get:
      summary: Get user details
      description: Get details about a specific user.
      operationId: getGetV2UsersUsername
      x-api-path-slug: get-v2usersusername-get
      responses:
        200:
          description: OK
      tags:
      - ""
      - Users
      - Username
---