swagger: "2.0"
x-collection-name: Expedia
x-complete: 1
info:
  title: Expedia
  description: expedia-mobile-api-documentation--brfont-colorblue-note-in-case-of-authorization-exception-just-a-hrefstaticmobileswaggeruiusersigninusersigninafont
  version: 0.0.1
host: apim.expedia.com
basePath: x/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/trips/{tripId}/updateTripNameDescription:
    post:
      summary: Update Trip Name and Description
      description: Mobile API Trips update trip name and description operation
      operationId: trips-update-trip
      x-api-path-slug: apitripstripidupdatetripnamedescription-post
      parameters:
      - in: path
        name: tripId
        description: Trip ID
      - in: formData
        name: tripname
        description: The name of the trip
      - in: formData
        name: tripnote
        description: The comments of the trip
      responses:
        200:
          description: OK
      tags:
      - Travel
      - Search
      - Trips