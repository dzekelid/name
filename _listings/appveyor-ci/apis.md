---
name: AppVeyor CI
x-slug: appveyor-ci
description: We provide continuous integration tools for Windows developers. The service
  is offered for free to open-source projects, we offer subscriptions for private
  projects and AppVeyor Enterprise installations on customer premises.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28368-app-veyor.jpg
x-kinRank: "7"
x-alexaRank: "35479"
tags: Name
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/appveyor-ci/apis.md
specificationVersion: "0.14"
apis:
- name: App Veyor Delete Builds Accountname Projectslug Buildversion
  x-api-slug: app-veyor
  description: Delete builds accountname projectslug buildversion.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28368-app-veyor.jpg
  humanURL: http://appveyor.com
  baseURL: https://ci.appveyor.com//api//builds/{accountName}/{projectSlug}/{buildVersion}
  tags: Builds,AccountName,ProjectSlug,BuildVersion
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/appveyor-ci/buildsaccountnameprojectslugbuildversion-delete-openapi.md
- name: App Veyor Parameters Builds Accountname Projectslug Buildversion
  x-api-slug: app-veyor
  description: Parameters builds accountname projectslug buildversion.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28368-app-veyor.jpg
  humanURL: http://appveyor.com
  baseURL: https://ci.appveyor.com//api//builds/{accountName}/{projectSlug}/{buildVersion}
  tags: Builds,AccountName,ProjectSlug,BuildVersion
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/appveyor-ci/buildsaccountnameprojectslugbuildversion-parameters-openapi.md
- name: App Veyor Get Projects Status Badgerepoprover Repoaccountname Reposlug
  x-api-slug: app-veyor
  description: Get projects status badgerepoprover repoaccountname reposlug.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28368-app-veyor.jpg
  humanURL: http://appveyor.com
  baseURL: https://ci.appveyor.com//api//projects/status/{badgeRepoProvider}/{repoAccountName}/{repoSlug}
  tags: Projects,Status,BadgeRepoProvider,RepoAccountName,RepoSlug
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/appveyor-ci/projectsstatusbadgerepoproviderrepoaccountnamereposlug-get-openapi.md
- name: App Veyor Parameters Projects Status Badgerepoprover Repoaccountname Reposlug
  x-api-slug: app-veyor
  description: Parameters projects status badgerepoprover repoaccountname reposlug.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28368-app-veyor.jpg
  humanURL: http://appveyor.com
  baseURL: https://ci.appveyor.com//api//projects/status/{badgeRepoProvider}/{repoAccountName}/{repoSlug}
  tags: Projects,Status,BadgeRepoProvider,RepoAccountName,RepoSlug
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/appveyor-ci/projectsstatusbadgerepoproviderrepoaccountnamereposlug-parameters-openapi.md
- name: App Veyor Delete Projects Accountname Projectslug
  x-api-slug: app-veyor
  description: Delete projects accountname projectslug.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28368-app-veyor.jpg
  humanURL: http://appveyor.com
  baseURL: https://ci.appveyor.com//api//projects/{accountName}/{projectSlug}
  tags: Projects,AccountName,ProjectSlug
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/appveyor-ci/projectsaccountnameprojectslug-delete-openapi.md
- name: App Veyor Get Projects Accountname Projectslug
  x-api-slug: app-veyor
  description: Get projects accountname projectslug.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28368-app-veyor.jpg
  humanURL: http://appveyor.com
  baseURL: https://ci.appveyor.com//api//projects/{accountName}/{projectSlug}
  tags: Projects,AccountName,ProjectSlug
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/appveyor-ci/projectsaccountnameprojectslug-get-openapi.md
- name: App Veyor Parameters Projects Accountname Projectslug
  x-api-slug: app-veyor
  description: Parameters projects accountname projectslug.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28368-app-veyor.jpg
  humanURL: http://appveyor.com
  baseURL: https://ci.appveyor.com//api//projects/{accountName}/{projectSlug}
  tags: Projects,AccountName,ProjectSlug
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/appveyor-ci/projectsaccountnameprojectslug-parameters-openapi.md
- name: App Veyor Get Projects Accountname Projectslug Artifacts Artifactfilename
  x-api-slug: app-veyor
  description: Get projects accountname projectslug artifacts artifactfilename.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28368-app-veyor.jpg
  humanURL: http://appveyor.com
  baseURL: https://ci.appveyor.com//api//projects/{accountName}/{projectSlug}/artifacts/{artifactFileName}
  tags: Projects,AccountName,ProjectSlug,Artifacts,Files
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/appveyor-ci/projectsaccountnameprojectslugartifactsartifactfilename-get-openapi.md
- name: App Veyor Parameters Projects Accountname Projectslug Artifacts Artifactfilename
  x-api-slug: app-veyor
  description: Parameters projects accountname projectslug artifacts artifactfilename.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28368-app-veyor.jpg
  humanURL: http://appveyor.com
  baseURL: https://ci.appveyor.com//api//projects/{accountName}/{projectSlug}/artifacts/{artifactFileName}
  tags: Projects,AccountName,ProjectSlug,Artifacts,Files
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/appveyor-ci/projectsaccountnameprojectslugartifactsartifactfilename-parameters-openapi.md
- name: App Veyor Get Projects Accountname Projectslug Branch Buildbranch
  x-api-slug: app-veyor
  description: Get projects accountname projectslug branch buildbranch.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28368-app-veyor.jpg
  humanURL: http://appveyor.com
  baseURL: https://ci.appveyor.com//api//projects/{accountName}/{projectSlug}/branch/{buildBranch}
  tags: Projects,AccountName,ProjectSlug,Branch,BuildBranch
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/appveyor-ci/projectsaccountnameprojectslugbranchbuildbranch-get-openapi.md
- name: App Veyor Parameters Projects Accountname Projectslug Branch Buildbranch
  x-api-slug: app-veyor
  description: Parameters projects accountname projectslug branch buildbranch.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28368-app-veyor.jpg
  humanURL: http://appveyor.com
  baseURL: https://ci.appveyor.com//api//projects/{accountName}/{projectSlug}/branch/{buildBranch}
  tags: Projects,AccountName,ProjectSlug,Branch,BuildBranch
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/appveyor-ci/projectsaccountnameprojectslugbranchbuildbranch-parameters-openapi.md
- name: App Veyor Get Projects Accountname Projectslug Build Buildversion
  x-api-slug: app-veyor
  description: Get projects accountname projectslug build buildversion.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28368-app-veyor.jpg
  humanURL: http://appveyor.com
  baseURL: https://ci.appveyor.com//api//projects/{accountName}/{projectSlug}/build/{buildVersion}
  tags: Projects,AccountName,ProjectSlug,Build,BuildVersion
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/appveyor-ci/projectsaccountnameprojectslugbuildbuildversion-get-openapi.md
- name: App Veyor Parameters Projects Accountname Projectslug Build Buildversion
  x-api-slug: app-veyor
  description: Parameters projects accountname projectslug build buildversion.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28368-app-veyor.jpg
  humanURL: http://appveyor.com
  baseURL: https://ci.appveyor.com//api//projects/{accountName}/{projectSlug}/build/{buildVersion}
  tags: Projects,AccountName,ProjectSlug,Build,BuildVersion
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/appveyor-ci/projectsaccountnameprojectslugbuildbuildversion-parameters-openapi.md
- name: App Veyor Delete Projects Accountname Projectslug Buildcache
  x-api-slug: app-veyor
  description: Delete projects accountname projectslug buildcache.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28368-app-veyor.jpg
  humanURL: http://appveyor.com
  baseURL: https://ci.appveyor.com//api//projects/{accountName}/{projectSlug}/buildcache
  tags: Projects,AccountName,ProjectSlug,Buildcache
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/appveyor-ci/projectsaccountnameprojectslugbuildcache-delete-openapi.md
- name: App Veyor Parameters Projects Accountname Projectslug Buildcache
  x-api-slug: app-veyor
  description: Parameters projects accountname projectslug buildcache.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28368-app-veyor.jpg
  humanURL: http://appveyor.com
  baseURL: https://ci.appveyor.com//api//projects/{accountName}/{projectSlug}/buildcache
  tags: Projects,AccountName,ProjectSlug,Buildcache
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/appveyor-ci/projectsaccountnameprojectslugbuildcache-parameters-openapi.md
- name: App Veyor Get Projects Accountname Projectslug Deployments
  x-api-slug: app-veyor
  description: Get projects accountname projectslug deployments.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28368-app-veyor.jpg
  humanURL: http://appveyor.com
  baseURL: https://ci.appveyor.com//api//projects/{accountName}/{projectSlug}/deployments
  tags: Projects,AccountName,ProjectSlug,Deployments
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/appveyor-ci/projectsaccountnameprojectslugdeployments-get-openapi.md
- name: App Veyor Parameters Projects Accountname Projectslug Deployments
  x-api-slug: app-veyor
  description: Parameters projects accountname projectslug deployments.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28368-app-veyor.jpg
  humanURL: http://appveyor.com
  baseURL: https://ci.appveyor.com//api//projects/{accountName}/{projectSlug}/deployments
  tags: Projects,AccountName,ProjectSlug,Deployments
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/appveyor-ci/projectsaccountnameprojectslugdeployments-parameters-openapi.md
- name: App Veyor Get Projects Accountname Projectslug History
  x-api-slug: app-veyor
  description: Get projects accountname projectslug history.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28368-app-veyor.jpg
  humanURL: http://appveyor.com
  baseURL: https://ci.appveyor.com//api//projects/{accountName}/{projectSlug}/history
  tags: Projects,AccountName,ProjectSlug,History
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/appveyor-ci/projectsaccountnameprojectslughistory-get-openapi.md
- name: App Veyor Parameters Projects Accountname Projectslug History
  x-api-slug: app-veyor
  description: Parameters projects accountname projectslug history.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28368-app-veyor.jpg
  humanURL: http://appveyor.com
  baseURL: https://ci.appveyor.com//api//projects/{accountName}/{projectSlug}/history
  tags: Projects,AccountName,ProjectSlug,History
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/appveyor-ci/projectsaccountnameprojectslughistory-parameters-openapi.md
- name: App Veyor Get Projects Accountname Projectslug Settings
  x-api-slug: app-veyor
  description: Get projects accountname projectslug settings.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28368-app-veyor.jpg
  humanURL: http://appveyor.com
  baseURL: https://ci.appveyor.com//api//projects/{accountName}/{projectSlug}/settings
  tags: Projects,AccountName,ProjectSlug,Settings
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/appveyor-ci/projectsaccountnameprojectslugsettings-get-openapi.md
- name: App Veyor Parameters Projects Accountname Projectslug Settings
  x-api-slug: app-veyor
  description: Parameters projects accountname projectslug settings.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28368-app-veyor.jpg
  humanURL: http://appveyor.com
  baseURL: https://ci.appveyor.com//api//projects/{accountName}/{projectSlug}/settings
  tags: Projects,AccountName,ProjectSlug,Settings
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/appveyor-ci/projectsaccountnameprojectslugsettings-parameters-openapi.md
- name: App Veyor Parameters Projects Accountname Projectslug Settings Build Number
  x-api-slug: app-veyor
  description: Parameters projects accountname projectslug settings build number.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28368-app-veyor.jpg
  humanURL: http://appveyor.com
  baseURL: https://ci.appveyor.com//api//projects/{accountName}/{projectSlug}/settings/build-number
  tags: Projects,AccountName,ProjectSlug,Settings,Build,Number
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/appveyor-ci/projectsaccountnameprojectslugsettingsbuildnumber-parameters-openapi.md
- name: App Veyor Put Projects Accountname Projectslug Settings Build Number
  x-api-slug: app-veyor
  description: Put projects accountname projectslug settings build number.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28368-app-veyor.jpg
  humanURL: http://appveyor.com
  baseURL: https://ci.appveyor.com//api//projects/{accountName}/{projectSlug}/settings/build-number
  tags: Projects,AccountName,ProjectSlug,Settings,Build,Number
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/appveyor-ci/projectsaccountnameprojectslugsettingsbuildnumber-put-openapi.md
- name: App Veyor Get Projects Accountname Projectslug Settings Environment Variables
  x-api-slug: app-veyor
  description: Get projects accountname projectslug settings environment variables.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28368-app-veyor.jpg
  humanURL: http://appveyor.com
  baseURL: https://ci.appveyor.com//api//projects/{accountName}/{projectSlug}/settings/environment-variables
  tags: Projects,AccountName,ProjectSlug,Settings,Environment,Variables
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/appveyor-ci/projectsaccountnameprojectslugsettingsenvironmentvariables-get-openapi.md
- name: App Veyor Parameters Projects Accountname Projectslug Settings Environment
    Variables
  x-api-slug: app-veyor
  description: Parameters projects accountname projectslug settings environment variables.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28368-app-veyor.jpg
  humanURL: http://appveyor.com
  baseURL: https://ci.appveyor.com//api//projects/{accountName}/{projectSlug}/settings/environment-variables
  tags: Projects,AccountName,ProjectSlug,Settings,Environment,Variables
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/appveyor-ci/projectsaccountnameprojectslugsettingsenvironmentvariables-parameters-openapi.md
- name: App Veyor Put Projects Accountname Projectslug Settings Environment Variables
  x-api-slug: app-veyor
  description: Put projects accountname projectslug settings environment variables.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28368-app-veyor.jpg
  humanURL: http://appveyor.com
  baseURL: https://ci.appveyor.com//api//projects/{accountName}/{projectSlug}/settings/environment-variables
  tags: Projects,AccountName,ProjectSlug,Settings,Environment,Variables
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/appveyor-ci/projectsaccountnameprojectslugsettingsenvironmentvariables-put-openapi.md
- name: App Veyor Get Projects Accountname Projectslug Settings Yaml
  x-api-slug: app-veyor
  description: Get projects accountname projectslug settings yaml.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28368-app-veyor.jpg
  humanURL: http://appveyor.com
  baseURL: https://ci.appveyor.com//api//projects/{accountName}/{projectSlug}/settings/yaml
  tags: Projects,AccountName,ProjectSlug,Settings,Yaml
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/appveyor-ci/projectsaccountnameprojectslugsettingsyaml-get-openapi.md
- name: App Veyor Parameters Projects Accountname Projectslug Settings Yaml
  x-api-slug: app-veyor
  description: Parameters projects accountname projectslug settings yaml.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28368-app-veyor.jpg
  humanURL: http://appveyor.com
  baseURL: https://ci.appveyor.com//api//projects/{accountName}/{projectSlug}/settings/yaml
  tags: Projects,AccountName,ProjectSlug,Settings,Yaml
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/appveyor-ci/projectsaccountnameprojectslugsettingsyaml-parameters-openapi.md
- name: App Veyor Put Projects Accountname Projectslug Settings Yaml
  x-api-slug: app-veyor
  description: Put projects accountname projectslug settings yaml.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28368-app-veyor.jpg
  humanURL: http://appveyor.com
  baseURL: https://ci.appveyor.com//api//projects/{accountName}/{projectSlug}/settings/yaml
  tags: Projects,AccountName,ProjectSlug,Settings,Yaml
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/appveyor-ci/projectsaccountnameprojectslugsettingsyaml-put-openapi.md
- name: App Veyor
  x-api-slug: app-veyor
  description: We provide continuous integration tools for Windows developers. The
    service is offered for free to open-source projects, we offer subscriptions for
    private projects and AppVeyor Enterprise installations on customer premises.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28368-app-veyor.jpg
  humanURL: http://appveyor.com
  baseURL: https://ci.appveyor.com//api
  tags: Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/appveyor-ci/openapi.md
x-common:
- type: x-crunchbase
  url: https://crunchbase.com/organization/appveyor-systems-inc
- type: x-documentation
  url: https://www.appveyor.com/docs/
- type: x-email
  url: jobs@appveyor.com
- type: x-email
  url: team@appveyor.com
- type: x-email
  url: privacy@appveyor.com
- type: x-twitter
  url: https://twitter.com/appveyor
- type: x-website
  url: http://appveyor.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---