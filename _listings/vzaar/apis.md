---
name: Vzaar
x-slug: vzaar
description: vzaar is an online video hosting service, which launched in 2007. The
  site supports video streaming, embedding, sharing, and video storage. Originally
  targeted at eBay sellers, the service expanded in 2008 and now provides online video
  services designed for business and other commercial operations.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/523_logo.png
x-kinRank: "8"
x-alexaRank: "0"
tags: Name
created: "2018-06-20"
modified: "2018-06-20"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/vzaar/apis.md
specificationVersion: "0.14"
apis:
- name: Vzaar API Get Api Users Username
  x-api-slug: vzaar-api
  description: nnThis API call returns the users public details along with its relevant
    metadata.nn
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/523_logo.png
  humanURL: http://vzaar.com/
  baseURL: https://vzaar.com////api/users/{username}.{format}
  tags: Api,Users,Username,Format
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/vzaar/apiusersusername-format-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/vzaar/apiusersusername-format-get-openapi.md
- name: Vzaar API Get Api Username Videos
  x-api-slug: vzaar-api
  description: nnThis API call returns a list of the users active videos along with
    its relevant metadata. 20 videos are returned by default but this is customisable.nn
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/523_logo.png
  humanURL: http://vzaar.com/
  baseURL: https://vzaar.com////api/{username}/videos.xml
  tags: Api,Username,Videos,Xml
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/vzaar/apiusernamevideos-xml-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/vzaar/apiusernamevideos-xml-get-openapi.md
- name: Vzaar API
  x-api-slug: vzaar-api
  description: vzaar is anonline video hostingservice with fantasticfeaturesthat are
    designed for business. Deliver tomobileor the web straight from your site.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/523_logo.png
  humanURL: http://vzaar.com/
  baseURL: https://vzaar.com//
  tags: Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/vzaar/openapi.md
x-common:
- type: x-base
  url: http://vzaar.com/api/
- type: x-blog
  url: http://vzaar.com/blog/
- type: x-blog-rss
  url: http://vzaar.com/blog/feed/
- type: x-case-studies
  url: http://vzaar.com/case_studies
- type: x-contact-form
  url: http://vzaar.com/contact/new
- type: x-crunchbase
  url: http://www.crunchbase.com/company/vzaar
- type: x-developer
  url: http://developer.vzaar.com/
- type: x-facebook
  url: https://www.facebook.com/vzaar
- type: x-forum
  url: https://vzaar.com/help/discussions
- type: x-github
  url: https://github.com/vzaar
- type: x-glossary
  url: https://vzaar.com/help/kb/glossary/glossary
- type: x-google-plus
  url: https://plus.google.com/+vzaar_video_hosting
- type: x-knowledgebase
  url: https://vzaar.com/help/kb
- type: x-partners
  url: http://vzaar.com/partners
- type: x-pricing
  url: http://vzaar.com/pricing
- type: x-privacy
  url: http://vzaar.com/privacy
- type: x-terms-of-service
  url: http://vzaar.com/policies
- type: x-twitter
  url: https://twitter.com/vzaar
- type: x-website
  url: http://vzaar.com/
- type: x-website
  url: http://vzaar.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---