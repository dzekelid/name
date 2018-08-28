swagger: "2.0"
x-collection-name: Reddit
x-complete: 1
info:
  title: Reddit
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