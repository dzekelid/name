swagger: "2.0"
x-collection-name: ClimaCell
x-complete: 1
info:
  title: ClimaCell API
  description: the-climacell-rest-api-provides-access-to-high-resolution-weather-data-for-locations-across-the-u-s--with-global-data-coming-soon--it-uses-https-and-requires-an-access-token-key--the-api-requests-carry-query-parameters-and-the-responses-return-results-in-json-format-
  version: 1.0.0
host: api2.climacell.co
basePath: /v2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /alerts:
    post:
      summary: Post Alerts
      description: |-
        ### Create an Alert
        Creates a new Alert with the following information:

        * ```name``` - Alert Name
        * ```location_name``` - Location name for which the alert pertains (location has to be created earlier)
        * ```notice``` - Prior notice in seconds
        * ```conditions``` - logical expression defining a weather event such as: rain with intensity of more than 1 mm/hr. Several expressions can be concatenated with ???or??? logical operator. An alert will trigger for it if any of its contained conditions are met. ORs can contain any number of conditions.

        NOTE:??? AND condition ??? coming soon

        ### In addition to the format below, this is an example with an "OR" conditional statement:
          ```
          {
            "name": "alert with or",
            "location_name": "your-location-name",
            "notice": 3600,
            "conditions": [
              {
                "or": [
                  {
                    "parameter": "Rain",
                    "value": 0.15,
                    "operator": "lt"
                  },
                  {
                    "parameter": "Temperature",
                    "value": 25,
                    "operator": "lt"
                  }
                ]
              }
            ],
            "groups": [
              {
                "name": "your-group-name",
                "delivery": {
                  "sms": true,
                  "email": false
                }
              }
            ],
            "webhooks": [507f1f77bcf86cd799439011]
          }
          ```
        ### In addition to the format below, this is an example with an "AND" conditional statement:

          ```
          {
            "name": "alert with AND conditions",
            "location_name": "your-location-name",
            "notice": 3600,
            "conditions": [
              {
                "parameter": "Rain",
                "value": 0.15,
                "operator": "gt"
              },
              {
                "parameter": "Temperature",
                "value": 40,
                "operator": "lt"
              }
            ],
            "groups": [
              {
                "name": "your-group-name",
                "delivery": {
                  "sms": true,
                  "email": false
                }
              }
            ],
            "webhooks": [507f1f77bcf86cd799439011]
          }
          ```
      operationId: -create-an-alertcreates-a-new-alert-with-the-following-information-name--alert-name-location-name--l
      x-api-path-slug: alerts-post
      parameters:
      - in: body
        name: alert
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Weather
      - Alerts