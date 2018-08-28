---
name: HERE
x-slug: here
description: HERE Technologies enables people, enterprises and cities around the world
  to harness the power of location and create innovative solutions that make our lives
  safer and more efficient. We transform information from devices, vehicles, infrastructure
  and...
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
x-kinRank: "7"
x-alexaRank: "3011"
tags: Name
created: "2018-08-28"
modified: "2018-08-28"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/here/apis.md
specificationVersion: "0.14"
apis:
- name: Public Transport API - Find Stations by Name
  x-api-slug: searchby-name-json-get
  description: "*Request a list of public transit stations based on name*\n\nA station
    search request can be made using the `search/by_name.json` endpoint and adding
    the `name` parameter. The focal point of the search is defined using the `x` and
    `y` parameters. The number of results can be further restricted by `max `and the
    `radius `parameters.\n  \n\n\n\n* **x**  `number`\n \\- The longitude of the center
    point of your search.    e.g. `13.377`\n\n* **y**  `number`\n \\- The latitude
    of the center point of your search.    e.g. `52.515`\n\n* **name**  `text`\n \\-
    Specifies the name or a part of the name of the station to search for and can
    be one word, multiple words or partial word separated by either comma or space.\n\n*
    **app_id**  `text`\n \\- A 20 bytes Base64 URL-safe encoded string used for the
    authentication of the client application.    You must include an app_code and
    app_code with every request.\n\n* **app_code**  `text`\n \\- A 20 bytes Base64
    URL-safe encoded string used for the authentication of the client application.
    \   You must include an app_code and app_code with every request.\n\n* **max**
    \ `number`\n \\- Specifies the maximum number of stations/stops included in the
    response.\n  The minimum value is 1 and the maximum value is not limited.\n  The
    default value is 5.     \n\n* **method**  `enum`\n \\- Specifies if the matching
    method is *fuzzy* or *strict*.\n  The default value is *fuzzy*.\n    * fuzzy -
    search for stations with the name having similar sounding and/or similar spelling
    to the names requested\n    * strict - search for stations with the name exactly
    matching the names requested or contains it as its part.\n\n   Valid values are
    : `fuzzy`, `strict`\n\n* **radius**  `number`\n \\- Specifies a radius in meters
    when combined with a center point defines the area of the search. The minimum
    value is 0 and the maximum value is not limited.\n  The default value is 20000km."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/20089-here-maps.jpg
  humanURL: https://developer.here.com
  baseURL: https://cit.transit.api.here.com//
  tags: Technology, Mobile, internet, API Provider, Profiles, General Data, Relative
    Data, Maps
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/here/searchby-name-json-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/here/searchby-name-json-get-openapi.md
x-common:
- type: x-blog-rss
  url: https://developer.here.com/blog/feed
- type: x-github
  url: https://github.com/heremaps
- type: x-postman-collection
  url: https://github.com/heremaps/postman-collections
- type: x-api-gallery
  url: http://healthcare.gov.api.gallery.streamdata.io
- type: x-api-stack
  url: http://here.stack.network
- type: x-blog
  url: https://developer.here.com/blog
- type: x-crunchbase
  url: https://crunchbase.com/organization/here-inc
- type: x-developer
  url: https://developer.here.com
- type: x-email
  url: dirk.popp@here.com
- type: x-email
  url: sebastian.kurme@here.com
- type: x-email
  url: jordan.stark@here.com
- type: x-email
  url: amy.stupavsky@here.com
- type: x-email
  url: minna.laub@here.com
- type: x-email
  url: stefanie.sirc@here.com
- type: x-email
  url: rachel.kuta@here.com
- type: x-email
  url: laurel.davis-lyons@here.com
- type: x-email
  url: linda.bradley@here.com
- type: x-email
  url: press@here.com
- type: x-twitter
  url: https://twitter.com/here
- type: x-website
  url: https://here.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---