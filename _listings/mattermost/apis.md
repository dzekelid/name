---
name: Mattermost
x-slug: mattermost
description: Open source, private cloud Slack-alternative, Workplace messaging for
  web, PCs and phones. MIT-licensed. Hundreds of contributors. 14 languages. Secure,
  configurable, and scalable from teams to the enterprise.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/mattermost-logo.png
x-kinRank: "8"
x-alexaRank: "95684"
tags: Name
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/mattermost/apis.md
specificationVersion: "0.14"
apis:
- name: Mattermost API Get users by usernames
  x-api-slug: mattermost-api
  description: |-
    Get a list of users based on a provided list of usernames.
    ##### Permissions
    Requires an active session but no other permissions.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/mattermost-logo.png
  humanURL: https://mattermost.com
  baseURL: https://your-mattermost-url.com//api/v4//users/usernames
  tags: Users,By,Usernames
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/mattermost/usersusernames-post-openapi.md
- name: Mattermost API Get a user by username
  x-api-slug: mattermost-api
  description: |-
    Get a user object by providing a username. Sensitive information will be sanitized out.
    ##### Permissions
    Requires an active session but no other permissions.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/mattermost-logo.png
  humanURL: https://mattermost.com
  baseURL: https://your-mattermost-url.com//api/v4//users/username/{username}
  tags: User,By,Username
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/mattermost/usersusernameusername-get-openapi.md
- name: Mattermost API Get a team by name
  x-api-slug: mattermost-api
  description: |-
    Get a team based on provided name string
    ##### Permissions
    Must be authenticated, team type is open and have the `view_team` permission.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/mattermost-logo.png
  humanURL: https://mattermost.com
  baseURL: https://your-mattermost-url.com//api/v4//teams/name/{name}
  tags: Team,By,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/mattermost/teamsnamename-get-openapi.md
- name: Mattermost API Get a channel by name
  x-api-slug: mattermost-api
  description: |-
    Gets channel from the provided team id and channel name strings.
    ##### Permissions
    `read_channel` permission for the channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/mattermost-logo.png
  humanURL: https://mattermost.com
  baseURL: https://your-mattermost-url.com//api/v4//teams/{team_id}/channels/name/{channel_name}
  tags: Channel,By,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/mattermost/teamsteam-idchannelsnamechannel-name-get-openapi.md
- name: Mattermost API Get a channel by name and team name
  x-api-slug: mattermost-api
  description: |-
    Gets a channel from the provided team name and channel name strings.
    ##### Permissions
    `read_channel` permission for the channel.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/mattermost-logo.png
  humanURL: https://mattermost.com
  baseURL: https://your-mattermost-url.com//api/v4//teams/name/{team_name}/channels/name/{channel_name}
  tags: Channel,By,Name,Team,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/mattermost/teamsnameteam-namechannelsnamechannel-name-get-openapi.md
- name: Mattermost API Get a custom emoji by name
  x-api-slug: mattermost-api
  description: |-
    Get some metadata for a custom emoji using its name.
    ##### Permissions
    Must be authenticated.

    __Minimum server version__: 4.7
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/mattermost-logo.png
  humanURL: https://mattermost.com
  baseURL: https://your-mattermost-url.com//api/v4//emoji/name/{emoji_name}
  tags: Custom,Emoji,By,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/mattermost/emojinameemoji-name-get-openapi.md
- name: Mattermost API Get a list of roles by name
  x-api-slug: mattermost-api
  description: |-
    Get a list of roles from their names.

    ##### Permissions
    Requires an active session but no other permissions.

    __Minimum server version__: 4.9
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/mattermost-logo.png
  humanURL: https://mattermost.com
  baseURL: https://your-mattermost-url.com//api/v4//roles/names
  tags: List,Of,Roles,By,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/mattermost/rolesnames-post-openapi.md
- name: Mattermost API
  x-api-slug: mattermost-api
  description: Open source, private cloud Slack-alternative, Workplace messaging for
    web, PCs and phones. MIT-licensed. Hundreds of contributors. 14 languages. Secure,
    configurable, and scalable from teams to the enterprise.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/mattermost-logo.png
  humanURL: https://mattermost.com
  baseURL: https://your-mattermost-url.com//api/v4
  tags: Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/mattermost/openapi.md
x-common:
- type: x-blog
  url: https://about.mattermost.com/blog/
- type: x-blog-rss
  url: https://about.mattermost.com/feed/
- type: x-crunchbase
  url: https://crunchbase.com/organization/mattermost
- type: x-developer
  url: https://api.mattermost.com/
- type: x-github
  url: https://github.com/mattermost
- type: x-pricing
  url: https://about.mattermost.com/pricing/
- type: x-security
  url: https://docs.mattermost.com/overview/security.html
- type: x-twitter
  url: https://twitter.com/mattermosthq
- type: x-website
  url: https://mattermost.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---