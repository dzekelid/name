---
swagger: "2.0"
x-collection-name: VictorOps
x-complete: 0
info:
  title: Victor Ops Get a rule from a paging policy step
  description: |-
    Get a rule from a paging policy step

    This API may be called a maximum of 15 times per minute.
  version: 0.0.2
host: api.victorops.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api-public/v1/profile/{username}/policies:
    get:
      summary: Get the user's paging policy
      description: |-
        Get all the paging policy steps for the user on the org associated with the API key

        This API may be called a maximum of 15 times per minute.
      operationId: api_public.v1.profile.username.policies.get
      x-api-path-slug: apipublicv1profileusernamepolicies-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Profile
      - Username
      - Policies
    post:
      summary: Create a paging policy step
      description: |-
        Create a paging policy step

        This API may be called a maximum of 15 times per minute.
      operationId: api_public.v1.profile.username.policies.post
      x-api-path-slug: apipublicv1profileusernamepolicies-post
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Profile
      - Username
      - Policies
  /api-public/v1/profile/{username}/policies/{step}:
    get:
      summary: Get a paging policy step
      description: |-
        Get a paging policy step

        This API may be called a maximum of 15 times per minute.
      operationId: api_public.v1.profile.username.policies.step.get
      x-api-path-slug: apipublicv1profileusernamepoliciesstep-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Profile
      - Username
      - Policies
      - Step
    post:
      summary: Create a rule for a paging policy step
      description: |-
        Create a rule for a paging policy step

        This API may be called a maximum of 15 times per minute.
      operationId: api_public.v1.profile.username.policies.step.post
      x-api-path-slug: apipublicv1profileusernamepoliciesstep-post
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Profile
      - Username
      - Policies
      - Step
    put:
      summary: Update a paging policy step
      description: |-
        Update a paging policy step

        This API may be called a maximum of 15 times per minute.
      operationId: api_public.v1.profile.username.policies.step.put
      x-api-path-slug: apipublicv1profileusernamepoliciesstep-put
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Profile
      - Username
      - Policies
      - Step
  /api-public/v1/profile/{username}/policies/{step}/{rule}:
    delete:
      summary: Delete a rule from a paging policy step
      description: |-
        Delete a rule from a paging policy step

        This API may be called a maximum of 15 times per minute.
      operationId: api_public.v1.profile.username.policies.step.rule.delete
      x-api-path-slug: apipublicv1profileusernamepoliciessteprule-delete
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Profile
      - Username
      - Policies
      - Step
      - Rule
    get:
      summary: Get a rule from a paging policy step
      description: |-
        Get a rule from a paging policy step

        This API may be called a maximum of 15 times per minute.
      operationId: api_public.v1.profile.username.policies.step.rule.get
      x-api-path-slug: apipublicv1profileusernamepoliciessteprule-get
      parameters:
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Profile
      - Username
      - Policies
      - Step
      - Rule
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