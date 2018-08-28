---
swagger: "2.0"
x-collection-name: NxtPort
x-complete: 0
info:
  title: Port+ Portdirectory API Get Companies Name Name
  description: Get a company by its name.
  version: 1.0.0
host: api.nxtport.eu
basePath: /portdirectory/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /companies/name/{name}:
    get:
      summary: Get Companies Name Name
      description: Get a company by its name.
      operationId: Company_GetCompanyByName
      x-api-path-slug: companiesnamename-get
      parameters:
      - in: path
        name: name
        description: Name of the company
      responses:
        200:
          description: OK
      tags:
      - Companies
      - Name
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