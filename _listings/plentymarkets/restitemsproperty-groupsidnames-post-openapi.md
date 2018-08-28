---
swagger: "2.0"
x-collection-name: Plentymarkets
x-complete: 0
info:
  title: Plentymarkets Create a property group name
  description: Creates a property group name. The ID of the property group must be
    specified.
  contact:
    name: plentymarkets
    url: https://forum.plentymarkets.com/c/rest-api
  version: 1.0.0
host: example.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /rest/backend/users/search_name/{name}:
    get:
      summary: Find all users having a name or username like the given one.
      description: Find all users having a name or username like the given one..
      operationId: getRestBackendUsersSearchNameName
      x-api-path-slug: restbackenduserssearch-namename-get
      parameters:
      - in: path
        name: name
      responses:
        200:
          description: OK
      tags:
      - Find
      - ""
      - Users
      - Having
      - Name
      - Username
      - Like
      - Given
  /rest/items/attribute_values/{valueId}/names:
    get:
      summary: Get name and language for an attribute value ID
      description: Gets name and language for an attribute value ID. The attribute
        value ID must be specified.
      operationId: getRestItemsAttributeValuesValueNames
      x-api-path-slug: restitemsattribute-valuesvalueidnames-get
      parameters:
      - in: path
        name: valueId
      responses:
        200:
          description: OK
      tags:
      - Name
      - Languagean
      - Attribute
      - Value
      - ID
    post:
      summary: Create an attribute value name
      description: Creates an attribute value name.
      operationId: postRestItemsAttributeValuesValueNames
      x-api-path-slug: restitemsattribute-valuesvalueidnames-post
      parameters:
      - in: body
        name: /rest/items/attribute_values/{valueId}/names
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: valueId
      responses:
        200:
          description: OK
      tags:
      - Attribute
      - Value
      - Name
  /rest/items/attribute_values/{valueId}/names/{lang}:
    delete:
      summary: Delete an attribute value name
      description: Deletes an attribute value name. The attribute value ID and language
        must be specified.
      operationId: deleteRestItemsAttributeValuesValueNamesLang
      x-api-path-slug: restitemsattribute-valuesvalueidnameslang-delete
      parameters:
      - in: path
        name: lang
      - in: path
        name: valueId
      responses:
        200:
          description: OK
      tags:
      - Attribute
      - Value
      - Name
    get:
      summary: Get an attribute value name
      description: Gets the attribute value name. The attribute value ID and language
        must be specified.
      operationId: getRestItemsAttributeValuesValueNamesLang
      x-api-path-slug: restitemsattribute-valuesvalueidnameslang-get
      parameters:
      - in: path
        name: lang
      - in: path
        name: valueId
      responses:
        200:
          description: OK
      tags:
      - Attribute
      - Value
      - Name
    put:
      summary: Update an attribute value name
      description: Updates an attribute value name.
      operationId: putRestItemsAttributeValuesValueNamesLang
      x-api-path-slug: restitemsattribute-valuesvalueidnameslang-put
      parameters:
      - in: body
        name: /rest/items/attribute_values/{valueId}/names/{lang}
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: lang
      - in: path
        name: valueId
      responses:
        200:
          description: OK
      tags:
      - Attribute
      - Value
      - Name
  /rest/items/attributes/{attributeId}/names:
    get:
      summary: Get an attribute name
      description: Gets the attribute name in the specified language. The language
        code must be specified.
      operationId: getRestItemsAttributesAttributeNames
      x-api-path-slug: restitemsattributesattributeidnames-get
      parameters:
      - in: path
        name: attributeId
      responses:
        200:
          description: OK
      tags:
      - Attribute
      - Name
    post:
      summary: Create an attribute name
      description: Creates an attribute name in the specified language. The language
        code must be specified.
      operationId: postRestItemsAttributesAttributeNames
      x-api-path-slug: restitemsattributesattributeidnames-post
      parameters:
      - in: body
        name: /rest/items/attributes/{attributeId}/names
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: attributeId
      responses:
        200:
          description: OK
      tags:
      - Attribute
      - Name
  /rest/items/attributes/{attributeId}/names/{lang}:
    delete:
      summary: Delete an attribute name
      description: Deletes the attribute name in the specified language. The language
        code and attribute name must be specified.
      operationId: deleteRestItemsAttributesAttributeNamesLang
      x-api-path-slug: restitemsattributesattributeidnameslang-delete
      parameters:
      - in: path
        name: attributeId
      - in: path
        name: lang
      responses:
        200:
          description: OK
      tags:
      - Attribute
      - Name
    put:
      summary: Update an attribute name
      description: Updates the attribute name in the specified language. The language
        code and attribute name must be specified.
      operationId: putRestItemsAttributesAttributeNamesLang
      x-api-path-slug: restitemsattributesattributeidnameslang-put
      parameters:
      - in: body
        name: /rest/items/attributes/{attributeId}/names/{lang}
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: attributeId
      - in: path
        name: lang
      responses:
        200:
          description: OK
      tags:
      - Attribute
      - Name
  /rest/items/attributes/{attributeId}/value_market_names:
    post:
      summary: Create an attribute value market name
      description: Creates an attribute value market name.
      operationId: postRestItemsAttributesAttributeValueMarketNames
      x-api-path-slug: restitemsattributesattributeidvalue-market-names-post
      parameters:
      - in: body
        name: /rest/items/attributes/{attributeId}/value_market_names
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: attributeId
      responses:
        200:
          description: OK
      tags:
      - Attribute
      - Value
      - Market
      - Name
  /rest/items/attributes/{attributeId}/value_market_names/{valueId}/{lang}/{referenceType}:
    delete:
      summary: Delete an attribute value market name
      description: Deletes an attribute value market name. The attribute value ID
        and language must be specified.
      operationId: deleteRestItemsAttributesAttributeValueMarketNamesValueLangReferencetype
      x-api-path-slug: restitemsattributesattributeidvalue-market-namesvalueidlangreferencetype-delete
      parameters:
      - in: path
        name: attributeId
      - in: path
        name: lang
      - in: path
        name: referenceType
      - in: path
        name: valueId
      responses:
        200:
          description: OK
      tags:
      - Attribute
      - Value
      - Market
      - Name
    put:
      summary: Update an attribute value market name
      description: Updates an attribute value market name. The attribute value ID
        and language must be specified.
      operationId: putRestItemsAttributesAttributeValueMarketNamesValueLangReferencetype
      x-api-path-slug: restitemsattributesattributeidvalue-market-namesvalueidlangreferencetype-put
      parameters:
      - in: body
        name: /rest/items/attributes/{attributeId}/value_market_names/{valueId}/{lang}/{referenceType}
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: attributeId
      - in: path
        name: lang
      - in: path
        name: referenceType
      - in: path
        name: valueId
      responses:
        200:
          description: OK
      tags:
      - Attribute
      - Value
      - Market
      - Name
  /rest/items/properties/{id}/names:
    post:
      summary: Create a property name
      description: Creates a property name. The ID of the property must be specified.
      operationId: postRestItemsPropertiesNames
      x-api-path-slug: restitemspropertiesidnames-post
      parameters:
      - in: body
        name: /rest/items/properties/{id}/names
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - Property
      - Name
  /rest/items/properties/{id}/names/{lang}:
    delete:
      summary: Delete a property name
      description: Deletes a property name. The ID of the property must be specified.
      operationId: deleteRestItemsPropertiesNamesLang
      x-api-path-slug: restitemspropertiesidnameslang-delete
      parameters:
      - in: path
        name: id
      - in: path
        name: lang
      responses:
        200:
          description: OK
      tags:
      - Property
      - Name
    get:
      summary: Get a property name
      description: Gets a property name in a specified language. The ID of the property
        and the language code must be specified.
      operationId: getRestItemsPropertiesNamesLang
      x-api-path-slug: restitemspropertiesidnameslang-get
      parameters:
      - in: path
        name: id
      - in: path
        name: lang
      responses:
        200:
          description: OK
      tags:
      - Property
      - Name
    put:
      summary: Update a property name
      description: Updates a property name. The ID of the property and the language
        code must be specified.
      operationId: putRestItemsPropertiesNamesLang
      x-api-path-slug: restitemspropertiesidnameslang-put
      parameters:
      - in: body
        name: /rest/items/properties/{id}/names/{lang}
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
      - in: path
        name: lang
      responses:
        200:
          description: OK
      tags:
      - Property
      - Name
  /rest/items/property_groups/{id}/names:
    post:
      summary: Create a property group name
      description: Creates a property group name. The ID of the property group must
        be specified.
      operationId: postRestItemsPropertyGroupsNames
      x-api-path-slug: restitemsproperty-groupsidnames-post
      parameters:
      - in: body
        name: /rest/items/property_groups/{id}/names
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - Property
      - Group
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