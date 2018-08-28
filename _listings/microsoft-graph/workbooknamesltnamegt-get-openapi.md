---
swagger: "2.0"
x-collection-name: Microsoft Graph
x-complete: 0
info:
  title: Microsoft Graph Get Named Item
  description: Get NamedItem Retrieve the properties and relationships of nameditem
    object.
  version: 1.0.0
host: graph.microsoft.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /me/drive/special/{name}:
    get:
      summary: Get A Special Folder By Name
      description: Get a special folder by name Use the special collection to access
        a special folder by name.
      operationId: GetASpecialFolderByName
      x-api-path-slug: medrivespecialname-get
      parameters:
      - in: header
        name: Authorization
        description: 'Bearer '
        type: string
      - in: path
        name: name
        type: string
      responses:
        200:
          description: OK
      tags:
      - Special
      - FolderName
  /workbook/names/add:
    post:
      summary: Add Named Item
      description: Add Named Item Adds a new name to the collection of the given scope
        using the user's locale for the formula.
      operationId: AddNamedItem
      x-api-path-slug: workbooknamesadd-post
      parameters:
      - in: header
        name: Authorization
        description: Bearer {code}
      responses:
        200:
          description: OK
      tags:
      - Named
      - Item
  /workbook/worksheets({id|name})/names/add:
    post:
      summary: Add Named Item
      description: Add Named Item Adds a new name to the collection of the given scope
        using the user's locale for the formula.
      operationId: AddNamedItem
      x-api-path-slug: workbookworksheetsidnamenamesadd-post
      parameters:
      - in: header
        name: Authorization
        description: Bearer {code}
      - in: path
        name: id|name
        type: string
      responses:
        200:
          description: OK
      tags:
      - Named
      - Item
  /workbook/names(&lt;name&gt;):
    get:
      summary: Get Named Item
      description: Get NamedItem Retrieve the properties and relationships of nameditem
        object.
      operationId: GetNamedItem
      x-api-path-slug: workbooknamesltnamegt-get
      parameters:
      - in: header
        name: Authorization
        description: Bearer
      responses:
        200:
          description: OK
      tags:
      - Named
      - Item
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