swagger: "2.0"
x-collection-name: AWS Storage Gateway Service
x-complete: 1
info:
  title: AWS Storage Gateway Service API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=DescribeTapes:
    get:
      summary: Describe Tapes
      description: Returns a description of the specified Amazon Resource Name (ARN)
        of virtual tapes.
      operationId: describeTapes
      x-api-path-slug: actiondescribetapes-get
      parameters:
      - in: query
        name: GatewayARN
        description: The Amazon Resource Name (ARN) of the gateway
        type: string
      - in: query
        name: Limit
        description: Specifies that the number of virtual tapes described be limited
          to the specified         number
        type: string
      - in: query
        name: Marker
        description: A marker value, obtained in a previous call to DescribeTapes
        type: string
      - in: query
        name: TapeARNs
        description: Specifies one or more unique Amazon Resource Names (ARNs) that
          represent the virtual         tapes you want to describe
        type: string
      responses:
        200:
          description: OK
      tags:
      - Tapes