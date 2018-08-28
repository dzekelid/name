---
swagger: "2.0"
x-collection-name: CallFire
x-complete: 0
info:
  title: Callfire Get call mp3 recording by name
  description: Returns a MP3 recording of a particular call, response contains binary
    data, content type is 'audio/mpeg'
  termsOfService: https://www.callfire.com/legal/terms
  contact:
    name: CallFire
    url: https://www.callfire.com
    email: support@callfire.com
  version: 1.0.0
host: www.callfire.com
basePath: /v2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /calls/{id}/recordings/{name}:
    get:
      summary: Get call recording by name
      description: Returns recording metadata of particular call. Metadata contains
        link to a MP3 recording
      operationId: getCallRecordingByName
      x-api-path-slug: callsidrecordingsname-get
      parameters:
      - in: query
        name: fields
        description: Limit fields received in response
      - in: path
        name: id
        description: An id of a call
      - in: path
        name: name
        description: A name of a recording
      responses:
        200:
          description: OK
      tags:
      - Calls
      - Recordings
      - Name
  /calls/{id}/recordings/{name}.mp3:
    get:
      summary: Get call mp3 recording by name
      description: Returns a MP3 recording of a particular call, response contains
        binary data, content type is 'audio/mpeg'
      operationId: getCallRecordingMp3ByName
      x-api-path-slug: callsidrecordingsname-mp3-get
      parameters:
      - in: path
        name: id
        description: An id of a call
      - in: path
        name: name
        description: A name of a recording
      responses:
        200:
          description: OK
      tags:
      - Calls
      - Recordings
      - Name.mp3
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