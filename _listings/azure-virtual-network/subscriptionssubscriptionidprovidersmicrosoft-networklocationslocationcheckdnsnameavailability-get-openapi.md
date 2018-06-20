---
swagger: "2.0"
x-collection-name: Azure Virtual Network
x-complete: 0
info:
  title: Azure Virtual Network API Check Dns Name Availability
  description: Checks whether a domain name in the cloudapp.net zone is available
    for use.
  version: 1.0.0
host: management.azure.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /subscriptions/{subscriptionId}/providers/Microsoft.Network/locations/{location}/CheckDnsNameAvailability:
    get:
      summary: Check Dns Name Availability
      description: Checks whether a domain name in the cloudapp.net zone is available
        for use.
      operationId: CheckDnsNameAvailability
      x-api-path-slug: subscriptionssubscriptionidprovidersmicrosoft-networklocationslocationcheckdnsnameavailability-get
      parameters:
      - in: query
        name: domainNameLabel
        description: The domain name to be verified
      - in: path
        name: location
        description: The location of the domain name
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Dns Name Availability
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