---
swagger: "2.0"
x-collection-name: SendGrid
x-complete: 0
info:
  title: SendGrid Delete Subusers Subuser Name Monitor
  description: Subuser monitor settings allow you to receive a sample of an outgoing
    message by a specific customer at a specific frequency of emails.
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
  /ips/pools/{pool_name}/ips:
    post:
      summary: Add Ips Pools Pool Name Ips
      description: |-
        **This endpoint allows you to add an IP address to an IP pool.**

        You can add the same IP address to multiple pools. It may take up to 60 seconds for your IP address to be added to a pool after your request is made.

        A single IP address or a range of IP addresses may be dedicated to an account in order to send email for multiple domains. The reputation of this IP is based on the aggregate performance of all the senders who use it.
      operationId: ips.pools.pool_name.ips.post
      x-api-path-slug: ipspoolspool-nameips-post
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
      - Ips
  /ips/pools/{pool_name}/ips/{ip}:
    delete:
      summary: Delete Ips Pools Pool Name Ips Ip
      description: |-
        **This endpoint allows you to remove an IP address from an IP pool.**

        The same IP address can be added to multiple IP pools.

        A single IP address or a range of IP addresses may be dedicated to an account in order to send email for multiple domains. The reputation of this IP is based on the aggregate performance of all the senders who use it.
      operationId: ips.pools.pool_name.ips.ip.delete
      x-api-path-slug: ipspoolspool-nameipsip-delete
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
      - Ips
      - Ip
  /subusers/{subuser_name}:
    delete:
      summary: Delete Subusers Subuser Name
      description: |-
        This endpoint allows you to delete a subuser. This is a permanent action, once deleted a subuser cannot be retrieved.

        For more information about Subusers:

        * [User Guide > Subusers](https://sendgrid.com/docs/User_Guide/Settings/Subusers/index.html)
        * [Classroom > How do I add more subusers to my account?](https://sendgrid.com/docs/Classroom/Basics/Account/how_do_i_add_more_subusers_to_my_account.html)
      operationId: subusers.subuser_name.delete
      x-api-path-slug: subuserssubuser-name-delete
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
      - Subusers
      - Subuser
      - Name
    patch:
      summary: Patch Subusers Subuser Name
      description: |-
        This endpoint allows you to enable or disable a subuser.

        For more information about Subusers:

        * [User Guide > Subusers](https://sendgrid.com/docs/User_Guide/Settings/Subusers/index.html)
        * [Classroom > How do I add more subusers to my account?](https://sendgrid.com/docs/Classroom/Basics/Account/how_do_i_add_more_subusers_to_my_account.html)
      operationId: subusers.subuser_name.patch
      x-api-path-slug: subuserssubuser-name-patch
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
      - Subusers
      - Subuser
      - Name
  /subusers/{subuser_name}/ips:
    put:
      summary: Put Subusers Subuser Name Ips
      description: "Each subuser should be assigned to an IP address, from which all
        of this subuser's mail will be sent. Often, this is the same IP as the parent
        account, but each subuser can have their own, or multiple, IP addresses as
        well. \n\nMore information:\n\n* [How to request more IPs](https://sendgrid.com/docs/Classroom/Basics/Account/adding_an_additional_dedicated_ip_to_your_account.html)\n*
        [IPs can be whitelabeled](https://sendgrid.com/docs/User_Guide/Settings/Whitelabel/ips.html)"
      operationId: subusers.subuser_name.ips.put
      x-api-path-slug: subuserssubuser-nameips-put
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Subusers
      - Subuser
      - Name
      - Ips
  /subusers/{subuser_name}/monitor:
    delete:
      summary: Delete Subusers Subuser Name Monitor
      description: Subuser monitor settings allow you to receive a sample of an outgoing
        message by a specific customer at a specific frequency of emails.
      operationId: subusers.subuser_name.monitor.delete
      x-api-path-slug: subuserssubuser-namemonitor-delete
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: No Name
      responses:
        200:
          description: OK
      tags:
      - Email
      - Subusers
      - Subuser
      - Name
      - Monitor
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