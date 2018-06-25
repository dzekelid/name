---
swagger: "2.0"
x-collection-name: Swagger
x-complete: 1
info:
  title: Swagger Hub Registry
  description: the-registry-api-for-swaggerhub
  contact:
    name: SwaggerHub
    url: http://swaggerhub.com
    email: info@swaggerhub.com
  version: 1.0.45
host: api.swaggerhub.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /apis/{owner}/{api}/.newname:
    post:
      summary: Renames API
      description: Renames api.
      operationId: renameApi
      x-api-path-slug: apisownerapi-newname-post
      parameters:
      - in: path
        name: api
        description: API identifier
      - in: query
        name: newName
        description: New name
      - in: path
        name: owner
        description: API owner identifier
      responses:
        200:
          description: OK
      tags:
      - APIs
      - Owner
      - ""
      - Newname
  /domains/{owner}/{domain}/.newname:
    post:
      summary: Renames domain
      description: Renames domain.
      operationId: renameDomain
      x-api-path-slug: domainsownerdomain-newname-post
      parameters:
      - in: path
        name: domain
        description: domain identifier
      - in: query
        name: force
        description: force update
      - in: query
        name: newName
        description: New name
      - in: path
        name: owner
        description: API owner identifier
      responses:
        200:
          description: OK
      tags:
      - Domains
      - Owner
      - Domain
      - ""
      - Newname
---