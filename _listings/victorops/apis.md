---
name: VictorOps
x-slug: victorops
description: VictorOps incident managament software gives DevOps observability, collaboration,
  & real-time alerting, to build, deploy, & operate software. Learn more.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20023-victorops.jpg
x-kinRank: "8"
x-alexaRank: "196587"
tags: Name
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/victorops/apis.md
specificationVersion: "0.14"
apis:
- name: Victor Ops Get the user's paging policy
  x-api-slug: victor-ops
  description: |-
    Get all the paging policy steps for the user on the org associated with the API key

    This API may be called a maximum of 15 times per minute.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20023-victorops.jpg
  humanURL: http://victorops.com
  baseURL: https://api.victorops.com////api-public/v1/profile/{username}/policies
  tags: Profile,Username,Policies
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/victorops/apipublicv1profileusernamepolicies-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/victorops/apipublicv1profileusernamepolicies-get-openapi.md
- name: Victor Ops Create a paging policy step
  x-api-slug: victor-ops
  description: |-
    Create a paging policy step

    This API may be called a maximum of 15 times per minute.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20023-victorops.jpg
  humanURL: http://victorops.com
  baseURL: https://api.victorops.com////api-public/v1/profile/{username}/policies
  tags: Profile,Username,Policies
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/victorops/apipublicv1profileusernamepolicies-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/victorops/apipublicv1profileusernamepolicies-post-openapi.md
- name: Victor Ops Get a paging policy step
  x-api-slug: victor-ops
  description: |-
    Get a paging policy step

    This API may be called a maximum of 15 times per minute.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20023-victorops.jpg
  humanURL: http://victorops.com
  baseURL: https://api.victorops.com////api-public/v1/profile/{username}/policies/{step}
  tags: Profile,Username,Policies,Step
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/victorops/apipublicv1profileusernamepoliciesstep-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/victorops/apipublicv1profileusernamepoliciesstep-get-openapi.md
- name: Victor Ops Create a rule for a paging policy step
  x-api-slug: victor-ops
  description: |-
    Create a rule for a paging policy step

    This API may be called a maximum of 15 times per minute.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20023-victorops.jpg
  humanURL: http://victorops.com
  baseURL: https://api.victorops.com////api-public/v1/profile/{username}/policies/{step}
  tags: Profile,Username,Policies,Step
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/victorops/apipublicv1profileusernamepoliciesstep-post-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/victorops/apipublicv1profileusernamepoliciesstep-post-openapi.md
- name: Victor Ops Update a paging policy step
  x-api-slug: victor-ops
  description: |-
    Update a paging policy step

    This API may be called a maximum of 15 times per minute.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20023-victorops.jpg
  humanURL: http://victorops.com
  baseURL: https://api.victorops.com////api-public/v1/profile/{username}/policies/{step}
  tags: Profile,Username,Policies,Step
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/victorops/apipublicv1profileusernamepoliciesstep-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/victorops/apipublicv1profileusernamepoliciesstep-put-openapi.md
- name: Victor Ops Delete a rule from a paging policy step
  x-api-slug: victor-ops
  description: |-
    Delete a rule from a paging policy step

    This API may be called a maximum of 15 times per minute.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20023-victorops.jpg
  humanURL: http://victorops.com
  baseURL: https://api.victorops.com////api-public/v1/profile/{username}/policies/{step}/{rule}
  tags: Profile,Username,Policies,Step,Rule
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/victorops/apipublicv1profileusernamepoliciessteprule-delete-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/victorops/apipublicv1profileusernamepoliciessteprule-delete-openapi.md
- name: Victor Ops Get a rule from a paging policy step
  x-api-slug: victor-ops
  description: |-
    Get a rule from a paging policy step

    This API may be called a maximum of 15 times per minute.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20023-victorops.jpg
  humanURL: http://victorops.com
  baseURL: https://api.victorops.com////api-public/v1/profile/{username}/policies/{step}/{rule}
  tags: Profile,Username,Policies,Step,Rule
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/victorops/apipublicv1profileusernamepoliciessteprule-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/victorops/apipublicv1profileusernamepoliciessteprule-get-openapi.md
- name: Victor Ops Update a rule for a paging policy step
  x-api-slug: victor-ops
  description: |-
    Update a rule for a paging policy step

    This API may be called a maximum of 15 times per minute.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20023-victorops.jpg
  humanURL: http://victorops.com
  baseURL: https://api.victorops.com////api-public/v1/profile/{username}/policies/{step}/{rule}
  tags: Profile,Username,Policies,Step,Rule
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/victorops/apipublicv1profileusernamepoliciessteprule-put-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/victorops/apipublicv1profileusernamepoliciessteprule-put-openapi.md
- name: Victor Ops
  x-api-slug: victor-ops
  description: VictorOps incident managament software gives DevOps observability,
    collaboration, & real-time alerting, to build, deploy, & operate software. Learn
    more.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20023-victorops.jpg
  humanURL: http://victorops.com
  baseURL: https://api.victorops.com//
  tags: Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/victorops/openapi.md
x-common:
- type: x-blog
  url: https://victorops.com/blog/
- type: x-blog-rss
  url: https://victorops.com/feed/
- type: x-crunchbase
  url: https://crunchbase.com/organization/victorops
- type: x-email
  url: support@victorops.com
- type: x-email
  url: info@victorops.com
- type: x-email
  url: press@victorops.com
- type: x-email
  url: sales@victorops.com
- type: x-github
  url: https://github.com/victorops
- type: x-pricing
  url: https://victorops.com/pricing/
- type: x-twitter
  url: https://twitter.com/VictorOps
- type: x-website
  url: http://victorops.com
- type: x-website
  url: https://victorops.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---