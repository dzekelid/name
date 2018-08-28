swagger: "2.0"
x-collection-name: Atlassian
x-complete: 1
info:
  title: Stride API
  description: this-service-provides-public-api-for-the-stride-
  version: 1.0.0
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
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
  /api/2/status/{idOrName}:
    get:
      summary: Get status
      description: Returns a full representation of the Status having the given id
        or name. If there are two statuses with the same name, only the first found
        status will be returned. Therefore searching by id is encouraged.
      operationId: com.atlassian.jira.rest.v2.issue.StatusResource.getStatus_get
      x-api-path-slug: api2statusidorname-get
      parameters:
      - in: path
        name: idOrName
        description: a numeric Status id or a status name
      responses:
        200:
          description: OK
      tags:
      - Status
  /api/2/workflow:
    get:
      summary: Get all workflows
      description: |-
        Returns all workflows in Jira or a single workflow.

        If the `workflowName` parameter is specified, a workflow will be returned as an object (not in an array). Otherwise, an array of workflow objects will be returned.

        **[Permissions](https://confluence.atlassian.com/x/FQiiLQ) required:** _Administer Jira_ global permission.
      operationId: com.atlassian.jira.rest.v2.admin.WorkflowsResource.getAllWorkflows_get
      x-api-path-slug: api2workflow-get
      parameters:
      - in: query
        name: workflowName
        description: The name of the workflow to be returned
      responses:
        200:
          description: OK
      tags:
      - Workflows