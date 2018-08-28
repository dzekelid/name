---
swagger: "2.0"
x-collection-name: Google Beacons
x-complete: 0
info:
  title: Google Proximity Beacon API Update Namespace
  description: |-
    Updates the information about the specified namespace. Only the namespace
    visibility can be updated.
  contact:
    name: Google
    url: https://google.com
  version: v1beta1
host: proximitybeacon.googleapis.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1beta1/namespaces:
    get:
      summary: Get Namespace
      description: |-
        Lists all attachment namespaces owned by your Google Developers Console
        project. Attachment data associated with a beacon must include a
        namespaced type, and the namespace must be owned by your project.

        Authenticate using an [OAuth access token](https://developers.google.com/identity/protocols/OAuth2)
        from a signed-in user with **viewer**, **Is owner** or **Can edit**
        permissions in the Google Developers Console project.
      operationId: proximitybeacon.namespaces.list
      x-api-path-slug: v1beta1namespaces-get
      parameters:
      - in: query
        name: projectId
        description: The project id to list namespaces under
      responses:
        200:
          description: OK
      tags:
      - Namespace
  /v1beta1/{namespaceName}:
    put:
      summary: Update Namespace
      description: |-
        Updates the information about the specified namespace. Only the namespace
        visibility can be updated.
      operationId: proximitybeacon.namespaces.update
      x-api-path-slug: v1beta1namespacename-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: namespaceName
        description: Resource name of this namespace
      - in: query
        name: projectId
        description: The project id of the namespace to update
      responses:
        200:
          description: OK
      tags:
      - Namespace
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