---
swagger: "2.0"
x-collection-name: DataAtWork
x-complete: 1
info:
  title: Open Skills API
  description: a-complete-and-standard-data-store-for-canonical-and-emerging-skills-knowledge-abilities-tools-technolgies-and-how-they-relate-to-jobs-
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
  /skills:
    get:
      summary: Skill Names and Descriptions
      description: Retrieve the names, descriptions, and UUIDs of all skills.
      operationId: retrieve-the-names-descriptions-and-uuids-of-all-skills
      x-api-path-slug: skills-get
      parameters:
      - in: query
        name: limit
        description: Maximum number of items per page
      - in: query
        name: offset
        description: Pagination offset
      responses:
        200:
          description: OK
      tags:
      - Skill
      - Names
      - Descriptions
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
---