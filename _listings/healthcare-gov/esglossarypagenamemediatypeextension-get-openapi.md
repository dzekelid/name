---
swagger: "2.0"
x-collection-name: Healthcare.gov
x-complete: 0
info:
  title: HealthCare.gov Get Es Glossary Pagename
  version: 1.0.0
  description: Returns pages content.
host: www.healthcare.gov
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /blog/{pageName}{mediaTypeExtension}:
    get:
      summary: Get Blog Pagename
      description: Returns pages content.
      operationId: getBlogPagenameMediatypeextension
      x-api-path-slug: blogpagenamemediatypeextension-get
      parameters:
      - in: path
        name: mediaTypeExtension
        description: Omiting the param causes html to be returned
      - in: path
        name: pageName
      responses:
        200:
          description: OK
      tags:
      - Blog
      - Pagename
  /es/blog/{pageName}{mediaTypeExtension}:
    get:
      summary: Get Es Blog Pagename
      description: Returns pages content.
      operationId: getEsBlogPagenameMediatypeextension
      x-api-path-slug: esblogpagenamemediatypeextension-get
      parameters:
      - in: path
        name: mediaTypeExtension
        description: Omiting the param causes html to be returned
      - in: path
        name: pageName
      responses:
        200:
          description: OK
      tags:
      - Es
      - Blog
      - Pagename
  /es/glossary/{pageName}{mediaTypeExtension}:
    get:
      summary: Get Es Glossary Pagename
      description: Returns pages content.
      operationId: getEsGlossaryPagenameMediatypeextension
      x-api-path-slug: esglossarypagenamemediatypeextension-get
      parameters:
      - in: path
        name: mediaTypeExtension
        description: Omiting the param causes html to be returned
      - in: path
        name: pageName
      responses:
        200:
          description: OK
      tags:
      - Es
      - Glossary
      - Pagename
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