---
name: LinkedIn
x-slug: linkedin
description: 500 million+ members | Manage your professional identity. Build and engage
  with your professional network. Access knowledge, insights and opportunities.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/221-linkedin.jpg
x-kinRank: "8"
x-alexaRank: "31"
tags: Name
created: "2018-06-20"
modified: "2018-06-20"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/linkedin/apis.md
specificationVersion: "0.14"
apis:
- name: LinkedIn Get Companies (,name,ticker,description)
  x-api-slug: linkedin
  description: Get companies  (,name,ticker,description)
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/221-linkedin.jpg
  humanURL: http://linkedin.com
  baseURL: https://api.linkedin.com//v1//companies/{id}:(id,name,ticker,description)
  tags: Companies, , (,name,ticker,description)
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/linkedin/companiesididnametickerdescription-get-openapi.md
- name: LinkedIn
  x-api-slug: linkedin
  description: 500 million+ members | Manage your professional identity. Build and
    engage with your professional network. Access knowledge, insights and opportunities.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/221-linkedin.jpg
  humanURL: http://linkedin.com
  baseURL: https://api.linkedin.com//v1
  tags: Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/linkedin/openapi.md
x-common:
- type: x-authentication
  url: https://developer.linkedin.com/documents/authentication
- type: x-base
  url: https://api.linkedin.com
- type: x-blog
  url: http://blog.linkedin.com
- type: x-branding
  url: https://brand.linkedin.com/policies
- type: x-case-studies
  url: https://developer.linkedin.com/showcase/wordpress
- type: x-crunchbase
  url: https://crunchbase.com/organization/linkedin
- type: x-crunchbase
  url: http://www.crunchbase.com/company/linkedin
- type: x-developer
  url: https://developer.linkedin.com
- type: x-forum
  url: https://developer.linkedin.com/forum
- type: x-github
  url: https://github.com/linkedin
- type: x-javascript-api
  url: https://developer.linkedin.com/javascript
- type: x-partners
  url: https://developer.linkedin.com/partner-programs
- type: x-privacy
  url: http://www.linkedin.com/static?key=privacy_policy&trk=hb_ft_priv
- type: x-stack-overflow
  url: http://stackoverflow.com/questions/tagged/linkedin
- type: x-terms-of-service
  url: https://developer.linkedin.com/legal/api-terms-of-use
- type: x-transparency-report
  url: https://www.linkedin.com/legal/transparency
- type: x-twitter
  url: https://twitter.com/LinkedIn
- type: x-website
  url: http://linkedin.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---