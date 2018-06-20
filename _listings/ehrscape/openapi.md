---
swagger: "2.0"
x-collection-name: EhrScape
x-complete: 1
info:
  title: Ehr Scape Electronic Health Record APIs
  description: a-simple-yet-powerful-services-to-store-retrieve-and-query-health-data
  version: 1.0.0
host: rest.ehrscape.com
basePath: /rest/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /form/{name}/{version}:
    get:
      summary: Loads a Think!Ehr form.
      description: Loads a think!ehr form..
      operationId: getForm
      x-api-path-slug: formnameversion-get
      parameters:
      - in: path
        name: name
        description: The name of the form
      - in: query
        name: resources
        description: Which, if any, resources to expand
      - in: path
        name: version
        description: The version of the form, such as 1
      responses:
        200:
          description: OK
      tags:
      - Form
      - Name
      - Version
  /form/{name}/{version}/resource/{resource}:
    get:
      summary: Loads a Think!Ehr form resource content.
      description: Loads a think!ehr form resource content..
      operationId: getFormResource
      x-api-path-slug: formnameversionresourceresource-get
      parameters:
      - in: query
        name: envelope
        description: Whether or not to wrap a response in a JSON object that includes
          meta-data, or just return the resource content (default)
      - in: path
        name: name
        description: The name of the form
      - in: path
        name: resource
        description: The name of the form resource
      - in: path
        name: version
        description: The version of the form, such as 1
      responses:
        200:
          description: OK
      tags:
      - Form
      - Name
      - Version
      - Resource
      - Resource
  /session/ehr/{subjectNamespace}/{subjectId}:
    put:
      summary: Sets the EHR on the session (via subject namespace and ID).
      description: Sets the ehr on the session (via subject namespace and id)..
      operationId: findAndUseEhr
      x-api-path-slug: sessionehrsubjectnamespacesubjectid-put
      parameters:
      - in: header
        name: Ehr-Session
        description: The ID of the session to set the EHR on
      - in: query
        name: sessionId
        description: The ID of the session to set the EHR on
      - in: path
        name: subjectId
        description: The subject ID
      - in: path
        name: subjectNamespace
        description: The namespace where the subject ID lives
      responses:
        200:
          description: OK
      tags:
      - Session
      - Ehr
      - SubjectNamespace
      - SubjectId
  /smart/records/{ehrId}/{modelName}:
    get:
      summary: Returns SMART records for a patient.
      description: Returns smart records for a patient..
      operationId: getRecords
      x-api-path-slug: smartrecordsehridmodelname-get
      parameters:
      - in: path
        name: ehrId
        description: EHR id
      - in: path
        name: modelName
        description: SMART model name
      responses:
        200:
          description: OK
      tags:
      - Smart
      - Records
      - EhrId
      - ModelName
  /smart/records/{ehrId}/{modelName}/{recordId}:
    get:
      summary: Returns specific SMART record for a patient.
      description: Returns specific smart record for a patient..
      operationId: getRecord
      x-api-path-slug: smartrecordsehridmodelnamerecordid-get
      parameters:
      - in: path
        name: ehrId
        description: EHR id
      - in: path
        name: modelName
        description: SMART model name
      - in: path
        name: recordId
        description: Record id
      responses:
        200:
          description: OK
      tags:
      - Smart
      - Records
      - EhrId
      - ModelName
      - RecordId
---