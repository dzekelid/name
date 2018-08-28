---
swagger: "2.0"
x-collection-name: AWS CloudSearch
x-complete: 0
info:
  title: AWS CloudSearch List Domain Names
  version: 1.0.0
  description: Lists all search domains owned by an account.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=ListDomainNames:
    get:
      summary: List Domain Names
      description: Lists all search domains owned by an account.
      operationId: ListDomainNames
      x-api-path-slug: actionlistdomainnames-get
      parameters:
      - in: query
        name: DomainNames
        description: The names of the search domains owned by an account
        type: string
      responses:
        200:
          description: OK
      tags:
      - Domains
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