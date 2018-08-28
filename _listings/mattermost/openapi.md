swagger: "2.0"
x-collection-name: Mattermost
x-complete: 1
info:
  title: Mattermost
  version: 1.0.0
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
  /teams/name/{team_name}/channels/name/{channel_name}:
    get:
      summary: Get a channel by name and team name
      description: |-
        Gets a channel from the provided team name and channel name strings.
        ##### Permissions
        `read_channel` permission for the channel.
      operationId: gets-a-channel-from-the-provided-team-name-and-channel-name-strings-permissionsread-channel-permissi
      x-api-path-slug: teamsnameteam-namechannelsnamechannel-name-get
      parameters:
      - in: path
        name: channel_name
        description: Channel Name
      - in: path
        name: team_name
        description: Team Name
      responses:
        200:
          description: OK
      tags:
      - Channel
      - By
      - Name
      - Team
      - Name
  /emoji/name/{emoji_name}:
    get:
      summary: Get a custom emoji by name
      description: |-
        Get some metadata for a custom emoji using its name.
        ##### Permissions
        Must be authenticated.

        __Minimum server version__: 4.7
      operationId: get-some-metadata-for-a-custom-emoji-using-its-name-permissionsmust-be-authenticated-minimum-server-
      x-api-path-slug: emojinameemoji-name-get
      parameters:
      - in: path
        name: emoji_name
        description: Emoji name
      responses:
        200:
          description: OK
      tags:
      - Custom
      - Emoji
      - By
      - Name
  /roles/names:
    post:
      summary: Get a list of roles by name
      description: |-
        Get a list of roles from their names.

        ##### Permissions
        Requires an active session but no other permissions.

        __Minimum server version__: 4.9
      operationId: get-a-list-of-roles-from-their-names-permissionsrequires-an-active-session-but-no-other-permissions-
      x-api-path-slug: rolesnames-post
      parameters:
      - in: body
        name: body
        description: List of role names
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - List
      - Of
      - Roles
      - By
      - Name