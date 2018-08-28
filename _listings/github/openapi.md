swagger: "2.0"
x-collection-name: GitHub
x-complete: 1
info:
  title: GitHub
  version: 1.0.0
host: api.github.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /repos/{owner}/{repo}/issues/{number}/labels/{name}:
    delete:
      summary: Delete Repos Owner Repo Issues Number Labels Name
      description: Remove a label from an issue.
      operationId: remove-a-label-from-an-issue
      x-api-path-slug: reposownerrepoissuesnumberlabelsname-delete
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: name
        description: Name of the label
      - in: path
        name: number
        description: Number of issue
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Issues
      - Number
      - Labels
      - Name
  /repos/{owner}/{repo}/labels/{name}:
    delete:
      summary: Delete Repos Owner Repo Labels Name
      description: Delete a label.
      operationId: delete-a-label
      x-api-path-slug: reposownerrepolabelsname-delete
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: name
        description: Name of the label
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Labels
      - Name
    get:
      summary: Get Repos Owner Repo Labels Name
      description: Get a single label.
      operationId: get-a-single-label
      x-api-path-slug: reposownerrepolabelsname-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: name
        description: Name of the label
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Labels
      - Name
    patch:
      summary: Patch Repos Owner Repo Labels Name
      description: Update a label.
      operationId: update-a-label
      x-api-path-slug: reposownerrepolabelsname-patch
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: name
        description: Name of the label
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Labels
      - Name