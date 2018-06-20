---
swagger: "2.0"
x-collection-name: BC Geographical Names
x-complete: 0
info:
  title: BC Geographical Names Get all name authorities
  description: Gets a list of all name authorities responsible for naming decisions
    of the geographical names in the BC Geographical Names Information System (BCGNIS)
  contact:
    name: BC Geographical Names Office
    email: geographical.names@gov.bc.ca
  version: 3.x.x
host: apps.gov.bc.ca
basePath: /pub/bcgnws
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /nameAuthorities:
    get:
      summary: Get all name authorities
      description: Gets a list of all name authorities responsible for naming decisions
        of the geographical names in the BC Geographical Names Information System
        (BCGNIS)
      operationId: gets-a-list-of-all-name-authorities-responsible-for-naming-decisions-of-the-geographical-names-in-th
      x-api-path-slug: nameauthorities-get
      parameters:
      - in: query
        name: outputFormat
        description: The format of the output
      responses:
        200:
          description: OK
      tags:
      - NameAuthorities
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