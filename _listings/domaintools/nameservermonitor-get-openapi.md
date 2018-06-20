---
swagger: "2.0"
x-collection-name: DomainTools
x-complete: 0
info:
  title: Name Server Monitor API Name Server Monitor
  description: Receive notification when there are new and/or deleted domains on a
    given Domain Name Server
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
  /name-server-monitor/:
    get:
      summary: Name Server Monitor
      description: Receive notification when there are new and/or deleted domains
        on a given Domain Name Server
      operationId: nameServerMonitor
      x-api-path-slug: nameservermonitor-get
      parameters:
      - in: query
        name: days_back
        description: Use this parameter in exceptional circumstances where you need
          to search domain changes up to six days prior to the current date
        type: string
        format: string
      - in: query
        name: page
        description: If the result set is larger than 1000 records for a given day,
          request additional pages with this parameter
        type: string
        format: string
      - in: query
        name: query
        description: The hostname of the Name Server you wish to query
        type: string
        format: string
      responses:
        200:
          description: OK
      tags:
      - Name Server Monitor
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