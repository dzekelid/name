---
swagger: "2.0"
x-collection-name: Twilio
x-complete: 0
info:
  title: Twilio Add SIP Credentials List
  description: Change the FriendlyName of the list
  termsOfService: https://www.twilio.com/legal/tos
  version: v1
host: api.twilio.com
basePath: /2010-04-01/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /Accounts/{AccountSid}/Queues/{QueueSid}:
    post:
      summary: Add Queue Members
      description: This POST request allows you to change the FriendlyName or MaxSize.n
      operationId: this-post-request-allows-you-to-change-the-friendlyname-or-maxsize
      x-api-path-slug: accountsaccountsidqueuesqueuesid-post
      parameters:
      - in: path
        name: AccountSid
        description: The ID for the Twilio account
      - in: path
        name: QueueSid
        description: A 34 character string that uniquely identifies the queue
      responses:
        200:
          description: OK
      tags:
      - Queues
  /Accounts/{AccountSid}/SIP/CredentialLists/{CLSid}:
    post:
      summary: Add SIP Credentials List
      description: Change the FriendlyName of the list
      operationId: change-the-friendlyname-of-the-list
      x-api-path-slug: accountsaccountsidsipcredentiallistsclsid-post
      parameters:
      - in: path
        name: AccountSid
        description: The ID for the Twilio account
      - in: path
        name: CLSid
        description: A 34 character string that uniquely identifies the credential
          list
      responses:
        200:
          description: OK
      tags:
      - SIP Credential Lists
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