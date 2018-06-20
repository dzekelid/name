---
swagger: "2.0"
x-collection-name: Gumroad
x-complete: 0
info:
  title: Gumroad Put Products Custom Fields Name
  description: Edit an existing products custom field.
  termsOfService: https://gumroad.com/terms
  version: v1
host: api.gumroad.com
basePath: /v2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /products/:product_id/custom_fields/:name:
    put:
      summary: Put Products Custom Fields Name
      description: Edit an existing products custom field.
      operationId: putProductsProductCustomFieldsName
      x-api-path-slug: productsproduct-idcustom-fieldsname-put
      parameters:
      - in: query
        name: required
      - in: query
        name: variant
      responses:
        200:
          description: OK
      tags:
      - Products
      - Custom
      - Fields
      - :name
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