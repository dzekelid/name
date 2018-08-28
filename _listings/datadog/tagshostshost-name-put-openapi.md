---
swagger: "2.0"
x-collection-name: Datadog
x-complete: 0
info:
  title: DataDog API Put Tags Hosts Host Name
  version: 1.0.0
  description: This end point allows you to update all tags for a given host.
basePath: api/v1/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /tags/hosts/:host_name:
    get:
      summary: Get Tags Hosts Host Name
      description: Return the list of tags that apply to a given host.
      operationId: getTagsHostsHostName
      x-api-path-slug: tagshostshost-name-get
      responses:
        200:
          description: OK
      tags:
      - Monitoring
      - Tags
      - Hosts
      - Host
      - Name
    post:
      summary: Add Tags Hosts Host Name
      description: This end point allows you to add tags to a host.
      operationId: postTagsHostsHostName
      x-api-path-slug: tagshostshost-name-post
      responses:
        200:
          description: OK
      tags:
      - Monitoring
      - Tags
      - Hosts
      - Host
      - Name
    put:
      summary: Put Tags Hosts Host Name
      description: This end point allows you to update all tags for a given host.
      operationId: putTagsHostsHostName
      x-api-path-slug: tagshostshost-name-put
      responses:
        200:
          description: OK
      tags:
      - Monitoring
      - Tags
      - Hosts
      - Host
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