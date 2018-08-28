swagger: "2.0"
x-collection-name: LogMeIn
x-complete: 1
info:
  title: GoToWebinar API
  description: todo-add-description
  version: 1.0.0
host: api.getgo.com
basePath: /G2W/rest/organizers
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /organizers/{organizerKey}/trainings/{trainingKey}/nameDescription:
    put:
      summary: Update Training Name and Description
      description: Update training name and description.
      operationId: OrganizersTrainingsNameDescriptionByOrganizerKeyAndTrainingKeyPut
      x-api-path-slug: organizersorganizerkeytrainingstrainingkeynamedescription-put
      parameters:
      - in: header
        name: Accept
      - in: body
        name: Body
        schema:
          $ref: '#/definitions/holder'
      - in: header
        name: Content-Type
      - in: path
        name: organizerKey
      - in: path
        name: trainingKey
      responses:
        200:
          description: OK
      tags:
      - Training
      - Name
      - Description