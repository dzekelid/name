---
swagger: "2.0"
x-collection-name: Bitbucket
x-complete: 0
info:
  title: Bitbucket Get Repositories Username Repo Slug Downloads
  description: Returns a list of download links associated with the repository.
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
  /repositories/{username}/{repo_slug}/branch-restrictions:
    get:
      summary: Get Repositories Username Repo Slug Branch Restrictions
      description: |-
        Returns a paginated list of all branch restrictions on the
        repository.
      operationId: getRepositoriesUsernameRepoSlugBranchRestrictions
      x-api-path-slug: repositoriesusernamerepo-slugbranchrestrictions-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Branch
      - Restrictions
    parameters:
      summary: Parameters Repositories Username Repo Slug Branch Restrictions
      description: Parameters repositories username repo slug branch restrictions
      operationId: parametersRepositoriesUsernameRepoSlugBranchRestrictions
      x-api-path-slug: repositoriesusernamerepo-slugbranchrestrictions-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Branch
      - Restrictions
    post:
      summary: Add Repositories Username Repo Slug Branch Restrictions
      description: |-
        Creates a new branch restriction rule for a repository.

        `kind` describes what will be restricted. Allowed values are: `push`,
        `force`, `delete`, and `restrict_merges`.

        Different kinds of branch restrictions have different requirements:

        * `push` and `restrict_merges` require `users` and `groups` to be
          specified. Empty lists are allowed, in which case permission is
          denied for everybody.
        * `force` can not be specified in a Mercurial repository.

        `pattern` is used to determine which branches will be restricted.

        A `'*'` in `pattern` will expand to match zero or more characters, and
        every other character matches itself. For example, `'foo*'` will match
        `'foo'` and `'foobar'`, but not `'barfoo'`. `'*'` will match all
        branches.

        `users` and `groups` are lists of user names and group names.

        `kind` and `pattern` must be unique within a repository; adding new
        users or groups to an existing restriction should be done via `PUT`.

        Note that branch restrictions with overlapping patterns are allowed,
        but the resulting behavior may be surprising.
      operationId: postRepositoriesUsernameRepoSlugBranchRestrictions
      x-api-path-slug: repositoriesusernamerepo-slugbranchrestrictions-post
      parameters:
      - in: body
        name: _body
        description: The new rule
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
      - Branch
      - Restrictions
  /repositories/{username}/{repo_slug}/branch-restrictions/{id}:
    delete:
      summary: Delete Repositories Username Repo Slug Branch Restrictions
      description: Delete repositories username repo slug branch restrictions
      operationId: deleteRepositoriesUsernameRepoSlugBranchRestrictions
      x-api-path-slug: repositoriesusernamerepo-slugbranchrestrictionsid-delete
      parameters:
      - in: path
        name: id
        description: The restriction rules id
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Branch
      - Restrictions
    get:
      summary: Get Repositories Username Repo Slug Branch Restrictions
      description: Get repositories username repo slug branch restrictions
      operationId: getRepositoriesUsernameRepoSlugBranchRestrictions
      x-api-path-slug: repositoriesusernamerepo-slugbranchrestrictionsid-get
      parameters:
      - in: path
        name: id
        description: The restriction rules id
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Branch
      - Restrictions
    parameters:
      summary: Parameters Repositories Username Repo Slug Branch Restrictions
      description: Parameters repositories username repo slug branch restrictions
      operationId: parametersRepositoriesUsernameRepoSlugBranchRestrictions
      x-api-path-slug: repositoriesusernamerepo-slugbranchrestrictionsid-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Branch
      - Restrictions
    put:
      summary: Update Repositories Username Repo Slug Branch Restrictions
      description: |-
        Updates an existing branch restriction rule.

        Fields not present in the request body are ignored.

        See [`POST`](../../branch-restrictions#post) for details.
      operationId: putRepositoriesUsernameRepoSlugBranchRestrictions
      x-api-path-slug: repositoriesusernamerepo-slugbranchrestrictionsid-put
      parameters:
      - in: path
        name: id
        description: The restriction rules id
      - in: body
        name: _body
        description: The new version of the existing rule
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
      - Branch
      - Restrictions
  /repositories/{username}/{repo_slug}/commit/{node}/approve:
    delete:
      summary: Delete Repositories Username Repo Slug Commit Node Approve
      description: |-
        Redact the authenticated user's approval of the specified commit.

        This operation is only available to users that have explicit access to
        the repository. In contrast, just the fact that a repository is
        publicly accessible to users does not give them the ability to approve
        commits.
      operationId: deleteRepositoriesUsernameRepoSlugCommitNodeApprove
      x-api-path-slug: repositoriesusernamerepo-slugcommitnodeapprove-delete
      parameters:
      - in: path
        name: node
        description: The commits SHA1
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Node
      - Approve
    parameters:
      summary: Parameters Repositories Username Repo Slug Commit Node Approve
      description: Parameters repositories username repo slug commit node approve
      operationId: parametersRepositoriesUsernameRepoSlugCommitNodeApprove
      x-api-path-slug: repositoriesusernamerepo-slugcommitnodeapprove-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Node
      - Approve
    post:
      summary: Add Repositories Username Repo Slug Commit Node Approve
      description: |-
        Approve the specified commit as the authenticated user.

        This operation is only available to users that have explicit access to
        the repository. In contrast, just the fact that a repository is
        publicly accessible to users does not give them the ability to approve
        commits.
      operationId: postRepositoriesUsernameRepoSlugCommitNodeApprove
      x-api-path-slug: repositoriesusernamerepo-slugcommitnodeapprove-post
      parameters:
      - in: path
        name: node
        description: The commits SHA1
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Node
      - Approve
  /repositories/{username}/{repo_slug}/commit/{node}/statuses:
    get:
      summary: Get Repositories Username Repo Slug Commit Node Statuses
      description: Returns all statuses (e.g. build results) for a specific commit.
      operationId: getRepositoriesUsernameRepoSlugCommitNodeStatuses
      x-api-path-slug: repositoriesusernamerepo-slugcommitnodestatuses-get
      parameters:
      - in: path
        name: node
        description: The commits SHA1
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Node
      - Statuses
    parameters:
      summary: Parameters Repositories Username Repo Slug Commit Node Statuses
      description: Parameters repositories username repo slug commit node statuses
      operationId: parametersRepositoriesUsernameRepoSlugCommitNodeStatuses
      x-api-path-slug: repositoriesusernamerepo-slugcommitnodestatuses-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Node
      - Statuses
  /repositories/{username}/{repo_slug}/commit/{node}/statuses/build:
    parameters:
      summary: Parameters Repositories Username Repo Slug Commit Node Statuses Build
      description: Parameters repositories username repo slug commit node statuses
        build
      operationId: parametersRepositoriesUsernameRepoSlugCommitNodeStatusesBuild
      x-api-path-slug: repositoriesusernamerepo-slugcommitnodestatusesbuild-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Node
      - Statuses
      - Build
    post:
      summary: Add Repositories Username Repo Slug Commit Node Statuses Build
      description: |-
        Creates a new build status against the specified commit.

        If the specified key already exists, the existing status object will
        be overwritten.

        When creating a new commit status, you can use a URI template for the URL.
        Templates are URLs that contain variable names that Bitbucket will
        evaluate at runtime whenever the URL is displayed anywhere similar to
        parameter substitution in
        [Bitbucket Connect](https://developer.atlassian.com/bitbucket/concepts/context-parameters.html).
        For example, one could use `https://foo.com/builds/{repository.full_name}`
        which Bitbucket will turn into `https://foo.com/builds/foo/bar` at render time.
        The context variables available are `repository` and `commit`.
      operationId: postRepositoriesUsernameRepoSlugCommitNodeStatusesBuild
      x-api-path-slug: repositoriesusernamerepo-slugcommitnodestatusesbuild-post
      parameters:
      - in: path
        name: node
        description: The commits SHA1
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Node
      - Statuses
      - Build
  /repositories/{username}/{repo_slug}/commit/{node}/statuses/build/{key}:
    get:
      summary: Get Repositories Username Repo Slug Commit Node Statuses Build Key
      description: Get repositories username repo slug commit node statuses build
        key
      operationId: getRepositoriesUsernameRepoSlugCommitNodeStatusesBuildKey
      x-api-path-slug: repositoriesusernamerepo-slugcommitnodestatusesbuildkey-get
      parameters:
      - in: path
        name: key
        description: The build status unique key
      - in: path
        name: node
        description: The commits SHA1
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Node
      - Statuses
      - Build
      - Key
    parameters:
      summary: Parameters Repositories Username Repo Slug Commit Node Statuses Build
        Key
      description: Parameters repositories username repo slug commit node statuses
        build key
      operationId: parametersRepositoriesUsernameRepoSlugCommitNodeStatusesBuildKey
      x-api-path-slug: repositoriesusernamerepo-slugcommitnodestatusesbuildkey-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Node
      - Statuses
      - Build
      - Key
    put:
      summary: Update Repositories Username Repo Slug Commit Node Statuses Build Key
      description: |-
        Used to update the current status of a build status object on the
        specific commit.

        This operation can also be used to change other properties of the
        build status:

        * `state`
        * `name`
        * `description`
        * `url`
        * `refname`

        The `key` cannot be changed.
      operationId: putRepositoriesUsernameRepoSlugCommitNodeStatusesBuildKey
      x-api-path-slug: repositoriesusernamerepo-slugcommitnodestatusesbuildkey-put
      parameters:
      - in: path
        name: key
        description: The commit status unique key
      - in: path
        name: node
        description: The commits SHA1
      - in: body
        name: _body
        description: The updated build status object
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
      - Commit
      - Node
      - Statuses
      - Build
      - Key
  /repositories/{username}/{repo_slug}/commit/{revision}:
    get:
      summary: Get Repositories Username Repo Slug Commit Revision
      description: Get repositories username repo slug commit revision
      operationId: getRepositoriesUsernameRepoSlugCommitRevision
      x-api-path-slug: repositoriesusernamerepo-slugcommitrevision-get
      parameters:
      - in: path
        name: revision
        description: The commits SHA1
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Revision
    parameters:
      summary: Parameters Repositories Username Repo Slug Commit Revision
      description: Parameters repositories username repo slug commit revision
      operationId: parametersRepositoriesUsernameRepoSlugCommitRevision
      x-api-path-slug: repositoriesusernamerepo-slugcommitrevision-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Revision
  /repositories/{username}/{repo_slug}/commit/{sha}/comments:
    get:
      summary: Get Repositories Username Repo Slug Commit Sha Comments
      description: |-
        Returns the commit's comments.

        This includes both global and inline comments.

        The default sorting is oldest to newest and can be overridden with
        the `sort` query parameter.
      operationId: getRepositoriesUsernameRepoSlugCommitShaComments
      x-api-path-slug: repositoriesusernamerepo-slugcommitshacomments-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Sha
      - Comments
    parameters:
      summary: Parameters Repositories Username Repo Slug Commit Sha Comments
      description: Parameters repositories username repo slug commit sha comments
      operationId: parametersRepositoriesUsernameRepoSlugCommitShaComments
      x-api-path-slug: repositoriesusernamerepo-slugcommitshacomments-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Sha
      - Comments
  /repositories/{username}/{repo_slug}/commit/{sha}/comments/{comment_id}:
    get:
      summary: Get Repositories Username Repo Slug Commit Sha Comments Comment
      description: Get repositories username repo slug commit sha comments comment
      operationId: getRepositoriesUsernameRepoSlugCommitShaCommentsComment
      x-api-path-slug: repositoriesusernamerepo-slugcommitshacommentscomment-id-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Sha
      - Comments
      - Comment
    parameters:
      summary: Parameters Repositories Username Repo Slug Commit Sha Comments Comment
      description: Parameters repositories username repo slug commit sha comments
        comment
      operationId: parametersRepositoriesUsernameRepoSlugCommitShaCommentsComment
      x-api-path-slug: repositoriesusernamerepo-slugcommitshacommentscomment-id-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commit
      - Sha
      - Comments
      - Comment
  /repositories/{username}/{repo_slug}/commits:
    get:
      summary: Get Repositories Username Repo Slug Commits
      description: |-
        These are the repository's commits. They are paginated and returned
        in reverse chronological order, similar to the output of `git log` and
        `hg log`. Like these tools, the DAG can be filtered.

        ## GET /repositories/{username}/{repo_slug}/commits/

        Returns all commits in the repo in topological order (newest commit
        first). All branches and tags are included (similar to
        `git log --all` and `hg log`).

        ## GET /repositories/{username}/{repo_slug}/commits/master

        Returns all commits on rev `master` (similar to `git log master`,
        `hg log master`).

        ## GET /repositories/{username}/{repo_slug}/commits/dev?exclude=master

        Returns all commits on ref `dev`, except those that are reachable on
        `master` (similar to `git log dev ^master`).

        ## GET /repositories/{username}/{repo_slug}/commits/?exclude=master

        Returns all commits in the repo that are not on master
        (similar to `git log --all ^master`).

        ## GET /repositories/{username}/{repo_slug}/commits/?include=foo&include=bar&exclude=fu&exclude=fubar

        Returns all commits that are on refs `foo` or `bar`, but not on `fu` or
        `fubar` (similar to `git log foo bar ^fu ^fubar`).

        Because the response could include a very large number of commits, it
        is paginated. Follow the 'next' link in the response to navigate to the
        next page of commits. As with other paginated resources, do not
        construct your own links.

        When the include and exclude parameters are more than can fit in a
        query string, clients can use a `x-www-form-urlencoded` POST instead.
      operationId: getRepositoriesUsernameRepoSlugCommits
      x-api-path-slug: repositoriesusernamerepo-slugcommits-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commits
    parameters:
      summary: Parameters Repositories Username Repo Slug Commits
      description: Parameters repositories username repo slug commits
      operationId: parametersRepositoriesUsernameRepoSlugCommits
      x-api-path-slug: repositoriesusernamerepo-slugcommits-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commits
    post:
      summary: Add Repositories Username Repo Slug Commits
      description: |-
        Identical to `GET /repositories/{username}/{repo_slug}/commits`,
        except that POST allows clients to place the include and exclude
        parameters in the request body to avoid URL length issues.

        **Note that this resource does NOT support new commit creation.**
      operationId: postRepositoriesUsernameRepoSlugCommits
      x-api-path-slug: repositoriesusernamerepo-slugcommits-post
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commits
  /repositories/{username}/{repo_slug}/commits/{revision}:
    get:
      summary: Get Repositories Username Repo Slug Commits Revision
      description: |-
        These are the repository's commits. They are paginated and returned
        in reverse chronological order, similar to the output of `git log` and
        `hg log`. Like these tools, the DAG can be filtered.

        ## GET /repositories/{username}/{repo_slug}/commits/

        Returns all commits in the repo in topological order (newest commit
        first). All branches and tags are included (similar to
        `git log --all` and `hg log`).

        ## GET /repositories/{username}/{repo_slug}/commits/master

        Returns all commits on rev `master` (similar to `git log master`,
        `hg log master`).

        ## GET /repositories/{username}/{repo_slug}/commits/dev?exclude=master

        Returns all commits on ref `dev`, except those that are reachable on
        `master` (similar to `git log dev ^master`).

        ## GET /repositories/{username}/{repo_slug}/commits/?exclude=master

        Returns all commits in the repo that are not on master
        (similar to `git log --all ^master`).

        ## GET /repositories/{username}/{repo_slug}/commits/?include=foo&include=bar&exclude=fu&exclude=fubar

        Returns all commits that are on refs `foo` or `bar`, but not on `fu` or
        `fubar` (similar to `git log foo bar ^fu ^fubar`).

        Because the response could include a very large number of commits, it
        is paginated. Follow the 'next' link in the response to navigate to the
        next page of commits. As with other paginated resources, do not
        construct your own links.

        When the include and exclude parameters are more than can fit in a
        query string, clients can use a `x-www-form-urlencoded` POST instead.
      operationId: getRepositoriesUsernameRepoSlugCommitsRevision
      x-api-path-slug: repositoriesusernamerepo-slugcommitsrevision-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commits
      - Revision
    parameters:
      summary: Parameters Repositories Username Repo Slug Commits Revision
      description: Parameters repositories username repo slug commits revision
      operationId: parametersRepositoriesUsernameRepoSlugCommitsRevision
      x-api-path-slug: repositoriesusernamerepo-slugcommitsrevision-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commits
      - Revision
    post:
      summary: Add Repositories Username Repo Slug Commits Revision
      description: |-
        Identical to `GET /repositories/{username}/{repo_slug}/commits`,
        except that POST allows clients to place the include and exclude
        parameters in the request body to avoid URL length issues.

        **Note that this resource does NOT support new commit creation.**
      operationId: postRepositoriesUsernameRepoSlugCommitsRevision
      x-api-path-slug: repositoriesusernamerepo-slugcommitsrevision-post
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Commits
      - Revision
  /repositories/{username}/{repo_slug}/components:
    get:
      summary: Get Repositories Username Repo Slug Components
      description: |-
        Returns the components that have been defined in the issue tracker.

        This resource is only available on repositories that have the issue
        tracker enabled.
      operationId: getRepositoriesUsernameRepoSlugComponents
      x-api-path-slug: repositoriesusernamerepo-slugcomponents-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Components
    parameters:
      summary: Parameters Repositories Username Repo Slug Components
      description: Parameters repositories username repo slug components
      operationId: parametersRepositoriesUsernameRepoSlugComponents
      x-api-path-slug: repositoriesusernamerepo-slugcomponents-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Components
  /repositories/{username}/{repo_slug}/components/{component_id}:
    get:
      summary: Get Repositories Username Repo Slug Components Component
      description: Get repositories username repo slug components component
      operationId: getRepositoriesUsernameRepoSlugComponentsComponent
      x-api-path-slug: repositoriesusernamerepo-slugcomponentscomponent-id-get
      parameters:
      - in: path
        name: component_id
        description: The components id
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Components
      - Component
    parameters:
      summary: Parameters Repositories Username Repo Slug Components Component
      description: Parameters repositories username repo slug components component
      operationId: parametersRepositoriesUsernameRepoSlugComponentsComponent
      x-api-path-slug: repositoriesusernamerepo-slugcomponentscomponent-id-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Components
      - Component
  /repositories/{username}/{repo_slug}/default-reviewers:
    get:
      summary: Get Repositories Username Repo Slug Default Reviewers
      description: |-
        Returns the repository's default reviewers.

        These are the users that are automatically added as reviewers on every
        new pull request that is created.
      operationId: getRepositoriesUsernameRepoSlugDefaultReviewers
      x-api-path-slug: repositoriesusernamerepo-slugdefaultreviewers-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Default
      - Reviewers
    parameters:
      summary: Parameters Repositories Username Repo Slug Default Reviewers
      description: Parameters repositories username repo slug default reviewers
      operationId: parametersRepositoriesUsernameRepoSlugDefaultReviewers
      x-api-path-slug: repositoriesusernamerepo-slugdefaultreviewers-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Default
      - Reviewers
  /repositories/{username}/{repo_slug}/default-reviewers/{target_username}:
    delete:
      summary: Delete Repositories Username Repo Slug Default Reviewers Target Username
      description: Delete repositories username repo slug default reviewers target
        username
      operationId: deleteRepositoriesUsernameRepoSlugDefaultReviewersTargetUsername
      x-api-path-slug: repositoriesusernamerepo-slugdefaultreviewerstarget-username-delete
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Default
      - Reviewers
      - Target
      - Username
    get:
      summary: Get Repositories Username Repo Slug Default Reviewers Target Username
      description: |-
        Returns the specified reviewer.

        This can be used to test whether a user is among the repository's
        default reviewers list. A 404 indicates that that specified user is not
        a default reviewer.
      operationId: getRepositoriesUsernameRepoSlugDefaultReviewersTargetUsername
      x-api-path-slug: repositoriesusernamerepo-slugdefaultreviewerstarget-username-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Default
      - Reviewers
      - Target
      - Username
    parameters:
      summary: Parameters Repositories Username Repo Slug Default Reviewers Target
        Username
      description: Parameters repositories username repo slug default reviewers target
        username
      operationId: parametersRepositoriesUsernameRepoSlugDefaultReviewersTargetUsername
      x-api-path-slug: repositoriesusernamerepo-slugdefaultreviewerstarget-username-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Default
      - Reviewers
      - Target
      - Username
    put:
      summary: Update Repositories Username Repo Slug Default Reviewers Target Username
      description: |-
        Adds the specified user to the repository's list of default
        reviewers.

        This method is idempotent. Adding a user a second time has no effect.
      operationId: putRepositoriesUsernameRepoSlugDefaultReviewersTargetUsername
      x-api-path-slug: repositoriesusernamerepo-slugdefaultreviewerstarget-username-put
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Default
      - Reviewers
      - Target
      - Username
  /repositories/{username}/{repo_slug}/diff/{spec}:
    get:
      summary: Get Repositories Username Repo Slug Diff Spec
      description: |-
        Produces a raw, git-style diff for either a single commit (diffed
        against its first parent), or a revspec of 2 commits (e.g.
        `3a8b42..9ff173` where the first commit represents the source and the
        second commit the destination).

        In case of the latter (diffing a revspec), a 3-way diff, or merge diff,
        is computed. This shows the changes introduced by the left branch
        (`3a8b42` in our example) as compared againt the right branch
        (`9ff173`).

        This is equivalent to merging the left branch into the right branch and
        then computing the diff of the merge commit against its first parent
        (the right branch). This follows the same behavior as pull requests
        that also show this style of 3-way, or merge diff.

        While similar to patches, diffs:

        * Don't have a commit header (username, commit message, etc)
        * Support the optional `path=foo/bar.py` query param to filter
          the diff to just that one file diff

        The raw diff is returned as-is, in whatever encoding the files in the
        repository use. It is not decoded into unicode. As such, the
        content-type is `text/plain`.
      operationId: getRepositoriesUsernameRepoSlugDiffSpec
      x-api-path-slug: repositoriesusernamerepo-slugdiffspec-get
      parameters:
      - in: query
        name: context
        description: Generate diffs with  lines of context instead of the usual three
      - in: query
        name: path
        description: Limit the diff to a single file
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Diff
      - Spec
    parameters:
      summary: Parameters Repositories Username Repo Slug Diff Spec
      description: Parameters repositories username repo slug diff spec
      operationId: parametersRepositoriesUsernameRepoSlugDiffSpec
      x-api-path-slug: repositoriesusernamerepo-slugdiffspec-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Diff
      - Spec
  /repositories/{username}/{repo_slug}/downloads:
    get:
      summary: Get Repositories Username Repo Slug Downloads
      description: Returns a list of download links associated with the repository.
      operationId: getRepositoriesUsernameRepoSlugDownloads
      x-api-path-slug: repositoriesusernamerepo-slugdownloads-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Downloads
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