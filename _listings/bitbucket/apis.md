---
name: Bitbucket
x-slug: bitbucket
description: Collaborate on code with inline comments and pull requests. Manage and
  share your Git repositories to build and ship software, as a team.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
x-kinRank: "8"
x-alexaRank: "901"
tags: Name
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/apis.md
specificationVersion: "0.14"
apis:
- name: Bitbucket Get Repositories Username
  x-api-slug: bitbucket
  description: |-
    Returns a paginated list of all repositories owned by the specified
    account or UUID.

    The result can be narrowed down based on the authenticated user's role.

    E.g. with `?role=contributor`, only those repositories that the
    authenticated user has write access to are returned (this includes any
    repo the user is an admin on, as that implies write access).

    This endpoint also supports filtering and sorting of the results. See
    [filtering and sorting](../../meta/filtering) for more details.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}
  tags: Repositories, Username
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusername-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusername-get-openapi.md
- name: Bitbucket Parameters Repositories Username
  x-api-slug: bitbucket
  description: Parameters repositories username
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}
  tags: Repositories, Username
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusername-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusername-parameters-openapi.md
- name: Bitbucket Delete Repositories Username Repo Slug
  x-api-slug: bitbucket
  description: |-
    Deletes the repository. This is an irreversible operation.

    This does not affect its forks.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}
  tags: Repositories, Username, Repo, Slug
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slug-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slug-delete-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug
  x-api-slug: bitbucket
  description: Returns the object describing this repository.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}
  tags: Repositories, Username, Repo, Slug
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slug-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slug-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}
  tags: Repositories, Username, Repo, Slug
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slug-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slug-parameters-openapi.md
- name: Bitbucket Add Repositories Username Repo Slug
  x-api-slug: bitbucket
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}
  tags: Repositories, Username, Repo, Slug
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slug-post-openapi.md
- name: Bitbucket Update Repositories Username Repo Slug
  x-api-slug: bitbucket
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}
  tags: Repositories, Username, Repo, Slug
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slug-put-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Branch Restrictions
  x-api-slug: bitbucket
  description: |-
    Returns a paginated list of all branch restrictions on the
    repository.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/branch-restrictions
  tags: Repositories, Username, Repo, Slug, Branch, Restrictions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugbranchrestrictions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugbranchrestrictions-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Branch Restrictions
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug branch restrictions
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/branch-restrictions
  tags: Repositories, Username, Repo, Slug, Branch, Restrictions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugbranchrestrictions-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugbranchrestrictions-parameters-openapi.md
- name: Bitbucket Add Repositories Username Repo Slug Branch Restrictions
  x-api-slug: bitbucket
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/branch-restrictions
  tags: Repositories, Username, Repo, Slug, Branch, Restrictions
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugbranchrestrictions-post-openapi.md
- name: Bitbucket Delete Repositories Username Repo Slug Branch Restrictions
  x-api-slug: bitbucket
  description: Delete repositories username repo slug branch restrictions
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/branch-restrictions/{id}
  tags: Repositories, Username, Repo, Slug, Branch, Restrictions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugbranchrestrictionsid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugbranchrestrictionsid-delete-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Branch Restrictions
  x-api-slug: bitbucket
  description: Get repositories username repo slug branch restrictions
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/branch-restrictions/{id}
  tags: Repositories, Username, Repo, Slug, Branch, Restrictions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugbranchrestrictionsid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugbranchrestrictionsid-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Branch Restrictions
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug branch restrictions
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/branch-restrictions/{id}
  tags: Repositories, Username, Repo, Slug, Branch, Restrictions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugbranchrestrictionsid-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugbranchrestrictionsid-parameters-openapi.md
- name: Bitbucket Update Repositories Username Repo Slug Branch Restrictions
  x-api-slug: bitbucket
  description: |-
    Updates an existing branch restriction rule.

    Fields not present in the request body are ignored.

    See [`POST`](../../branch-restrictions#post) for details.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/branch-restrictions/{id}
  tags: Repositories, Username, Repo, Slug, Branch, Restrictions
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugbranchrestrictionsid-put-openapi.md
- name: Bitbucket Delete Repositories Username Repo Slug Commit Node Approve
  x-api-slug: bitbucket
  description: |-
    Redact the authenticated user's approval of the specified commit.

    This operation is only available to users that have explicit access to
    the repository. In contrast, just the fact that a repository is
    publicly accessible to users does not give them the ability to approve
    commits.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/commit/{node}/approve
  tags: Repositories, Username, Repo, Slug, Commit, Node, Approve
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitnodeapprove-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitnodeapprove-delete-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Commit Node Approve
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug commit node approve
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/commit/{node}/approve
  tags: Repositories, Username, Repo, Slug, Commit, Node, Approve
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitnodeapprove-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitnodeapprove-parameters-openapi.md
- name: Bitbucket Add Repositories Username Repo Slug Commit Node Approve
  x-api-slug: bitbucket
  description: |-
    Approve the specified commit as the authenticated user.

    This operation is only available to users that have explicit access to
    the repository. In contrast, just the fact that a repository is
    publicly accessible to users does not give them the ability to approve
    commits.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/commit/{node}/approve
  tags: Repositories, Username, Repo, Slug, Commit, Node, Approve
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitnodeapprove-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitnodeapprove-post-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Commit Node Statuses
  x-api-slug: bitbucket
  description: Returns all statuses (e.g. build results) for a specific commit.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/commit/{node}/statuses
  tags: Repositories, Username, Repo, Slug, Commit, Node, Statuses
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitnodestatuses-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitnodestatuses-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Commit Node Statuses
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug commit node statuses
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/commit/{node}/statuses
  tags: Repositories, Username, Repo, Slug, Commit, Node, Statuses
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitnodestatuses-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitnodestatuses-parameters-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Commit Node Statuses
    Build
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug commit node statuses build
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/commit/{node}/statuses/build
  tags: Repositories, Username, Repo, Slug, Commit, Node, Statuses, Build
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitnodestatusesbuild-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitnodestatusesbuild-parameters-openapi.md
- name: Bitbucket Add Repositories Username Repo Slug Commit Node Statuses Build
  x-api-slug: bitbucket
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/commit/{node}/statuses/build
  tags: Repositories, Username, Repo, Slug, Commit, Node, Statuses, Build
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitnodestatusesbuild-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitnodestatusesbuild-post-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Commit Node Statuses Build Key
  x-api-slug: bitbucket
  description: Get repositories username repo slug commit node statuses build key
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/commit/{node}/statuses/build/{key}
  tags: Repositories, Username, Repo, Slug, Commit, Node, Statuses, Build, Key
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitnodestatusesbuildkey-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitnodestatusesbuildkey-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Commit Node Statuses
    Build Key
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug commit node statuses build
    key
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/commit/{node}/statuses/build/{key}
  tags: Repositories, Username, Repo, Slug, Commit, Node, Statuses, Build, Key
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitnodestatusesbuildkey-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitnodestatusesbuildkey-parameters-openapi.md
- name: Bitbucket Update Repositories Username Repo Slug Commit Node Statuses Build
    Key
  x-api-slug: bitbucket
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/commit/{node}/statuses/build/{key}
  tags: Repositories, Username, Repo, Slug, Commit, Node, Statuses, Build, Key
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitnodestatusesbuildkey-put-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Commit Revision
  x-api-slug: bitbucket
  description: Get repositories username repo slug commit revision
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/commit/{revision}
  tags: Repositories, Username, Repo, Slug, Commit, Revision
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitrevision-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitrevision-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Commit Revision
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug commit revision
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/commit/{revision}
  tags: Repositories, Username, Repo, Slug, Commit, Revision
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitrevision-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitrevision-parameters-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Commit Sha Comments
  x-api-slug: bitbucket
  description: |-
    Returns the commit's comments.

    This includes both global and inline comments.

    The default sorting is oldest to newest and can be overridden with
    the `sort` query parameter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/commit/{sha}/comments
  tags: Repositories, Username, Repo, Slug, Commit, Sha, Comments
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitshacomments-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitshacomments-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Commit Sha Comments
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug commit sha comments
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/commit/{sha}/comments
  tags: Repositories, Username, Repo, Slug, Commit, Sha, Comments
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitshacomments-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitshacomments-parameters-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Commit Sha Comments Comment
  x-api-slug: bitbucket
  description: Get repositories username repo slug commit sha comments comment
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/commit/{sha}/comments/{comment_id}
  tags: Repositories, Username, Repo, Slug, Commit, Sha, Comments, Comment
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitshacommentscomment-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitshacommentscomment-id-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Commit Sha Comments Comment
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug commit sha comments comment
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/commit/{sha}/comments/{comment_id}
  tags: Repositories, Username, Repo, Slug, Commit, Sha, Comments, Comment
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitshacommentscomment-id-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitshacommentscomment-id-parameters-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Commits
  x-api-slug: bitbucket
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/commits
  tags: Repositories, Username, Repo, Slug, Commits
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommits-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommits-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Commits
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug commits
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/commits
  tags: Repositories, Username, Repo, Slug, Commits
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommits-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommits-parameters-openapi.md
- name: Bitbucket Add Repositories Username Repo Slug Commits
  x-api-slug: bitbucket
  description: |-
    Identical to `GET /repositories/{username}/{repo_slug}/commits`,
    except that POST allows clients to place the include and exclude
    parameters in the request body to avoid URL length issues.

    **Note that this resource does NOT support new commit creation.**
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/commits
  tags: Repositories, Username, Repo, Slug, Commits
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommits-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommits-post-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Commits Revision
  x-api-slug: bitbucket
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/commits/{revision}
  tags: Repositories, Username, Repo, Slug, Commits, Revision
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitsrevision-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitsrevision-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Commits Revision
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug commits revision
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/commits/{revision}
  tags: Repositories, Username, Repo, Slug, Commits, Revision
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitsrevision-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitsrevision-parameters-openapi.md
- name: Bitbucket Add Repositories Username Repo Slug Commits Revision
  x-api-slug: bitbucket
  description: |-
    Identical to `GET /repositories/{username}/{repo_slug}/commits`,
    except that POST allows clients to place the include and exclude
    parameters in the request body to avoid URL length issues.

    **Note that this resource does NOT support new commit creation.**
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/commits/{revision}
  tags: Repositories, Username, Repo, Slug, Commits, Revision
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitsrevision-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcommitsrevision-post-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Components
  x-api-slug: bitbucket
  description: |-
    Returns the components that have been defined in the issue tracker.

    This resource is only available on repositories that have the issue
    tracker enabled.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/components
  tags: Repositories, Username, Repo, Slug, Components
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcomponents-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcomponents-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Components
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug components
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/components
  tags: Repositories, Username, Repo, Slug, Components
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcomponents-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcomponents-parameters-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Components Component
  x-api-slug: bitbucket
  description: Get repositories username repo slug components component
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/components/{component_id}
  tags: Repositories, Username, Repo, Slug, Components, Component
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcomponentscomponent-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcomponentscomponent-id-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Components Component
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug components component
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/components/{component_id}
  tags: Repositories, Username, Repo, Slug, Components, Component
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcomponentscomponent-id-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugcomponentscomponent-id-parameters-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Default Reviewers
  x-api-slug: bitbucket
  description: |-
    Returns the repository's default reviewers.

    These are the users that are automatically added as reviewers on every
    new pull request that is created.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/default-reviewers
  tags: Repositories, Username, Repo, Slug, Default, Reviewers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugdefaultreviewers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugdefaultreviewers-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Default Reviewers
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug default reviewers
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/default-reviewers
  tags: Repositories, Username, Repo, Slug, Default, Reviewers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugdefaultreviewers-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugdefaultreviewers-parameters-openapi.md
- name: Bitbucket Delete Repositories Username Repo Slug Default Reviewers Target
    Username
  x-api-slug: bitbucket
  description: Delete repositories username repo slug default reviewers target username
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/default-reviewers/{target_username}
  tags: Repositories, Username, Repo, Slug, Default, Reviewers, Target, Username
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugdefaultreviewerstarget-username-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugdefaultreviewerstarget-username-delete-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Default Reviewers Target Username
  x-api-slug: bitbucket
  description: |-
    Returns the specified reviewer.

    This can be used to test whether a user is among the repository's
    default reviewers list. A 404 indicates that that specified user is not
    a default reviewer.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/default-reviewers/{target_username}
  tags: Repositories, Username, Repo, Slug, Default, Reviewers, Target, Username
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugdefaultreviewerstarget-username-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugdefaultreviewerstarget-username-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Default Reviewers Target
    Username
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug default reviewers target
    username
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/default-reviewers/{target_username}
  tags: Repositories, Username, Repo, Slug, Default, Reviewers, Target, Username
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugdefaultreviewerstarget-username-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugdefaultreviewerstarget-username-parameters-openapi.md
- name: Bitbucket Update Repositories Username Repo Slug Default Reviewers Target
    Username
  x-api-slug: bitbucket
  description: |-
    Adds the specified user to the repository's list of default
    reviewers.

    This method is idempotent. Adding a user a second time has no effect.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/default-reviewers/{target_username}
  tags: Repositories, Username, Repo, Slug, Default, Reviewers, Target, Username
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugdefaultreviewerstarget-username-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugdefaultreviewerstarget-username-put-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Diff Spec
  x-api-slug: bitbucket
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/diff/{spec}
  tags: Repositories, Username, Repo, Slug, Diff, Spec
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugdiffspec-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugdiffspec-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Diff Spec
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug diff spec
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/diff/{spec}
  tags: Repositories, Username, Repo, Slug, Diff, Spec
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugdiffspec-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugdiffspec-parameters-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Downloads
  x-api-slug: bitbucket
  description: Returns a list of download links associated with the repository.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/downloads
  tags: Repositories, Username, Repo, Slug, Downloads
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugdownloads-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugdownloads-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Downloads
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug downloads
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/downloads
  tags: Repositories, Username, Repo, Slug, Downloads
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugdownloads-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugdownloads-parameters-openapi.md
- name: Bitbucket Add Repositories Username Repo Slug Downloads
  x-api-slug: bitbucket
  description: |-
    Upload new download artifacts.

    To upload files, perform a `multipart/form-data` POST containing one
    or more `files` fields:

        $ echo Hello World > hello.txt
        $ curl -s -u evzijst -X POST https://api.bitbucket.org/2.0/repositories/evzijst/git-tests/downloads -F files=@hello.txt

    When a file is uploaded with the same name as an existing artifact,
    then the existing file will be replaced.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/downloads
  tags: Repositories, Username, Repo, Slug, Downloads
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugdownloads-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugdownloads-post-openapi.md
- name: Bitbucket Delete Repositories Username Repo Slug Downloads Filename
  x-api-slug: bitbucket
  description: Deletes the specified download artifact from the repository.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/downloads/{filename}
  tags: Repositories, Username, Repo, Slug, Downloads, Filename
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugdownloadsfilename-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugdownloadsfilename-delete-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Downloads Filename
  x-api-slug: bitbucket
  description: |-
    Return a redirect to the contents of a download artifact.

    This endpoint returns the actual file contents and not the artifact's
    metadata.

        $ curl -s -L https://api.bitbucket.org/2.0/repositories/evzijst/git-tests/downloads/hello.txt
        Hello World
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/downloads/{filename}
  tags: Repositories, Username, Repo, Slug, Downloads, Filename
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugdownloadsfilename-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugdownloadsfilename-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Downloads Filename
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug downloads filename
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/downloads/{filename}
  tags: Repositories, Username, Repo, Slug, Downloads, Filename
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugdownloadsfilename-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugdownloadsfilename-parameters-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Forks
  x-api-slug: bitbucket
  description: |-
    Returns a paginated list of all the forks of the specified
    repository.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/forks
  tags: Repositories, Username, Repo, Slug, Forks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugforks-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugforks-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Forks
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug forks
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/forks
  tags: Repositories, Username, Repo, Slug, Forks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugforks-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugforks-parameters-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Hooks
  x-api-slug: bitbucket
  description: Returns a paginated list of webhooks installed on this repository.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/hooks
  tags: Repositories, Username, Repo, Slug, Hooks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slughooks-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slughooks-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Hooks
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug hooks
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/hooks
  tags: Repositories, Username, Repo, Slug, Hooks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slughooks-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slughooks-parameters-openapi.md
- name: Bitbucket Add Repositories Username Repo Slug Hooks
  x-api-slug: bitbucket
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/hooks
  tags: Repositories, Username, Repo, Slug, Hooks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slughooks-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slughooks-post-openapi.md
- name: Bitbucket Delete Repositories Username Repo Slug Hooks U
  x-api-slug: bitbucket
  description: |-
    Deletes the specified webhook subscription from the given
    repository.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/hooks/{uid}
  tags: Repositories, Username, Repo, Slug, Hooks, U
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slughooksuid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slughooksuid-delete-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Hooks U
  x-api-slug: bitbucket
  description: |-
    Returns the webhook with the specified id installed on the specified
    repository.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/hooks/{uid}
  tags: Repositories, Username, Repo, Slug, Hooks, U
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slughooksuid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slughooksuid-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Hooks U
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug hooks u
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/hooks/{uid}
  tags: Repositories, Username, Repo, Slug, Hooks, U
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slughooksuid-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slughooksuid-parameters-openapi.md
- name: Bitbucket Update Repositories Username Repo Slug Hooks U
  x-api-slug: bitbucket
  description: |-
    Updates the specified webhook subscription.

    The following properties can be mutated:

    * `description`
    * `url`
    * `active`
    * `events`
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/hooks/{uid}
  tags: Repositories, Username, Repo, Slug, Hooks, U
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slughooksuid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slughooksuid-put-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Issues
  x-api-slug: bitbucket
  description: Get repositories username repo slug issues
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/issues
  tags: Repositories, Username, Repo, Slug, Issues
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissues-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissues-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Issues
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug issues
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/issues
  tags: Repositories, Username, Repo, Slug, Issues
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissues-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissues-parameters-openapi.md
- name: Bitbucket Add Repositories Username Repo Slug Issues
  x-api-slug: bitbucket
  description: |-
    Creates a new issue.

    This call requires authentication. Private repositories or private
    issue trackers require the caller to authenticate with an account that
    has appropriate authorisation.

    The authenticated user is used for the issue's `reporter` field.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/issues
  tags: Repositories, Username, Repo, Slug, Issues
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissues-post-openapi.md
- name: Bitbucket Delete Repositories Username Repo Slug Issues Issue
  x-api-slug: bitbucket
  description: |-
    Deletes the specified issue. This requires write access to the
    repository.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/issues/{issue_id}
  tags: Repositories, Username, Repo, Slug, Issues, Issue
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-id-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-id-delete-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Issues Issue
  x-api-slug: bitbucket
  description: Get repositories username repo slug issues issue
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/issues/{issue_id}
  tags: Repositories, Username, Repo, Slug, Issues, Issue
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-id-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Issues Issue
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug issues issue
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/issues/{issue_id}
  tags: Repositories, Username, Repo, Slug, Issues, Issue
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-id-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-id-parameters-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Issues Issue  Attachments
  x-api-slug: bitbucket
  description: |-
    Returns all attachments for this issue.

    This returns the files' meta data. This does not return the files'
    actual contents.

    The files are always ordered by their upload date.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/issues/{issue_id}/attachments
  tags: Repositories, Username, Repo, Slug, Issues, Issue, , Attachments
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-idattachments-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-idattachments-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Issues Issue  Attachments
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug issues issue  attachments
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/issues/{issue_id}/attachments
  tags: Repositories, Username, Repo, Slug, Issues, Issue, , Attachments
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-idattachments-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-idattachments-parameters-openapi.md
- name: Bitbucket Add Repositories Username Repo Slug Issues Issue  Attachments
  x-api-slug: bitbucket
  description: |-
    Upload new issue attachments.

    To upload files, perform a `multipart/form-data` POST containing one
    or more file fields.

    When a file is uploaded with the same name as an existing attachment,
    then the existing file will be replaced.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/issues/{issue_id}/attachments
  tags: Repositories, Username, Repo, Slug, Issues, Issue, , Attachments
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-idattachments-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-idattachments-post-openapi.md
- name: Bitbucket Delete Repositories Username Repo Slug Issues Issue  Attachments
    Path
  x-api-slug: bitbucket
  description: Delete repositories username repo slug issues issue  attachments path
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/issues/{issue_id}/attachments/{path}
  tags: Repositories, Username, Repo, Slug, Issues, Issue, , Attachments, Path
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-idattachmentspath-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-idattachmentspath-delete-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Issues Issue  Attachments Path
  x-api-slug: bitbucket
  description: |-
    Returns the contents of the specified file attachment.

    Note that this endpoint does not return a JSON response, but instead
    returns a redirect pointing to the actual file that in turn will return
    the raw contents.

    The redirect URL contains a one-time token that has a limited lifetime.
    As a result, the link should not be persisted, stored, or shared.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/issues/{issue_id}/attachments/{path}
  tags: Repositories, Username, Repo, Slug, Issues, Issue, , Attachments, Path
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-idattachmentspath-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-idattachmentspath-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Issues Issue  Attachments
    Path
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug issues issue  attachments
    path
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/issues/{issue_id}/attachments/{path}
  tags: Repositories, Username, Repo, Slug, Issues, Issue, , Attachments, Path
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-idattachmentspath-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-idattachmentspath-parameters-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Issues Issue  Comments
  x-api-slug: bitbucket
  description: |-
    Returns all comments that were made on the specified issue.

    The default sorting is oldest to newest and can be overridden with
    the `sort` query parameter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/issues/{issue_id}/comments
  tags: Repositories, Username, Repo, Slug, Issues, Issue, , Comments
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-idcomments-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-idcomments-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Issues Issue  Comments
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug issues issue  comments
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/issues/{issue_id}/comments
  tags: Repositories, Username, Repo, Slug, Issues, Issue, , Comments
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-idcomments-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-idcomments-parameters-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Issues Issue  Comments Comment
  x-api-slug: bitbucket
  description: Get repositories username repo slug issues issue  comments comment
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/issues/{issue_id}/comments/{comment_id}
  tags: Repositories, Username, Repo, Slug, Issues, Issue, , Comments, Comment
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-idcommentscomment-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-idcommentscomment-id-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Issues Issue  Comments
    Comment
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug issues issue  comments comment
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/issues/{issue_id}/comments/{comment_id}
  tags: Repositories, Username, Repo, Slug, Issues, Issue, , Comments, Comment
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-idcommentscomment-id-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-idcommentscomment-id-parameters-openapi.md
- name: Bitbucket Delete Repositories Username Repo Slug Issues Issue  Vote
  x-api-slug: bitbucket
  description: Delete repositories username repo slug issues issue  vote
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/issues/{issue_id}/vote
  tags: Repositories, Username, Repo, Slug, Issues, Issue, , Vote
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-idvote-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-idvote-delete-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Issues Issue  Vote
  x-api-slug: bitbucket
  description: |-
    Check whether the authenticated user has voted for this issue.
    A 204 status code indicates that the user has voted, while a 404
    implies they haven't.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/issues/{issue_id}/vote
  tags: Repositories, Username, Repo, Slug, Issues, Issue, , Vote
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-idvote-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-idvote-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Issues Issue  Vote
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug issues issue  vote
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/issues/{issue_id}/vote
  tags: Repositories, Username, Repo, Slug, Issues, Issue, , Vote
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-idvote-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-idvote-parameters-openapi.md
- name: Bitbucket Update Repositories Username Repo Slug Issues Issue  Vote
  x-api-slug: bitbucket
  description: |-
    Vote for this issue.

    To cast your vote, do an empty PUT. The 204 status code indicates that
    the operation was successful.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/issues/{issue_id}/vote
  tags: Repositories, Username, Repo, Slug, Issues, Issue, , Vote
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-idvote-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-idvote-put-openapi.md
- name: Bitbucket Delete Repositories Username Repo Slug Issues Issue  Watch
  x-api-slug: bitbucket
  description: Delete repositories username repo slug issues issue  watch
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/issues/{issue_id}/watch
  tags: Repositories, Username, Repo, Slug, Issues, Issue, , Watch
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-idwatch-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-idwatch-delete-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Issues Issue  Watch
  x-api-slug: bitbucket
  description: |-
    Indicated whether or not the authenticated user is watching this
    issue.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/issues/{issue_id}/watch
  tags: Repositories, Username, Repo, Slug, Issues, Issue, , Watch
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-idwatch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-idwatch-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Issues Issue  Watch
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug issues issue  watch
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/issues/{issue_id}/watch
  tags: Repositories, Username, Repo, Slug, Issues, Issue, , Watch
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-idwatch-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-idwatch-parameters-openapi.md
- name: Bitbucket Update Repositories Username Repo Slug Issues Issue  Watch
  x-api-slug: bitbucket
  description: |-
    Start watching this issue.

    To start watching this issue, do an empty PUT. The 204 status code
    indicates that the operation was successful.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/issues/{issue_id}/watch
  tags: Repositories, Username, Repo, Slug, Issues, Issue, , Watch
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-idwatch-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugissuesissue-idwatch-put-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Milestones
  x-api-slug: bitbucket
  description: |-
    Returns the milestones that have been defined in the issue tracker.

    This resource is only available on repositories that have the issue
    tracker enabled.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/milestones
  tags: Repositories, Username, Repo, Slug, Milestones
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugmilestones-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugmilestones-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Milestones
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug milestones
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/milestones
  tags: Repositories, Username, Repo, Slug, Milestones
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugmilestones-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugmilestones-parameters-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Milestones Milestone
  x-api-slug: bitbucket
  description: Get repositories username repo slug milestones milestone
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/milestones/{milestone_id}
  tags: Repositories, Username, Repo, Slug, Milestones, Milestone
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugmilestonesmilestone-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugmilestonesmilestone-id-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Milestones Milestone
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug milestones milestone
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/milestones/{milestone_id}
  tags: Repositories, Username, Repo, Slug, Milestones, Milestone
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugmilestonesmilestone-id-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugmilestonesmilestone-id-parameters-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Patch Spec
  x-api-slug: bitbucket
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/patch/{spec}
  tags: Repositories, Username, Repo, Slug, Patch, Spec
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpatchspec-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpatchspec-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Patch Spec
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug patch spec
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/patch/{spec}
  tags: Repositories, Username, Repo, Slug, Patch, Spec
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpatchspec-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpatchspec-parameters-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Pipelines
  x-api-slug: bitbucket
  description: Get repositories username repo slug pipelines
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pipelines/
  tags: Repositories, Username, Repo, Slug, Pipelines
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelines-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelines-get-openapi.md
- name: Bitbucket Add Repositories Username Repo Slug Pipelines
  x-api-slug: bitbucket
  description: "Endpoint to create and initiate a pipeline. \nThere are a couple of
    different options to initiate a pipeline, where the payload of the request will
    determine which type of pipeline will be instantiated.\n# Trigger a Pipeline for
    a branch or tag\nOne way to trigger pipelines is by specifying the reference for
    which you want to trigger a pipeline (e.g. a branch or tag). \nThe specified reference
    will be used to determine which pipeline definition from the `bitbucket-pipelines.yml`
    file will be applied to initiate the pipeline. The pipeline will then do a clone
    of the repository and checkout the latest revision of the specified reference.\n\n###
    Example\n\n```\n$ curl -X POST -is -u username:password \\\n  -H 'Content-Type:
    application/json' \\\n https://api.bitbucket.org/2.0/repositories/jeroendr/meat-demo2/pipelines/
    \\\n  -d '\n  {\n    \"target\": {\n      \"ref_type\": \"branch\", \n      \"type\":
    \"pipeline_ref_target\", \n      \"ref_name\": \"master\"\n    }\n  }'\n```\n#
    Trigger a Pipeline for a commit on a branch or tag\nYou can initiate a pipeline
    for a specific commit and in the context of a specified reference (e.g. a branch,
    tag or bookmark).\nThe specified reference will be used to determine which pipeline
    definition from the bitbucket-pipelines.yml file will be applied to initiate the
    pipeline. The pipeline will clone the repository and then do a checkout the specified
    reference. \n\nThe following reference types are supported:\n\n* `branch` \n*
    `named_branch`\n* `bookmark` \n * `tag`\n\n### Example\n\n```\n$ curl -X POST
    -is -u username:password \\\n  -H 'Content-Type: application/json' \\\n  https://api.bitbucket.org/2.0/repositories/jeroendr/meat-demo2/pipelines/
    \\\n  -d '\n  {\n    \"target\": {\n      \"commit\": {\n        \"type\": \"commit\",
    \n        \"hash\": \"ce5b7431602f7cbba007062eeb55225c6e18e956\"\n      }, \n
    \     \"ref_type\": \"branch\", \n      \"type\": \"pipeline_ref_target\", \n
    \     \"ref_name\": \"master\"\n    }\n  }'\n```\n# Trigger a specific pipeline
    definition for a commit\nYou can trigger a specific pipeline that is defined in
    your `bitbucket-pipelines.yml` file for a specific commit. \nIn addition to the
    commit revision, you specify the type and pattern of the selector that identifies
    the pipeline definition. The resulting pipeline will then clone the repository
    and checkout the specified revision.\n\n### Example\n\n```\n$ curl -X POST -is
    -u username:password \\\n  -H 'Content-Type: application/json' \\\n https://api.bitbucket.org/2.0/repositories/jeroendr/meat-demo2/pipelines/
    \\\n -d '\n  {\n     \"target\": {\n      \"commit\": {\n         \"hash\":\"a3c4e02c9a3755eccdc3764e6ea13facdf30f923\",\n
    \        \"type\":\"commit\"\n       },\n        \"selector\": {\n           \"type\":\"custom\",\n
    \             \"pattern\":\"Deploy to production\"\n          },\n        \"type\":\"pipeline_commit_target\"\n
    \  }\n  }'\n```\n# Trigger a specific pipeline definition for a commit on a branch
    or tag\nYou can trigger a specific pipeline that is defined in your `bitbucket-pipelines.yml`
    file for a specific commit in the context of a specified reference. \nIn addition
    to the commit revision, you specify the type and pattern of the selector that
    identifies the pipeline definition, as well as the reference information. The
    resulting pipeline will then clone the repository a checkout the specified reference.\n\n###
    Example\n\n```\n$ curl -X POST -is -u username:password \\\n  -H 'Content-Type:
    application/json' \\\n https://api.bitbucket.org/2.0/repositories/jeroendr/meat-demo2/pipelines/
    \\\n -d '\n  {\n     \"target\": {\n      \"commit\": {\n         \"hash\":\"a3c4e02c9a3755eccdc3764e6ea13facdf30f923\",\n
    \        \"type\":\"commit\"\n       },\n       \"selector\": {\n          \"type\":
    \"custom\",\n          \"pattern\": \"Deploy to production\"\n       },\n       \"type\":
    \"pipeline_ref_target\",\n       \"ref_name\": \"master\",\n       \"ref_type\":
    \"branch\"\n     }\n  }'\n```"
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pipelines/
  tags: Repositories, Username, Repo, Slug, Pipelines
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelines-post-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Pipelines Pipeline Uu
  x-api-slug: bitbucket
  description: Get repositories username repo slug pipelines pipeline uu
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pipelines/{pipeline_uuid}
  tags: Repositories, Username, Repo, Slug, Pipelines, Pipeline, Uu
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelinespipeline-uuid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelinespipeline-uuid-get-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Pipelines Pipeline Uu Steps
  x-api-slug: bitbucket
  description: Get repositories username repo slug pipelines pipeline uu steps
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pipelines/{pipeline_uuid}/steps/
  tags: Repositories, Username, Repo, Slug, Pipelines, Pipeline, Uu, Steps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelinespipeline-uuidsteps-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelinespipeline-uuidsteps-get-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Pipelines Pipeline Uu Steps
    Step Uu
  x-api-slug: bitbucket
  description: Get repositories username repo slug pipelines pipeline uu steps step
    uu
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pipelines/{pipeline_uuid}/steps/{step_uuid}
  tags: Repositories, Username, Repo, Slug, Pipelines, Pipeline, Uu, Steps, Step,
    Uu
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelinespipeline-uuidstepsstep-uuid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelinespipeline-uuidstepsstep-uuid-get-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Pipelines Pipeline Uu Steps
    Step Uu Log
  x-api-slug: bitbucket
  description: |-
    Retrieve the log file for a given step of a pipeline.

    This endpoint supports (and encourages!) the use of [HTTP Range requests](https://tools.ietf.org/html/rfc7233) to deal with potentially very large log files.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pipelines/{pipeline_uuid}/steps/{step_uuid}/log
  tags: Repositories, Username, Repo, Slug, Pipelines, Pipeline, Uu, Steps, Step,
    Uu, Log
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelinespipeline-uuidstepsstep-uuidlog-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelinespipeline-uuidstepsstep-uuidlog-get-openapi.md
- name: Bitbucket Add Repositories Username Repo Slug Pipelines Pipeline Uu Stoppipeline
  x-api-slug: bitbucket
  description: Signal the stop of a pipeline and all of its steps that not have completed
    yet.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pipelines/{pipeline_uuid}/stopPipeline
  tags: Repositories, Username, Repo, Slug, Pipelines, Pipeline, Uu, Stoppipeline
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelinespipeline-uuidstoppipeline-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelinespipeline-uuidstoppipeline-post-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Pipelines Config
  x-api-slug: bitbucket
  description: Get repositories username repo slug pipelines config
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pipelines_config
  tags: Repositories, Username, Repo, Slug, Pipelines, Config
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelines-config-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelines-config-get-openapi.md
- name: Bitbucket Update Repositories Username Repo Slug Pipelines Config
  x-api-slug: bitbucket
  description: Update the pipelines configuration for a repository.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pipelines_config
  tags: Repositories, Username, Repo, Slug, Pipelines, Config
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelines-config-put-openapi.md
- name: Bitbucket Delete Repositories Username Repo Slug Pipelines Config Ssh Key
    Pair
  x-api-slug: bitbucket
  description: Delete repositories username repo slug pipelines config ssh key pair
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pipelines_config/ssh/key_pair
  tags: Repositories, Username, Repo, Slug, Pipelines, Config, Ssh, Key, Pair
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelines-configsshkey-pair-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelines-configsshkey-pair-delete-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Pipelines Config Ssh Key Pair
  x-api-slug: bitbucket
  description: Retrieve the repository SSH key pair excluding the SSH private key.
    The private key is a write only field and will never be exposed in the logs or
    the REST API.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pipelines_config/ssh/key_pair
  tags: Repositories, Username, Repo, Slug, Pipelines, Config, Ssh, Key, Pair
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelines-configsshkey-pair-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelines-configsshkey-pair-get-openapi.md
- name: Bitbucket Update Repositories Username Repo Slug Pipelines Config Ssh Key
    Pair
  x-api-slug: bitbucket
  description: Create or update the repository SSH key pair. The private key will
    be set as a default SSH identity in your build container.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pipelines_config/ssh/key_pair
  tags: Repositories, Username, Repo, Slug, Pipelines, Config, Ssh, Key, Pair
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelines-configsshkey-pair-put-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Pipelines Config Ssh Known Hosts
  x-api-slug: bitbucket
  description: Get repositories username repo slug pipelines config ssh known hosts
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pipelines_config/ssh/known_hosts/
  tags: Repositories, Username, Repo, Slug, Pipelines, Config, Ssh, Known, Hosts
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelines-configsshknown-hosts-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelines-configsshknown-hosts-get-openapi.md
- name: Bitbucket Add Repositories Username Repo Slug Pipelines Config Ssh Known Hosts
  x-api-slug: bitbucket
  description: Post repositories username repo slug pipelines config ssh known hosts
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pipelines_config/ssh/known_hosts/
  tags: Repositories, Username, Repo, Slug, Pipelines, Config, Ssh, Known, Hosts
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelines-configsshknown-hosts-post-openapi.md
- name: Bitbucket Delete Repositories Username Repo Slug Pipelines Config Ssh Known
    Hosts Known Host Uu
  x-api-slug: bitbucket
  description: Delete repositories username repo slug pipelines config ssh known hosts
    known host uu
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pipelines_config/ssh/known_hosts/{known_host_uuid}
  tags: Repositories, Username, Repo, Slug, Pipelines, Config, Ssh, Known, Hosts,
    Known, Host, Uu
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelines-configsshknown-hostsknown-host-uuid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelines-configsshknown-hostsknown-host-uuid-delete-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Pipelines Config Ssh Known Hosts
    Known Host Uu
  x-api-slug: bitbucket
  description: Get repositories username repo slug pipelines config ssh known hosts
    known host uu
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pipelines_config/ssh/known_hosts/{known_host_uuid}
  tags: Repositories, Username, Repo, Slug, Pipelines, Config, Ssh, Known, Hosts,
    Known, Host, Uu
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelines-configsshknown-hostsknown-host-uuid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelines-configsshknown-hostsknown-host-uuid-get-openapi.md
- name: Bitbucket Update Repositories Username Repo Slug Pipelines Config Ssh Known
    Hosts Known Host Uu
  x-api-slug: bitbucket
  description: Put repositories username repo slug pipelines config ssh known hosts
    known host uu
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pipelines_config/ssh/known_hosts/{known_host_uuid}
  tags: Repositories, Username, Repo, Slug, Pipelines, Config, Ssh, Known, Hosts,
    Known, Host, Uu
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelines-configsshknown-hostsknown-host-uuid-put-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Pipelines Config Variables
  x-api-slug: bitbucket
  description: Get repositories username repo slug pipelines config variables
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pipelines_config/variables/
  tags: Repositories, Username, Repo, Slug, Pipelines, Config, Variables
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelines-configvariables-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelines-configvariables-get-openapi.md
- name: Bitbucket Add Repositories Username Repo Slug Pipelines Config Variables
  x-api-slug: bitbucket
  description: Post repositories username repo slug pipelines config variables
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pipelines_config/variables/
  tags: Repositories, Username, Repo, Slug, Pipelines, Config, Variables
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelines-configvariables-post-openapi.md
- name: Bitbucket Delete Repositories Username Repo Slug Pipelines Config Variables
    Variable Uu
  x-api-slug: bitbucket
  description: Delete repositories username repo slug pipelines config variables variable
    uu
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pipelines_config/variables/{variable_uuid}
  tags: Repositories, Username, Repo, Slug, Pipelines, Config, Variables, Variable,
    Uu
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelines-configvariablesvariable-uuid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelines-configvariablesvariable-uuid-delete-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Pipelines Config Variables Variable
    Uu
  x-api-slug: bitbucket
  description: Get repositories username repo slug pipelines config variables variable
    uu
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pipelines_config/variables/{variable_uuid}
  tags: Repositories, Username, Repo, Slug, Pipelines, Config, Variables, Variable,
    Uu
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelines-configvariablesvariable-uuid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelines-configvariablesvariable-uuid-get-openapi.md
- name: Bitbucket Update Repositories Username Repo Slug Pipelines Config Variables
    Variable Uu
  x-api-slug: bitbucket
  description: Put repositories username repo slug pipelines config variables variable
    uu
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pipelines_config/variables/{variable_uuid}
  tags: Repositories, Username, Repo, Slug, Pipelines, Config, Variables, Variable,
    Uu
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpipelines-configvariablesvariable-uuid-put-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Pullrequests
  x-api-slug: bitbucket
  description: |-
    Returns a paginated list of all pull requests on the specified
    repository. By default only open pull requests are returned. This can
    be controlled using the `state` query parameter. To retrieve pull
    requests that are in one of multiple states, repeat the `state`
    parameter for each individual state.

    This endpoint also supports filtering and sorting of the results. See
    [filtering and sorting](../../../../meta/filtering) for more details.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pullrequests
  tags: Repositories, Username, Repo, Slug, Pullrequests
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequests-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequests-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Pullrequests
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug pullrequests
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pullrequests
  tags: Repositories, Username, Repo, Slug, Pullrequests
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequests-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequests-parameters-openapi.md
- name: Bitbucket Add Repositories Username Repo Slug Pullrequests
  x-api-slug: bitbucket
  description: Post repositories username repo slug pullrequests
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pullrequests
  tags: Repositories, Username, Repo, Slug, Pullrequests
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequests-post-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Pullrequests Activity
  x-api-slug: bitbucket
  description: |-
    Returns a paginated list of the pull request's activity log.

    This includes comments that were made by the reviewers, updates and
    approvals.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pullrequests/activity
  tags: Repositories, Username, Repo, Slug, Pullrequests, Activity
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestsactivity-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestsactivity-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Pullrequests Activity
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug pullrequests activity
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pullrequests/activity
  tags: Repositories, Username, Repo, Slug, Pullrequests, Activity
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestsactivity-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestsactivity-parameters-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Pullrequests Pull Request
  x-api-slug: bitbucket
  description: Get repositories username repo slug pullrequests pull request
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}
  tags: Repositories, Username, Repo, Slug, Pullrequests, Pull, Request
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-id-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Pullrequests Pull Request
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug pullrequests pull request
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}
  tags: Repositories, Username, Repo, Slug, Pullrequests, Pull, Request
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-id-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-id-parameters-openapi.md
- name: Bitbucket Update Repositories Username Repo Slug Pullrequests Pull Request
  x-api-slug: bitbucket
  description: |-
    Mutates the specified pull request.

    This can be used to change the pull request's branches or description.

    Only open pull requests can be mutated.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}
  tags: Repositories, Username, Repo, Slug, Pullrequests, Pull, Request
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-id-put-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Pullrequests Pull Request  Activity
  x-api-slug: bitbucket
  description: |-
    Returns a paginated list of the pull request's activity log.

    This includes comments that were made by the reviewers, updates and
    approvals.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}/activity
  tags: Repositories, Username, Repo, Slug, Pullrequests, Pull, Request, , Activity
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idactivity-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idactivity-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Pullrequests Pull Request  Activity
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug pullrequests pull request  activity
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}/activity
  tags: Repositories, Username, Repo, Slug, Pullrequests, Pull, Request, , Activity
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idactivity-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idactivity-parameters-openapi.md
- name: Bitbucket Delete Repositories Username Repo Slug Pullrequests Pull Request  Approve
  x-api-slug: bitbucket
  description: Delete repositories username repo slug pullrequests pull request  approve
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}/approve
  tags: Repositories, Username, Repo, Slug, Pullrequests, Pull, Request, , Approve
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idapprove-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idapprove-delete-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Pullrequests Pull Request  Approve
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug pullrequests pull request  approve
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}/approve
  tags: Repositories, Username, Repo, Slug, Pullrequests, Pull, Request, , Approve
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idapprove-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idapprove-parameters-openapi.md
- name: Bitbucket Add Repositories Username Repo Slug Pullrequests Pull Request  Approve
  x-api-slug: bitbucket
  description: Post repositories username repo slug pullrequests pull request  approve
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}/approve
  tags: Repositories, Username, Repo, Slug, Pullrequests, Pull, Request, , Approve
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idapprove-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idapprove-post-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Pullrequests Pull Request  Comments
  x-api-slug: bitbucket
  description: |-
    Returns a paginated list of the pull request's comments.

    This includes both global, inline comments and replies.

    The default sorting is oldest to newest and can be overridden with
    the `sort` query parameter.

    This endpoint also supports filtering and sorting of the results. See
    [filtering and sorting](../../../../../../meta/filtering) for more
    details.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}/comments
  tags: Repositories, Username, Repo, Slug, Pullrequests, Pull, Request, , Comments
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idcomments-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idcomments-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Pullrequests Pull Request  Comments
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug pullrequests pull request  comments
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}/comments
  tags: Repositories, Username, Repo, Slug, Pullrequests, Pull, Request, , Comments
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idcomments-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idcomments-parameters-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Pullrequests Pull Request  Comments
    Comment
  x-api-slug: bitbucket
  description: Get repositories username repo slug pullrequests pull request  comments
    comment
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}/comments/{comment_id}
  tags: Repositories, Username, Repo, Slug, Pullrequests, Pull, Request, , Comments,
    Comment
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idcommentscomment-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idcommentscomment-id-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Pullrequests Pull Request  Comments
    Comment
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug pullrequests pull request  comments
    comment
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}/comments/{comment_id}
  tags: Repositories, Username, Repo, Slug, Pullrequests, Pull, Request, , Comments,
    Comment
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idcommentscomment-id-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idcommentscomment-id-parameters-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Pullrequests Pull Request  Commits
  x-api-slug: bitbucket
  description: |-
    Returns a paginated list of the pull request's commits.

    These are the commits that are being merged into the destination
    branch when the pull requests gets accepted.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}/commits
  tags: Repositories, Username, Repo, Slug, Pullrequests, Pull, Request, , Commits
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idcommits-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idcommits-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Pullrequests Pull Request  Commits
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug pullrequests pull request  commits
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}/commits
  tags: Repositories, Username, Repo, Slug, Pullrequests, Pull, Request, , Commits
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idcommits-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idcommits-parameters-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Pullrequests Pull Request  Decline
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug pullrequests pull request  decline
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}/decline
  tags: Repositories, Username, Repo, Slug, Pullrequests, Pull, Request, , Decline
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-iddecline-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-iddecline-parameters-openapi.md
- name: Bitbucket Add Repositories Username Repo Slug Pullrequests Pull Request  Decline
  x-api-slug: bitbucket
  description: Post repositories username repo slug pullrequests pull request  decline
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}/decline
  tags: Repositories, Username, Repo, Slug, Pullrequests, Pull, Request, , Decline
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-iddecline-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-iddecline-post-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Pullrequests Pull Request  Diff
  x-api-slug: bitbucket
  description: Get repositories username repo slug pullrequests pull request  diff
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}/diff
  tags: Repositories, Username, Repo, Slug, Pullrequests, Pull, Request, , Diff
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-iddiff-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-iddiff-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Pullrequests Pull Request  Diff
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug pullrequests pull request  diff
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}/diff
  tags: Repositories, Username, Repo, Slug, Pullrequests, Pull, Request, , Diff
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-iddiff-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-iddiff-parameters-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Pullrequests Pull Request  Merge
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug pullrequests pull request  merge
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}/merge
  tags: Repositories, Username, Repo, Slug, Pullrequests, Pull, Request, , Merge
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idmerge-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idmerge-parameters-openapi.md
- name: Bitbucket Add Repositories Username Repo Slug Pullrequests Pull Request  Merge
  x-api-slug: bitbucket
  description: Post repositories username repo slug pullrequests pull request  merge
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}/merge
  tags: Repositories, Username, Repo, Slug, Pullrequests, Pull, Request, , Merge
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idmerge-post-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Pullrequests Pull Request  Patch
  x-api-slug: bitbucket
  description: Get repositories username repo slug pullrequests pull request  patch
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}/patch
  tags: Repositories, Username, Repo, Slug, Pullrequests, Pull, Request, , Patch
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idpatch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idpatch-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Pullrequests Pull Request  Patch
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug pullrequests pull request  patch
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}/patch
  tags: Repositories, Username, Repo, Slug, Pullrequests, Pull, Request, , Patch
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idpatch-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idpatch-parameters-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Pullrequests Pull Request  Statuses
  x-api-slug: bitbucket
  description: Get repositories username repo slug pullrequests pull request  statuses
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}/statuses
  tags: Repositories, Username, Repo, Slug, Pullrequests, Pull, Request, , Statuses
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idstatuses-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idstatuses-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Pullrequests Pull Request  Statuses
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug pullrequests pull request  statuses
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/pullrequests/{pull_request_id}/statuses
  tags: Repositories, Username, Repo, Slug, Pullrequests, Pull, Request, , Statuses
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idstatuses-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugpullrequestspull-request-idstatuses-parameters-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Refs
  x-api-slug: bitbucket
  description: Get repositories username repo slug refs
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/refs
  tags: Repositories, Username, Repo, Slug, Refs
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugrefs-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugrefs-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Refs
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug refs
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/refs
  tags: Repositories, Username, Repo, Slug, Refs
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugrefs-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugrefs-parameters-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Refs Branches
  x-api-slug: bitbucket
  description: Get repositories username repo slug refs branches
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/refs/branches
  tags: Repositories, Username, Repo, Slug, Refs, Branches
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugrefsbranches-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugrefsbranches-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Refs Branches
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug refs branches
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/refs/branches
  tags: Repositories, Username, Repo, Slug, Refs, Branches
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugrefsbranches-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugrefsbranches-parameters-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Refs Branches Name
  x-api-slug: bitbucket
  description: Get repositories username repo slug refs branches name
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/refs/branches/{name}
  tags: Repositories, Username, Repo, Slug, Refs, Branches, Name
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugrefsbranchesname-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugrefsbranchesname-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Refs Branches Name
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug refs branches name
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/refs/branches/{name}
  tags: Repositories, Username, Repo, Slug, Refs, Branches, Name
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugrefsbranchesname-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugrefsbranchesname-parameters-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Refs Tags
  x-api-slug: bitbucket
  description: Get repositories username repo slug refs tags
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/refs/tags
  tags: Repositories, Username, Repo, Slug, Refs, Tags
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugrefstags-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugrefstags-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Refs Tags
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug refs tags
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/refs/tags
  tags: Repositories, Username, Repo, Slug, Refs, Tags
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugrefstags-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugrefstags-parameters-openapi.md
- name: Bitbucket Add Repositories Username Repo Slug Refs Tags
  x-api-slug: bitbucket
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/refs/tags
  tags: Repositories, Username, Repo, Slug, Refs, Tags
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugrefstags-post-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Refs Tags Name
  x-api-slug: bitbucket
  description: Get repositories username repo slug refs tags name
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/refs/tags/{name}
  tags: Repositories, Username, Repo, Slug, Refs, Tags, Name
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugrefstagsname-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugrefstagsname-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Refs Tags Name
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug refs tags name
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/refs/tags/{name}
  tags: Repositories, Username, Repo, Slug, Refs, Tags, Name
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugrefstagsname-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugrefstagsname-parameters-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Src Node Path
  x-api-slug: bitbucket
  description: Get repositories username repo slug src node path
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/src/{node}/{path}
  tags: Repositories, Username, Repo, Slug, Src, Node, Path
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugsrcnodepath-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugsrcnodepath-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Src Node Path
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug src node path
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/src/{node}/{path}
  tags: Repositories, Username, Repo, Slug, Src, Node, Path
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugsrcnodepath-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugsrcnodepath-parameters-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Versions
  x-api-slug: bitbucket
  description: |-
    Returns the versions that have been defined in the issue tracker.

    This resource is only available on repositories that have the issue
    tracker enabled.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/versions
  tags: Repositories, Username, Repo, Slug, Versions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugversions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugversions-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Versions
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug versions
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/versions
  tags: Repositories, Username, Repo, Slug, Versions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugversions-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugversions-parameters-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Versions Version
  x-api-slug: bitbucket
  description: Get repositories username repo slug versions version
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/versions/{version_id}
  tags: Repositories, Username, Repo, Slug, Versions, Version
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugversionsversion-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugversionsversion-id-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Versions Version
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug versions version
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/versions/{version_id}
  tags: Repositories, Username, Repo, Slug, Versions, Version
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugversionsversion-id-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugversionsversion-id-parameters-openapi.md
- name: Bitbucket Get Repositories Username Repo Slug Watchers
  x-api-slug: bitbucket
  description: |-
    Returns a paginated list of all the watchers on the specified
    repository.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/watchers
  tags: Repositories, Username, Repo, Slug, Watchers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugwatchers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugwatchers-get-openapi.md
- name: Bitbucket Parameters Repositories Username Repo Slug Watchers
  x-api-slug: bitbucket
  description: Parameters repositories username repo slug watchers
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//repositories/{username}/{repo_slug}/watchers
  tags: Repositories, Username, Repo, Slug, Watchers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugwatchers-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/repositoriesusernamerepo-slugwatchers-parameters-openapi.md
- name: Bitbucket Get Snippets Username
  x-api-slug: bitbucket
  description: |-
    Identical to `/snippets`, except that the result is further filtered
    by the snippet owner and only those that are owned by `{username}` are
    returned.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}
  tags: Snippets, Username
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusername-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusername-get-openapi.md
- name: Bitbucket Parameters Snippets Username
  x-api-slug: bitbucket
  description: Parameters snippets username
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}
  tags: Snippets, Username
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusername-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusername-parameters-openapi.md
- name: Bitbucket Add Snippets Username
  x-api-slug: bitbucket
  description: |-
    Identical to `/snippets`, except that the new snippet will be
    created under the account specified in the path parameter `{username}`.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}
  tags: Snippets, Username
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusername-post-openapi.md
- name: Bitbucket Delete Snippets Username Encoded
  x-api-slug: bitbucket
  description: Deletes a snippet and returns an empty response.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}/{encoded_id}
  tags: Snippets, Username, Encoded
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-id-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-id-delete-openapi.md
- name: Bitbucket Get Snippets Username Encoded
  x-api-slug: bitbucket
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}/{encoded_id}
  tags: Snippets, Username, Encoded
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-id-get-openapi.md
- name: Bitbucket Parameters Snippets Username Encoded
  x-api-slug: bitbucket
  description: Parameters snippets username encoded
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}/{encoded_id}
  tags: Snippets, Username, Encoded
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-id-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-id-parameters-openapi.md
- name: Bitbucket Update Snippets Username Encoded
  x-api-slug: bitbucket
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
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}/{encoded_id}
  tags: Snippets, Username, Encoded
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-id-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-id-put-openapi.md
- name: Bitbucket Get Snippets Username Encoded  Comments
  x-api-slug: bitbucket
  description: |-
    Used to retrieve a paginated list of all comments for a specific
    snippet.

    This resource works identical to commit and pull request comments.

    The default sorting is oldest to newest and can be overridden with
    the `sort` query parameter.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}/{encoded_id}/comments
  tags: Snippets, Username, Encoded, , Comments
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idcomments-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idcomments-get-openapi.md
- name: Bitbucket Parameters Snippets Username Encoded  Comments
  x-api-slug: bitbucket
  description: Parameters snippets username encoded  comments
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}/{encoded_id}/comments
  tags: Snippets, Username, Encoded, , Comments
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idcomments-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idcomments-parameters-openapi.md
- name: Bitbucket Add Snippets Username Encoded  Comments
  x-api-slug: bitbucket
  description: |-
    Creates a new comment.

    The only required field in the body is `content.raw`.

    To create a threaded reply to an existing comment, include `parent.id`.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}/{encoded_id}/comments
  tags: Snippets, Username, Encoded, , Comments
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idcomments-post-openapi.md
- name: Bitbucket Delete Snippets Username Encoded  Comments Comment
  x-api-slug: bitbucket
  description: |-
    Deletes a snippet comment.

    Comments can only be removed by their author.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}/{encoded_id}/comments/{comment_id}
  tags: Snippets, Username, Encoded, , Comments, Comment
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idcommentscomment-id-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idcommentscomment-id-delete-openapi.md
- name: Bitbucket Get Snippets Username Encoded  Comments Comment
  x-api-slug: bitbucket
  description: Get snippets username encoded  comments comment
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}/{encoded_id}/comments/{comment_id}
  tags: Snippets, Username, Encoded, , Comments, Comment
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idcommentscomment-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idcommentscomment-id-get-openapi.md
- name: Bitbucket Parameters Snippets Username Encoded  Comments Comment
  x-api-slug: bitbucket
  description: Parameters snippets username encoded  comments comment
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}/{encoded_id}/comments/{comment_id}
  tags: Snippets, Username, Encoded, , Comments, Comment
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idcommentscomment-id-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idcommentscomment-id-parameters-openapi.md
- name: Bitbucket Update Snippets Username Encoded  Comments Comment
  x-api-slug: bitbucket
  description: |-
    Updates a comment.

    Comments can only be updated by their author.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}/{encoded_id}/comments/{comment_id}
  tags: Snippets, Username, Encoded, , Comments, Comment
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idcommentscomment-id-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idcommentscomment-id-put-openapi.md
- name: Bitbucket Get Snippets Username Encoded  Commits
  x-api-slug: bitbucket
  description: Returns the changes (commits) made on this snippet.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}/{encoded_id}/commits
  tags: Snippets, Username, Encoded, , Commits
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idcommits-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idcommits-get-openapi.md
- name: Bitbucket Parameters Snippets Username Encoded  Commits
  x-api-slug: bitbucket
  description: Parameters snippets username encoded  commits
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}/{encoded_id}/commits
  tags: Snippets, Username, Encoded, , Commits
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idcommits-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idcommits-parameters-openapi.md
- name: Bitbucket Get Snippets Username Encoded  Commits Revision
  x-api-slug: bitbucket
  description: Get snippets username encoded  commits revision
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}/{encoded_id}/commits/{revision}
  tags: Snippets, Username, Encoded, , Commits, Revision
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idcommitsrevision-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idcommitsrevision-get-openapi.md
- name: Bitbucket Parameters Snippets Username Encoded  Commits Revision
  x-api-slug: bitbucket
  description: Parameters snippets username encoded  commits revision
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}/{encoded_id}/commits/{revision}
  tags: Snippets, Username, Encoded, , Commits, Revision
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idcommitsrevision-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idcommitsrevision-parameters-openapi.md
- name: Bitbucket Delete Snippets Username Encoded  Watch
  x-api-slug: bitbucket
  description: |-
    Used to stop watching a specific snippet. Returns 204 (No Content)
    to indicate success.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}/{encoded_id}/watch
  tags: Snippets, Username, Encoded, , Watch
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idwatch-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idwatch-delete-openapi.md
- name: Bitbucket Get Snippets Username Encoded  Watch
  x-api-slug: bitbucket
  description: |-
    Used to check if the current user is watching a specific snippet.

    Returns 204 (No Content) if the user is watching the snippet and 404 if
    not.

    Hitting this endpoint anonymously always returns a 404.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}/{encoded_id}/watch
  tags: Snippets, Username, Encoded, , Watch
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idwatch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idwatch-get-openapi.md
- name: Bitbucket Parameters Snippets Username Encoded  Watch
  x-api-slug: bitbucket
  description: Parameters snippets username encoded  watch
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}/{encoded_id}/watch
  tags: Snippets, Username, Encoded, , Watch
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idwatch-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idwatch-parameters-openapi.md
- name: Bitbucket Update Snippets Username Encoded  Watch
  x-api-slug: bitbucket
  description: Used to start watching a specific snippet. Returns 204 (No Content).
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}/{encoded_id}/watch
  tags: Snippets, Username, Encoded, , Watch
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idwatch-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idwatch-put-openapi.md
- name: Bitbucket Get Snippets Username Encoded  Watchers
  x-api-slug: bitbucket
  description: Returns a paginated list of all users watching a specific snippet.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}/{encoded_id}/watchers
  tags: Snippets, Username, Encoded, , Watchers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idwatchers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idwatchers-get-openapi.md
- name: Bitbucket Parameters Snippets Username Encoded  Watchers
  x-api-slug: bitbucket
  description: Parameters snippets username encoded  watchers
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}/{encoded_id}/watchers
  tags: Snippets, Username, Encoded, , Watchers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idwatchers-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idwatchers-parameters-openapi.md
- name: Bitbucket Delete Snippets Username Encoded  Node
  x-api-slug: bitbucket
  description: |-
    Deletes the snippet.

    Note that this only works for versioned URLs that point to the latest
    commit of the snippet. Pointing to an older commit results in a 405
    status code.

    To delete a snippet, regardless of whether or not concurrent changes
    are being made to it, use `DELETE /snippets/{encoded_id}` instead.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}/{encoded_id}/{node_id}
  tags: Snippets, Username, Encoded, , Node
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idnode-id-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idnode-id-delete-openapi.md
- name: Bitbucket Get Snippets Username Encoded  Node
  x-api-slug: bitbucket
  description: |-
    Identical to `GET /snippets/encoded_id`, except that this endpoint
    can be used to retrieve the contents of the snippet as it was at an
    older revision, while `/snippets/encoded_id` always returns the
    snippet's current revision.

    Note that only the snippet's file contents are versioned, not its
    meta data properties like the title.

    Other than that, the two endpoints are identical in behavior.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}/{encoded_id}/{node_id}
  tags: Snippets, Username, Encoded, , Node
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idnode-id-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idnode-id-get-openapi.md
- name: Bitbucket Parameters Snippets Username Encoded  Node
  x-api-slug: bitbucket
  description: Parameters snippets username encoded  node
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}/{encoded_id}/{node_id}
  tags: Snippets, Username, Encoded, , Node
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idnode-id-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idnode-id-parameters-openapi.md
- name: Bitbucket Update Snippets Username Encoded  Node
  x-api-slug: bitbucket
  description: |-
    Identical to `UPDATE /snippets/encoded_id`, except that this endpoint
    takes an explicit commit revision. Only the snippet's "HEAD"/"tip"
    (most recent) version can be updated and requests on all other,
    older revisions fail by returning a 405 status.

    Usage of this endpoint over the unrestricted `/snippets/encoded_id`
    could be desired if the caller wants to be sure no concurrent
    modifications have taken place between the moment of the UPDATE
    request and the original GET.

    This can be considered a so-called "Compare And Swap", or CAS
    operation.

    Other than that, the two endpoints are identical in behavior.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}/{encoded_id}/{node_id}
  tags: Snippets, Username, Encoded, , Node
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idnode-id-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idnode-id-put-openapi.md
- name: Bitbucket Get Snippets Username Encoded  Node  Files Path
  x-api-slug: bitbucket
  description: |-
    Retrieves the raw contents of a specific file in the snippet. The
    `Content-Disposition` header will be "attachment" to avoid issues with
    malevolent executable files.

    The file's mime type is derived from its filename and returned in the
    `Content-Type` header.

    Note that for text files, no character encoding is included as part of
    the content type.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}/{encoded_id}/{node_id}/files/{path}
  tags: Snippets, Username, Encoded, , Node, , Files, Path
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idnode-idfilespath-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idnode-idfilespath-get-openapi.md
- name: Bitbucket Parameters Snippets Username Encoded  Node  Files Path
  x-api-slug: bitbucket
  description: Parameters snippets username encoded  node  files path
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}/{encoded_id}/{node_id}/files/{path}
  tags: Snippets, Username, Encoded, , Node, , Files, Path
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idnode-idfilespath-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idnode-idfilespath-parameters-openapi.md
- name: Bitbucket Get Snippets Username Encoded  Revision Diff
  x-api-slug: bitbucket
  description: |-
    Returns the diff of the specified commit against its first parent.

    Note that this resource is different in functionality from the `patch`
    resource.

    The differences between a diff and a patch are:

    * patches have a commit header with the username, message, etc
    * diffs support the optional `path=foo/bar.py` query param to filter the
      diff to just that one file diff (not supported for patches)
    * for a merge, the diff will show the diff between the merge commit and
      its first parent (identical to how PRs work), while patch returns a
      response containing separate patches for each commit on the second
      parent's ancestry, up to the oldest common ancestor (identical to
      its reachability).

    Note that the character encoding of the contents of the diff is
    unspecified as Git and Mercurial do not track this, making it hard for
    Bitbucket to reliably determine this.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}/{encoded_id}/{revision}/diff
  tags: Snippets, Username, Encoded, , Revision, Diff
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idrevisiondiff-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idrevisiondiff-get-openapi.md
- name: Bitbucket Parameters Snippets Username Encoded  Revision Diff
  x-api-slug: bitbucket
  description: Parameters snippets username encoded  revision diff
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}/{encoded_id}/{revision}/diff
  tags: Snippets, Username, Encoded, , Revision, Diff
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idrevisiondiff-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idrevisiondiff-parameters-openapi.md
- name: Bitbucket Get Snippets Username Encoded  Revision Patch
  x-api-slug: bitbucket
  description: |-
    Returns the patch of the specified commit against its first
    parent.

    Note that this resource is different in functionality from the `diff`
    resource.

    The differences between a diff and a patch are:

    * patches have a commit header with the username, message, etc
    * diffs support the optional `path=foo/bar.py` query param to filter the
      diff to just that one file diff (not supported for patches)
    * for a merge, the diff will show the diff between the merge commit and
      its first parent (identical to how PRs work), while patch returns a
      response containing separate patches for each commit on the second
      parent's ancestry, up to the oldest common ancestor (identical to
      its reachability).

    Note that the character encoding of the contents of the patch is
    unspecified as Git and Mercurial do not track this, making it hard for
    Bitbucket to reliably determine this.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}/{encoded_id}/{revision}/patch
  tags: Snippets, Username, Encoded, , Revision, Patch
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idrevisionpatch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idrevisionpatch-get-openapi.md
- name: Bitbucket Parameters Snippets Username Encoded  Revision Patch
  x-api-slug: bitbucket
  description: Parameters snippets username encoded  revision patch
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//snippets/{username}/{encoded_id}/{revision}/patch
  tags: Snippets, Username, Encoded, , Revision, Patch
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idrevisionpatch-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/snippetsusernameencoded-idrevisionpatch-parameters-openapi.md
- name: Bitbucket Get Teams Username
  x-api-slug: bitbucket
  description: |-
    Gets the public information associated with a team.

    If the team's profile is private, `location`, `website` and
    `created_on` elements are omitted.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//teams/{username}
  tags: Teams, Username
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusername-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusername-get-openapi.md
- name: Bitbucket Parameters Teams Username
  x-api-slug: bitbucket
  description: Parameters teams username
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//teams/{username}
  tags: Teams, Username
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusername-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusername-parameters-openapi.md
- name: Bitbucket Get Teams Username Followers
  x-api-slug: bitbucket
  description: Returns the list of accounts that are following this team.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//teams/{username}/followers
  tags: Teams, Username, Followers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamefollowers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamefollowers-get-openapi.md
- name: Bitbucket Parameters Teams Username Followers
  x-api-slug: bitbucket
  description: Parameters teams username followers
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//teams/{username}/followers
  tags: Teams, Username, Followers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamefollowers-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamefollowers-parameters-openapi.md
- name: Bitbucket Get Teams Username Following
  x-api-slug: bitbucket
  description: Returns the list of accounts this team is following.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//teams/{username}/following
  tags: Teams, Username, Following
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamefollowing-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamefollowing-get-openapi.md
- name: Bitbucket Parameters Teams Username Following
  x-api-slug: bitbucket
  description: Parameters teams username following
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//teams/{username}/following
  tags: Teams, Username, Following
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamefollowing-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamefollowing-parameters-openapi.md
- name: Bitbucket Get Teams Username Hooks
  x-api-slug: bitbucket
  description: Returns a paginated list of webhooks installed on this team.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//teams/{username}/hooks
  tags: Teams, Username, Hooks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamehooks-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamehooks-get-openapi.md
- name: Bitbucket Parameters Teams Username Hooks
  x-api-slug: bitbucket
  description: Parameters teams username hooks
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//teams/{username}/hooks
  tags: Teams, Username, Hooks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamehooks-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamehooks-parameters-openapi.md
- name: Bitbucket Add Teams Username Hooks
  x-api-slug: bitbucket
  description: |-
    Creates a new webhook on the specified team.

    Team webhooks are fired for events from all repositories belonging to
    that team account.

    Note that only admins can install webhooks on teams.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//teams/{username}/hooks
  tags: Teams, Username, Hooks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamehooks-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamehooks-post-openapi.md
- name: Bitbucket Delete Teams Username Hooks U
  x-api-slug: bitbucket
  description: |-
    Deletes the specified webhook subscription from the given team
    account.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//teams/{username}/hooks/{uid}
  tags: Teams, Username, Hooks, U
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamehooksuid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamehooksuid-delete-openapi.md
- name: Bitbucket Get Teams Username Hooks U
  x-api-slug: bitbucket
  description: |-
    Returns the webhook with the specified id installed on the given
    team account.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//teams/{username}/hooks/{uid}
  tags: Teams, Username, Hooks, U
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamehooksuid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamehooksuid-get-openapi.md
- name: Bitbucket Parameters Teams Username Hooks U
  x-api-slug: bitbucket
  description: Parameters teams username hooks u
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//teams/{username}/hooks/{uid}
  tags: Teams, Username, Hooks, U
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamehooksuid-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamehooksuid-parameters-openapi.md
- name: Bitbucket Update Teams Username Hooks U
  x-api-slug: bitbucket
  description: |-
    Updates the specified webhook subscription.

    The following properties can be mutated:

    * `description`
    * `url`
    * `active`
    * `events`
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//teams/{username}/hooks/{uid}
  tags: Teams, Username, Hooks, U
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamehooksuid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamehooksuid-put-openapi.md
- name: Bitbucket Get Teams Username Members
  x-api-slug: bitbucket
  description: |-
    All members of a team.

    Returns all members of the specified team. Any member of any of the
    team's groups is considered a member of the team. This includes users
    in groups that may not actually have access to any of the team's
    repositories.

    Note that members using the "private profile" feature are not included.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//teams/{username}/members
  tags: Teams, Username, Members
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamemembers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamemembers-get-openapi.md
- name: Bitbucket Parameters Teams Username Members
  x-api-slug: bitbucket
  description: Parameters teams username members
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//teams/{username}/members
  tags: Teams, Username, Members
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamemembers-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamemembers-parameters-openapi.md
- name: Bitbucket Get Teams Username Pipelines Config Variables
  x-api-slug: bitbucket
  description: Get teams username pipelines config variables
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//teams/{username}/pipelines_config/variables/
  tags: Teams, Username, Pipelines, Config, Variables
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamepipelines-configvariables-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamepipelines-configvariables-get-openapi.md
- name: Bitbucket Add Teams Username Pipelines Config Variables
  x-api-slug: bitbucket
  description: Post teams username pipelines config variables
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//teams/{username}/pipelines_config/variables/
  tags: Teams, Username, Pipelines, Config, Variables
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamepipelines-configvariables-post-openapi.md
- name: Bitbucket Delete Teams Username Pipelines Config Variables Variable Uu
  x-api-slug: bitbucket
  description: Delete teams username pipelines config variables variable uu
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//teams/{username}/pipelines_config/variables/{variable_uuid}
  tags: Teams, Username, Pipelines, Config, Variables, Variable, Uu
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamepipelines-configvariablesvariable-uuid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamepipelines-configvariablesvariable-uuid-delete-openapi.md
- name: Bitbucket Get Teams Username Pipelines Config Variables Variable Uu
  x-api-slug: bitbucket
  description: Get teams username pipelines config variables variable uu
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//teams/{username}/pipelines_config/variables/{variable_uuid}
  tags: Teams, Username, Pipelines, Config, Variables, Variable, Uu
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamepipelines-configvariablesvariable-uuid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamepipelines-configvariablesvariable-uuid-get-openapi.md
- name: Bitbucket Update Teams Username Pipelines Config Variables Variable Uu
  x-api-slug: bitbucket
  description: Put teams username pipelines config variables variable uu
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//teams/{username}/pipelines_config/variables/{variable_uuid}
  tags: Teams, Username, Pipelines, Config, Variables, Variable, Uu
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamepipelines-configvariablesvariable-uuid-put-openapi.md
- name: Bitbucket Get Teams Username Repositories
  x-api-slug: bitbucket
  description: |-
    All repositories owned by a user/team. This includes private
    repositories, but filtered down to the ones that the calling user has
    access to.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//teams/{username}/repositories
  tags: Teams, Username, Repositories
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamerepositories-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamerepositories-get-openapi.md
- name: Bitbucket Parameters Teams Username Repositories
  x-api-slug: bitbucket
  description: Parameters teams username repositories
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//teams/{username}/repositories
  tags: Teams, Username, Repositories
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamerepositories-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/teamsusernamerepositories-parameters-openapi.md
- name: Bitbucket Get Users Username
  x-api-slug: bitbucket
  description: |-
    Gets the public information associated with a user account.

    If the user's profile is private, `location`, `website` and
    `created_on` elements are omitted.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//users/{username}
  tags: Users, Username
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusername-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusername-get-openapi.md
- name: Bitbucket Parameters Users Username
  x-api-slug: bitbucket
  description: Parameters users username
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//users/{username}
  tags: Users, Username
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusername-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusername-parameters-openapi.md
- name: Bitbucket Get Users Username Followers
  x-api-slug: bitbucket
  description: Returns the list of accounts that are following this team.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//users/{username}/followers
  tags: Users, Username, Followers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusernamefollowers-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusernamefollowers-get-openapi.md
- name: Bitbucket Parameters Users Username Followers
  x-api-slug: bitbucket
  description: Parameters users username followers
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//users/{username}/followers
  tags: Users, Username, Followers
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusernamefollowers-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusernamefollowers-parameters-openapi.md
- name: Bitbucket Get Users Username Following
  x-api-slug: bitbucket
  description: Returns the list of accounts this user is following.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//users/{username}/following
  tags: Users, Username, Following
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusernamefollowing-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusernamefollowing-get-openapi.md
- name: Bitbucket Parameters Users Username Following
  x-api-slug: bitbucket
  description: Parameters users username following
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//users/{username}/following
  tags: Users, Username, Following
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusernamefollowing-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusernamefollowing-parameters-openapi.md
- name: Bitbucket Get Users Username Hooks
  x-api-slug: bitbucket
  description: Returns a paginated list of webhooks installed on this user account.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//users/{username}/hooks
  tags: Users, Username, Hooks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusernamehooks-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusernamehooks-get-openapi.md
- name: Bitbucket Parameters Users Username Hooks
  x-api-slug: bitbucket
  description: Parameters users username hooks
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//users/{username}/hooks
  tags: Users, Username, Hooks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusernamehooks-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusernamehooks-parameters-openapi.md
- name: Bitbucket Add Users Username Hooks
  x-api-slug: bitbucket
  description: |-
    Creates a new webhook on the specified user account.

    Account-level webhooks are fired for events from all repositories
    belonging to that account.

    Note that one can only register webhooks on one's own account, not that
    of others.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//users/{username}/hooks
  tags: Users, Username, Hooks
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusernamehooks-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusernamehooks-post-openapi.md
- name: Bitbucket Delete Users Username Hooks U
  x-api-slug: bitbucket
  description: |-
    Deletes the specified webhook subscription from the given user
    account.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//users/{username}/hooks/{uid}
  tags: Users, Username, Hooks, U
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusernamehooksuid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusernamehooksuid-delete-openapi.md
- name: Bitbucket Get Users Username Hooks U
  x-api-slug: bitbucket
  description: |-
    Returns the webhook with the specified id installed on the given
    user account.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//users/{username}/hooks/{uid}
  tags: Users, Username, Hooks, U
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusernamehooksuid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusernamehooksuid-get-openapi.md
- name: Bitbucket Parameters Users Username Hooks U
  x-api-slug: bitbucket
  description: Parameters users username hooks u
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//users/{username}/hooks/{uid}
  tags: Users, Username, Hooks, U
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusernamehooksuid-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusernamehooksuid-parameters-openapi.md
- name: Bitbucket Update Users Username Hooks U
  x-api-slug: bitbucket
  description: |-
    Updates the specified webhook subscription.

    The following properties can be mutated:

    * `description`
    * `url`
    * `active`
    * `events`
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//users/{username}/hooks/{uid}
  tags: Users, Username, Hooks, U
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusernamehooksuid-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusernamehooksuid-put-openapi.md
- name: Bitbucket Get Users Username Pipelines Config Variables
  x-api-slug: bitbucket
  description: Get users username pipelines config variables
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//users/{username}/pipelines_config/variables/
  tags: Users, Username, Pipelines, Config, Variables
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusernamepipelines-configvariables-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusernamepipelines-configvariables-get-openapi.md
- name: Bitbucket Add Users Username Pipelines Config Variables
  x-api-slug: bitbucket
  description: Post users username pipelines config variables
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//users/{username}/pipelines_config/variables/
  tags: Users, Username, Pipelines, Config, Variables
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusernamepipelines-configvariables-post-openapi.md
- name: Bitbucket Delete Users Username Pipelines Config Variables Variable Uu
  x-api-slug: bitbucket
  description: Delete users username pipelines config variables variable uu
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//users/{username}/pipelines_config/variables/{variable_uuid}
  tags: Users, Username, Pipelines, Config, Variables, Variable, Uu
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusernamepipelines-configvariablesvariable-uuid-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusernamepipelines-configvariablesvariable-uuid-delete-openapi.md
- name: Bitbucket Get Users Username Pipelines Config Variables Variable Uu
  x-api-slug: bitbucket
  description: Get users username pipelines config variables variable uu
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//users/{username}/pipelines_config/variables/{variable_uuid}
  tags: Users, Username, Pipelines, Config, Variables, Variable, Uu
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusernamepipelines-configvariablesvariable-uuid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusernamepipelines-configvariablesvariable-uuid-get-openapi.md
- name: Bitbucket Update Users Username Pipelines Config Variables Variable Uu
  x-api-slug: bitbucket
  description: Put users username pipelines config variables variable uu
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//users/{username}/pipelines_config/variables/{variable_uuid}
  tags: Users, Username, Pipelines, Config, Variables, Variable, Uu
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusernamepipelines-configvariablesvariable-uuid-put-openapi.md
- name: Bitbucket Get Users Username Repositories
  x-api-slug: bitbucket
  description: |-
    All repositories owned by a user/team. This includes private
    repositories, but filtered down to the ones that the calling user has
    access to.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//users/{username}/repositories
  tags: Users, Username, Repositories
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusernamerepositories-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusernamerepositories-get-openapi.md
- name: Bitbucket Parameters Users Username Repositories
  x-api-slug: bitbucket
  description: Parameters users username repositories
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0//users/{username}/repositories
  tags: Users, Username, Repositories
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusernamerepositories-parameters-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/usersusernamerepositories-parameters-openapi.md
- name: Bitbucket
  x-api-slug: bitbucket
  description: Collaborate on code with inline comments and pull requests. Manage
    and share your Git repositories to build and ship software, as a team.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/19810-bitbucket.jpg
  humanURL: http://bitbucket.org
  baseURL: https://api.bitbucket.org//2.0
  tags: Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bitbucket/openapi.md
x-common:
- type: x-crunchbase
  url: https://crunchbase.com/organization/bitbucket
- type: x-developer
  url: https://developer.atlassian.com/cloud/bitbucket/
- type: x-documentation
  url: https://confluence.atlassian.com/bitbucket/bitbucket-cloud-documentation-221448814.html?_ga=2.77295890.629375793.1519179030-1077111323.1516485126
- type: x-status
  url: https://status.bitbucket.org/?_ga=2.76365714.629375793.1519179030-1077111323.1516485126
- type: x-support
  url: https://support.atlassian.com/bitbucket-cloud/
- type: x-terms-of-service
  url: https://www.atlassian.com/legal/customer-agreement?_ga=2.76365714.629375793.1519179030-1077111323.1516485126
- type: x-twitter
  url: https://twitter.com/bitbucket
- type: x-website
  url: http://bitbucket.org
- type: x-website
  url: https://bitbucket.org/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---