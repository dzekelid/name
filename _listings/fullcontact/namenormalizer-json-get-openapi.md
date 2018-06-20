---
swagger: "2.0"
x-collection-name: FullContact
x-complete: 0
info:
  title: FullContact Name Normalization
  description: The Name Normalization method takes quasi-structured name data provided
    as a string and outputs the data in a structured manner. It also returns a likelihood
    based only on the order of the given name and family name as seen in the US population.
  termsOfService: https://www.fullcontact.com/terms/
  version: 1.0.0
host: api.fullcontact.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /name/normalizer.json:
    get:
      summary: Name Normalization
      description: The Name Normalization method takes quasi-structured name data
        provided as a string and outputs the data in a structured manner. It also
        returns a likelihood based only on the order of the given name and family
        name as seen in the US population.
      operationId: normalizeName
      x-api-path-slug: namenormalizer-json-get
      parameters:
      - in: query
        name: casing
        description: Uppercase, lowercase, title case
      - in: query
        name: q
        description: The q parameter allows you to pass a quasi-structured full name
          string which can include standard prefix, first name, nickname, middle name,
          last name and suffix
      responses:
        200:
          description: OK
      tags:
      - Name
      - Normalizers
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