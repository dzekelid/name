---
swagger: "2.0"
x-collection-name: Bitbucket
x-complete: 0
info:
  title: Bitbucket Update Repositories Username Repo Slug
  description: |-
    Since this endpoint can be used to both update and to create a
    repository, the request body depends on the intent.

    ### Creation

    See the POST documentation for the repository endpoint for an example
    of the request body.

    ### Update

    Note: Changing the `name` of the repository will cause the location to
    be changed. This is because the URL of the repo is derived from the
    name (a process called slugification). In such a scenario, it is
    possible for the request to fail if the newly created slug conflicts
    with an existing repository's slug. But if there is no conflict,
    the new location will be returned in the `Location` header of the
    response.
  termsOfService: https://www.atlassian.com/legal/customer-agreement
  contact:
    name: Bitbucket Support
    url: https://support.atlassian.com/bitbucket
    email: support@bitbucket.org
  version: 1.0.0
host: api.bitbucket.org
basePath: /2.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /repositories/{username}:
    get:
      summary: Get Repositories Username
      description: |-
        Returns a paginated list of all repositories owned by the specified
        account or UUID.

        The result can be narrowed down based on the authenticated user's role.

        E.g. with `?role=contributor`, only those repositories that the
        authenticated user has write access to are returned (this includes any
        repo the user is an admin on, as that implies write access).

        This endpoint also supports filtering and sorting of the results. See
        [filtering and sorting](../../meta/filtering) for more details.
      operationId: getRepositoriesUsername
      x-api-path-slug: repositoriesusername-get
      parameters:
      - in: query
        name: role
        description: Filters the result based on the authenticated users role on each
          repository
      - in: path
        name: username
        description: 'This can either be the username or the UUID of the user,surrounded
          by curly-braces, for example: `{user UUID}`'
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
    parameters:
      summary: Parameters Repositories Username
      description: Parameters repositories username
      operationId: parametersRepositoriesUsername
      x-api-path-slug: repositoriesusername-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
  /repositories/{username}/{repo_slug}:
    delete:
      summary: Delete Repositories Username Repo Slug
      description: |-
        Deletes the repository. This is an irreversible operation.

        This does not affect its forks.
      operationId: deleteRepositoriesUsernameRepoSlug
      x-api-path-slug: repositoriesusernamerepo-slug-delete
      parameters:
      - in: path
        name: repo_slug
        description: 'This can either be the repository slug or the UUID of the repository,surrounded
          by curly-braces, for example: `{repository UUID}`'
      - in: path
        name: username
        description: 'This can either be the username or the UUID of the user,surrounded
          by curly-braces, for example: `{user UUID}`'
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
    get:
      summary: Get Repositories Username Repo Slug
      description: Returns the object describing this repository.
      operationId: getRepositoriesUsernameRepoSlug
      x-api-path-slug: repositoriesusernamerepo-slug-get
      parameters:
      - in: path
        name: repo_slug
        description: 'This can either be the repository slug or the UUID of the repository,surrounded
          by curly-braces, for example: `{repository UUID}`'
      - in: path
        name: username
        description: 'This can either be the username or the UUID of the user,surrounded
          by curly-braces, for example: `{user UUID}`'
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
    parameters:
      summary: Parameters Repositories Username Repo Slug
      description: Parameters repositories username repo slug
      operationId: parametersRepositoriesUsernameRepoSlug
      x-api-path-slug: repositoriesusernamerepo-slug-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
    post:
      summary: Add Repositories Username Repo Slug
      description: |-
        Creates a new repository.

        Note: In order to set the project for the newly created repository,
        pass in either the project key or the project UUID as part of the
        request body as shown in the examples below:

        ```
        $ curl -X POST -H "Content-Type: application/json" -d '{
            "scm": "git",
            "project": {
                "key": "MARS"
            }
        }' https://api.bitbucket.org/2.0/repositories/teamsinspace/hablanding
        ```

        or

        ```
        $ curl -X POST -H "Content-Type: application/json" -d '{
            "scm": "git",
            "project": {
                "key": "{ba516952-992a-4c2d-acbd-17d502922f96}"
            }
        }' https://api.bitbucket.org/2.0/repositories/teamsinspace/hablanding
        ```

        The project must only be assigned for repositories belonging to a team.
        If the repository owner is a team and the project is not provided, the
        repository is automatically assigned to the oldest project in the team.

        Note: In the examples above, the username `teamsinspace`,
        and/or the repository name `hablanding` can be replaced by UUIDs.
      operationId: postRepositoriesUsernameRepoSlug
      x-api-path-slug: repositoriesusernamerepo-slug-post
      parameters:
      - in: path
        name: repo_slug
        description: 'This can either be the repository slug or the UUID of the repository,surrounded
          by curly-braces, for example: `{repository UUID}`'
      - in: path
        name: username
        description: 'This can either be the username or the UUID of the user,surrounded
          by curly-braces, for example: `{user UUID}`'
      - in: body
        name: _body
        description: The repository that is to be created
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
    put:
      summary: Update Repositories Username Repo Slug
      description: |-
        Since this endpoint can be used to both update and to create a
        repository, the request body depends on the intent.

        ### Creation

        See the POST documentation for the repository endpoint for an example
        of the request body.

        ### Update

        Note: Changing the `name` of the repository will cause the location to
        be changed. This is because the URL of the repo is derived from the
        name (a process called slugification). In such a scenario, it is
        possible for the request to fail if the newly created slug conflicts
        with an existing repository's slug. But if there is no conflict,
        the new location will be returned in the `Location` header of the
        response.
      operationId: putRepositoriesUsernameRepoSlug
      x-api-path-slug: repositoriesusernamerepo-slug-put
      parameters:
      - in: path
        name: repo_slug
        description: 'This can either be the repository slug or the UUID of the repository,surrounded
          by curly-braces, for example: `{repository UUID}`'
      - in: path
        name: username
        description: 'This can either be the username or the UUID of the user,surrounded
          by curly-braces, for example: `{user UUID}`'
      - in: body
        name: _body
        description: The repository that is to be updated
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
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