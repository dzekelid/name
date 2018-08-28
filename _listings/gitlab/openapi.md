swagger: "2.0"
x-collection-name: GitLab
x-complete: 1
info:
  title: API title
  version: 1.0.0
host: localhost:3000
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v3/projects/{id}/builds/artifacts/{ref_name}/download:
    get:
      summary: Get Projects Builds Artifacts Ref Name Download
      description: Get projects builds artifacts ref name download.
      operationId: getV3ProjectsIdBuildsArtifactsRefNameDownload
      x-api-path-slug: v3projectsidbuildsartifactsref-namedownload-get
      parameters:
      - in: path
        name: id
        description: The ID of a project
      - in: query
        name: job
        description: The name for the build
      - in: path
        name: ref_name
        description: The ref from repository
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Builds
      - Artifacts
      - Ref
      - Name
      - Download
  /v3/projects/{id}/repository/tags/{tag_name}:
    get:
      summary: Get Projects Repository Tags Tag Name
      description: Get projects repository tags tag name.
      operationId: getV3ProjectsIdRepositoryTagsTagName
      x-api-path-slug: v3projectsidrepositorytagstag-name-get
      parameters:
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: tag_name
        description: The name of the tag
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Repository
      - Tags
      - Tag
      - Name
    delete:
      summary: Delete Projects Repository Tags Tag Name
      description: Delete projects repository tags tag name.
      operationId: deleteV3ProjectsIdRepositoryTagsTagName
      x-api-path-slug: v3projectsidrepositorytagstag-name-delete
      parameters:
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: tag_name
        description: The name of the tag
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Repository
      - Tags
      - Tag
      - Name
  /v3/projects/{id}/repository/tags/{tag_name}/release:
    post:
      summary: Post Projects Repository Tags Tag Name Release
      description: Post projects repository tags tag name release.
      operationId: postV3ProjectsIdRepositoryTagsTagNameRelease
      x-api-path-slug: v3projectsidrepositorytagstag-namerelease-post
      parameters:
      - in: formData
        name: description
        description: Release notes with markdown support
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: tag_name
        description: The name of the tag
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Repository
      - Tags
      - Tag
      - Name
      - Release
    put:
      summary: Put Projects Repository Tags Tag Name Release
      description: Put projects repository tags tag name release.
      operationId: putV3ProjectsIdRepositoryTagsTagNameRelease
      x-api-path-slug: v3projectsidrepositorytagstag-namerelease-put
      parameters:
      - in: formData
        name: description
        description: Release notes with markdown support
      - in: path
        name: id
        description: The ID of a project
      - in: path
        name: tag_name
        description: The name of the tag
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Repository
      - Tags
      - Tag
      - Name
      - Release
  /v3/licenses/{name}:
    get:
      summary: Get Licenses Name
      description: This feature was introduced in GitLab 8.7. This endpoint is deprecated
        and will be removed in GitLab 9.0.
      operationId: getV3LicensesName
      x-api-path-slug: v3licensesname-get
      parameters:
      - in: path
        name: name
        description: The name of the template
      responses:
        200:
          description: OK
      tags:
      - Licenses
      - Name
  /v3/templates/licenses/{name}:
    get:
      summary: Get Templates Licenses Name
      description: This feature was introduced in GitLab 8.7.
      operationId: getV3TemplatesLicensesName
      x-api-path-slug: v3templateslicensesname-get
      parameters:
      - in: path
        name: name
        description: The name of the template
      responses:
        200:
          description: OK
      tags:
      - Templates
      - Licenses
      - Name
  /v3/templates/gitignores/{name}:
    get:
      summary: Get Templates Gitignores Name
      description: This feature was introduced in GitLab 8.8.
      operationId: getV3TemplatesGitignoresName
      x-api-path-slug: v3templatesgitignoresname-get
      parameters:
      - in: path
        name: name
        description: The name of the template
      responses:
        200:
          description: OK
      tags:
      - Templates
      - Gitignores
      - Name
  /v3/templates/gitlab_ci_ymls/{name}:
    get:
      summary: Get Templates Gitlab Ci Ymls Name
      description: This feature was introduced in GitLab 8.9.
      operationId: getV3TemplatesGitlabCiYmlsName
      x-api-path-slug: v3templatesgitlab-ci-ymlsname-get
      parameters:
      - in: path
        name: name
        description: The name of the template
      responses:
        200:
          description: OK
      tags:
      - Templates
      - Gitlab
      - Ci
      - Ymls
      - Name
  /v3/templates/dockerfiles/{name}:
    get:
      summary: Get Templates Dockerfiles Name
      description: This feature was introduced in GitLab 8.15.
      operationId: getV3TemplatesDockerfilesName
      x-api-path-slug: v3templatesdockerfilesname-get
      parameters:
      - in: path
        name: name
        description: The name of the template
      responses:
        200:
          description: OK
      tags:
      - Templates
      - Dockerfiles
      - Name
  /v3/gitignores/{name}:
    get:
      summary: Get Gitignores Name
      description: This feature was introduced in GitLab 8.8. This endpoint is deprecated
        and will be removed in GitLab 9.0.
      operationId: getV3GitignoresName
      x-api-path-slug: v3gitignoresname-get
      parameters:
      - in: path
        name: name
        description: The name of the template
      responses:
        200:
          description: OK
      tags:
      - Gitignores
      - Name
  /v3/gitlab_ci_ymls/{name}:
    get:
      summary: Get Gitlab Ci Ymls Name
      description: This feature was introduced in GitLab 8.9. This endpoint is deprecated
        and will be removed in GitLab 9.0.
      operationId: getV3GitlabCiYmlsName
      x-api-path-slug: v3gitlab-ci-ymlsname-get
      parameters:
      - in: path
        name: name
        description: The name of the template
      responses:
        200:
          description: OK
      tags:
      - Gitlab
      - Ci
      - Ymls
      - Name
  /v3/dockerfiles/{name}:
    get:
      summary: Get Dockerfiles Name
      description: This feature was introduced in GitLab 8.15. This endpoint is deprecated
        and will be removed in GitLab 9.0.
      operationId: getV3DockerfilesName
      x-api-path-slug: v3dockerfilesname-get
      parameters:
      - in: path
        name: name
        description: The name of the template
      responses:
        200:
          description: OK
      tags:
      - Dockerfiles
      - Name