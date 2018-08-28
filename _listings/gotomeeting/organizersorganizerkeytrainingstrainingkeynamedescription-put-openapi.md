---
swagger: "2.0"
x-collection-name: GoToMeeting
x-complete: 0
info:
  title: Go To Training Update Training Name and Description
  description: Request to update a scheduled training name and description.
  termsOfService: https://developer.citrixonline.com/terms-use
  contact:
    name: Developer Support
    url: https://developer.citrixonline.com
    email: developer-support@citrixonline.com
  version: 1.0.0
host: api.citrixonline.com
basePath: /G2T/rest
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
      description: Request to update a scheduled training name and description.
      operationId: updateTrainingNameDescription
      x-api-path-slug: organizersorganizerkeytrainingstrainingkeynamedescription-put
      parameters:
      - in: body
        name: body
        description: The new name and description for the training
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Organizers
      - OrganizerKey
      - Trainings
      - TrainingKey
      - NameDescription
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