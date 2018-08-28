---
swagger: "2.0"
x-collection-name: Kubernetes
x-complete: 0
info:
  title: Kubernetes Put Namespaces Secrets Name
  version: 1.0.0
  description: Update the specified secret.
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
    get:
      summary: Get Namespaces Pods Name
      description: Read the specified pod.
      operationId: readPod
      x-api-path-slug: apiv1beta3namespacesnamespacespodsname-get
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
    put:
      summary: Put Namespaces Pods Name
      description: Update the specified pod.
      operationId: updatePod
      x-api-path-slug: apiv1beta3namespacesnamespacespodsname-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
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
  /api/v1beta3/namespaces/{namespaces}/replicationcontrollers/{name}:
    delete:
      summary: Delete Namespaces Replicationcontrollers Name
      description: Delete a replicationcontroller.
      operationId: deleteReplicationController
      x-api-path-slug: apiv1beta3namespacesnamespacesreplicationcontrollersname-delete
      parameters:
      - in: path
        name: name
        description: name of the ReplicationController
      - in: path
        name: namespaces
        description: object name and auth scope, such as for teams and projects
      responses:
        200:
          description: OK
      tags:
      - Namespaces
      - Replicationcontrollers
      - Name
    get:
      summary: Get Namespaces Replicationcontrollers Name
      description: Read the specified replicationcontroller.
      operationId: readReplicationController
      x-api-path-slug: apiv1beta3namespacesnamespacesreplicationcontrollersname-get
      parameters:
      - in: path
        name: name
        description: name of the ReplicationController
      - in: path
        name: namespaces
        description: object name and auth scope, such as for teams and projects
      responses:
        200:
          description: OK
      tags:
      - Namespaces
      - Replicationcontrollers
      - Name
    put:
      summary: Put Namespaces Replicationcontrollers Name
      description: Update the specified replicationcontroller.
      operationId: updateReplicationController
      x-api-path-slug: apiv1beta3namespacesnamespacesreplicationcontrollersname-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: name
        description: name of the ReplicationController
      - in: path
        name: namespaces
        description: object name and auth scope, such as for teams and projects
      responses:
        200:
          description: OK
      tags:
      - Namespaces
      - Replicationcontrollers
      - Name
  /api/v1beta3/namespaces/{namespaces}/resourcequotas/{name}:
    delete:
      summary: Delete Namespaces Resourcequotas Name
      description: Delete a resourcequota.
      operationId: deleteResourceQuota
      x-api-path-slug: apiv1beta3namespacesnamespacesresourcequotasname-delete
      parameters:
      - in: path
        name: name
        description: name of the ResourceQuota
      - in: path
        name: namespaces
        description: object name and auth scope, such as for teams and projects
      responses:
        200:
          description: OK
      tags:
      - Namespaces
      - Resourcequotas
      - Name
    get:
      summary: Get Namespaces Resourcequotas Name
      description: Read the specified resourcequota.
      operationId: readResourceQuota
      x-api-path-slug: apiv1beta3namespacesnamespacesresourcequotasname-get
      parameters:
      - in: path
        name: name
        description: name of the ResourceQuota
      - in: path
        name: namespaces
        description: object name and auth scope, such as for teams and projects
      responses:
        200:
          description: OK
      tags:
      - Namespaces
      - Resourcequotas
      - Name
    put:
      summary: Put Namespaces Resourcequotas Name
      description: Update the specified resourcequota.
      operationId: updateResourceQuota
      x-api-path-slug: apiv1beta3namespacesnamespacesresourcequotasname-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: name
        description: name of the ResourceQuota
      - in: path
        name: namespaces
        description: object name and auth scope, such as for teams and projects
      responses:
        200:
          description: OK
      tags:
      - Namespaces
      - Resourcequotas
      - Name
  /api/v1beta3/namespaces/{namespaces}/secrets/{name}:
    delete:
      summary: Delete Namespaces Secrets Name
      description: Delete a secret.
      operationId: deleteSecret
      x-api-path-slug: apiv1beta3namespacesnamespacessecretsname-delete
      parameters:
      - in: path
        name: name
        description: name of the Secret
      - in: path
        name: namespaces
        description: object name and auth scope, such as for teams and projects
      responses:
        200:
          description: OK
      tags:
      - Namespaces
      - Secrets
      - Name
    get:
      summary: Get Namespaces Secrets Name
      description: Read the specified secret.
      operationId: readSecret
      x-api-path-slug: apiv1beta3namespacesnamespacessecretsname-get
      parameters:
      - in: path
        name: name
        description: name of the Secret
      - in: path
        name: namespaces
        description: object name and auth scope, such as for teams and projects
      responses:
        200:
          description: OK
      tags:
      - Namespaces
      - Secrets
      - Name
    put:
      summary: Put Namespaces Secrets Name
      description: Update the specified secret.
      operationId: updateSecret
      x-api-path-slug: apiv1beta3namespacesnamespacessecretsname-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: name
        description: name of the Secret
      - in: path
        name: namespaces
        description: object name and auth scope, such as for teams and projects
      responses:
        200:
          description: OK
      tags:
      - Namespaces
      - Secrets
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