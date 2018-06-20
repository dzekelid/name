---
swagger: "2.0"
x-collection-name: Microsoft Graph
x-complete: 1
info:
  title: Microsoft Graph API
  description: microsoft-graph-exposes-multiple-apis-from-office-365-and-other-microsoft-cloud-services-through-a-single-endpoint-httpsgraph-microsoft-com--microsoft-graph-simplifies-queries-that-would-otherwise-be-more-complex-
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
    patch:
      summary: Update Nameditem
      description: Update nameditem Update the properties of nameditem object.
      operationId: UpdateNameditem
      x-api-path-slug: workbooknamesltnamegt-patch
      parameters:
      - in: header
        name: Authorization
        description: Bearer {code}
      responses:
        200:
          description: OK
      tags:
      - Nameditem
  /workbook/names:
    get:
      summary: List Named Item Collection
      description: List NamedItemCollection Retrieve a list of nameditem objects.
      operationId: ListNamedItemCollection
      x-api-path-slug: workbooknames-get
      parameters:
      - in: header
        name: Authorization
        description: Bearer
      responses:
        200:
          description: OK
      tags:
      - List
      - Named
      - Item
      - Collection
  /workbook/names(&lt;name&gt;)/Range:
    post:
      summary: Named Item Range
      description: 'NamedItem: Range Returns the range object that is associated with
        the name. Throws an exception if the named item''s type is not a range.'
      operationId: NamedItem:Range
      x-api-path-slug: workbooknamesltnamegtrange-post
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
      - Range
  /workbook/worksheets({id|name})/names:
    get:
      summary: List Names
      description: List names Retrieve a list of named item associated with the worksheet.
      operationId: ListNames
      x-api-path-slug: workbookworksheetsidnamenames-get
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
      - List
      - Names
---