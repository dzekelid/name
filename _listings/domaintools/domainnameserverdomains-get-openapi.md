---
swagger: "2.0"
x-collection-name: DomainTools
x-complete: 0
info:
  title: Reverse Name Server API Reverse Name Server
  description: List of domains that share the same primary name server
  version: 1.0.0
host: api.domaintools.com
basePath: /v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /{domain]/name-server-domains/:
    get:
      summary: Reverse Name Server
      description: List of domains that share the same primary name server
      operationId: reverseNameServer
      x-api-path-slug: domainnameserverdomains-get
      parameters:
      - in: query
        name: limit
        description: Limits the size of the domain list than can appear in a response
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - Reverse Name Server
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