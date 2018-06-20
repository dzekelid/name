---
name: DataAtWork
x-slug: dataatwork
description: ""
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Screen
  Shot 2016-10-12 at 11.19.25 PM.png
x-kinRank: "8"
x-alexaRank: "0"
tags: Name
created: "2018-06-20"
modified: "2018-06-20"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/dataatwork/apis.md
specificationVersion: "0.14"
apis:
- name: Open Skills API Skill Names and Descriptions
  x-api-slug: open-skills-api
  description: Retrieve the names, descriptions, and UUIDs of all skills.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Screen
    Shot 2016-10-12 at 11.19.25 PM.png
  humanURL: http://www.dataatwork.org/
  baseURL: ://api.dataatwork.org//v1//skills
  tags: Skill, Names, Descriptions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/dataatwork/skills-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/dataatwork/skills-get-openapi.md
- name: Open Skills API Skill Name and Description
  x-api-slug: open-skills-api
  description: Retrieves the name, description, and UUID of a job by specifying its
    UUID.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Screen
    Shot 2016-10-12 at 11.19.25 PM.png
  humanURL: http://www.dataatwork.org/
  baseURL: ://api.dataatwork.org//v1//skills/{id}
  tags: Skill, Name, Description
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/dataatwork/skillsid-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/dataatwork/skillsid-get-openapi.md
- name: Open Skills API Skill Name Autocomplete
  x-api-slug: open-skills-api
  description: Retrieves the names, descriptions, and UUIDs of all skills matching
    a given search criteria.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Screen
    Shot 2016-10-12 at 11.19.25 PM.png
  humanURL: http://www.dataatwork.org/
  baseURL: ://api.dataatwork.org//v1//skills/autocomplete
  tags: Skill, Name, Autocomplete
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/dataatwork/skillsautocomplete-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/dataatwork/skillsautocomplete-get-openapi.md
- name: Open Skills API Skill Name Normalization
  x-api-slug: open-skills-api
  description: Retrieves the canonical skill name for a synonymous skill name
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Screen
    Shot 2016-10-12 at 11.19.25 PM.png
  humanURL: http://www.dataatwork.org/
  baseURL: ://api.dataatwork.org//v1//skills/normalize
  tags: Skill, Name, Normalization
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/dataatwork/skillsnormalize-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/dataatwork/skillsnormalize-get-openapi.md
- name: Open Skills API
  x-api-slug: open-skills-api
  description: ""
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/Screen
    Shot 2016-10-12 at 11.19.25 PM.png
  humanURL: http://www.dataatwork.org/
  baseURL: ://api.dataatwork.org//v1
  tags: Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/dataatwork/openapi.md
x-common:
- type: x-developer
  url: http://api.dataatwork.org/v1/spec/
- type: x-website
  url: http://www.dataatwork.org/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---