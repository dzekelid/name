---
name: GitHub
x-slug: github
description: GitHub brings together the worlds largest community of developers to
  discover, share, and build better software. From open source projects to private
  team repositories, were your all-in-one platform for collaborative development.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/github-logo.png
x-kinRank: "10"
x-alexaRank: "64"
tags: Name
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/apis.md
specificationVersion: "0.14"
apis:
- name: Github Delete Orgs Org Members Username
  x-api-slug: github
  description: |-
    Remove a member.
    Removing a user from this list will remove them from all teams and they
    will no longer have any access to the organization's repositories.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/github-logo.png
  humanURL: https://github.com
  baseURL: https://api.github.com////orgs/{org}/members/{username}
  tags: Orgs, Org, Members, Username
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/orgsorgmembersusername-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/orgsorgmembersusername-delete-openapi.md
- name: Github Get Orgs Org Members Username
  x-api-slug: github
  description: Check if a user is, publicly or privately, a member of the organization.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/github-logo.png
  humanURL: https://github.com
  baseURL: https://api.github.com////orgs/{org}/members/{username}
  tags: Orgs, Org, Members, Username
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/orgsorgmembersusername-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/orgsorgmembersusername-get-openapi.md
- name: Github Delete Orgs Org Public Members Username
  x-api-slug: github
  description: Conceal a user's membership.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/github-logo.png
  humanURL: https://github.com
  baseURL: https://api.github.com////orgs/{org}/public_members/{username}
  tags: Orgs, Org, Public, Members, Username
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/orgsorgpublic-membersusername-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/orgsorgpublic-membersusername-delete-openapi.md
- name: Github Get Orgs Org Public Members Username
  x-api-slug: github
  description: Check public membership.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/github-logo.png
  humanURL: https://github.com
  baseURL: https://api.github.com////orgs/{org}/public_members/{username}
  tags: Orgs, Org, Public, Members, Username
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/orgsorgpublic-membersusername-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/orgsorgpublic-membersusername-get-openapi.md
- name: Github Put Orgs Org Public Members Username
  x-api-slug: github
  description: Publicize a user's membership.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/github-logo.png
  humanURL: https://github.com
  baseURL: https://api.github.com////orgs/{org}/public_members/{username}
  tags: Orgs, Org, Public, Members, Username
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/orgsorgpublic-membersusername-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/orgsorgpublic-membersusername-put-openapi.md
- name: Github Delete Repos Owner Repo Issues Number Labels Name
  x-api-slug: github
  description: Remove a label from an issue.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/github-logo.png
  humanURL: https://github.com
  baseURL: https://api.github.com////repos/{owner}/{repo}/issues/{number}/labels/{name}
  tags: Repos, Owner, Repo, Issues, Number, Labels, Name
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/reposownerrepoissuesnumberlabelsname-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/reposownerrepoissuesnumberlabelsname-delete-openapi.md
- name: Github Delete Repos Owner Repo Labels Name
  x-api-slug: github
  description: Delete a label.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/github-logo.png
  humanURL: https://github.com
  baseURL: https://api.github.com////repos/{owner}/{repo}/labels/{name}
  tags: Repos, Owner, Repo, Labels, Name
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/reposownerrepolabelsname-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/reposownerrepolabelsname-delete-openapi.md
- name: Github Get Repos Owner Repo Labels Name
  x-api-slug: github
  description: Get a single label.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/github-logo.png
  humanURL: https://github.com
  baseURL: https://api.github.com////repos/{owner}/{repo}/labels/{name}
  tags: Repos, Owner, Repo, Labels, Name
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/reposownerrepolabelsname-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/reposownerrepolabelsname-get-openapi.md
- name: Github Patch Repos Owner Repo Labels Name
  x-api-slug: github
  description: Update a label.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/github-logo.png
  humanURL: https://github.com
  baseURL: https://api.github.com////repos/{owner}/{repo}/labels/{name}
  tags: Repos, Owner, Repo, Labels, Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/reposownerrepolabelsname-patch-openapi.md
- name: Github Delete Teams Team Members Username
  x-api-slug: github
  description: |-
    The "Remove team member" API is deprecated and is scheduled for removal in the next major version of the API. We recommend using the Remove team membership API instead. It allows you to remove both active and pending memberships.

    Remove team member.
    In order to remove a user from a team, the authenticated user must have 'admin'
    permissions to the team or be an owner of the org that the team is associated
    with.
    NOTE This does not delete the user, it just remove them from the team.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/github-logo.png
  humanURL: https://github.com
  baseURL: https://api.github.com////teams/{teamId}/members/{username}
  tags: Teams, Team, Members, Username
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/teamsteamidmembersusername-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/teamsteamidmembersusername-delete-openapi.md
- name: Github Get Teams Team Members Username
  x-api-slug: github
  description: |-
    The "Get team member" API is deprecated and is scheduled for removal in the next major version of the API. We recommend using the Get team membership API instead. It allows you to get both active and pending memberships.

    Get team member.
    In order to get if a user is a member of a team, the authenticated user mus
    be a member of the team.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/github-logo.png
  humanURL: https://github.com
  baseURL: https://api.github.com////teams/{teamId}/members/{username}
  tags: Teams, Team, Members, Username
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/teamsteamidmembersusername-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/teamsteamidmembersusername-get-openapi.md
- name: Github Put Teams Team Members Username
  x-api-slug: github
  description: |-
    The API (described below) is deprecated and is scheduled for removal in the next major version of the API. We recommend using the Add team membership API instead. It allows you to invite new organization members to your teams.

    Add team member.
    In order to add a user to a team, the authenticated user must have 'admin'
    permissions to the team or be an owner of the org that the team is associated
    with.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/github-logo.png
  humanURL: https://github.com
  baseURL: https://api.github.com////teams/{teamId}/members/{username}
  tags: Teams, Team, Members, Username
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/teamsteamidmembersusername-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/teamsteamidmembersusername-put-openapi.md
- name: Github Delete Teams Team Memberships Username
  x-api-slug: github
  description: |-
    Remove team membership.
    In order to remove a membership between a user and a team, the authenticated user must have 'admin' permissions to the team or be an owner of the organization that the team is associated with. NOTE: This does not delete the user, it just removes their membership from the team.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/github-logo.png
  humanURL: https://github.com
  baseURL: https://api.github.com////teams/{teamId}/memberships/{username}
  tags: Teams, Team, Memberships, Username
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/teamsteamidmembershipsusername-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/teamsteamidmembershipsusername-delete-openapi.md
- name: Github Get Teams Team Memberships Username
  x-api-slug: github
  description: |-
    Get team membership.
    In order to get a user's membership with a team, the authenticated user must be a member of the team or an owner of the team's organization.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/github-logo.png
  humanURL: https://github.com
  baseURL: https://api.github.com////teams/{teamId}/memberships/{username}
  tags: Teams, Team, Memberships, Username
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/teamsteamidmembershipsusername-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/teamsteamidmembershipsusername-get-openapi.md
- name: Github Put Teams Team Memberships Username
  x-api-slug: github
  description: |-
    Add team membership.
    In order to add a membership between a user and a team, the authenticated user must have 'admin' permissions to the team or be an owner of the organization that the team is associated with.

    If the user is already a part of the team's organization (meaning they're on at least one other team in the organization), this endpoint will add the user to the team.

    If the user is completely unaffiliated with the team's organization (meaning they're on none of the organization's teams), this endpoint will send an invitation to the user via email. This newly-created membership will be in the 'pending' state until the user accepts the invitation, at which point the membership will transition to the 'active' state and the user will be added as a member of the team.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/github-logo.png
  humanURL: https://github.com
  baseURL: https://api.github.com////teams/{teamId}/memberships/{username}
  tags: Teams, Team, Memberships, Username
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/teamsteamidmembershipsusername-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/teamsteamidmembershipsusername-put-openapi.md
- name: Github Delete User Following Username
  x-api-slug: github
  description: |-
    Unfollow a user.
    Unfollowing a user requires the user to be logged in and authenticated with
    basic auth or OAuth with the user:follow scope.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/github-logo.png
  humanURL: https://github.com
  baseURL: https://api.github.com////user/following/{username}
  tags: User, Following, Username
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/userfollowingusername-delete-openapi.md
- name: Github Get User Following Username
  x-api-slug: github
  description: Check if you are following a user.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/github-logo.png
  humanURL: https://github.com
  baseURL: https://api.github.com////user/following/{username}
  tags: User, Following, Username
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/userfollowingusername-get-openapi.md
- name: Github Put User Following Username
  x-api-slug: github
  description: |-
    Follow a user.
    Following a user requires the user to be logged in and authenticated with
    basic auth or OAuth with the user:follow scope.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/github-logo.png
  humanURL: https://github.com
  baseURL: https://api.github.com////user/following/{username}
  tags: User, Following, Username
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/userfollowingusername-put-openapi.md
- name: Github Get Users Username
  x-api-slug: github
  description: Get a single user.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/github-logo.png
  humanURL: https://github.com
  baseURL: https://api.github.com////users/{username}
  tags: Users, Username
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/usersusername-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/usersusername-get-openapi.md
- name: Github Get Users Username Events
  x-api-slug: github
  description: If you are authenticated as the given user, you will see your private
    events. Otherwise, you'll only see public events.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/github-logo.png
  humanURL: https://github.com
  baseURL: https://api.github.com////users/{username}/events
  tags: Users, Username, Events
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/usersusernameevents-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/usersusernameevents-get-openapi.md
- name: Github Get Users Username Events Orgs Org
  x-api-slug: github
  description: This is the user's organization dashboard. You must be authenticated
    as the user to view this.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/github-logo.png
  humanURL: https://github.com
  baseURL: https://api.github.com////users/{username}/events/orgs/{org}
  tags: Users, Username, Events, Orgs, Org
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/usersusernameeventsorgsorg-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/usersusernameeventsorgsorg-get-openapi.md
- name: Github Get Users Username Followers
  x-api-slug: github
  description: List a user's followers
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/github-logo.png
  humanURL: https://github.com
  baseURL: https://api.github.com////users/{username}/followers
  tags: Users, Username, Followers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/usersusernamefollowers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/usersusernamefollowers-get-openapi.md
- name: Github Get Users Username Following Targetuser
  x-api-slug: github
  description: Check if one user follows another.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/github-logo.png
  humanURL: https://github.com
  baseURL: https://api.github.com////users/{username}/following/{targetUser}
  tags: Users, Username, Following, Targetuser
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/usersusernamefollowingtargetuser-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/usersusernamefollowingtargetuser-get-openapi.md
- name: Github Get Users Username Gists
  x-api-slug: github
  description: List a users gists.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/github-logo.png
  humanURL: https://github.com
  baseURL: https://api.github.com////users/{username}/gists
  tags: Users, Username, Gists
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/usersusernamegists-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/usersusernamegists-get-openapi.md
- name: Github Get Users Username Keys
  x-api-slug: github
  description: |-
    List public keys for a user.
    Lists the verified public keys for a user. This is accessible by anyone.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/github-logo.png
  humanURL: https://github.com
  baseURL: https://api.github.com////users/{username}/keys
  tags: Users, Username, Keys
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/usersusernamekeys-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/usersusernamekeys-get-openapi.md
- name: Github Get Users Username Orgs
  x-api-slug: github
  description: List all public organizations for a user.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/github-logo.png
  humanURL: https://github.com
  baseURL: https://api.github.com////users/{username}/orgs
  tags: Users, Username, Orgs
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/usersusernameorgs-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/usersusernameorgs-get-openapi.md
- name: Github Get Users Username Received Events
  x-api-slug: github
  description: These are events that you'll only see public events.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/github-logo.png
  humanURL: https://github.com
  baseURL: https://api.github.com////users/{username}/received_events
  tags: Users, Username, Received, Events
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/usersusernamereceived-events-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/usersusernamereceived-events-get-openapi.md
- name: Github Get Users Username Received Events Public
  x-api-slug: github
  description: List public events that a user has received
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/github-logo.png
  humanURL: https://github.com
  baseURL: https://api.github.com////users/{username}/received_events/public
  tags: Users, Username, Received, Events, Public
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/usersusernamereceived-eventspublic-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/usersusernamereceived-eventspublic-get-openapi.md
- name: Github Get Users Username Repos
  x-api-slug: github
  description: List public repositories for the specified user.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/github-logo.png
  humanURL: https://github.com
  baseURL: https://api.github.com////users/{username}/repos
  tags: Users, Username, Repos
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/usersusernamerepos-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/usersusernamerepos-get-openapi.md
- name: Github Get Users Username Starred
  x-api-slug: github
  description: List repositories being starred by a user.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/github-logo.png
  humanURL: https://github.com
  baseURL: https://api.github.com////users/{username}/starred
  tags: Users, Username, Starred
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/usersusernamestarred-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/usersusernamestarred-get-openapi.md
- name: Github Get Users Username Subscriptions
  x-api-slug: github
  description: List repositories being watched by a user.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/github-logo.png
  humanURL: https://github.com
  baseURL: https://api.github.com////users/{username}/subscriptions
  tags: Users, Username, Subscriptions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/usersusernamesubscriptions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/usersusernamesubscriptions-get-openapi.md
- name: Github
  x-api-slug: github
  description: GitHub brings together the worlds largest community of developers to
    discover, share, and build better software. From open source projects to private
    team repositories, were your all-in-one platform for collaborative development.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/github-logo.png
  humanURL: https://github.com
  baseURL: https://api.github.com//
  tags: Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/github/openapi.md
x-common:
- type: x--net-library
  url: https://github.com/octokit/octokit.net
- type: x-base
  url: https://api.github.com
- type: x-blog
  url: http://github.com/blog
- type: x-blog-rss
  url: https://github.com/blog/subscribe
- type: x-change-log
  url: https://developer.github.com/changes/
- type: x-contact-form
  url: https://github.com/contact
- type: x-crunchbase
  url: http://www.crunchbase.com/company/github
- type: x-crunchbase
  url: https://crunchbase.com/organization/github
- type: x-developer
  url: https://developer.github.com/
- type: x-github
  url: https://github.com/github
- type: x-guides
  url: https://developer.github.com/guides/
- type: x-ios-sdk
  url: https://github.com/octokit/octokit.objc
- type: x-pricing
  url: https://github.com/pricing
- type: x-privacy
  url: http://help.github.com/privacy-policy/
- type: x-ruby-library
  url: https://github.com/octokit/octokit.rb
- type: x-security
  url: http://help.github.com/security/
- type: x-status
  url: https://status.github.com/
- type: x-terms-of-service
  url: http://help.github.com/terms-of-service/
- type: x-transparency-report
  url: https://github.com/blog/1987-github-s-2014-transparency-report
- type: x-twitter
  url: https://twitter.com/github
- type: x-webhooks
  url: https://developer.github.com/webhooks/
- type: x-website
  url: https://github.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---