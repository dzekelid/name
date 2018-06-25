---
name: EhrScape
x-slug: ehrscape
description: Health app development shouldnt be harder than other verticals. EhrScape
  is all about making awesome healthcare apps easy to build and integrate into your
  environment. Healthcare computing that just works. EhrScape handles all the hard
  bits, including detailed clinical models, semantic interoperability, vendor independent
  data storage, health data query and more. Our mission is to empower you to build
  amazing healthcare apps and services. Welcome aboard. Were just getting started
  and weve got very big plans!
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/EHRScape-Logo.png
x-kinRank: "8"
x-alexaRank: "0"
tags: Name
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/ehrscape/apis.md
specificationVersion: "0.14"
apis:
- name: Ehr Scape Electronic Health Record APIs Loads a Think!Ehr form.
  x-api-slug: ehr-scape-electronic-health-record-apis
  description: Loads a think!ehr form..
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/EHRScape-Logo.png
  humanURL: https://www.ehrscape.com
  baseURL: https://rest.ehrscape.com//rest/v1//form/{name}/{version}
  tags: Form,Name,Version
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/ehrscape/formnameversion-get-openapi.md
- name: Ehr Scape Electronic Health Record APIs Loads a Think!Ehr form resource content.
  x-api-slug: ehr-scape-electronic-health-record-apis
  description: Loads a think!ehr form resource content..
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/EHRScape-Logo.png
  humanURL: https://www.ehrscape.com
  baseURL: https://rest.ehrscape.com//rest/v1//form/{name}/{version}/resource/{resource}
  tags: Form,Name,Version,Resource,Resource
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/ehrscape/formnameversionresourceresource-get-openapi.md
- name: Ehr Scape Electronic Health Record APIs Sets the EHR on the session (via subject
    namespace and ID).
  x-api-slug: ehr-scape-electronic-health-record-apis
  description: Sets the ehr on the session (via subject namespace and id)..
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/EHRScape-Logo.png
  humanURL: https://www.ehrscape.com
  baseURL: https://rest.ehrscape.com//rest/v1//session/ehr/{subjectNamespace}/{subjectId}
  tags: Session,Ehr,SubjectNamespace,SubjectId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/ehrscape/sessionehrsubjectnamespacesubjectid-put-openapi.md
- name: Ehr Scape Electronic Health Record APIs Returns SMART records for a patient.
  x-api-slug: ehr-scape-electronic-health-record-apis
  description: Returns smart records for a patient..
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/EHRScape-Logo.png
  humanURL: https://www.ehrscape.com
  baseURL: https://rest.ehrscape.com//rest/v1//smart/records/{ehrId}/{modelName}
  tags: Smart,Records,EhrId,ModelName
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/ehrscape/smartrecordsehridmodelname-get-openapi.md
- name: Ehr Scape Electronic Health Record APIs Returns specific SMART record for
    a patient.
  x-api-slug: ehr-scape-electronic-health-record-apis
  description: Returns specific smart record for a patient..
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/EHRScape-Logo.png
  humanURL: https://www.ehrscape.com
  baseURL: https://rest.ehrscape.com//rest/v1//smart/records/{ehrId}/{modelName}/{recordId}
  tags: Smart,Records,EhrId,ModelName,RecordId
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/ehrscape/smartrecordsehridmodelnamerecordid-get-openapi.md
- name: Ehr Scape Electronic Health Record APIs
  x-api-slug: ehr-scape-electronic-health-record-apis
  description: Health app development shouldnt be harder than other verticals. EhrScape
    is all about making awesome healthcare apps easy to build and integrate into your
    environment. Healthcare computing that just works. EhrScape handles all the hard
    bits, including detailed clinical models, semantic interoperability, vendor independent
    data storage, health data query and more. Our mission is to empower you to build
    amazing healthcare apps and services. Welcome aboard. Were just getting started
    and weve got very big plans!
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/EHRScape-Logo.png
  humanURL: https://www.ehrscape.com
  baseURL: https://rest.ehrscape.com//rest/v1
  tags: Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/ehrscape/openapi.md
x-common:
- type: x-contact-form
  url: https://www.ehrscape.com/contact.html
- type: x-faq
  url: https://www.ehrscape.com/index.html
- type: x-github
  url: https://github.com/ehrscape
- type: x-privacy
  url: https://www.ehrscape.com/privacy.html
- type: x-terms-of-service
  url: https://www.ehrscape.com/terms.html
- type: x-twitter
  url: https://twitter.com/ehrscape
- type: x-website
  url: https://www.ehrscape.com
- type: x-website
  url: http://ehrscape.com
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---