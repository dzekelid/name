---
swagger: "2.0"
x-collection-name: Instructure
x-complete: 1
info:
  title: Instructure Canvas Users API
  description: canvas-lms-includes-a-rest-api-for-accessing-and-modifying-data-externally-from-the-main-application-in-your-own-programs-and-scripts--
  termsOfService: https://www.canvaslms.com/policies/api-policy
  version: v1
host: canvas.instructure.com
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /users/self/course_nicknames:
    delete:
      summary: Clear course nicknames
      description: Clear course nicknames.
      operationId: clear-course-nicknames
      x-api-path-slug: usersselfcourse-nicknames-delete
      responses:
        200:
          description: OK
      tags:
      - Users
      - Self
      - Course
      - Nicknames
    get:
      summary: List course nicknames
      description: List course nicknames.
      operationId: list-course-nicknames
      x-api-path-slug: usersselfcourse-nicknames-get
      responses:
        200:
          description: OK
      tags:
      - Users
      - Self
      - Course
      - Nicknames
  /users/self/course_nicknames/{course_id}:
    delete:
      summary: Remove course nickname
      description: Remove course nickname.
      operationId: remove-course-nickname
      x-api-path-slug: usersselfcourse-nicknamescourse-id-delete
      responses:
        200:
          description: OK
      tags:
      - Users
      - Self
      - Course
      - Nicknames
      - Course
      - Id
    get:
      summary: Get course nickname
      description: Get course nickname.
      operationId: get-course-nickname
      x-api-path-slug: usersselfcourse-nicknamescourse-id-get
      responses:
        200:
          description: OK
      tags:
      - Users
      - Self
      - Course
      - Nicknames
      - Course
      - Id
    put:
      summary: Set course nickname
      description: Set course nickname.
      operationId: set-course-nickname
      x-api-path-slug: usersselfcourse-nicknamescourse-id-put
      parameters:
      - in: query
        name: nickname
        description: The nickname to set
      responses:
        200:
          description: OK
      tags:
      - Users
      - Self
      - Course
      - Nicknames
      - Course
      - Id
---