swagger: "2.0"
x-collection-name: NxtPort
x-complete: 1
info:
  title: Portcall+ API (sandbox)
  description: portplus-api
  version: 1.0.0
host: api-sb.nxtport.eu
basePath: /PortCallPlus/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /companies/name/{name}:
    get:
      summary: Get Companies Name Name
      description: Get a company by its name.
      operationId: Company_GetCompanyByName
      x-api-path-slug: companiesnamename-get
      parameters:
      - in: path
        name: name
        description: Name of the company
      responses:
        200:
          description: OK
      tags:
      - Companies
      - Name
      - Name