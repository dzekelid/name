---
swagger: "2.0"
x-collection-name: SendGrid
x-complete: 0
info:
  title: SendGrid Put Ips Pools Pool Name
  description: |-
    **This endpoint allows you to update the name of an IP pool.**

    IP Pools allow you to group your dedicated SendGrid IP addresses together. For example, you could create separate pools for your transactional and marketing email. When sending marketing emails, specify that you want to use the marketing IP pool. This allows you to maintain separate reputations for your different email traffic.

    IP pools can only be used with whitelabeled IP addresses.

    If an IP pool is NOT specified for an email, it will use any IP available, including ones in pools.
  version: 1.0.0
host: api.sendgrid.com
basePath: /v3
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /ips/pools/{pool_name}:
    delete:
      summary: Delete Ips Pools Pool Name
      description: |-
        **This endpoint allows you to delete an IP pool.**

        IP Pools allow you to group your dedicated SendGrid IP addresses together. For example, you could create separate pools for your transactional and marketing email. When sending marketing emails, specify that you want to use the marketing IP pool. This allows you to maintain separate reputations for your different email traffic.

        IP pools can only be used with whitelabeled IP addresses.

        If an IP pool is NOT specified for an email, it will use any IP available, including ones in pools.
      operationId: ips.pools.pool_name.delete
      x-api-path-slug: ipspoolspool-name-delete
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Email
      - Ips
      - Pools
      - Pool
      - Name
    get:
      summary: Get Ips Pools Pool Name
      description: |-
        **This endpoint allows you to list all of the IP addresses that are in a specific IP pool.**

        IP Pools allow you to group your dedicated SendGrid IP addresses together. For example, you could create separate pools for your transactional and marketing email. When sending marketing emails, specify that you want to use the marketing IP pool. This allows you to maintain separate reputations for your different email traffic.

        IP pools can only be used with whitelabeled IP addresses.

        If an IP pool is NOT specified for an email, it will use any IP available, including ones in pools.
      operationId: ips.pools.pool_name.get
      x-api-path-slug: ipspoolspool-name-get
      responses:
        200:
          description: OK
      tags:
      - Email
      - Ips
      - Pools
      - Pool
      - Name
    put:
      summary: Put Ips Pools Pool Name
      description: |-
        **This endpoint allows you to update the name of an IP pool.**

        IP Pools allow you to group your dedicated SendGrid IP addresses together. For example, you could create separate pools for your transactional and marketing email. When sending marketing emails, specify that you want to use the marketing IP pool. This allows you to maintain separate reputations for your different email traffic.

        IP pools can only be used with whitelabeled IP addresses.

        If an IP pool is NOT specified for an email, it will use any IP available, including ones in pools.
      operationId: ips.pools.pool_name.put
      x-api-path-slug: ipspoolspool-name-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Email
      - Ips
      - Pools
      - Pool
      - Name
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