---
swagger: "2.0"
x-collection-name: DataAtWork
x-complete: 0
info:
  title: Open Skills API Skill Name Normalization
  description: Retrieves the canonical skill name for a synonymous skill name
  contact:
    name: Work Data Initiative
    url: http://www.dataatwork.org
  version: "1.0"
host: api.dataatwork.org
basePath: /v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /skills/{id}:
    get:
      summary: Skill Name and Description
      description: Retrieves the name, description, and UUID of a job by specifying
        its UUID.
      operationId: retrieves-the-name-description-and-uuid-of-a-job-by-specifying-its-uuid
      x-api-path-slug: skillsid-get
      parameters:
      - in: path
        name: id
        description: The UUID of the skill name to retrieve
      responses:
        200:
          description: OK
      tags:
      - Skill
      - Name
      - Description
  /skills/autocomplete:
    get:
      summary: Skill Name Autocomplete
      description: Retrieves the names, descriptions, and UUIDs of all skills matching
        a given search criteria.
      operationId: retrieves-the-names-descriptions-and-uuids-of-all-skills-matching-a-given-search-criteria
      x-api-path-slug: skillsautocomplete-get
      parameters:
      - in: query
        name: begins_with
        description: Find skill names beginning with the given text fragment
      - in: query
        name: contains
        description: Find skill names containing the given text fragment
      - in: query
        name: ends_with
        description: Find skill names ending with the given text fragment
      responses:
        200:
          description: OK
      tags:
      - Skill
      - Name
      - Autocomplete
  /skills/normalize:
    get:
      summary: Skill Name Normalization
      description: Retrieves the canonical skill name for a synonymous skill name
      operationId: retrieves-the-canonical-skill-name-for-a-synonymous-skill-name
      x-api-path-slug: skillsnormalize-get
      parameters:
      - in: query
        name: skill_name
        description: Find the canonical skill name(s) for skills matching the given
          text fragment
      responses:
        200:
          description: OK
      tags:
      - Skill
      - Name
      - Normalization
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---