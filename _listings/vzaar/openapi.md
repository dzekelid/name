---
swagger: "2.0"
x-collection-name: Vzaar
x-complete: 1
info:
  title: VZaar API
  description: vzaar-is-an-online-video-hosting-service-with-fantastic-features-that-are-designed-for-business--deliver-to-mobile-or-the-web-straight-from-your-site-
  termsOfService: http://vzaar.com/policies
  version: v1
host: vzaar.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /api/users/{username}.{format}:
    get:
      summary: Get Api Users Username
      description: nnThis API call returns the users public details along with its
        relevant metadata.nn
      operationId: getApiUsersUsername.Format
      x-api-path-slug: apiusersusername-format-get
      parameters:
      - in: query
        name: 'username is the vzaar login name for the user. Note: This must be the
          actual username and not the email address'
      responses:
        200:
          description: OK
      tags:
      - Api
      - Users
      - Username
      - Format
  /api/{username}/videos.xml:
    get:
      summary: Get Api Username Videos
      description: nnThis API call returns a list of the users active videos along
        with its relevant metadata. 20 videos are returned by default but this is
        customisable.nn
      operationId: getApiUsernameVeos.xml
      x-api-path-slug: apiusernamevideos-xml-get
      parameters:
      - in: query
        name: count,
        description: Specifies the number of videos to retrieve per page
      - in: query
        name: page,
        description: Specifies the page number to retrieve
      - in: query
        name: sort,
        description: Values can be asc (least_recent) or desc (most_recent)
      - in: query
        name: status,
        description: Values can be processing, active, replaced, deleted and failed
      - in: query
        name: title,
        description: Return only videos with title containing given string
      - in: query
        name: 'username is the vzaar login name for the user. Note: This must be the
          actual username and not the email address'
      responses:
        200:
          description: OK
      tags:
      - Api
      - Username
      - Videos
      - Xml
---