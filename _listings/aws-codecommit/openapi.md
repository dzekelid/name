swagger: "2.0"
x-collection-name: AWS CodeCommit
x-complete: 1
info:
  title: AWS CodeCommit API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /?Action=UpdateRepositoryName:
    get:
      summary: Update Repository Name
      description: Renames a repository.
      operationId: updateRepositoryName
      x-api-path-slug: actionupdaterepositoryname-get
      parameters:
      - in: query
        name: newName
        description: The new name for the repository
        type: string
      - in: query
        name: oldName
        description: The existing name of the repository
        type: string
      responses:
        200:
          description: OK
      tags:
      - Repositories