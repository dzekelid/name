swagger: "2.0"
x-collection-name: Gumroad
x-complete: 1
info:
  title: Gumroad
  description: api-for-selling-of-digital-goods-and-media-
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