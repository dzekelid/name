---
swagger: "2.0"
x-collection-name: Mattermost
x-complete: 0
info:
  title: Mattermost API Get a channel by name
  description: |-
    Gets channel from the provided team id and channel name strings.
    ##### Permissions
    `read_channel` permission for the channel.
  termsOfService: https://about.mattermost.com/default-terms/
  version: 4.0.0
host: your-mattermost-url.com
basePath: /api/v4
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /teams/name/{name}:
    get:
      summary: Get a team by name
      description: |-
        Get a team based on provided name string
        ##### Permissions
        Must be authenticated, team type is open and have the `view_team` permission.
      operationId: get-a-team-based-on-provided-name-string-permissionsmust-be-authenticated-team-type-is-open-and-have
      x-api-path-slug: teamsnamename-get
      parameters:
      - in: path
        name: name
        description: Team Name
      responses:
        200:
          description: OK
      tags:
      - Team
      - By
      - Name
  /teams/{team_id}/channels/name/{channel_name}:
    get:
      summary: Get a channel by name
      description: |-
        Gets channel from the provided team id and channel name strings.
        ##### Permissions
        `read_channel` permission for the channel.
      operationId: gets-channel-from-the-provided-team-id-and-channel-name-strings-permissionsread-channel-permission-f
      x-api-path-slug: teamsteam-idchannelsnamechannel-name-get
      parameters:
      - in: path
        name: channel_name
        description: Channel Name
      - in: path
        name: team_id
        description: Team GUID
      responses:
        200:
          description: OK
      tags:
      - Channel
      - By
      - Name
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