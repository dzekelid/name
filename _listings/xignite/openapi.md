swagger: "2.0"
x-collection-name: Xignite
x-complete: 1
info:
  title: Xignite VWAP
  description: provides-delayed-and-historical-volumeweightedaverage-price-vwap-information-
  version: 1.0.0
host: www.xignite.com
basePath: xVWAP.json/XigniteVWAP
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /GetEventsByEventName:
    get:
      summary: Get Events By Event Name
      description: Get events based on the event name and optionally within a specified
        released range.
      operationId: postGeteventsbyeventname
      x-api-path-slug: geteventsbyeventname-get
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
      - Events
      - Event
      - Name
  /SearchIndicesByName:
    get:
      summary: Search Indices By Name
      description: Search indices by name.
      operationId: SearchIndicesByName
      x-api-path-slug: searchindicesbyname-get
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
      - Indices
      - Name
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