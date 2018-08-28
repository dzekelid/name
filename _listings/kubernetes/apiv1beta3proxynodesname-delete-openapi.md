---
swagger: "2.0"
x-collection-name: Kubernetes
x-complete: 0
info:
  title: Kubernetes Delete Proxy Nodes Name
  version: 1.0.0
  description: Proxy delete requests to node.
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
  /api/v1beta3/namespaces/{namespaces}/services/{name}:
    delete:
      summary: Delete Namespaces Services Name
      description: Delete a service.
      operationId: deleteService
      x-api-path-slug: apiv1beta3namespacesnamespacesservicesname-delete
      parameters:
      - in: path
        name: name
        description: name of the Service
      - in: path
        name: namespaces
        description: object name and auth scope, such as for teams and projects
      responses:
        200:
          description: OK
      tags:
      - Namespaces
      - Services
      - Name
    get:
      summary: Get Namespaces Services Name
      description: Read the specified service.
      operationId: readService
      x-api-path-slug: apiv1beta3namespacesnamespacesservicesname-get
      parameters:
      - in: path
        name: name
        description: name of the Service
      - in: path
        name: namespaces
        description: object name and auth scope, such as for teams and projects
      responses:
        200:
          description: OK
      tags:
      - Namespaces
      - Services
      - Name
    put:
      summary: Put Namespaces Services Name
      description: Update the specified service.
      operationId: updateService
      x-api-path-slug: apiv1beta3namespacesnamespacesservicesname-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: name
        description: name of the Service
      - in: path
        name: namespaces
        description: object name and auth scope, such as for teams and projects
      responses:
        200:
          description: OK
      tags:
      - Namespaces
      - Services
      - Name
  /api/v1beta3/namespaces/{name}:
    delete:
      summary: Delete Namespaces Name
      description: Delete a namespace.
      operationId: deleteNamespace
      x-api-path-slug: apiv1beta3namespacesname-delete
      parameters:
      - in: path
        name: name
        description: name of the Namespace
      responses:
        200:
          description: OK
      tags:
      - Namespaces
      - Name
    get:
      summary: Get Namespaces Name
      description: Read the specified namespace.
      operationId: readNamespace
      x-api-path-slug: apiv1beta3namespacesname-get
      parameters:
      - in: path
        name: name
        description: name of the Namespace
      responses:
        200:
          description: OK
      tags:
      - Namespaces
      - Name
    put:
      summary: Put Namespaces Name
      description: Update the specified namespace.
      operationId: updateNamespace
      x-api-path-slug: apiv1beta3namespacesname-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: name
        description: name of the Namespace
      responses:
        200:
          description: OK
      tags:
      - Namespaces
      - Name
  /api/v1beta3/nodes/{name}:
    delete:
      summary: Delete Nodes Name
      description: Delete a node.
      operationId: deleteNode
      x-api-path-slug: apiv1beta3nodesname-delete
      parameters:
      - in: path
        name: name
        description: name of the Node
      responses:
        200:
          description: OK
      tags:
      - Nodes
      - Name
    get:
      summary: Get Nodes Name
      description: Read the specified node.
      operationId: readNode
      x-api-path-slug: apiv1beta3nodesname-get
      parameters:
      - in: path
        name: name
        description: name of the Node
      responses:
        200:
          description: OK
      tags:
      - Nodes
      - Name
    put:
      summary: Put Nodes Name
      description: Update the specified node.
      operationId: updateNode
      x-api-path-slug: apiv1beta3nodesname-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: name
        description: name of the Node
      responses:
        200:
          description: OK
      tags:
      - Nodes
      - Name
  /api/v1beta3/proxy/namespaces/{namespaces}/pods/{name}:
    delete:
      summary: Delete Proxy Namespaces Pods Name
      description: Proxy delete requests to pod.
      operationId: proxyDELETEPod
      x-api-path-slug: apiv1beta3proxynamespacesnamespacespodsname-delete
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
      - Proxy
      - Namespaces
      - Pods
      - Name
    get:
      summary: Get Proxy Namespaces Pods Name
      description: Proxy get requests to pod.
      operationId: proxyGETPod
      x-api-path-slug: apiv1beta3proxynamespacesnamespacespodsname-get
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
      - Proxy
      - Namespaces
      - Pods
      - Name
    post:
      summary: Post Proxy Namespaces Pods Name
      description: Proxy post requests to pod.
      operationId: proxyPOSTPod
      x-api-path-slug: apiv1beta3proxynamespacesnamespacespodsname-post
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
      - Proxy
      - Namespaces
      - Pods
      - Name
    put:
      summary: Put Proxy Namespaces Pods Name
      description: Proxy put requests to pod.
      operationId: proxyPUTPod
      x-api-path-slug: apiv1beta3proxynamespacesnamespacespodsname-put
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
      - Proxy
      - Namespaces
      - Pods
      - Name
  /api/v1beta3/proxy/namespaces/{namespaces}/pods/{name}/{path:*}:
    delete:
      summary: Delete Proxy Namespaces Pods Name Path *
      description: Proxy delete requests to pod.
      operationId: proxyDELETEPod
      x-api-path-slug: apiv1beta3proxynamespacesnamespacespodsnamepath-delete
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
      - Proxy
      - Namespaces
      - Pods
      - Name
      - Path
      - '*'
    get:
      summary: Get Proxy Namespaces Pods Name Path *
      description: Proxy get requests to pod.
      operationId: proxyGETPod
      x-api-path-slug: apiv1beta3proxynamespacesnamespacespodsnamepath-get
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
      - Proxy
      - Namespaces
      - Pods
      - Name
      - Path
      - '*'
    post:
      summary: Post Proxy Namespaces Pods Name Path *
      description: Proxy post requests to pod.
      operationId: proxyPOSTPod
      x-api-path-slug: apiv1beta3proxynamespacesnamespacespodsnamepath-post
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
      - Proxy
      - Namespaces
      - Pods
      - Name
      - Path
      - '*'
    put:
      summary: Put Proxy Namespaces Pods Name Path *
      description: Proxy put requests to pod.
      operationId: proxyPUTPod
      x-api-path-slug: apiv1beta3proxynamespacesnamespacespodsnamepath-put
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
      - Proxy
      - Namespaces
      - Pods
      - Name
      - Path
      - '*'
  /api/v1beta3/proxy/namespaces/{namespaces}/services/{name}:
    delete:
      summary: Delete Proxy Namespaces Services Name
      description: Proxy delete requests to service.
      operationId: proxyDELETEService
      x-api-path-slug: apiv1beta3proxynamespacesnamespacesservicesname-delete
      parameters:
      - in: path
        name: name
        description: name of the Service
      - in: path
        name: namespaces
        description: object name and auth scope, such as for teams and projects
      responses:
        200:
          description: OK
      tags:
      - Proxy
      - Namespaces
      - Services
      - Name
    get:
      summary: Get Proxy Namespaces Services Name
      description: Proxy get requests to service.
      operationId: proxyGETService
      x-api-path-slug: apiv1beta3proxynamespacesnamespacesservicesname-get
      parameters:
      - in: path
        name: name
        description: name of the Service
      - in: path
        name: namespaces
        description: object name and auth scope, such as for teams and projects
      responses:
        200:
          description: OK
      tags:
      - Proxy
      - Namespaces
      - Services
      - Name
    post:
      summary: Post Proxy Namespaces Services Name
      description: Proxy post requests to service.
      operationId: proxyPOSTService
      x-api-path-slug: apiv1beta3proxynamespacesnamespacesservicesname-post
      parameters:
      - in: path
        name: name
        description: name of the Service
      - in: path
        name: namespaces
        description: object name and auth scope, such as for teams and projects
      responses:
        200:
          description: OK
      tags:
      - Proxy
      - Namespaces
      - Services
      - Name
    put:
      summary: Put Proxy Namespaces Services Name
      description: Proxy put requests to service.
      operationId: proxyPUTService
      x-api-path-slug: apiv1beta3proxynamespacesnamespacesservicesname-put
      parameters:
      - in: path
        name: name
        description: name of the Service
      - in: path
        name: namespaces
        description: object name and auth scope, such as for teams and projects
      responses:
        200:
          description: OK
      tags:
      - Proxy
      - Namespaces
      - Services
      - Name
  /api/v1beta3/proxy/namespaces/{namespaces}/services/{name}/{path:*}:
    delete:
      summary: Delete Proxy Namespaces Services Name Path *
      description: Proxy delete requests to service.
      operationId: proxyDELETEService
      x-api-path-slug: apiv1beta3proxynamespacesnamespacesservicesnamepath-delete
      parameters:
      - in: path
        name: name
        description: name of the Service
      - in: path
        name: namespaces
        description: object name and auth scope, such as for teams and projects
      responses:
        200:
          description: OK
      tags:
      - Proxy
      - Namespaces
      - Services
      - Name
      - Path
      - '*'
    get:
      summary: Get Proxy Namespaces Services Name Path *
      description: Proxy get requests to service.
      operationId: proxyGETService
      x-api-path-slug: apiv1beta3proxynamespacesnamespacesservicesnamepath-get
      parameters:
      - in: path
        name: name
        description: name of the Service
      - in: path
        name: namespaces
        description: object name and auth scope, such as for teams and projects
      responses:
        200:
          description: OK
      tags:
      - Proxy
      - Namespaces
      - Services
      - Name
      - Path
      - '*'
    post:
      summary: Post Proxy Namespaces Services Name Path *
      description: Proxy post requests to service.
      operationId: proxyPOSTService
      x-api-path-slug: apiv1beta3proxynamespacesnamespacesservicesnamepath-post
      parameters:
      - in: path
        name: name
        description: name of the Service
      - in: path
        name: namespaces
        description: object name and auth scope, such as for teams and projects
      responses:
        200:
          description: OK
      tags:
      - Proxy
      - Namespaces
      - Services
      - Name
      - Path
      - '*'
    put:
      summary: Put Proxy Namespaces Services Name Path *
      description: Proxy put requests to service.
      operationId: proxyPUTService
      x-api-path-slug: apiv1beta3proxynamespacesnamespacesservicesnamepath-put
      parameters:
      - in: path
        name: name
        description: name of the Service
      - in: path
        name: namespaces
        description: object name and auth scope, such as for teams and projects
      responses:
        200:
          description: OK
      tags:
      - Proxy
      - Namespaces
      - Services
      - Name
      - Path
      - '*'
  /api/v1beta3/proxy/nodes/{name}:
    delete:
      summary: Delete Proxy Nodes Name
      description: Proxy delete requests to node.
      operationId: proxyDELETENode
      x-api-path-slug: apiv1beta3proxynodesname-delete
      parameters:
      - in: path
        name: name
        description: name of the Node
      responses:
        200:
          description: OK
      tags:
      - Proxy
      - Nodes
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