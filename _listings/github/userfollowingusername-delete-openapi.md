---
swagger: "2.0"
x-collection-name: GitHub
x-complete: 0
info:
  title: Github Delete User Following Username
  description: |-
    Unfollow a user.
    Unfollowing a user requires the user to be logged in and authenticated with
    basic auth or OAuth with the user:follow scope.
  termsOfService: https://help.github.com/articles/github-terms-of-service/#b-api-terms
  version: 1.0.0
host: api.github.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /orgs/{org}/members/{username}:
    delete:
      summary: Delete Orgs Org Members Username
      description: |-
        Remove a member.
        Removing a user from this list will remove them from all teams and they
        will no longer have any access to the organization's repositories.
      operationId: remove-a-memberremoving-a-user-from-this-list-will-remove-them-from-all-teams-and-theywill-no-longer
      x-api-path-slug: orgsorgmembersusername-delete
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: org
        description: Name of organisation
      - in: path
        name: username
        description: Name of the user
      responses:
        200:
          description: OK
      tags:
      - Orgs
      - Org
      - Members
      - Username
    get:
      summary: Get Orgs Org Members Username
      description: Check if a user is, publicly or privately, a member of the organization.
      operationId: check-if-a-user-is-publicly-or-privately-a-member-of-the-organization
      x-api-path-slug: orgsorgmembersusername-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: org
        description: Name of organisation
      - in: path
        name: username
        description: Name of the user
      responses:
        200:
          description: OK
      tags:
      - Orgs
      - Org
      - Members
      - Username
  /orgs/{org}/public_members/{username}:
    delete:
      summary: Delete Orgs Org Public Members Username
      description: Conceal a user's membership.
      operationId: conceal-a-users-membership
      x-api-path-slug: orgsorgpublic-membersusername-delete
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: org
        description: Name of organisation
      - in: path
        name: username
        description: Name of the user
      responses:
        200:
          description: OK
      tags:
      - Orgs
      - Org
      - Public
      - Members
      - Username
    get:
      summary: Get Orgs Org Public Members Username
      description: Check public membership.
      operationId: check-public-membership
      x-api-path-slug: orgsorgpublic-membersusername-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: org
        description: Name of organisation
      - in: path
        name: username
        description: Name of the user
      responses:
        200:
          description: OK
      tags:
      - Orgs
      - Org
      - Public
      - Members
      - Username
    put:
      summary: Put Orgs Org Public Members Username
      description: Publicize a user's membership.
      operationId: publicize-a-users-membership
      x-api-path-slug: orgsorgpublic-membersusername-put
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: org
        description: Name of organisation
      - in: path
        name: username
        description: Name of the user
      responses:
        200:
          description: OK
      tags:
      - Orgs
      - Org
      - Public
      - Members
      - Username
  /repos/{owner}/{repo}/issues/{number}/labels/{name}:
    delete:
      summary: Delete Repos Owner Repo Issues Number Labels Name
      description: Remove a label from an issue.
      operationId: remove-a-label-from-an-issue
      x-api-path-slug: reposownerrepoissuesnumberlabelsname-delete
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: name
        description: Name of the label
      - in: path
        name: number
        description: Number of issue
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Issues
      - Number
      - Labels
      - Name
  /repos/{owner}/{repo}/labels/{name}:
    delete:
      summary: Delete Repos Owner Repo Labels Name
      description: Delete a label.
      operationId: delete-a-label
      x-api-path-slug: reposownerrepolabelsname-delete
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: name
        description: Name of the label
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Labels
      - Name
    get:
      summary: Get Repos Owner Repo Labels Name
      description: Get a single label.
      operationId: get-a-single-label
      x-api-path-slug: reposownerrepolabelsname-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: name
        description: Name of the label
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Labels
      - Name
    patch:
      summary: Patch Repos Owner Repo Labels Name
      description: Update a label.
      operationId: update-a-label
      x-api-path-slug: reposownerrepolabelsname-patch
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: name
        description: Name of the label
      - in: path
        name: owner
        description: Name of repository owner
      - in: path
        name: repo
        description: Name of repository
      responses:
        200:
          description: OK
      tags:
      - Repos
      - Owner
      - Repo
      - Labels
      - Name
  /teams/{teamId}/members/{username}:
    delete:
      summary: Delete Teams Team Members Username
      description: |-
        The "Remove team member" API is deprecated and is scheduled for removal in the next major version of the API. We recommend using the Remove team membership API instead. It allows you to remove both active and pending memberships.

        Remove team member.
        In order to remove a user from a team, the authenticated user must have 'admin'
        permissions to the team or be an owner of the org that the team is associated
        with.
        NOTE This does not delete the user, it just remove them from the team.
      operationId: the-remove-team-member-api-is-deprecated-and-is-scheduled-for-removal-in-the-next-major-version-of-t
      x-api-path-slug: teamsteamidmembersusername-delete
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: teamId
        description: Id of team
      - in: path
        name: username
        description: Name of a member
      responses:
        200:
          description: OK
      tags:
      - Teams
      - Team
      - Members
      - Username
    get:
      summary: Get Teams Team Members Username
      description: |-
        The "Get team member" API is deprecated and is scheduled for removal in the next major version of the API. We recommend using the Get team membership API instead. It allows you to get both active and pending memberships.

        Get team member.
        In order to get if a user is a member of a team, the authenticated user mus
        be a member of the team.
      operationId: the-get-team-member-api-is-deprecated-and-is-scheduled-for-removal-in-the-next-major-version-of-the-
      x-api-path-slug: teamsteamidmembersusername-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: teamId
        description: Id of team
      - in: path
        name: username
        description: Name of a member
      responses:
        200:
          description: OK
      tags:
      - Teams
      - Team
      - Members
      - Username
    put:
      summary: Put Teams Team Members Username
      description: |-
        The API (described below) is deprecated and is scheduled for removal in the next major version of the API. We recommend using the Add team membership API instead. It allows you to invite new organization members to your teams.

        Add team member.
        In order to add a user to a team, the authenticated user must have 'admin'
        permissions to the team or be an owner of the org that the team is associated
        with.
      operationId: the-api-described-below-is-deprecated-and-is-scheduled-for-removal-in-the-next-major-version-of-the-
      x-api-path-slug: teamsteamidmembersusername-put
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: teamId
        description: Id of team
      - in: path
        name: username
        description: Name of a member
      responses:
        200:
          description: OK
      tags:
      - Teams
      - Team
      - Members
      - Username
  /teams/{teamId}/memberships/{username}:
    delete:
      summary: Delete Teams Team Memberships Username
      description: |-
        Remove team membership.
        In order to remove a membership between a user and a team, the authenticated user must have 'admin' permissions to the team or be an owner of the organization that the team is associated with. NOTE: This does not delete the user, it just removes their membership from the team.
      operationId: remove-team-membershipin-order-to-remove-a-membership-between-a-user-and-a-team-the-authenticated-us
      x-api-path-slug: teamsteamidmembershipsusername-delete
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: teamId
        description: Id of team
      - in: path
        name: username
        description: Name of a member
      responses:
        200:
          description: OK
      tags:
      - Teams
      - Team
      - Memberships
      - Username
    get:
      summary: Get Teams Team Memberships Username
      description: |-
        Get team membership.
        In order to get a user's membership with a team, the authenticated user must be a member of the team or an owner of the team's organization.
      operationId: get-team-membershipin-order-to-get-a-users-membership-with-a-team-the-authenticated-user-must-be-a-m
      x-api-path-slug: teamsteamidmembershipsusername-get
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: teamId
        description: Id of team
      - in: path
        name: username
        description: Name of a member
      responses:
        200:
          description: OK
      tags:
      - Teams
      - Team
      - Memberships
      - Username
    put:
      summary: Put Teams Team Memberships Username
      description: |-
        Add team membership.
        In order to add a membership between a user and a team, the authenticated user must have 'admin' permissions to the team or be an owner of the organization that the team is associated with.

        If the user is already a part of the team's organization (meaning they're on at least one other team in the organization), this endpoint will add the user to the team.

        If the user is completely unaffiliated with the team's organization (meaning they're on none of the organization's teams), this endpoint will send an invitation to the user via email. This newly-created membership will be in the 'pending' state until the user accepts the invitation, at which point the membership will transition to the 'active' state and the user will be added as a member of the team.
      operationId: add-team-membershipin-order-to-add-a-membership-between-a-user-and-a-team-the-authenticated-user-mus
      x-api-path-slug: teamsteamidmembershipsusername-put
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: teamId
        description: Id of team
      - in: path
        name: username
        description: Name of a member
      responses:
        200:
          description: OK
      tags:
      - Teams
      - Team
      - Memberships
      - Username
  /user/following/{username}:
    delete:
      summary: Delete User Following Username
      description: |-
        Unfollow a user.
        Unfollowing a user requires the user to be logged in and authenticated with
        basic auth or OAuth with the user:follow scope.
      operationId: unfollow-a-userunfollowing-a-user-requires-the-user-to-be-logged-in-and-authenticated-withbasic-auth
      x-api-path-slug: userfollowingusername-delete
      parameters:
      - in: header
        name: Accept
        description: Is used to set specified media type
      - in: query
        name: access_token
        description: Your Github OAuth token
      - in: path
        name: username
        description: Name of user
      responses:
        200:
          description: OK
      tags:
      - User
      - Following
      - Username
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