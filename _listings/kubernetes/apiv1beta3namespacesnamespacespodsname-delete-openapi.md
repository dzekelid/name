---
swagger: "2.0"
x-collection-name: Kubernetes
x-complete: 0
info:
  title: Kubernetes Delete Namespaces Pods Name
  version: 1.0.0
  description: Delete a pod.
host: /api/v1beta3
basePath: 127.0.0.1:6443
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/v1beta3/namespaces/{namespaces}/endpoints/{name}:
    get:
      summary: Get Namespaces Endpoints Name
      description: Read the specified endpoints.
      operationId: readEndpoints
      x-api-path-slug: apiv1beta3namespacesnamespacesendpointsname-get
      parameters:
      - in: path
        name: name
        description: name of the Endpoints
      - in: path
        name: namespaces
        description: object name and auth scope, such as for teams and projects
      responses:
        200:
          description: OK
      tags:
      - Namespaces
      - Endpoints
      - Name
    put:
      summary: Put Namespaces Endpoints Name
      description: Update the specified endpoints.
      operationId: updateEndpoints
      x-api-path-slug: apiv1beta3namespacesnamespacesendpointsname-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: name
        description: name of the Endpoints
      - in: path
        name: namespaces
        description: object name and auth scope, such as for teams and projects
      responses:
        200:
          description: OK
      tags:
      - Namespaces
      - Endpoints
      - Name
  /api/v1beta3/namespaces/{namespaces}/events/{name}:
    delete:
      summary: Delete Namespaces Events Name
      description: Delete a event.
      operationId: deleteEvent
      x-api-path-slug: apiv1beta3namespacesnamespaceseventsname-delete
      parameters:
      - in: path
        name: name
        description: name of the Event
      - in: path
        name: namespaces
        description: object name and auth scope, such as for teams and projects
      responses:
        200:
          description: OK
      tags:
      - Namespaces
      - Events
      - Name
    get:
      summary: Get Namespaces Events Name
      description: Read the specified event.
      operationId: readEvent
      x-api-path-slug: apiv1beta3namespacesnamespaceseventsname-get
      parameters:
      - in: path
        name: name
        description: name of the Event
      - in: path
        name: namespaces
        description: object name and auth scope, such as for teams and projects
      responses:
        200:
          description: OK
      tags:
      - Namespaces
      - Events
      - Name
    put:
      summary: Put Namespaces Events Name
      description: Update the specified event.
      operationId: updateEvent
      x-api-path-slug: apiv1beta3namespacesnamespaceseventsname-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: name
        description: name of the Event
      - in: path
        name: namespaces
        description: object name and auth scope, such as for teams and projects
      responses:
        200:
          description: OK
      tags:
      - Namespaces
      - Events
      - Name
  /api/v1beta3/namespaces/{namespaces}/limitranges/{name}:
    delete:
      summary: Delete Namespaces Limitranges Name
      description: Delete a limitrange.
      operationId: deleteLimitRange
      x-api-path-slug: apiv1beta3namespacesnamespaceslimitrangesname-delete
      parameters:
      - in: path
        name: name
        description: name of the LimitRange
      - in: path
        name: namespaces
        description: object name and auth scope, such as for teams and projects
      responses:
        200:
          description: OK
      tags:
      - Namespaces
      - Limitranges
      - Name
    get:
      summary: Get Namespaces Limitranges Name
      description: Read the specified limitrange.
      operationId: readLimitRange
      x-api-path-slug: apiv1beta3namespacesnamespaceslimitrangesname-get
      parameters:
      - in: path
        name: name
        description: name of the LimitRange
      - in: path
        name: namespaces
        description: object name and auth scope, such as for teams and projects
      responses:
        200:
          description: OK
      tags:
      - Namespaces
      - Limitranges
      - Name
    put:
      summary: Put Namespaces Limitranges Name
      description: Update the specified limitrange.
      operationId: updateLimitRange
      x-api-path-slug: apiv1beta3namespacesnamespaceslimitrangesname-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: name
        description: name of the LimitRange
      - in: path
        name: namespaces
        description: object name and auth scope, such as for teams and projects
      responses:
        200:
          description: OK
      tags:
      - Namespaces
      - Limitranges
      - Name
  /api/v1beta3/namespaces/{namespaces}/pods/{name}:
    delete:
      summary: Delete Namespaces Pods Name
      description: Delete a pod.
      operationId: deletePod
      x-api-path-slug: apiv1beta3namespacesnamespacespodsname-delete
      parameters:
      - in: path
        name: name
        description: name of the Pod
      - in: path
        name: namespaces
        description: object name and auth scope, such as for teams and projects
      responses:
        200:
          description: OK
      tags:
      - Namespaces
      - Pods
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