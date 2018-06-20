---
swagger: "2.0"
x-collection-name: Bitbucket
x-complete: 0
info:
  title: Bitbucket Get Snippets Username Encoded  Commits Revision
  description: Get snippets username encoded  commits revision
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
    parameters:
      summary: Parameters Repositories Username Repo Slug Downloads
      description: Parameters repositories username repo slug downloads
      operationId: parametersRepositoriesUsernameRepoSlugDownloads
      x-api-path-slug: repositoriesusernamerepo-slugdownloads-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Downloads
    post:
      summary: Add Repositories Username Repo Slug Downloads
      description: |-
        Upload new download artifacts.

        To upload files, perform a `multipart/form-data` POST containing one
        or more `files` fields:

            $ echo Hello World > hello.txt
            $ curl -s -u evzijst -X POST https://api.bitbucket.org/2.0/repositories/evzijst/git-tests/downloads -F files=@hello.txt

        When a file is uploaded with the same name as an existing artifact,
        then the existing file will be replaced.
      operationId: postRepositoriesUsernameRepoSlugDownloads
      x-api-path-slug: repositoriesusernamerepo-slugdownloads-post
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Downloads
  /repositories/{username}/{repo_slug}/downloads/{filename}:
    delete:
      summary: Delete Repositories Username Repo Slug Downloads Filename
      description: Deletes the specified download artifact from the repository.
      operationId: deleteRepositoriesUsernameRepoSlugDownloadsFilename
      x-api-path-slug: repositoriesusernamerepo-slugdownloadsfilename-delete
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Downloads
      - Filename
    get:
      summary: Get Repositories Username Repo Slug Downloads Filename
      description: |-
        Return a redirect to the contents of a download artifact.

        This endpoint returns the actual file contents and not the artifact's
        metadata.

            $ curl -s -L https://api.bitbucket.org/2.0/repositories/evzijst/git-tests/downloads/hello.txt
            Hello World
      operationId: getRepositoriesUsernameRepoSlugDownloadsFilename
      x-api-path-slug: repositoriesusernamerepo-slugdownloadsfilename-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Downloads
      - Filename
    parameters:
      summary: Parameters Repositories Username Repo Slug Downloads Filename
      description: Parameters repositories username repo slug downloads filename
      operationId: parametersRepositoriesUsernameRepoSlugDownloadsFilename
      x-api-path-slug: repositoriesusernamerepo-slugdownloadsfilename-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Downloads
      - Filename
  /repositories/{username}/{repo_slug}/forks:
    get:
      summary: Get Repositories Username Repo Slug Forks
      description: |-
        Returns a paginated list of all the forks of the specified
        repository.
      operationId: getRepositoriesUsernameRepoSlugForks
      x-api-path-slug: repositoriesusernamerepo-slugforks-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Forks
    parameters:
      summary: Parameters Repositories Username Repo Slug Forks
      description: Parameters repositories username repo slug forks
      operationId: parametersRepositoriesUsernameRepoSlugForks
      x-api-path-slug: repositoriesusernamerepo-slugforks-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Forks
  /repositories/{username}/{repo_slug}/hooks:
    get:
      summary: Get Repositories Username Repo Slug Hooks
      description: Returns a paginated list of webhooks installed on this repository.
      operationId: getRepositoriesUsernameRepoSlugHooks
      x-api-path-slug: repositoriesusernamerepo-slughooks-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Hooks
    parameters:
      summary: Parameters Repositories Username Repo Slug Hooks
      description: Parameters repositories username repo slug hooks
      operationId: parametersRepositoriesUsernameRepoSlugHooks
      x-api-path-slug: repositoriesusernamerepo-slughooks-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Hooks
    post:
      summary: Add Repositories Username Repo Slug Hooks
      description: |-
        Creates a new webhook on the specified repository.

        Example:

        ```
        $ curl -X POST -u credentials -H 'Content-Type: application/json'           https://api.bitbucket.org/2.0/repositories/username/slug/hooks           -d '
            {
              "description": "Webhook Description",
              "url": "https://example.com/",
              "active": true,
              "events": [
                "repo:push",
                "issue:created",
                "issue:updated"
              ]
            }'
        ```

        Note that this call requires the webhook scope, as well as any scope
        that applies to the events that the webhook subscribes to. In the
        example above that means: `webhook`, `repository` and `issue`.

        Also note that the `url` must properly resolve and cannot be an
        internal, non-routed address.
      operationId: postRepositoriesUsernameRepoSlugHooks
      x-api-path-slug: repositoriesusernamerepo-slughooks-post
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Hooks
  /repositories/{username}/{repo_slug}/hooks/{uid}:
    delete:
      summary: Delete Repositories Username Repo Slug Hooks U
      description: |-
        Deletes the specified webhook subscription from the given
        repository.
      operationId: deleteRepositoriesUsernameRepoSlugHooksU
      x-api-path-slug: repositoriesusernamerepo-slughooksuid-delete
      parameters:
      - in: path
        name: uid
        description: The installed webhooks id
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Hooks
      - U
    get:
      summary: Get Repositories Username Repo Slug Hooks U
      description: |-
        Returns the webhook with the specified id installed on the specified
        repository.
      operationId: getRepositoriesUsernameRepoSlugHooksU
      x-api-path-slug: repositoriesusernamerepo-slughooksuid-get
      parameters:
      - in: path
        name: uid
        description: The installed webhooks id
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Hooks
      - U
    parameters:
      summary: Parameters Repositories Username Repo Slug Hooks U
      description: Parameters repositories username repo slug hooks u
      operationId: parametersRepositoriesUsernameRepoSlugHooksU
      x-api-path-slug: repositoriesusernamerepo-slughooksuid-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Hooks
      - U
    put:
      summary: Update Repositories Username Repo Slug Hooks U
      description: |-
        Updates the specified webhook subscription.

        The following properties can be mutated:

        * `description`
        * `url`
        * `active`
        * `events`
      operationId: putRepositoriesUsernameRepoSlugHooksU
      x-api-path-slug: repositoriesusernamerepo-slughooksuid-put
      parameters:
      - in: path
        name: uid
        description: The installed webhooks id
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Hooks
      - U
  /repositories/{username}/{repo_slug}/issues:
    get:
      summary: Get Repositories Username Repo Slug Issues
      description: Get repositories username repo slug issues
      operationId: getRepositoriesUsernameRepoSlugIssues
      x-api-path-slug: repositoriesusernamerepo-slugissues-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Issues
    parameters:
      summary: Parameters Repositories Username Repo Slug Issues
      description: Parameters repositories username repo slug issues
      operationId: parametersRepositoriesUsernameRepoSlugIssues
      x-api-path-slug: repositoriesusernamerepo-slugissues-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Issues
    post:
      summary: Add Repositories Username Repo Slug Issues
      description: |-
        Creates a new issue.

        This call requires authentication. Private repositories or private
        issue trackers require the caller to authenticate with an account that
        has appropriate authorisation.

        The authenticated user is used for the issue's `reporter` field.
      operationId: postRepositoriesUsernameRepoSlugIssues
      x-api-path-slug: repositoriesusernamerepo-slugissues-post
      parameters:
      - in: body
        name: _body
        description: The new issue
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
      - Issues
  /repositories/{username}/{repo_slug}/issues/{issue_id}:
    delete:
      summary: Delete Repositories Username Repo Slug Issues Issue
      description: |-
        Deletes the specified issue. This requires write access to the
        repository.
      operationId: deleteRepositoriesUsernameRepoSlugIssuesIssue
      x-api-path-slug: repositoriesusernamerepo-slugissuesissue-id-delete
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Issues
      - Issue
    get:
      summary: Get Repositories Username Repo Slug Issues Issue
      description: Get repositories username repo slug issues issue
      operationId: getRepositoriesUsernameRepoSlugIssuesIssue
      x-api-path-slug: repositoriesusernamerepo-slugissuesissue-id-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Issues
      - Issue
    parameters:
      summary: Parameters Repositories Username Repo Slug Issues Issue
      description: Parameters repositories username repo slug issues issue
      operationId: parametersRepositoriesUsernameRepoSlugIssuesIssue
      x-api-path-slug: repositoriesusernamerepo-slugissuesissue-id-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Issues
      - Issue
  /repositories/{username}/{repo_slug}/issues/{issue_id}/attachments:
    get:
      summary: Get Repositories Username Repo Slug Issues Issue  Attachments
      description: |-
        Returns all attachments for this issue.

        This returns the files' meta data. This does not return the files'
        actual contents.

        The files are always ordered by their upload date.
      operationId: getRepositoriesUsernameRepoSlugIssuesIssueAttachments
      x-api-path-slug: repositoriesusernamerepo-slugissuesissue-idattachments-get
      parameters:
      - in: path
        name: issue_id
        description: The issues id
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Issues
      - Issue
      - ""
      - Attachments
    parameters:
      summary: Parameters Repositories Username Repo Slug Issues Issue  Attachments
      description: Parameters repositories username repo slug issues issue  attachments
      operationId: parametersRepositoriesUsernameRepoSlugIssuesIssueAttachments
      x-api-path-slug: repositoriesusernamerepo-slugissuesissue-idattachments-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Issues
      - Issue
      - ""
      - Attachments
    post:
      summary: Add Repositories Username Repo Slug Issues Issue  Attachments
      description: |-
        Upload new issue attachments.

        To upload files, perform a `multipart/form-data` POST containing one
        or more file fields.

        When a file is uploaded with the same name as an existing attachment,
        then the existing file will be replaced.
      operationId: postRepositoriesUsernameRepoSlugIssuesIssueAttachments
      x-api-path-slug: repositoriesusernamerepo-slugissuesissue-idattachments-post
      parameters:
      - in: path
        name: issue_id
        description: The issues id
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Issues
      - Issue
      - ""
      - Attachments
  /repositories/{username}/{repo_slug}/issues/{issue_id}/attachments/{path}:
    delete:
      summary: Delete Repositories Username Repo Slug Issues Issue  Attachments Path
      description: Delete repositories username repo slug issues issue  attachments
        path
      operationId: deleteRepositoriesUsernameRepoSlugIssuesIssueAttachmentsPath
      x-api-path-slug: repositoriesusernamerepo-slugissuesissue-idattachmentspath-delete
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Issues
      - Issue
      - ""
      - Attachments
      - Path
    get:
      summary: Get Repositories Username Repo Slug Issues Issue  Attachments Path
      description: |-
        Returns the contents of the specified file attachment.

        Note that this endpoint does not return a JSON response, but instead
        returns a redirect pointing to the actual file that in turn will return
        the raw contents.

        The redirect URL contains a one-time token that has a limited lifetime.
        As a result, the link should not be persisted, stored, or shared.
      operationId: getRepositoriesUsernameRepoSlugIssuesIssueAttachmentsPath
      x-api-path-slug: repositoriesusernamerepo-slugissuesissue-idattachmentspath-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Issues
      - Issue
      - ""
      - Attachments
      - Path
    parameters:
      summary: Parameters Repositories Username Repo Slug Issues Issue  Attachments
        Path
      description: Parameters repositories username repo slug issues issue  attachments
        path
      operationId: parametersRepositoriesUsernameRepoSlugIssuesIssueAttachmentsPath
      x-api-path-slug: repositoriesusernamerepo-slugissuesissue-idattachmentspath-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Issues
      - Issue
      - ""
      - Attachments
      - Path
  /repositories/{username}/{repo_slug}/issues/{issue_id}/comments:
    get:
      summary: Get Repositories Username Repo Slug Issues Issue  Comments
      description: |-
        Returns all comments that were made on the specified issue.

        The default sorting is oldest to newest and can be overridden with
        the `sort` query parameter.
      operationId: getRepositoriesUsernameRepoSlugIssuesIssueComments
      x-api-path-slug: repositoriesusernamerepo-slugissuesissue-idcomments-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Issues
      - Issue
      - ""
      - Comments
    parameters:
      summary: Parameters Repositories Username Repo Slug Issues Issue  Comments
      description: Parameters repositories username repo slug issues issue  comments
      operationId: parametersRepositoriesUsernameRepoSlugIssuesIssueComments
      x-api-path-slug: repositoriesusernamerepo-slugissuesissue-idcomments-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Issues
      - Issue
      - ""
      - Comments
  /repositories/{username}/{repo_slug}/issues/{issue_id}/comments/{comment_id}:
    get:
      summary: Get Repositories Username Repo Slug Issues Issue  Comments Comment
      description: Get repositories username repo slug issues issue  comments comment
      operationId: getRepositoriesUsernameRepoSlugIssuesIssueCommentsComment
      x-api-path-slug: repositoriesusernamerepo-slugissuesissue-idcommentscomment-id-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Issues
      - Issue
      - ""
      - Comments
      - Comment
    parameters:
      summary: Parameters Repositories Username Repo Slug Issues Issue  Comments Comment
      description: Parameters repositories username repo slug issues issue  comments
        comment
      operationId: parametersRepositoriesUsernameRepoSlugIssuesIssueCommentsComment
      x-api-path-slug: repositoriesusernamerepo-slugissuesissue-idcommentscomment-id-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Issues
      - Issue
      - ""
      - Comments
      - Comment
  /repositories/{username}/{repo_slug}/issues/{issue_id}/vote:
    delete:
      summary: Delete Repositories Username Repo Slug Issues Issue  Vote
      description: Delete repositories username repo slug issues issue  vote
      operationId: deleteRepositoriesUsernameRepoSlugIssuesIssueVote
      x-api-path-slug: repositoriesusernamerepo-slugissuesissue-idvote-delete
      parameters:
      - in: path
        name: issue_id
        description: The issues id
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Issues
      - Issue
      - ""
      - Vote
    get:
      summary: Get Repositories Username Repo Slug Issues Issue  Vote
      description: |-
        Check whether the authenticated user has voted for this issue.
        A 204 status code indicates that the user has voted, while a 404
        implies they haven't.
      operationId: getRepositoriesUsernameRepoSlugIssuesIssueVote
      x-api-path-slug: repositoriesusernamerepo-slugissuesissue-idvote-get
      parameters:
      - in: path
        name: issue_id
        description: The issues id
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Issues
      - Issue
      - ""
      - Vote
    parameters:
      summary: Parameters Repositories Username Repo Slug Issues Issue  Vote
      description: Parameters repositories username repo slug issues issue  vote
      operationId: parametersRepositoriesUsernameRepoSlugIssuesIssueVote
      x-api-path-slug: repositoriesusernamerepo-slugissuesissue-idvote-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Issues
      - Issue
      - ""
      - Vote
    put:
      summary: Update Repositories Username Repo Slug Issues Issue  Vote
      description: |-
        Vote for this issue.

        To cast your vote, do an empty PUT. The 204 status code indicates that
        the operation was successful.
      operationId: putRepositoriesUsernameRepoSlugIssuesIssueVote
      x-api-path-slug: repositoriesusernamerepo-slugissuesissue-idvote-put
      parameters:
      - in: path
        name: issue_id
        description: The issues id
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Issues
      - Issue
      - ""
      - Vote
  /repositories/{username}/{repo_slug}/issues/{issue_id}/watch:
    delete:
      summary: Delete Repositories Username Repo Slug Issues Issue  Watch
      description: Delete repositories username repo slug issues issue  watch
      operationId: deleteRepositoriesUsernameRepoSlugIssuesIssueWatch
      x-api-path-slug: repositoriesusernamerepo-slugissuesissue-idwatch-delete
      parameters:
      - in: path
        name: issue_id
        description: The issues id
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Issues
      - Issue
      - ""
      - Watch
    get:
      summary: Get Repositories Username Repo Slug Issues Issue  Watch
      description: |-
        Indicated whether or not the authenticated user is watching this
        issue.
      operationId: getRepositoriesUsernameRepoSlugIssuesIssueWatch
      x-api-path-slug: repositoriesusernamerepo-slugissuesissue-idwatch-get
      parameters:
      - in: path
        name: issue_id
        description: The issues id
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Issues
      - Issue
      - ""
      - Watch
    parameters:
      summary: Parameters Repositories Username Repo Slug Issues Issue  Watch
      description: Parameters repositories username repo slug issues issue  watch
      operationId: parametersRepositoriesUsernameRepoSlugIssuesIssueWatch
      x-api-path-slug: repositoriesusernamerepo-slugissuesissue-idwatch-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Issues
      - Issue
      - ""
      - Watch
    put:
      summary: Update Repositories Username Repo Slug Issues Issue  Watch
      description: |-
        Start watching this issue.

        To start watching this issue, do an empty PUT. The 204 status code
        indicates that the operation was successful.
      operationId: putRepositoriesUsernameRepoSlugIssuesIssueWatch
      x-api-path-slug: repositoriesusernamerepo-slugissuesissue-idwatch-put
      parameters:
      - in: path
        name: issue_id
        description: The issues id
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Issues
      - Issue
      - ""
      - Watch
  /repositories/{username}/{repo_slug}/milestones:
    get:
      summary: Get Repositories Username Repo Slug Milestones
      description: |-
        Returns the milestones that have been defined in the issue tracker.

        This resource is only available on repositories that have the issue
        tracker enabled.
      operationId: getRepositoriesUsernameRepoSlugMilestones
      x-api-path-slug: repositoriesusernamerepo-slugmilestones-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Milestones
    parameters:
      summary: Parameters Repositories Username Repo Slug Milestones
      description: Parameters repositories username repo slug milestones
      operationId: parametersRepositoriesUsernameRepoSlugMilestones
      x-api-path-slug: repositoriesusernamerepo-slugmilestones-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Milestones
  /repositories/{username}/{repo_slug}/milestones/{milestone_id}:
    get:
      summary: Get Repositories Username Repo Slug Milestones Milestone
      description: Get repositories username repo slug milestones milestone
      operationId: getRepositoriesUsernameRepoSlugMilestonesMilestone
      x-api-path-slug: repositoriesusernamerepo-slugmilestonesmilestone-id-get
      parameters:
      - in: path
        name: milestone_id
        description: The milestones id
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Milestones
      - Milestone
    parameters:
      summary: Parameters Repositories Username Repo Slug Milestones Milestone
      description: Parameters repositories username repo slug milestones milestone
      operationId: parametersRepositoriesUsernameRepoSlugMilestonesMilestone
      x-api-path-slug: repositoriesusernamerepo-slugmilestonesmilestone-id-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Milestones
      - Milestone
  /repositories/{username}/{repo_slug}/patch/{spec}:
    get:
      summary: Get Repositories Username Repo Slug Patch Spec
      description: |-
        Produces a raw patch for a single commit (diffed against its first
        parent), or a patch-series for a revspec of 2 commits (e.g.
        `3a8b42..9ff173` where the first commit represents the source and the
        second commit the destination).

        In case of the latter (diffing a revspec), a patch series is returned
        for the commits on the source branch (`3a8b42` and its ancestors in
        our example). For Mercurial, a single patch is returned that combines
        the changes of all commits on the source branch.

        While similar to diffs, patches:

        * Have a commit header (username, commit message, etc)
        * Do not support the `path=foo/bar.py` query parameter

        The raw patch is returned as-is, in whatever encoding the files in the
        repository use. It is not decoded into unicode. As such, the
        content-type is `text/plain`.
      operationId: getRepositoriesUsernameRepoSlugPatchSpec
      x-api-path-slug: repositoriesusernamerepo-slugpatchspec-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Patch
      - Spec
    parameters:
      summary: Parameters Repositories Username Repo Slug Patch Spec
      description: Parameters repositories username repo slug patch spec
      operationId: parametersRepositoriesUsernameRepoSlugPatchSpec
      x-api-path-slug: repositoriesusernamerepo-slugpatchspec-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Patch
      - Spec
  /repositories/{username}/{repo_slug}/pipelines/:
    get:
      summary: Get Repositories Username Repo Slug Pipelines
      description: Get repositories username repo slug pipelines
      operationId: getRepositoriesUsernameRepoSlugPipelines
      x-api-path-slug: repositoriesusernamerepo-slugpipelines-get
      parameters:
      - in: path
        name: repo_slug
        description: The repository
      - in: path
        name: username
        description: The account
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pipelines
    post:
      summary: Add Repositories Username Repo Slug Pipelines
      description: "Endpoint to create and initiate a pipeline. \nThere are a couple
        of different options to initiate a pipeline, where the payload of the request
        will determine which type of pipeline will be instantiated.\n# Trigger a Pipeline
        for a branch or tag\nOne way to trigger pipelines is by specifying the reference
        for which you want to trigger a pipeline (e.g. a branch or tag). \nThe specified
        reference will be used to determine which pipeline definition from the `bitbucket-pipelines.yml`
        file will be applied to initiate the pipeline. The pipeline will then do a
        clone of the repository and checkout the latest revision of the specified
        reference.\n\n### Example\n\n```\n$ curl -X POST -is -u username:password
        \\\n  -H 'Content-Type: application/json' \\\n https://api.bitbucket.org/2.0/repositories/jeroendr/meat-demo2/pipelines/
        \\\n  -d '\n  {\n    \"target\": {\n      \"ref_type\": \"branch\", \n      \"type\":
        \"pipeline_ref_target\", \n      \"ref_name\": \"master\"\n    }\n  }'\n```\n#
        Trigger a Pipeline for a commit on a branch or tag\nYou can initiate a pipeline
        for a specific commit and in the context of a specified reference (e.g. a
        branch, tag or bookmark).\nThe specified reference will be used to determine
        which pipeline definition from the bitbucket-pipelines.yml file will be applied
        to initiate the pipeline. The pipeline will clone the repository and then
        do a checkout the specified reference. \n\nThe following reference types are
        supported:\n\n* `branch` \n* `named_branch`\n* `bookmark` \n * `tag`\n\n###
        Example\n\n```\n$ curl -X POST -is -u username:password \\\n  -H 'Content-Type:
        application/json' \\\n  https://api.bitbucket.org/2.0/repositories/jeroendr/meat-demo2/pipelines/
        \\\n  -d '\n  {\n    \"target\": {\n      \"commit\": {\n        \"type\":
        \"commit\", \n        \"hash\": \"ce5b7431602f7cbba007062eeb55225c6e18e956\"\n
        \     }, \n      \"ref_type\": \"branch\", \n      \"type\": \"pipeline_ref_target\",
        \n      \"ref_name\": \"master\"\n    }\n  }'\n```\n# Trigger a specific pipeline
        definition for a commit\nYou can trigger a specific pipeline that is defined
        in your `bitbucket-pipelines.yml` file for a specific commit. \nIn addition
        to the commit revision, you specify the type and pattern of the selector that
        identifies the pipeline definition. The resulting pipeline will then clone
        the repository and checkout the specified revision.\n\n### Example\n\n```\n$
        curl -X POST -is -u username:password \\\n  -H 'Content-Type: application/json'
        \\\n https://api.bitbucket.org/2.0/repositories/jeroendr/meat-demo2/pipelines/
        \\\n -d '\n  {\n     \"target\": {\n      \"commit\": {\n         \"hash\":\"a3c4e02c9a3755eccdc3764e6ea13facdf30f923\",\n
        \        \"type\":\"commit\"\n       },\n        \"selector\": {\n           \"type\":\"custom\",\n
        \             \"pattern\":\"Deploy to production\"\n          },\n        \"type\":\"pipeline_commit_target\"\n
        \  }\n  }'\n```\n# Trigger a specific pipeline definition for a commit on
        a branch or tag\nYou can trigger a specific pipeline that is defined in your
        `bitbucket-pipelines.yml` file for a specific commit in the context of a specified
        reference. \nIn addition to the commit revision, you specify the type and
        pattern of the selector that identifies the pipeline definition, as well as
        the reference information. The resulting pipeline will then clone the repository
        a checkout the specified reference.\n\n### Example\n\n```\n$ curl -X POST
        -is -u username:password \\\n  -H 'Content-Type: application/json' \\\n https://api.bitbucket.org/2.0/repositories/jeroendr/meat-demo2/pipelines/
        \\\n -d '\n  {\n     \"target\": {\n      \"commit\": {\n         \"hash\":\"a3c4e02c9a3755eccdc3764e6ea13facdf30f923\",\n
        \        \"type\":\"commit\"\n       },\n       \"selector\": {\n          \"type\":
        \"custom\",\n          \"pattern\": \"Deploy to production\"\n       },\n
        \      \"type\": \"pipeline_ref_target\",\n       \"ref_name\": \"master\",\n
        \      \"ref_type\": \"branch\"\n     }\n  }'\n```"
      operationId: postRepositoriesUsernameRepoSlugPipelines
      x-api-path-slug: repositoriesusernamerepo-slugpipelines-post
      parameters:
      - in: path
        name: repo_slug
        description: The repository
      - in: path
        name: username
        description: The account
      - in: body
        name: _body
        description: The pipeline to initiate
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
      - Pipelines
  /repositories/{username}/{repo_slug}/pipelines/{pipeline_uuid}:
    get:
      summary: Get Repositories Username Repo Slug Pipelines Pipeline Uu
      description: Get repositories username repo slug pipelines pipeline uu
      operationId: getRepositoriesUsernameRepoSlugPipelinesPipelineUu
      x-api-path-slug: repositoriesusernamerepo-slugpipelinespipeline-uuid-get
      parameters:
      - in: path
        name: pipeline_uuid
        description: The pipeline UUID
      - in: path
        name: repo_slug
        description: The repository
      - in: path
        name: username
        description: The account
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pipelines
      - Pipeline
      - Uu
  /repositories/{username}/{repo_slug}/pipelines/{pipeline_uuid}/steps/:
    get:
      summary: Get Repositories Username Repo Slug Pipelines Pipeline Uu Steps
      description: Get repositories username repo slug pipelines pipeline uu steps
      operationId: getRepositoriesUsernameRepoSlugPipelinesPipelineUuSteps
      x-api-path-slug: repositoriesusernamerepo-slugpipelinespipeline-uuidsteps-get
      parameters:
      - in: path
        name: pipeline_uuid
        description: The UUID of the pipeline
      - in: path
        name: repo_slug
        description: The repository
      - in: path
        name: username
        description: The account
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pipelines
      - Pipeline
      - Uu
      - Steps
  /repositories/{username}/{repo_slug}/pipelines/{pipeline_uuid}/steps/{step_uuid}:
    get:
      summary: Get Repositories Username Repo Slug Pipelines Pipeline Uu Steps Step
        Uu
      description: Get repositories username repo slug pipelines pipeline uu steps
        step uu
      operationId: getRepositoriesUsernameRepoSlugPipelinesPipelineUuStepsStepUu
      x-api-path-slug: repositoriesusernamerepo-slugpipelinespipeline-uuidstepsstep-uuid-get
      parameters:
      - in: path
        name: pipeline_uuid
        description: The UUID of the pipeline
      - in: path
        name: repo_slug
        description: The repository
      - in: path
        name: step_uuid
        description: The UUID of the step
      - in: path
        name: username
        description: The account
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pipelines
      - Pipeline
      - Uu
      - Steps
      - Step
      - Uu
  /repositories/{username}/{repo_slug}/pipelines/{pipeline_uuid}/steps/{step_uuid}/log:
    get:
      summary: Get Repositories Username Repo Slug Pipelines Pipeline Uu Steps Step
        Uu Log
      description: |-
        Retrieve the log file for a given step of a pipeline.

        This endpoint supports (and encourages!) the use of [HTTP Range requests](https://tools.ietf.org/html/rfc7233) to deal with potentially very large log files.
      operationId: getRepositoriesUsernameRepoSlugPipelinesPipelineUuStepsStepUuLog
      x-api-path-slug: repositoriesusernamerepo-slugpipelinespipeline-uuidstepsstep-uuidlog-get
      parameters:
      - in: path
        name: pipeline_uuid
        description: The UUID of the pipeline
      - in: path
        name: repo_slug
        description: The repository
      - in: path
        name: step_uuid
        description: The UUID of the step
      - in: path
        name: username
        description: The account
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pipelines
      - Pipeline
      - Uu
      - Steps
      - Step
      - Uu
      - Log
  /repositories/{username}/{repo_slug}/pipelines/{pipeline_uuid}/stopPipeline:
    post:
      summary: Add Repositories Username Repo Slug Pipelines Pipeline Uu Stoppipeline
      description: Signal the stop of a pipeline and all of its steps that not have
        completed yet.
      operationId: postRepositoriesUsernameRepoSlugPipelinesPipelineUuStoppipeline
      x-api-path-slug: repositoriesusernamerepo-slugpipelinespipeline-uuidstoppipeline-post
      parameters:
      - in: path
        name: pipeline_uuid
        description: The UUID of the pipeline
      - in: path
        name: repo_slug
        description: The repository
      - in: path
        name: username
        description: The account
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pipelines
      - Pipeline
      - Uu
      - Stoppipeline
  /repositories/{username}/{repo_slug}/pipelines_config:
    get:
      summary: Get Repositories Username Repo Slug Pipelines Config
      description: Get repositories username repo slug pipelines config
      operationId: getRepositoriesUsernameRepoSlugPipelinesConfig
      x-api-path-slug: repositoriesusernamerepo-slugpipelines-config-get
      parameters:
      - in: path
        name: repo_slug
        description: The repository
      - in: path
        name: username
        description: The account
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pipelines
      - Config
    put:
      summary: Update Repositories Username Repo Slug Pipelines Config
      description: Update the pipelines configuration for a repository.
      operationId: putRepositoriesUsernameRepoSlugPipelinesConfig
      x-api-path-slug: repositoriesusernamerepo-slugpipelines-config-put
      parameters:
      - in: path
        name: repo_slug
        description: The repository
      - in: path
        name: username
        description: The account
      - in: body
        name: _body
        description: The updated repository pipelines configuration
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
      - Pipelines
      - Config
  /repositories/{username}/{repo_slug}/pipelines_config/ssh/key_pair:
    delete:
      summary: Delete Repositories Username Repo Slug Pipelines Config Ssh Key Pair
      description: Delete repositories username repo slug pipelines config ssh key
        pair
      operationId: deleteRepositoriesUsernameRepoSlugPipelinesConfigSshKeyPair
      x-api-path-slug: repositoriesusernamerepo-slugpipelines-configsshkey-pair-delete
      parameters:
      - in: path
        name: repo_slug
        description: The repository
      - in: path
        name: username
        description: The account
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pipelines
      - Config
      - Ssh
      - Key
      - Pair
    get:
      summary: Get Repositories Username Repo Slug Pipelines Config Ssh Key Pair
      description: Retrieve the repository SSH key pair excluding the SSH private
        key. The private key is a write only field and will never be exposed in the
        logs or the REST API.
      operationId: getRepositoriesUsernameRepoSlugPipelinesConfigSshKeyPair
      x-api-path-slug: repositoriesusernamerepo-slugpipelines-configsshkey-pair-get
      parameters:
      - in: path
        name: repo_slug
        description: The repository
      - in: path
        name: username
        description: The account
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pipelines
      - Config
      - Ssh
      - Key
      - Pair
    put:
      summary: Update Repositories Username Repo Slug Pipelines Config Ssh Key Pair
      description: Create or update the repository SSH key pair. The private key will
        be set as a default SSH identity in your build container.
      operationId: putRepositoriesUsernameRepoSlugPipelinesConfigSshKeyPair
      x-api-path-slug: repositoriesusernamerepo-slugpipelines-configsshkey-pair-put
      parameters:
      - in: path
        name: repo_slug
        description: The repository
      - in: path
        name: username
        description: The account
      - in: body
        name: _body
        description: The created or updated SSH key pair
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
      - Pipelines
      - Config
      - Ssh
      - Key
      - Pair
  /repositories/{username}/{repo_slug}/pipelines_config/ssh/known_hosts/:
    get:
      summary: Get Repositories Username Repo Slug Pipelines Config Ssh Known Hosts
      description: Get repositories username repo slug pipelines config ssh known
        hosts
      operationId: getRepositoriesUsernameRepoSlugPipelinesConfigSshKnownHosts
      x-api-path-slug: repositoriesusernamerepo-slugpipelines-configsshknown-hosts-get
      parameters:
      - in: path
        name: repo_slug
        description: The repository
      - in: path
        name: username
        description: The account
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pipelines
      - Config
      - Ssh
      - Known
      - Hosts
    post:
      summary: Add Repositories Username Repo Slug Pipelines Config Ssh Known Hosts
      description: Post repositories username repo slug pipelines config ssh known
        hosts
      operationId: postRepositoriesUsernameRepoSlugPipelinesConfigSshKnownHosts
      x-api-path-slug: repositoriesusernamerepo-slugpipelines-configsshknown-hosts-post
      parameters:
      - in: path
        name: repo_slug
        description: The repository
      - in: path
        name: username
        description: The account
      - in: body
        name: _body
        description: The known host to create
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
      - Pipelines
      - Config
      - Ssh
      - Known
      - Hosts
  /repositories/{username}/{repo_slug}/pipelines_config/ssh/known_hosts/{known_host_uuid}:
    delete:
      summary: Delete Repositories Username Repo Slug Pipelines Config Ssh Known Hosts
        Known Host Uu
      description: Delete repositories username repo slug pipelines config ssh known
        hosts known host uu
      operationId: deleteRepositoriesUsernameRepoSlugPipelinesConfigSshKnownHostsKnownHostUu
      x-api-path-slug: repositoriesusernamerepo-slugpipelines-configsshknown-hostsknown-host-uuid-delete
      parameters:
      - in: path
        name: known_host_uuid
        description: The UUID of the known host to delete
      - in: path
        name: repo_slug
        description: The repository
      - in: path
        name: username
        description: The account
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pipelines
      - Config
      - Ssh
      - Known
      - Hosts
      - Known
      - Host
      - Uu
    get:
      summary: Get Repositories Username Repo Slug Pipelines Config Ssh Known Hosts
        Known Host Uu
      description: Get repositories username repo slug pipelines config ssh known
        hosts known host uu
      operationId: getRepositoriesUsernameRepoSlugPipelinesConfigSshKnownHostsKnownHostUu
      x-api-path-slug: repositoriesusernamerepo-slugpipelines-configsshknown-hostsknown-host-uuid-get
      parameters:
      - in: path
        name: known_host_uuid
        description: The UUID of the known host to retrieve
      - in: path
        name: repo_slug
        description: The repository
      - in: path
        name: username
        description: The account
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pipelines
      - Config
      - Ssh
      - Known
      - Hosts
      - Known
      - Host
      - Uu
    put:
      summary: Update Repositories Username Repo Slug Pipelines Config Ssh Known Hosts
        Known Host Uu
      description: Put repositories username repo slug pipelines config ssh known
        hosts known host uu
      operationId: putRepositoriesUsernameRepoSlugPipelinesConfigSshKnownHostsKnownHostUu
      x-api-path-slug: repositoriesusernamerepo-slugpipelines-configsshknown-hostsknown-host-uuid-put
      parameters:
      - in: path
        name: known_host_uuid
        description: The UUID of the known host to update
      - in: path
        name: repo_slug
        description: The repository
      - in: path
        name: username
        description: The account
      - in: body
        name: _body
        description: The updated known host
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
      - Pipelines
      - Config
      - Ssh
      - Known
      - Hosts
      - Known
      - Host
      - Uu
  /repositories/{username}/{repo_slug}/pipelines_config/variables/:
    get:
      summary: Get Repositories Username Repo Slug Pipelines Config Variables
      description: Get repositories username repo slug pipelines config variables
      operationId: getRepositoriesUsernameRepoSlugPipelinesConfigVariables
      x-api-path-slug: repositoriesusernamerepo-slugpipelines-configvariables-get
      parameters:
      - in: path
        name: repo_slug
        description: The repository
      - in: path
        name: username
        description: The account
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pipelines
      - Config
      - Variables
    post:
      summary: Add Repositories Username Repo Slug Pipelines Config Variables
      description: Post repositories username repo slug pipelines config variables
      operationId: postRepositoriesUsernameRepoSlugPipelinesConfigVariables
      x-api-path-slug: repositoriesusernamerepo-slugpipelines-configvariables-post
      parameters:
      - in: path
        name: repo_slug
        description: The repository
      - in: path
        name: username
        description: The account
      - in: body
        name: _body
        description: The variable to create
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
      - Pipelines
      - Config
      - Variables
  /repositories/{username}/{repo_slug}/pipelines_config/variables/{variable_uuid}:
    delete:
      summary: Delete Repositories Username Repo Slug Pipelines Config Variables Variable
        Uu
      description: Delete repositories username repo slug pipelines config variables
        variable uu
      operationId: deleteRepositoriesUsernameRepoSlugPipelinesConfigVariablesVariableUu
      x-api-path-slug: repositoriesusernamerepo-slugpipelines-configvariablesvariable-uuid-delete
      parameters:
      - in: path
        name: repo_slug
        description: The repository
      - in: path
        name: username
        description: The account
      - in: path
        name: variable_uuid
        description: The UUID of the variable to delete
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pipelines
      - Config
      - Variables
      - Variable
      - Uu
    get:
      summary: Get Repositories Username Repo Slug Pipelines Config Variables Variable
        Uu
      description: Get repositories username repo slug pipelines config variables
        variable uu
      operationId: getRepositoriesUsernameRepoSlugPipelinesConfigVariablesVariableUu
      x-api-path-slug: repositoriesusernamerepo-slugpipelines-configvariablesvariable-uuid-get
      parameters:
      - in: path
        name: repo_slug
        description: The repository
      - in: path
        name: username
        description: The account
      - in: path
        name: variable_uuid
        description: The UUID of the variable to retrieve
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pipelines
      - Config
      - Variables
      - Variable
      - Uu
    put:
      summary: Update Repositories Username Repo Slug Pipelines Config Variables Variable
        Uu
      description: Put repositories username repo slug pipelines config variables
        variable uu
      operationId: putRepositoriesUsernameRepoSlugPipelinesConfigVariablesVariableUu
      x-api-path-slug: repositoriesusernamerepo-slugpipelines-configvariablesvariable-uuid-put
      parameters:
      - in: path
        name: repo_slug
        description: The repository
      - in: path
        name: username
        description: The account
      - in: path
        name: variable_uuid
        description: The UUID of the variable to update
      - in: body
        name: _body
        description: The updated variable
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
      - Pipelines
      - Config
      - Variables
      - Variable
      - Uu
  /repositories/{username}/{repo_slug}/pullrequests:
    get:
      summary: Get Repositories Username Repo Slug Pullrequests
      description: |-
        Returns a paginated list of all pull requests on the specified
        repository. By default only open pull requests are returned. This can
        be controlled using the `state` query parameter. To retrieve pull
        requests that are in one of multiple states, repeat the `state`
        parameter for each individual state.

        This endpoint also supports filtering and sorting of the results. See
        [filtering and sorting](../../../../meta/filtering) for more details.
      operationId: getRepositoriesUsernameRepoSlugPullrequests
      x-api-path-slug: repositoriesusernamerepo-slugpullrequests-get
      parameters:
      - in: path
        name: repo_slug
        description: 'This can either be the repository slug or the UUID of the repository,surrounded
          by curly-braces, for example: `{repository UUID}`'
      - in: query
        name: state
        description: Only return pull requests that are in this state
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
      - Pullrequests
    parameters:
      summary: Parameters Repositories Username Repo Slug Pullrequests
      description: Parameters repositories username repo slug pullrequests
      operationId: parametersRepositoriesUsernameRepoSlugPullrequests
      x-api-path-slug: repositoriesusernamerepo-slugpullrequests-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pullrequests
    post:
      summary: Add Repositories Username Repo Slug Pullrequests
      description: Post repositories username repo slug pullrequests
      operationId: postRepositoriesUsernameRepoSlugPullrequests
      x-api-path-slug: repositoriesusernamerepo-slugpullrequests-post
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
        description: The new pull request
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
      - Pullrequests
  /repositories/{username}/{repo_slug}/pullrequests/activity:
    get:
      summary: Get Repositories Username Repo Slug Pullrequests Activity
      description: |-
        Returns a paginated list of the pull request's activity log.

        This includes comments that were made by the reviewers, updates and
        approvals.
      operationId: getRepositoriesUsernameRepoSlugPullrequestsActivity
      x-api-path-slug: repositoriesusernamerepo-slugpullrequestsactivity-get
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
      - Pullrequests
      - Activity
    parameters:
      summary: Parameters Repositories Username Repo Slug Pullrequests Activity
      description: Parameters repositories username repo slug pullrequests activity
      operationId: parametersRepositoriesUsernameRepoSlugPullrequestsActivity
      x-api-path-slug: repositoriesusernamerepo-slugpullrequestsactivity-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pullrequests
      - Activity
  /repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}:
    get:
      summary: Get Repositories Username Repo Slug Pullrequests Pull Request
      description: Get repositories username repo slug pullrequests pull request
      operationId: getRepositoriesUsernameRepoSlugPullrequestsPullRequest
      x-api-path-slug: repositoriesusernamerepo-slugpullrequestspull-request-id-get
      parameters:
      - in: path
        name: pull_request_id
        description: The id of the pull request
      - in: path
        name: repo_slug
        description: 'This can either be the repository slug or the UUID of the repository,surrounded
          by curly-braces, for example: `{repository UUID}`'
      - in: path
        name: username
        description: 'This can either be the username or the UUID of the account,surrounded
          by curly-braces, for example: `{user UUID}`'
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pullrequests
      - Pull
      - Request
    parameters:
      summary: Parameters Repositories Username Repo Slug Pullrequests Pull Request
      description: Parameters repositories username repo slug pullrequests pull request
      operationId: parametersRepositoriesUsernameRepoSlugPullrequestsPullRequest
      x-api-path-slug: repositoriesusernamerepo-slugpullrequestspull-request-id-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pullrequests
      - Pull
      - Request
    put:
      summary: Update Repositories Username Repo Slug Pullrequests Pull Request
      description: |-
        Mutates the specified pull request.

        This can be used to change the pull request's branches or description.

        Only open pull requests can be mutated.
      operationId: putRepositoriesUsernameRepoSlugPullrequestsPullRequest
      x-api-path-slug: repositoriesusernamerepo-slugpullrequestspull-request-id-put
      parameters:
      - in: path
        name: pull_request_id
        description: The id of the open pull request
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
        description: The pull request that is to be updated
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
      - Pullrequests
      - Pull
      - Request
  /repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}/activity:
    get:
      summary: Get Repositories Username Repo Slug Pullrequests Pull Request  Activity
      description: |-
        Returns a paginated list of the pull request's activity log.

        This includes comments that were made by the reviewers, updates and
        approvals.
      operationId: getRepositoriesUsernameRepoSlugPullrequestsPullRequestActivity
      x-api-path-slug: repositoriesusernamerepo-slugpullrequestspull-request-idactivity-get
      parameters:
      - in: path
        name: pull_request_id
        description: The id of the pull request
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
      - Pullrequests
      - Pull
      - Request
      - ""
      - Activity
    parameters:
      summary: Parameters Repositories Username Repo Slug Pullrequests Pull Request  Activity
      description: Parameters repositories username repo slug pullrequests pull request  activity
      operationId: parametersRepositoriesUsernameRepoSlugPullrequestsPullRequestActivity
      x-api-path-slug: repositoriesusernamerepo-slugpullrequestspull-request-idactivity-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pullrequests
      - Pull
      - Request
      - ""
      - Activity
  /repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}/approve:
    delete:
      summary: Delete Repositories Username Repo Slug Pullrequests Pull Request  Approve
      description: Delete repositories username repo slug pullrequests pull request  approve
      operationId: deleteRepositoriesUsernameRepoSlugPullrequestsPullRequestApprove
      x-api-path-slug: repositoriesusernamerepo-slugpullrequestspull-request-idapprove-delete
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pullrequests
      - Pull
      - Request
      - ""
      - Approve
    parameters:
      summary: Parameters Repositories Username Repo Slug Pullrequests Pull Request  Approve
      description: Parameters repositories username repo slug pullrequests pull request  approve
      operationId: parametersRepositoriesUsernameRepoSlugPullrequestsPullRequestApprove
      x-api-path-slug: repositoriesusernamerepo-slugpullrequestspull-request-idapprove-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pullrequests
      - Pull
      - Request
      - ""
      - Approve
    post:
      summary: Add Repositories Username Repo Slug Pullrequests Pull Request  Approve
      description: Post repositories username repo slug pullrequests pull request  approve
      operationId: postRepositoriesUsernameRepoSlugPullrequestsPullRequestApprove
      x-api-path-slug: repositoriesusernamerepo-slugpullrequestspull-request-idapprove-post
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pullrequests
      - Pull
      - Request
      - ""
      - Approve
  /repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}/comments:
    get:
      summary: Get Repositories Username Repo Slug Pullrequests Pull Request  Comments
      description: |-
        Returns a paginated list of the pull request's comments.

        This includes both global, inline comments and replies.

        The default sorting is oldest to newest and can be overridden with
        the `sort` query parameter.

        This endpoint also supports filtering and sorting of the results. See
        [filtering and sorting](../../../../../../meta/filtering) for more
        details.
      operationId: getRepositoriesUsernameRepoSlugPullrequestsPullRequestComments
      x-api-path-slug: repositoriesusernamerepo-slugpullrequestspull-request-idcomments-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pullrequests
      - Pull
      - Request
      - ""
      - Comments
    parameters:
      summary: Parameters Repositories Username Repo Slug Pullrequests Pull Request  Comments
      description: Parameters repositories username repo slug pullrequests pull request  comments
      operationId: parametersRepositoriesUsernameRepoSlugPullrequestsPullRequestComments
      x-api-path-slug: repositoriesusernamerepo-slugpullrequestspull-request-idcomments-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pullrequests
      - Pull
      - Request
      - ""
      - Comments
  /repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}/comments/{comment_id}:
    get:
      summary: Get Repositories Username Repo Slug Pullrequests Pull Request  Comments
        Comment
      description: Get repositories username repo slug pullrequests pull request  comments
        comment
      operationId: getRepositoriesUsernameRepoSlugPullrequestsPullRequestCommentsComment
      x-api-path-slug: repositoriesusernamerepo-slugpullrequestspull-request-idcommentscomment-id-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pullrequests
      - Pull
      - Request
      - ""
      - Comments
      - Comment
    parameters:
      summary: Parameters Repositories Username Repo Slug Pullrequests Pull Request  Comments
        Comment
      description: Parameters repositories username repo slug pullrequests pull request  comments
        comment
      operationId: parametersRepositoriesUsernameRepoSlugPullrequestsPullRequestCommentsComment
      x-api-path-slug: repositoriesusernamerepo-slugpullrequestspull-request-idcommentscomment-id-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pullrequests
      - Pull
      - Request
      - ""
      - Comments
      - Comment
  /repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}/commits:
    get:
      summary: Get Repositories Username Repo Slug Pullrequests Pull Request  Commits
      description: |-
        Returns a paginated list of the pull request's commits.

        These are the commits that are being merged into the destination
        branch when the pull requests gets accepted.
      operationId: getRepositoriesUsernameRepoSlugPullrequestsPullRequestCommits
      x-api-path-slug: repositoriesusernamerepo-slugpullrequestspull-request-idcommits-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pullrequests
      - Pull
      - Request
      - ""
      - Commits
    parameters:
      summary: Parameters Repositories Username Repo Slug Pullrequests Pull Request  Commits
      description: Parameters repositories username repo slug pullrequests pull request  commits
      operationId: parametersRepositoriesUsernameRepoSlugPullrequestsPullRequestCommits
      x-api-path-slug: repositoriesusernamerepo-slugpullrequestspull-request-idcommits-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pullrequests
      - Pull
      - Request
      - ""
      - Commits
  /repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}/decline:
    parameters:
      summary: Parameters Repositories Username Repo Slug Pullrequests Pull Request  Decline
      description: Parameters repositories username repo slug pullrequests pull request  decline
      operationId: parametersRepositoriesUsernameRepoSlugPullrequestsPullRequestDecline
      x-api-path-slug: repositoriesusernamerepo-slugpullrequestspull-request-iddecline-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pullrequests
      - Pull
      - Request
      - ""
      - Decline
    post:
      summary: Add Repositories Username Repo Slug Pullrequests Pull Request  Decline
      description: Post repositories username repo slug pullrequests pull request  decline
      operationId: postRepositoriesUsernameRepoSlugPullrequestsPullRequestDecline
      x-api-path-slug: repositoriesusernamerepo-slugpullrequestspull-request-iddecline-post
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pullrequests
      - Pull
      - Request
      - ""
      - Decline
  /repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}/diff:
    get:
      summary: Get Repositories Username Repo Slug Pullrequests Pull Request  Diff
      description: Get repositories username repo slug pullrequests pull request  diff
      operationId: getRepositoriesUsernameRepoSlugPullrequestsPullRequestDiff
      x-api-path-slug: repositoriesusernamerepo-slugpullrequestspull-request-iddiff-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pullrequests
      - Pull
      - Request
      - ""
      - Diff
    parameters:
      summary: Parameters Repositories Username Repo Slug Pullrequests Pull Request  Diff
      description: Parameters repositories username repo slug pullrequests pull request  diff
      operationId: parametersRepositoriesUsernameRepoSlugPullrequestsPullRequestDiff
      x-api-path-slug: repositoriesusernamerepo-slugpullrequestspull-request-iddiff-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pullrequests
      - Pull
      - Request
      - ""
      - Diff
  /repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}/merge:
    parameters:
      summary: Parameters Repositories Username Repo Slug Pullrequests Pull Request  Merge
      description: Parameters repositories username repo slug pullrequests pull request  merge
      operationId: parametersRepositoriesUsernameRepoSlugPullrequestsPullRequestMerge
      x-api-path-slug: repositoriesusernamerepo-slugpullrequestspull-request-idmerge-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pullrequests
      - Pull
      - Request
      - ""
      - Merge
    post:
      summary: Add Repositories Username Repo Slug Pullrequests Pull Request  Merge
      description: Post repositories username repo slug pullrequests pull request  merge
      operationId: postRepositoriesUsernameRepoSlugPullrequestsPullRequestMerge
      x-api-path-slug: repositoriesusernamerepo-slugpullrequestspull-request-idmerge-post
      parameters:
      - in: body
        name: _body
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
      - Pullrequests
      - Pull
      - Request
      - ""
      - Merge
  /repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}/patch:
    get:
      summary: Get Repositories Username Repo Slug Pullrequests Pull Request  Patch
      description: Get repositories username repo slug pullrequests pull request  patch
      operationId: getRepositoriesUsernameRepoSlugPullrequestsPullRequestPatch
      x-api-path-slug: repositoriesusernamerepo-slugpullrequestspull-request-idpatch-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pullrequests
      - Pull
      - Request
      - ""
      - Patch
    parameters:
      summary: Parameters Repositories Username Repo Slug Pullrequests Pull Request  Patch
      description: Parameters repositories username repo slug pullrequests pull request  patch
      operationId: parametersRepositoriesUsernameRepoSlugPullrequestsPullRequestPatch
      x-api-path-slug: repositoriesusernamerepo-slugpullrequestspull-request-idpatch-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pullrequests
      - Pull
      - Request
      - ""
      - Patch
  /repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}/statuses:
    get:
      summary: Get Repositories Username Repo Slug Pullrequests Pull Request  Statuses
      description: Get repositories username repo slug pullrequests pull request  statuses
      operationId: getRepositoriesUsernameRepoSlugPullrequestsPullRequestStatuses
      x-api-path-slug: repositoriesusernamerepo-slugpullrequestspull-request-idstatuses-get
      parameters:
      - in: path
        name: pull_request_id
        description: The pull requests id
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pullrequests
      - Pull
      - Request
      - ""
      - Statuses
    parameters:
      summary: Parameters Repositories Username Repo Slug Pullrequests Pull Request  Statuses
      description: Parameters repositories username repo slug pullrequests pull request  statuses
      operationId: parametersRepositoriesUsernameRepoSlugPullrequestsPullRequestStatuses
      x-api-path-slug: repositoriesusernamerepo-slugpullrequestspull-request-idstatuses-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Pullrequests
      - Pull
      - Request
      - ""
      - Statuses
  /repositories/{username}/{repo_slug}/refs:
    get:
      summary: Get Repositories Username Repo Slug Refs
      description: Get repositories username repo slug refs
      operationId: getRepositoriesUsernameRepoSlugRefs
      x-api-path-slug: repositoriesusernamerepo-slugrefs-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Refs
    parameters:
      summary: Parameters Repositories Username Repo Slug Refs
      description: Parameters repositories username repo slug refs
      operationId: parametersRepositoriesUsernameRepoSlugRefs
      x-api-path-slug: repositoriesusernamerepo-slugrefs-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Refs
  /repositories/{username}/{repo_slug}/refs/branches:
    get:
      summary: Get Repositories Username Repo Slug Refs Branches
      description: Get repositories username repo slug refs branches
      operationId: getRepositoriesUsernameRepoSlugRefsBranches
      x-api-path-slug: repositoriesusernamerepo-slugrefsbranches-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Refs
      - Branches
    parameters:
      summary: Parameters Repositories Username Repo Slug Refs Branches
      description: Parameters repositories username repo slug refs branches
      operationId: parametersRepositoriesUsernameRepoSlugRefsBranches
      x-api-path-slug: repositoriesusernamerepo-slugrefsbranches-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Refs
      - Branches
  /repositories/{username}/{repo_slug}/refs/branches/{name}:
    get:
      summary: Get Repositories Username Repo Slug Refs Branches Name
      description: Get repositories username repo slug refs branches name
      operationId: getRepositoriesUsernameRepoSlugRefsBranchesName
      x-api-path-slug: repositoriesusernamerepo-slugrefsbranchesname-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Refs
      - Branches
      - Name
    parameters:
      summary: Parameters Repositories Username Repo Slug Refs Branches Name
      description: Parameters repositories username repo slug refs branches name
      operationId: parametersRepositoriesUsernameRepoSlugRefsBranchesName
      x-api-path-slug: repositoriesusernamerepo-slugrefsbranchesname-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Refs
      - Branches
      - Name
  /repositories/{username}/{repo_slug}/refs/tags:
    get:
      summary: Get Repositories Username Repo Slug Refs Tags
      description: Get repositories username repo slug refs tags
      operationId: getRepositoriesUsernameRepoSlugRefsTags
      x-api-path-slug: repositoriesusernamerepo-slugrefstags-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Refs
      - Tags
    parameters:
      summary: Parameters Repositories Username Repo Slug Refs Tags
      description: Parameters repositories username repo slug refs tags
      operationId: parametersRepositoriesUsernameRepoSlugRefsTags
      x-api-path-slug: repositoriesusernamerepo-slugrefstags-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Refs
      - Tags
    post:
      summary: Add Repositories Username Repo Slug Refs Tags
      description: |-
        Creates a new tag in the specified repository.

        The payload of the POST should consist of a JSON document that
        contains the name of the tag and the target hash.

        ```
        {
            "name" : "new tag name",
            "target" : {
                "hash" : "target commit hash",
            }
        }
        ```

        This endpoint does support using short hash prefixes for the commit
        hash, but it may return a 400 response if the provided prefix is
        ambiguous. Using a full commit hash is the preferred approach.
      operationId: postRepositoriesUsernameRepoSlugRefsTags
      x-api-path-slug: repositoriesusernamerepo-slugrefstags-post
      parameters:
      - in: body
        name: _body
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
      - Refs
      - Tags
  /repositories/{username}/{repo_slug}/refs/tags/{name}:
    get:
      summary: Get Repositories Username Repo Slug Refs Tags Name
      description: Get repositories username repo slug refs tags name
      operationId: getRepositoriesUsernameRepoSlugRefsTagsName
      x-api-path-slug: repositoriesusernamerepo-slugrefstagsname-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Refs
      - Tags
      - Name
    parameters:
      summary: Parameters Repositories Username Repo Slug Refs Tags Name
      description: Parameters repositories username repo slug refs tags name
      operationId: parametersRepositoriesUsernameRepoSlugRefsTagsName
      x-api-path-slug: repositoriesusernamerepo-slugrefstagsname-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Refs
      - Tags
      - Name
  /repositories/{username}/{repo_slug}/src/{node}/{path}:
    get:
      summary: Get Repositories Username Repo Slug Src Node Path
      description: Get repositories username repo slug src node path
      operationId: getRepositoriesUsernameRepoSlugSrcNodePath
      x-api-path-slug: repositoriesusernamerepo-slugsrcnodepath-get
      parameters:
      - in: query
        name: format
        description: Instead of returning the files contents, return the (json) meta
          data for it
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Src
      - Node
      - Path
    parameters:
      summary: Parameters Repositories Username Repo Slug Src Node Path
      description: Parameters repositories username repo slug src node path
      operationId: parametersRepositoriesUsernameRepoSlugSrcNodePath
      x-api-path-slug: repositoriesusernamerepo-slugsrcnodepath-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Src
      - Node
      - Path
  /repositories/{username}/{repo_slug}/versions:
    get:
      summary: Get Repositories Username Repo Slug Versions
      description: |-
        Returns the versions that have been defined in the issue tracker.

        This resource is only available on repositories that have the issue
        tracker enabled.
      operationId: getRepositoriesUsernameRepoSlugVersions
      x-api-path-slug: repositoriesusernamerepo-slugversions-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Versions
    parameters:
      summary: Parameters Repositories Username Repo Slug Versions
      description: Parameters repositories username repo slug versions
      operationId: parametersRepositoriesUsernameRepoSlugVersions
      x-api-path-slug: repositoriesusernamerepo-slugversions-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Versions
  /repositories/{username}/{repo_slug}/versions/{version_id}:
    get:
      summary: Get Repositories Username Repo Slug Versions Version
      description: Get repositories username repo slug versions version
      operationId: getRepositoriesUsernameRepoSlugVersionsVersion
      x-api-path-slug: repositoriesusernamerepo-slugversionsversion-id-get
      parameters:
      - in: path
        name: version_id
        description: The versions id
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Versions
      - Version
    parameters:
      summary: Parameters Repositories Username Repo Slug Versions Version
      description: Parameters repositories username repo slug versions version
      operationId: parametersRepositoriesUsernameRepoSlugVersionsVersion
      x-api-path-slug: repositoriesusernamerepo-slugversionsversion-id-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Versions
      - Version
  /repositories/{username}/{repo_slug}/watchers:
    get:
      summary: Get Repositories Username Repo Slug Watchers
      description: |-
        Returns a paginated list of all the watchers on the specified
        repository.
      operationId: getRepositoriesUsernameRepoSlugWatchers
      x-api-path-slug: repositoriesusernamerepo-slugwatchers-get
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Watchers
    parameters:
      summary: Parameters Repositories Username Repo Slug Watchers
      description: Parameters repositories username repo slug watchers
      operationId: parametersRepositoriesUsernameRepoSlugWatchers
      x-api-path-slug: repositoriesusernamerepo-slugwatchers-parameters
      responses:
        200:
          description: OK
      tags:
      - Repositories
      - Username
      - Repo
      - Slug
      - Watchers
  /snippets/{username}:
    get:
      summary: Get Snippets Username
      description: |-
        Identical to `/snippets`, except that the result is further filtered
        by the snippet owner and only those that are owned by `{username}` are
        returned.
      operationId: getSnippetsUsername
      x-api-path-slug: snippetsusername-get
      parameters:
      - in: query
        name: role
        description: Filter down the result based on the authenticated users role
          (`owner`, `contributor`, or `member`)
      - in: path
        name: username
        description: Limits the result to snippets owned by this user
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
    parameters:
      summary: Parameters Snippets Username
      description: Parameters snippets username
      operationId: parametersSnippetsUsername
      x-api-path-slug: snippetsusername-parameters
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
    post:
      summary: Add Snippets Username
      description: |-
        Identical to `/snippets`, except that the new snippet will be
        created under the account specified in the path parameter `{username}`.
      operationId: postSnippetsUsername
      x-api-path-slug: snippetsusername-post
      parameters:
      - in: body
        name: _body
        description: The new snippet object
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
  /snippets/{username}/{encoded_id}:
    delete:
      summary: Delete Snippets Username Encoded
      description: Deletes a snippet and returns an empty response.
      operationId: deleteSnippetsUsernameEncoded
      x-api-path-slug: snippetsusernameencoded-id-delete
      parameters:
      - in: path
        name: encoded_id
        description: The snippets id
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
    get:
      summary: Get Snippets Username Encoded
      description: |-
        Retrieves a single snippet.

        Snippets support multiple content types:

        * application/json
        * multipart/related
        * multipart/form-data


        application/json
        ----------------

        The default content type of the response is `application/json`.
        Since JSON is always `utf-8`, it cannot reliably contain file contents
        for files that are not text. Therefore, JSON snippet documents only
        contain the filename and links to the file contents.

        This means that in order to retrieve all parts of a snippet, N+1
        requests need to be made (where N is the number of files in the
        snippet).


        multipart/related
        -----------------

        To retrieve an entire snippet in a single response, use the
        `Accept: multipart/related` HTTP request header.

            $ curl -H "Accept: multipart/related" https://api.bitbucket.org/2.0/snippets/evzijst/1

        Response:

            HTTP/1.1 200 OK
            Content-Length: 2214
            Content-Type: multipart/related; start="snippet"; boundary="===============1438169132528273974=="
            MIME-Version: 1.0

            --===============1438169132528273974==
            Content-Type: application/json; charset="utf-8"
            MIME-Version: 1.0
            Content-ID: snippet

            {
              "links": {
                "self": {
                  "href": "https://api.bitbucket.org/2.0/snippets/evzijst/kypj"
                },
                "html": {
                  "href": "https://bitbucket.org/snippets/evzijst/kypj"
                },
                "comments": {
                  "href": "https://api.bitbucket.org/2.0/snippets/evzijst/kypj/comments"
                },
                "watchers": {
                  "href": "https://api.bitbucket.org/2.0/snippets/evzijst/kypj/watchers"
                },
                "commits": {
                  "href": "https://api.bitbucket.org/2.0/snippets/evzijst/kypj/commits"
                }
              },
              "id": kypj,
              "title": "My snippet",
              "created_on": "2014-12-29T22:22:04.790331+00:00",
              "updated_on": "2014-12-29T22:22:04.790331+00:00",
              "is_private": false,
              "files": {
                "foo.txt": {
                  "links": {
                    "self": {
                      "href": "https://api.bitbucket.org/2.0/snippets/evzijst/kypj/files/367ab19/foo.txt"
                    },
                    "html": {
                      "href": "https://bitbucket.org/snippets/evzijst/kypj#file-foo.txt"
                    }
                  }
                },
                "image.png": {
                  "links": {
                    "self": {
                      "href": "https://api.bitbucket.org/2.0/snippets/evzijst/kypj/files/367ab19/image.png"
                    },
                    "html": {
                      "href": "https://bitbucket.org/snippets/evzijst/kypj#file-image.png"
                    }
                  }
                }
              ],
              "owner": {
                "username": "evzijst",
                "display_name": "Erik van Zijst",
                "uuid": "{d301aafa-d676-4ee0-88be-962be7417567}",
                "links": {
                  "self": {
                    "href": "https://api.bitbucket.org/2.0/users/evzijst"
                  },
                  "html": {
                    "href": "https://bitbucket.org/evzijst"
                  },
                  "avatar": {
                    "href": "https://bitbucket-staging-assetroot.s3.amazonaws.com/c/photos/2013/Jul/31/erik-avatar-725122544-0_avatar.png"
                  }
                }
              },
              "creator": {
                "username": "evzijst",
                "display_name": "Erik van Zijst",
                "uuid": "{d301aafa-d676-4ee0-88be-962be7417567}",
                "links": {
                  "self": {
                    "href": "https://api.bitbucket.org/2.0/users/evzijst"
                  },
                  "html": {
                    "href": "https://bitbucket.org/evzijst"
                  },
                  "avatar": {
                    "href": "https://bitbucket-staging-assetroot.s3.amazonaws.com/c/photos/2013/Jul/31/erik-avatar-725122544-0_avatar.png"
                  }
                }
              }
            }

            --===============1438169132528273974==
            Content-Type: text/plain; charset="us-ascii"
            MIME-Version: 1.0
            Content-Transfer-Encoding: 7bit
            Content-ID: "foo.txt"
            Content-Disposition: attachment; filename="foo.txt"

            foo

            --===============1438169132528273974==
            Content-Type: image/png
            MIME-Version: 1.0
            Content-Transfer-Encoding: base64
            Content-ID: "image.png"
            Content-Disposition: attachment; filename="image.png"

            iVBORw0KGgoAAAANSUhEUgAAABQAAAAoCAYAAAD+MdrbAAABD0lEQVR4Ae3VMUoDQRTG8ccUaW2m
            TKONFxArJYJamCvkCnZTaa+VnQdJSBFl2SMsLFrEWNjZBZs0JgiL/+KrhhVmJRbCLPx4O+/DT2TB
            cbblJxf+UWFVVRNsEGAtgvJxnLm2H+A5RQ93uIl+3632PZyl/skjfOn9Gvdwmlcw5aPUwimG+NT5
            EnNN036IaZePUuIcK533NVfal7/5yjWeot2z9ta1cAczHEf7I+3J0ws9Cgx0fsOFpmlfwKcWPuBQ
            73Oc4FHzBaZ8llq4q1mr5B2mOUCt815qYR8eB1hG2VJ7j35q4RofaH7IG+Xrf/PfJhfmwtfFYoIN
            AqxFUD6OMxcvkO+UfKfkOyXfKdsv/AYCHMLVkHAFWgAAAABJRU5ErkJggg==
            --===============1438169132528273974==--

        multipart/form-data
        -------------------

        As with creating new snippets, `multipart/form-data` can be used as an
        alternative to `multipart/related`. However, the inherently flat
        structure of form-data means that only basic, root-level properties
        can be returned, while nested elements like `links` are omitted:

            $ curl -H "Accept: multipart/form-data" https://api.bitbucket.org/2.0/snippets/evzijst/kypj

        Response:

            HTTP/1.1 200 OK
            Content-Length: 951
            Content-Type: multipart/form-data; boundary=----------------------------63a4b224c59f

            ------------------------------63a4b224c59f
            Content-Disposition: form-data; name="title"
            Content-Type: text/plain; charset="utf-8"

            My snippet
            ------------------------------63a4b224c59f--
            Content-Disposition: attachment; name="file"; filename="foo.txt"
            Content-Type: text/plain

            foo

            ------------------------------63a4b224c59f
            Content-Disposition: attachment; name="file"; filename="image.png"
            Content-Transfer-Encoding: base64
            Content-Type: application/octet-stream

            iVBORw0KGgoAAAANSUhEUgAAABQAAAAoCAYAAAD+MdrbAAABD0lEQVR4Ae3VMUoDQRTG8ccUaW2m
            TKONFxArJYJamCvkCnZTaa+VnQdJSBFl2SMsLFrEWNjZBZs0JgiL/+KrhhVmJRbCLPx4O+/DT2TB
            cbblJxf+UWFVVRNsEGAtgvJxnLm2H+A5RQ93uIl+3632PZyl/skjfOn9Gvdwmlcw5aPUwimG+NT5
            EnNN036IaZePUuIcK533NVfal7/5yjWeot2z9ta1cAczHEf7I+3J0ws9Cgx0fsOFpmlfwKcWPuBQ
            73Oc4FHzBaZ8llq4q1mr5B2mOUCt815qYR8eB1hG2VJ7j35q4RofaH7IG+Xrf/PfJhfmwtfFYoIN
            AqxFUD6OMxcvkO+UfKfkOyXfKdsv/AYCHMLVkHAFWgAAAABJRU5ErkJggg==
            ------------------------------5957323a6b76--
      operationId: getSnippetsUsernameEncoded
      x-api-path-slug: snippetsusernameencoded-id-get
      parameters:
      - in: path
        name: encoded_id
        description: The snippets id
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
    parameters:
      summary: Parameters Snippets Username Encoded
      description: Parameters snippets username encoded
      operationId: parametersSnippetsUsernameEncoded
      x-api-path-slug: snippetsusernameencoded-id-parameters
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
    put:
      summary: Update Snippets Username Encoded
      description: |-
        Used to update a snippet. Use this to add and delete files and to
        change a snippet's title.

        To update a snippet, one can either PUT a full snapshot, or only the
        parts that need to be changed.

        The contract for PUT on this API is that properties missing from the
        request remain untouched so that snippets can be efficiently
        manipulated with differential payloads.

        To delete a property (e.g. the title, or a file), include its name in
        the request, but omit its value (use `null`).

        As in Git, explicit renaming of files is not supported. Instead, to
        rename a file, delete it and add it again under another name. This can
        be done atomically in a single request. Rename detection is left to
        the SCM.

        PUT supports three different content types for both request and
        response bodies:

        * `application/json`
        * `multipart/related`
        * `multipart/form-data`

        The content type used for the request body can be different than that
        used for the response. Content types are specified using standard HTTP
        headers.

        Use the `Content-Type` and `Accept` headers to select the desired
        request and response format.


        application/json
        ----------------

        As with creation and retrieval, the content type determines what
        properties can be manipulated. `application/json` does not support
        file contents and is therefore limited to a snippet's meta data.

        To update the title, without changing any of its files:

            $ curl -X POST -H "Content-Type: application/json" https://api.bitbucket.org/2.0/snippets/evzijst/kypj             -d '{"title": "Updated title"}'


        To delete the title:

            $ curl -X POST -H "Content-Type: application/json" https://api.bitbucket.org/2.0/snippets/evzijst/kypj             -d '{"title": null}'

        Not all parts of a snippet can be manipulated. The owner and creator
        for instance are immutable.


        multipart/related
        -----------------

        `multipart/related` can be used to manipulate all of a snippet's
        properties. The body is identical to a POST. properties omitted from
        the request are left unchanged. Since the `start` part contains JSON,
        the mechanism for manipulating the snippet's meta data is identical
        to `application/json` requests.

        To update one of a snippet's file contents, while also changing its
        title:

            PUT /2.0/snippets/evzijst/kypj HTTP/1.1
            Content-Length: 288
            Content-Type: multipart/related; start="snippet"; boundary="===============1438169132528273974=="
            MIME-Version: 1.0

            --===============1438169132528273974==
            Content-Type: application/json; charset="utf-8"
            MIME-Version: 1.0
            Content-ID: snippet

            {
              "title": "My updated snippet",
              "files": {
                  "foo.txt": {}
                }
            }

            --===============1438169132528273974==
            Content-Type: text/plain; charset="us-ascii"
            MIME-Version: 1.0
            Content-Transfer-Encoding: 7bit
            Content-ID: "foo.txt"
            Content-Disposition: attachment; filename="foo.txt"

            Updated file contents.

            --===============1438169132528273974==--

        Here only the parts that are changed are included in the body. The
        other files remain untouched.

        Note the use of the `files` list in the JSON part. This list contains
        the files that are being manipulated. This list should have
        corresponding multiparts in the request that contain the new contents
        of these files.

        If a filename in the `files` list does not have a corresponding part,
        it will be deleted from the snippet, as shown below:

            PUT /2.0/snippets/evzijst/kypj HTTP/1.1
            Content-Length: 188
            Content-Type: multipart/related; start="snippet"; boundary="===============1438169132528273974=="
            MIME-Version: 1.0

            --===============1438169132528273974==
            Content-Type: application/json; charset="utf-8"
            MIME-Version: 1.0
            Content-ID: snippet

            {
              "files": {
                "image.png": {}
              }
            }

            --===============1438169132528273974==--

        To simulate a rename, delete a file and add the same file under
        another name:

            PUT /2.0/snippets/evzijst/kypj HTTP/1.1
            Content-Length: 212
            Content-Type: multipart/related; start="snippet"; boundary="===============1438169132528273974=="
            MIME-Version: 1.0

            --===============1438169132528273974==
            Content-Type: application/json; charset="utf-8"
            MIME-Version: 1.0
            Content-ID: snippet

            {
                "files": {
                  "foo.txt": {},
                  "bar.txt": {}
                }
            }

            --===============1438169132528273974==
            Content-Type: text/plain; charset="us-ascii"
            MIME-Version: 1.0
            Content-Transfer-Encoding: 7bit
            Content-ID: "bar.txt"
            Content-Disposition: attachment; filename="bar.txt"

            foo

            --===============1438169132528273974==--


        multipart/form-data
        -----------------

        Again, one can also use `multipart/form-data` to manipulate file
        contents and meta data atomically.

            $ curl -X PUT http://localhost:12345/2.0/snippets/evzijst/kypj             -F title="My updated snippet" -F file=@foo.txt

            PUT /2.0/snippets/evzijst/kypj HTTP/1.1
            Content-Length: 351
            Content-Type: multipart/form-data; boundary=----------------------------63a4b224c59f

            ------------------------------63a4b224c59f
            Content-Disposition: form-data; name="file"; filename="foo.txt"
            Content-Type: text/plain

            foo

            ------------------------------63a4b224c59f
            Content-Disposition: form-data; name="title"

            My updated snippet
            ------------------------------63a4b224c59f

        To delete a file, omit its contents while including its name in the
        `files` field:

            $ curl -X PUT https://api.bitbucket.org/2.0/snippets/evzijst/kypj -F files=image.png

            PUT /2.0/snippets/evzijst/kypj HTTP/1.1
            Content-Length: 149
            Content-Type: multipart/form-data; boundary=----------------------------ef8871065a86

            ------------------------------ef8871065a86
            Content-Disposition: form-data; name="files"

            image.png
            ------------------------------ef8871065a86--

        The explicit use of the `files` element in `multipart/related` and
        `multipart/form-data` is only required when deleting files.
        The default mode of operation is for file parts to be processed,
        regardless of whether or not they are listed in `files`, as a
        convenience to the client.
      operationId: putSnippetsUsernameEncoded
      x-api-path-slug: snippetsusernameencoded-id-put
      parameters:
      - in: path
        name: encoded_id
        description: The snippets id
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
  /snippets/{username}/{encoded_id}/comments:
    get:
      summary: Get Snippets Username Encoded  Comments
      description: |-
        Used to retrieve a paginated list of all comments for a specific
        snippet.

        This resource works identical to commit and pull request comments.

        The default sorting is oldest to newest and can be overridden with
        the `sort` query parameter.
      operationId: getSnippetsUsernameEncodedComments
      x-api-path-slug: snippetsusernameencoded-idcomments-get
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Comments
    parameters:
      summary: Parameters Snippets Username Encoded  Comments
      description: Parameters snippets username encoded  comments
      operationId: parametersSnippetsUsernameEncodedComments
      x-api-path-slug: snippetsusernameencoded-idcomments-parameters
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Comments
    post:
      summary: Add Snippets Username Encoded  Comments
      description: |-
        Creates a new comment.

        The only required field in the body is `content.raw`.

        To create a threaded reply to an existing comment, include `parent.id`.
      operationId: postSnippetsUsernameEncodedComments
      x-api-path-slug: snippetsusernameencoded-idcomments-post
      parameters:
      - in: body
        name: _body
        description: The contents of the new comment
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Comments
  /snippets/{username}/{encoded_id}/comments/{comment_id}:
    delete:
      summary: Delete Snippets Username Encoded  Comments Comment
      description: |-
        Deletes a snippet comment.

        Comments can only be removed by their author.
      operationId: deleteSnippetsUsernameEncodedCommentsComment
      x-api-path-slug: snippetsusernameencoded-idcommentscomment-id-delete
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Comments
      - Comment
    get:
      summary: Get Snippets Username Encoded  Comments Comment
      description: Get snippets username encoded  comments comment
      operationId: getSnippetsUsernameEncodedCommentsComment
      x-api-path-slug: snippetsusernameencoded-idcommentscomment-id-get
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Comments
      - Comment
    parameters:
      summary: Parameters Snippets Username Encoded  Comments Comment
      description: Parameters snippets username encoded  comments comment
      operationId: parametersSnippetsUsernameEncodedCommentsComment
      x-api-path-slug: snippetsusernameencoded-idcommentscomment-id-parameters
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Comments
      - Comment
    put:
      summary: Update Snippets Username Encoded  Comments Comment
      description: |-
        Updates a comment.

        Comments can only be updated by their author.
      operationId: putSnippetsUsernameEncodedCommentsComment
      x-api-path-slug: snippetsusernameencoded-idcommentscomment-id-put
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Comments
      - Comment
  /snippets/{username}/{encoded_id}/commits:
    get:
      summary: Get Snippets Username Encoded  Commits
      description: Returns the changes (commits) made on this snippet.
      operationId: getSnippetsUsernameEncodedCommits
      x-api-path-slug: snippetsusernameencoded-idcommits-get
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Commits
    parameters:
      summary: Parameters Snippets Username Encoded  Commits
      description: Parameters snippets username encoded  commits
      operationId: parametersSnippetsUsernameEncodedCommits
      x-api-path-slug: snippetsusernameencoded-idcommits-parameters
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Commits
  /snippets/{username}/{encoded_id}/commits/{revision}:
    get:
      summary: Get Snippets Username Encoded  Commits Revision
      description: Get snippets username encoded  commits revision
      operationId: getSnippetsUsernameEncodedCommitsRevision
      x-api-path-slug: snippetsusernameencoded-idcommitsrevision-get
      responses:
        200:
          description: OK
      tags:
      - Snippets
      - Username
      - Encoded
      - ""
      - Commits
      - Revision
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