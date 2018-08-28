swagger: "2.0"
x-collection-name: AWS CloudSearch
x-complete: 1
info:
  title: AWS CloudSearch
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=ListDomainNames:
    get:
      summary: List Domain Names
      description: Lists all search domains owned by an account.
      operationId: ListDomainNames
      x-api-path-slug: actionlistdomainnames-get
      parameters:
      - in: query
        name: DomainNames
        description: The names of the search domains owned by an account
        type: string
      responses:
        200:
          description: OK
      tags:
      - Domains