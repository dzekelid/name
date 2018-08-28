swagger: "2.0"
x-collection-name: Datadog
x-complete: 1
info:
  title: DataDog Merged API
  version: 1.0.0
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
    delete:
      summary: Delete Tags Hosts Host Name
      description: This end point allows you to remove all tags for a given host.
      operationId: deleteTagsHostsHostName
      x-api-path-slug: tagshostshost-name-delete
      responses:
        200:
          description: OK
      tags:
      - Monitoring
      - Tags
      - Hosts
      - Host
      - Name