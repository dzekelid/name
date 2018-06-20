---
swagger: "2.0"
x-collection-name: Xignite
x-complete: 1
info:
  title: Xignite IPOs
  description: this-web-service-provides-ipo-data-
  version: 1.0.0
host: ipos.xignite.com
basePath: xIPOs.json/XigniteIPOs
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /SearchIPOByName:
    get:
      summary: Search IPO By Name
      description: Post searchipobyname
      operationId: SearchIPOByName
      x-api-path-slug: searchipobyname-get
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Market Data
      - Search
      - IPO
      - Name
---