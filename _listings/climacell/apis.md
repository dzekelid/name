---
name: ClimaCell
x-slug: climacell
description: ClimaCell provides the most accurate weather data in the world by integrating
  proprietary data extracted from wireless networks and other new sensing technologies
  with data from traditional sensors. With 90% correlation to ground truth (vs. 50%
  using radar), it&rsquo;s the best you can get for your enterprise.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28707-climacell.jpg
x-kinRank: "9"
x-alexaRank: "617213"
tags: Name
created: "2018-08-28"
modified: "2018-08-28"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/climacell/apis.md
specificationVersion: "0.14"
apis:
- name: ClimaCell API - Post Alerts
  x-api-slug: alerts-post
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28707-climacell.jpg
  humanURL: https://www.climacell.co
  baseURL: https://api2.climacell.co//v2
  tags: Weather, API Provider, Profiles, General Data
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/climacell/alerts-post-openapi.md
x-common:
- type: x-api-gallery
  url: http://clickatell.api.gallery.streamdata.io
- type: x-api-stack
  url: http://climacell.stack.network
- type: x-blog
  url: https://www.climacell.co/blog/
- type: x-crunchbase
  url: https://crunchbase.com/organization/climacell
- type: x-developer
  url: https://www.climacell.co/api/
- type: x-email
  url: info@climacell.co
- type: x-email
  url: support@climacell.co
- type: x-email
  url: sales@climacell.co
- type: x-faq
  url: https://developer.climacell.co/FAQ
- type: x-github
  url: https://github.com/climacell
- type: x-pricing
  url: https://developer.climacell.co/
- type: x-privacy-policy
  url: https://www.climacell.co/privacy/
- type: x-terms-of-service
  url: https://www.climacell.co/terms-of-service/
- type: x-twitter
  url: https://twitter.com/WeatherRevealed
- type: x-website
  url: https://www.climacell.co
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---