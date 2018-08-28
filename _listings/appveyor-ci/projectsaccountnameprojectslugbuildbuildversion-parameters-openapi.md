---
swagger: "2.0"
x-collection-name: AppVeyor CI
x-complete: 0
info:
  title: App Veyor Parameters Projects Accountname Projectslug Build Buildversion
  description: Parameters projects accountname projectslug build buildversion.
  termsOfService: https://www.appveyor.com/terms-of-service/
  contact:
    name: AppVeyor Team
    url: https://www.appveyor.com/about/
    email: team@appveyor.com
  version: 0.20170106.0
host: ci.appveyor.com
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /builds/{accountName}/{projectSlug}/{buildVersion}:
    delete:
      summary: Delete Builds Accountname Projectslug Buildversion
      description: Delete builds accountname projectslug buildversion.
      operationId: deleteBuildsAccountnameProjectslugBuildversion
      x-api-path-slug: buildsaccountnameprojectslugbuildversion-delete
      responses:
        200:
          description: OK
      tags:
      - Builds
      - AccountName
      - ProjectSlug
      - BuildVersion
    parameters:
      summary: Parameters Builds Accountname Projectslug Buildversion
      description: Parameters builds accountname projectslug buildversion.
      operationId: parametersBuildsAccountnameProjectslugBuildversion
      x-api-path-slug: buildsaccountnameprojectslugbuildversion-parameters
      responses:
        200:
          description: OK
      tags:
      - Builds
      - AccountName
      - ProjectSlug
      - BuildVersion
  /projects/status/{badgeRepoProvider}/{repoAccountName}/{repoSlug}:
    get:
      summary: Get Projects Status Badgerepoprover Repoaccountname Reposlug
      description: Get projects status badgerepoprover repoaccountname reposlug.
      operationId: getProjectsStatusBadgerepoproverRepoaccountnameReposlug
      x-api-path-slug: projectsstatusbadgerepoproviderrepoaccountnamereposlug-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Status
      - BadgeRepoProvider
      - RepoAccountName
      - RepoSlug
    parameters:
      summary: Parameters Projects Status Badgerepoprover Repoaccountname Reposlug
      description: Parameters projects status badgerepoprover repoaccountname reposlug.
      operationId: parametersProjectsStatusBadgerepoproverRepoaccountnameReposlug
      x-api-path-slug: projectsstatusbadgerepoproviderrepoaccountnamereposlug-parameters
      responses:
        200:
          description: OK
      tags:
      - Projects
      - Status
      - BadgeRepoProvider
      - RepoAccountName
      - RepoSlug
  /projects/{accountName}/{projectSlug}:
    delete:
      summary: Delete Projects Accountname Projectslug
      description: Delete projects accountname projectslug.
      operationId: deleteProjectsAccountnameProjectslug
      x-api-path-slug: projectsaccountnameprojectslug-delete
      responses:
        200:
          description: OK
      tags:
      - Projects
      - AccountName
      - ProjectSlug
    get:
      summary: Get Projects Accountname Projectslug
      description: Get projects accountname projectslug.
      operationId: getProjectsAccountnameProjectslug
      x-api-path-slug: projectsaccountnameprojectslug-get
      responses:
        200:
          description: OK
      tags:
      - Projects
      - AccountName
      - ProjectSlug
    parameters:
      summary: Parameters Projects Accountname Projectslug
      description: Parameters projects accountname projectslug.
      operationId: parametersProjectsAccountnameProjectslug
      x-api-path-slug: projectsaccountnameprojectslug-parameters
      responses:
        200:
          description: OK
      tags:
      - Projects
      - AccountName
      - ProjectSlug
  /projects/{accountName}/{projectSlug}/artifacts/{artifactFileName}:
    get:
      summary: Get Projects Accountname Projectslug Artifacts Artifactfilename
      description: Get projects accountname projectslug artifacts artifactfilename.
      operationId: getProjectsAccountnameProjectslugArtifactsArtifactfilename
      x-api-path-slug: projectsaccountnameprojectslugartifactsartifactfilename-get
      responses:
        200:
          description: OK
      tags:
      - Projects
      - AccountName
      - ProjectSlug
      - Artifacts
      - Files
    parameters:
      summary: Parameters Projects Accountname Projectslug Artifacts Artifactfilename
      description: Parameters projects accountname projectslug artifacts artifactfilename.
      operationId: parametersProjectsAccountnameProjectslugArtifactsArtifactfilename
      x-api-path-slug: projectsaccountnameprojectslugartifactsartifactfilename-parameters
      responses:
        200:
          description: OK
      tags:
      - Projects
      - AccountName
      - ProjectSlug
      - Artifacts
      - Files
  /projects/{accountName}/{projectSlug}/branch/{buildBranch}:
    get:
      summary: Get Projects Accountname Projectslug Branch Buildbranch
      description: Get projects accountname projectslug branch buildbranch.
      operationId: getProjectsAccountnameProjectslugBranchBuildbranch
      x-api-path-slug: projectsaccountnameprojectslugbranchbuildbranch-get
      responses:
        200:
          description: OK
      tags:
      - Projects
      - AccountName
      - ProjectSlug
      - Branch
      - BuildBranch
    parameters:
      summary: Parameters Projects Accountname Projectslug Branch Buildbranch
      description: Parameters projects accountname projectslug branch buildbranch.
      operationId: parametersProjectsAccountnameProjectslugBranchBuildbranch
      x-api-path-slug: projectsaccountnameprojectslugbranchbuildbranch-parameters
      responses:
        200:
          description: OK
      tags:
      - Projects
      - AccountName
      - ProjectSlug
      - Branch
      - BuildBranch
  /projects/{accountName}/{projectSlug}/build/{buildVersion}:
    get:
      summary: Get Projects Accountname Projectslug Build Buildversion
      description: Get projects accountname projectslug build buildversion.
      operationId: getProjectsAccountnameProjectslugBuildBuildversion
      x-api-path-slug: projectsaccountnameprojectslugbuildbuildversion-get
      responses:
        200:
          description: OK
      tags:
      - Projects
      - AccountName
      - ProjectSlug
      - Build
      - BuildVersion
    parameters:
      summary: Parameters Projects Accountname Projectslug Build Buildversion
      description: Parameters projects accountname projectslug build buildversion.
      operationId: parametersProjectsAccountnameProjectslugBuildBuildversion
      x-api-path-slug: projectsaccountnameprojectslugbuildbuildversion-parameters
      responses:
        200:
          description: OK
      tags:
      - Projects
      - AccountName
      - ProjectSlug
      - Build
      - BuildVersion
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