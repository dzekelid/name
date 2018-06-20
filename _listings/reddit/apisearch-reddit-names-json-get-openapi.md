---
swagger: "2.0"
x-collection-name: Reddit
x-complete: 0
info:
  title: Reddit Get Search Reddit Names
  description: List subreddit names that begin with a query string.
  version: 1.0.0
host: www.reddit.com
basePath: /
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v1/subreddit/emoji/emoji_name:
    delete&nbsp;:
      summary: Delete Subreddit Emoji Emoji Name
      description: |-
        Delete a Subreddit emoji.
        Remove the emoji from Cassandra and purge the assets from S3
        and the image resizing provider.
      operationId: delete&nbsp;V1SubredditEmojiEmojiName
      x-api-path-slug: v1subredditemojiemoji-name-deletenbsp
      responses:
        200:
          description: OK
      tags:
      - Subreddit
      - Emoji
      - Emoji
      - Name
  /v1/gold/gild/fullname:
    post&nbsp;:
      summary: Add Gold Gild Fullname
      description: fullname of a thing
      operationId: post&nbsp;V1GoldGildFullname
      x-api-path-slug: v1goldgildfullname-postnbsp
      parameters:
      - in: query
        name: fullname
        description: fullname of a thing
        type: string
      responses:
        200:
          description: OK
      tags:
      - Gold
      - Gild
      - Fullname
  /v1/gold/give/username:
    post&nbsp;:
      summary: Add Gold Give Username
      description: an integer between 1 and 36
      operationId: post&nbsp;V1GoldGiveUsername
      x-api-path-slug: v1goldgiveusername-postnbsp
      parameters:
      - in: query
        name: months
        description: an integer between 1 and 36
        type: string
      - in: query
        name: username
        description: A valid, existing reddit username
        type: string
      responses:
        200:
          description: OK
      tags:
      - Gold
      - Give
      - Username
  /by_id/names:
    get:
      summary: Get By Names
      description: Get a listing of links by fullname.
      operationId: get&nbsp;ByNames
      x-api-path-slug: by-idnames-get
      parameters:
      - in: query
        name: names
        description: A comma-separated list of link fullnames
        type: string
      responses:
        200:
          description: OK
      tags:
      - Names
  /multi/rename:
    post&nbsp;:
      summary: Add Multi Rename
      description: Rename a multi.
      operationId: post&nbsp;MultiRename
      x-api-path-slug: multirename-postnbsp
      parameters:
      - in: query
        name: display_name
        description: a string no longer than 50 characters
        type: string
      - in: query
        name: from
        description: multireddit url path
        type: string
      - in: query
        name: to
        description: destination multireddit url path
        type: string
      - in: query
        name: uh / X-Modhash header
        description: a modhash
        type: string
      responses:
        200:
          description: OK
      tags:
      - Multi
      - Rename
  /multi/user/username:
    get&nbsp;:
      summary: Get Multi User Username
      description: Fetch a list of public multis belonging to username
      operationId: get&nbsp;MultiUserUsername
      x-api-path-slug: multiuserusername-getnbsp
      parameters:
      - in: query
        name: expand_srs
        description: boolean value
        type: string
      - in: query
        name: username
        description: A valid, existing reddit username
        type: string
      responses:
        200:
          description: OK
      tags:
      - Multi
      - User
      - Username
  /multi/multipath/r/srname:
    delete&nbsp;:
      summary: Delete Multi Multipath Srname
      description: Remove a subreddit from a multi.
      operationId: delete&nbsp;MultiMultipathRSrname
      x-api-path-slug: multimultipathrsrname-deletenbsp
      parameters:
      - in: query
        name: multipath
        description: multireddit url path
        type: string
      - in: query
        name: srname
        description: subreddit name
        type: string
      - in: query
        name: uh / X-Modhash header
        description: a modhash
        type: string
      responses:
        200:
          description: OK
      tags:
      - Multi
      - Multipath
      - Srname
    get&nbsp;:
      summary: Get Multi Multipath Srname
      description: Get data about a subreddit in a multi.
      operationId: get&nbsp;MultiMultipathRSrname
      x-api-path-slug: multimultipathrsrname-getnbsp
      parameters:
      - in: query
        name: multipath
        description: multireddit url path
        type: string
      - in: query
        name: srname
        description: subreddit name
        type: string
      responses:
        200:
          description: OK
      tags:
      - Multi
      - Multipath
      - Srname
    put&nbsp;:
      summary: Put Multi Multipath Srname
      description: Add a subreddit to a multi.
      operationId: put&nbsp;MultiMultipathRSrname
      x-api-path-slug: multimultipathrsrname-putnbsp
      parameters:
      - in: query
        name: model
        description: 'json data:{  &quot;name&quot;: subreddit name,}'
        type: string
      - in: query
        name: multipath
        description: multireddit url path
        type: string
      - in: query
        name: srname
        description: subreddit name
        type: string
      - in: query
        name: uh / X-Modhash header
        description: a modhash
        type: string
      responses:
        200:
          description: OK
      tags:
      - Multi
      - Multipath
      - Srname
  /recommend/sr/srnames:
    get&nbsp;:
      summary: Get Recommend Sr Srnames
      description: Return subreddits recommended for the given subreddit(s).
      operationId: get&nbsp;RecommendSrSrnames
      x-api-path-slug: recommendsrsrnames-getnbsp
      parameters:
      - in: query
        name: omit
        description: comma-delimited list of subreddit names
        type: string
      - in: query
        name: over_18
        description: boolean value
        type: string
      - in: query
        name: srnames
        description: comma-delimited list of subreddit names
        type: string
      responses:
        200:
          description: OK
      tags:
      - Recommend
      - Sr
      - Srnames
  /api/search_reddit_names.json:
    get:
      summary: Get Search Reddit Names
      description: List subreddit names that begin with a query string.
      operationId: get&nbsp;SearchRedditNames
      x-api-path-slug: apisearch-reddit-names-json-get
      parameters:
      - in: query
        name: exact
        description: boolean value
        type: string
      - in: query
        name: include_over_18
        description: boolean value
        type: string
      - in: query
        name: include_unadvertisable
        description: boolean value
        type: string
      - in: query
        name: query
        description: a string up to 50 characters long, consisting of printable characters
        type: string
      responses:
        200:
          description: OK
      tags:
      - Search
      - Reddit
      - Names
x-streamrank:
  polling_total_time_average: "0.56"
  polling_size_download_average: "376.76"
  streaming_total_time_average: "0.36"
  streaming_size_download_average: "301.15"
  change_yes: "10"
  change_no: "195"
  time_percentage: "35"
  size_percentage: "20"
  change_percentage: "5"
  last_run: "2018-05-06"
  days_run: "1"
  minute_run: "0"
---