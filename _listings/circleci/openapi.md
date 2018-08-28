swagger: "2.0"
x-collection-name: CircleCI
x-complete: 1
info:
  title: CircleCI
  description: the-circleci-api-is-a-restful-fullyfeatured-api-that-allows-you-to-do-almost-anything-in-circleci--you-can-access-all-information-and-trigger-all-actions--the-only-thing-we-dont-provide-access-to-is-billing-functions-which-must-be-done-from-the-circleci-web-ui-
  version: 1.0.0
host: circleci.com
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /project/{username}/{project}/envvar/{name}:
    delete:
      summary: Delete Project Username Project Envvar Name
      description: Deletes the environment variable named ':name'
      operationId: deleteProjectUsernameProjectEnvvarName
      x-api-path-slug: projectusernameprojectenvvarname-delete
      responses:
        200:
          description: OK
      tags:
      - Project
      - Username
      - Project
      - Envvar
      - Name
    get:
      summary: Get Project Username Project Envvar Name
      description: Gets the hidden value of environment variable :name
      operationId: getProjectUsernameProjectEnvvarName
      x-api-path-slug: projectusernameprojectenvvarname-get
      responses:
        200:
          description: OK
      tags:
      - Project
      - Username
      - Project
      - Envvar
      - Name
    parameters:
      summary: Parameters Project Username Project Envvar Name
      description: Parameters project username project envvar name.
      operationId: parametersProjectUsernameProjectEnvvarName
      x-api-path-slug: projectusernameprojectenvvarname-parameters
      responses:
        200:
          description: OK
      tags:
      - Parameters
      - Project
      - Username
      - Project
      - Envvar
      - Name