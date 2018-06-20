---
name: BC Geographical Names
x-slug: bc-geographical-names
description: Geographical names are more than labels on maps and road signs. They
  can reveal patterns of settlement, exploration and migration, and mirror outside
  influences to our history - aspects of the heritage and promise of an area that
  might otherwise be overlooked or forgotten by visitors and later generations.
image: ""
x-kinRank: "7"
x-alexaRank: "0"
tags: Name
created: "2018-06-20"
modified: "2018-06-20"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bc-geographical-names/apis.md
specificationVersion: "0.14"
apis:
- name: BC Geographical Names Get all name authorities
  x-api-slug: bc-geographical-names
  description: Gets a list of all name authorities responsible for naming decisions
    of the geographical names in the BC Geographical Names Information System (BCGNIS)
  image: ""
  humanURL: https://apps.gov.bc.ca/pub/bcgnws/
  baseURL: https://apps.gov.bc.ca//pub/bcgnws//nameAuthorities
  tags: NameAuthorities
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bc-geographical-names/nameauthorities-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bc-geographical-names/nameauthorities-get-openapi.md
- name: BC Geographical Names Search for names with metadata changes in a given period
  x-api-slug: bc-geographical-names
  description: Search for information about geographical names which have changed
    most recently within a specified time window.  Changes may include status cupdates
    and metadata corrections.
  image: ""
  humanURL: https://apps.gov.bc.ca/pub/bcgnws/
  baseURL: https://apps.gov.bc.ca//pub/bcgnws//names/changes
  tags: Names,Changes
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bc-geographical-names/nameschanges-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bc-geographical-names/nameschanges-get-openapi.md
- name: BC Geographical Names Search for names affected by recent naming decision
  x-api-slug: bc-geographical-names
  description: Search for information about geographical names affected by naming
    'decisions' made by the BC Geographical Names Office (naming authority) within
    the last X days.
  image: ""
  humanURL: https://apps.gov.bc.ca/pub/bcgnws/
  baseURL: https://apps.gov.bc.ca//pub/bcgnws//names/decisions/recent
  tags: Names,Decisions,Recent
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bc-geographical-names/namesdecisionsrecent-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bc-geographical-names/namesdecisionsrecent-get-openapi.md
- name: BC Geographical Names Search for names affected by naming decisions in a given
    year
  x-api-slug: bc-geographical-names
  description: Search for information about geographical names affected by naming
    'decisions' made by the BC Geographical Names Office (naming authority) in a given
    year.
  image: ""
  humanURL: https://apps.gov.bc.ca/pub/bcgnws/
  baseURL: https://apps.gov.bc.ca//pub/bcgnws//names/decisions/year
  tags: Names,Decisions,Year
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bc-geographical-names/namesdecisionsyear-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bc-geographical-names/namesdecisionsyear-get-openapi.md
- name: BC Geographical Names Search in a geographic area
  x-api-slug: bc-geographical-names
  description: Search for information about geographical names that correspond to
    features within a geographic bounding box.  Various options and filter parameters
    are available to refine the search.
  image: ""
  humanURL: https://apps.gov.bc.ca/pub/bcgnws/
  baseURL: https://apps.gov.bc.ca//pub/bcgnws//names/inside
  tags: Names,Inside
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bc-geographical-names/namesinside-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bc-geographical-names/namesinside-get-openapi.md
- name: BC Geographical Names Search near to a geographic point
  x-api-slug: bc-geographical-names
  description: Search for information about geographical names that correspond to
    features within a geographic area defined by a centre point and a radius.  Various
    options and filter parameters are available to refine the search.
  image: ""
  humanURL: https://apps.gov.bc.ca/pub/bcgnws/
  baseURL: https://apps.gov.bc.ca//pub/bcgnws//names/near
  tags: Names,Near
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bc-geographical-names/namesnear-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bc-geographical-names/namesnear-get-openapi.md
- name: BC Geographical Names Search by name, limit to unofficial names only
  x-api-slug: bc-geographical-names
  description: Search for information about unofficial geographical names by the text
    of the name itself.  Various options and filter parameters are available to refine
    the search.
  image: ""
  humanURL: https://apps.gov.bc.ca/pub/bcgnws/
  baseURL: https://apps.gov.bc.ca//pub/bcgnws//names/notOfficial/search
  tags: Names,NotOfficial,Search
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bc-geographical-names/namesnotofficialsearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bc-geographical-names/namesnotofficialsearch-get-openapi.md
- name: BC Geographical Names Search by name, limit to official names only
  x-api-slug: bc-geographical-names
  description: Search for information about official geographical names by the text
    of the name itself.  Various options and filter parameters are available to refine
    the search.
  image: ""
  humanURL: https://apps.gov.bc.ca/pub/bcgnws/
  baseURL: https://apps.gov.bc.ca//pub/bcgnws//names/official/search
  tags: Names,Official,Search
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bc-geographical-names/namesofficialsearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bc-geographical-names/namesofficialsearch-get-openapi.md
- name: BC Geographical Names Search by name
  x-api-slug: bc-geographical-names
  description: Search for information about geographical names by the text of the
    name itself.  The response will include both official and unofficial names.  Various
    options and filter parameters are available to refine the search.
  image: ""
  humanURL: https://apps.gov.bc.ca/pub/bcgnws/
  baseURL: https://apps.gov.bc.ca//pub/bcgnws//names/search
  tags: Names,Search
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bc-geographical-names/namessearch-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bc-geographical-names/namessearch-get-openapi.md
- name: BC Geographical Names Get a name by its nameId
  x-api-slug: bc-geographical-names
  description: Get information about the geographical name with the specified nameId.
  image: ""
  humanURL: https://apps.gov.bc.ca/pub/bcgnws/
  baseURL: https://apps.gov.bc.ca//pub/bcgnws//names/{nameId}.{outputFormat}
  tags: Names,NameId,OutputFormat
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bc-geographical-names/namesnameid-outputformat-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bc-geographical-names/namesnameid-outputformat-get-openapi.md
- name: BC Geographical Names
  x-api-slug: bc-geographical-names
  description: Geographical names are more than labels on maps and road signs. They
    can reveal patterns of settlement, exploration and migration, and mirror outside
    influences to our history - aspects of the heritage and promise of an area that
    might otherwise be overlooked or forgotten by visitors and later generations.
  image: ""
  humanURL: https://apps.gov.bc.ca/pub/bcgnws/
  baseURL: https://apps.gov.bc.ca//pub/bcgnws
  tags: Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/bc-geographical-names/openapi.md
x-common:
- type: x-website
  url: https://apps.gov.bc.ca/pub/bcgnws/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---