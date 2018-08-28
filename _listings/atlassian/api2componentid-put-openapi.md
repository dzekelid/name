---
swagger: "2.0"
x-collection-name: Atlassian
x-complete: 0
info:
  title: Jira Cloud API Update component
  description: |-
    Modifies a component. Any fields included in the request are overwritten. If `leadUserName` is an empty string ("") the component lead is removed. [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required: Any of the following:

    *   _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
    *   _Administer projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
  termsOfService: http://atlassian.com/terms/
  version: 1.0.0
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/2/projectvalidate/validProjectName:
    get:
      summary: Get valid project name
      description: Validates a project name. If the name is invalid, an attempt is
        made to produce a valid name based on the supplied one. If no such valid name
        can be found, an empty string is returned.
      operationId: com.atlassian.jira.rest.v2.issue.ProjectValidateResource.getValidProjectName_get
      x-api-path-slug: api2projectvalidatevalidprojectname-get
      parameters:
      - in: query
        name: name
        description: the project name
      responses:
        200:
          description: OK
      tags:
      - Valid
      - Project
      - Name
  /api/2/component/{id}:
    put:
      summary: Update component
      description: |-
        Modifies a component. Any fields included in the request are overwritten. If `leadUserName` is an empty string ("") the component lead is removed. [Permissions](https://confluence.atlassian.com/x/FQiiLQ) required: Any of the following:

        *   _Administer Jira_ [global permission](https://confluence.atlassian.com/x/x4dKLg).
        *   _Administer projects_ [project permission](https://confluence.atlassian.com/x/yodKLg).
      operationId: com.atlassian.jira.rest.v2.issue.ComponentResource.updateComponent_put
      x-api-path-slug: api2componentid-put
      parameters:
      - in: header
        name: force-account-id
      - in: path
        name: id
      responses:
        200:
          description: OK
      tags:
      - Component
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