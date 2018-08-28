---
name: Fire Browse Beta API
x-slug: fire-browse-beta-api
description: A simple and elegant way to explore cancer data. Sitting above one of
  the deepest and most integratively characterized open cancer datasets in the world.
  Backed by a powerful computational infrastructure, application programming interface
  (API), graphical tools and online reports. With over 80K sample aliquots from 11,000+
  cancer patients, spanning 38 unique disease cohorts.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
x-kinRank: "7"
x-alexaRank: "0"
tags: Name
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/fire-browse-beta-api/apis.md
specificationVersion: "0.14"
apis:
- name: Fire Browse Beta API Retrieve names of all TCGA clinical data elements (CDEs).
  x-api-slug: fire-browse-beta-api
  description: Retrieve names of all patient-level clinical data elements (CDES) available
    in TCGA, unioned across all disease cohorts. A CDE will be listed here only when
    it has a value other than NA for at least 1 patient case in any disease cohort.
    For more information on how these CDEs are processed see our pipeline documentation.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1//Metadata/ClinicalNames
  tags: Metadata,ClinicalNames
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/fire-browse-beta-api/metadataclinicalnames-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/fire-browse-beta-api/metadataclinicalnames-get-openapi.md
- name: Fire Browse Beta API Retrieve names of CDEs normalized by Firehose and selected
    for analyses.
  x-api-slug: fire-browse-beta-api
  description: This service returns the names of patient-level clinical data elements
    (CDEs) that have been normalized by Firehose for use in analyses, unioned across
    all disease cohorts. For more information on how these CDEs are processed, see
    our pipeline documentation.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1//Metadata/ClinicalNames_FH
  tags: Metadata,ClinicalNames,FH
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/fire-browse-beta-api/metadataclinicalnames-fh-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/fire-browse-beta-api/metadataclinicalnames-fh-get-openapi.md
- name: Fire Browse Beta API Retrieve names of all columns in the mutation annotation
    files (MAFs) served by FireBrowse.
  x-api-slug: fire-browse-beta-api
  description: Retrieve the names of all columns in the mutation annotation files
    (MAFs) hosted by FireBrowse.  For more information on the mutation data, and how
    it is processed by Firehose, please consult the pipeline documentation.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1//Metadata/MAFColNames
  tags: Metadata,MAFColNames
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/fire-browse-beta-api/metadatamafcolnames-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/fire-browse-beta-api/metadatamafcolnames-get-openapi.md
- name: Fire Browse Beta API
  x-api-slug: fire-browse-beta-api
  description: A simple and elegant way to explore cancer data. Sitting above one
    of the deepest and most integratively characterized open cancer datasets in the
    world. Backed by a powerful computational infrastructure, application programming
    interface (API), graphical tools and online reports. With over 80K sample aliquots
    from 11,000+ cancer patients, spanning 38 unique disease cohorts.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/firebrowse.png
  humanURL: http://firebrowse.org
  baseURL: https://firebrowse.org//api/v1
  tags: Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/fire-browse-beta-api/openapi.md
x-common:
- type: x-website
  url: http://firebrowse.org
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---