---
name: IBM Cloud
x-slug: ibm-cloud
description: The IBM Cloud has been built to help you solve problems and advance opportunities
  in a world flush with data. Whether it&rsquo;s data you possess, data outside your
  firewall, or data that&rsquo;s coming, the IBM Cloud helps you protect it, move
  it, integrate it and unlock intelligence from it &mdash; giving you what it takes
  to prevail in a competitive market.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
x-kinRank: "8"
x-alexaRank: "11207"
tags: Name
created: "2018-06-25"
modified: "2018-06-25"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/ibm-cloud/apis.md
specificationVersion: "0.14"
apis:
- name: IBM Containers Stop and delete all container instances in a container group.
  x-api-slug: ibm-containers
  description: 'Stops and deletes the container instances that run in a container
    group (corresponding IBM Containers command: `cf ic group rm <group_name>`). When
    you delete a container group, all floating private IP addresses are released.'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3//containers/groups/{name_or_id}
  tags: Containers,Groups,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/ibm-cloud/containersgroupsname-or-id-delete-openapi.md
- name: IBM Containers Inspect a container group.
  x-api-slug: ibm-containers
  description: 'This endpoint retrieves detailed information about a container group
    with a given name (corresponding IBM Containers command: `cf ic group inspect
    GROUP`).'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3//containers/groups/{name_or_id}
  tags: Containers,Groups,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/ibm-cloud/containersgroupsname-or-id-get-openapi.md
- name: IBM Containers Update a container group.
  x-api-slug: ibm-containers
  description: "Update the number of container instances that run in a container group
    (corresponding IBM Containers command: `cf ic group update <option> <group>`).
    \n\nNote: You can run only one update at a time.  \n\n The desired number is the
    number of container instances that you require. It must be within the current
    limits of Max and Min. To increase the number of desired container instances above
    the Max value, you must first execute an update on the Max value. Once this update
    is completed, you can increase the desired number of container instances."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3//containers/groups/{name_or_id}
  tags: Containers,Groups,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/ibm-cloud/containersgroupsname-or-id-patch-openapi.md
- name: IBM Containers Map a public route to a container group.
  x-api-slug: ibm-containers
  description: 'If you want your container group to be accessible from the Internet,
    you need to expose a public port and map a public route to it (corresponding IBM
    Containers command: `cf ic route map -n <host> -d <domain> <group>`). Every route
    consists of the host name and domain.'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3//containers/groups/{name_or_id}/maproute
  tags: Containers,Groups,Name,Maproute
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/ibm-cloud/containersgroupsname-or-idmaproute-post-openapi.md
- name: IBM Containers Unmap a public route from a container group
  x-api-slug: ibm-containers
  description: "This endpoint unmaps a public route from a container group (corresponding
    IBM Containers command: `cf ic route unmap -n <host> -d <domain> <group>`). If
    no other public route is mapped to the container group, then the container group
    is no longer available from the internet. \n\n When you unmap a route from a container
    group, the route is not deleted and can be mapped to other container groups."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3//containers/groups/{name_or_id}/unmaproute
  tags: Containers,Groups,Name,Unmaproute
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/ibm-cloud/containersgroupsname-or-idunmaproute-post-openapi.md
- name: IBM Containers Remove a single container
  x-api-slug: ibm-containers
  description: 'Remove a single container that is identified by container ID or name
    from a space (corresponding IBM Containers command: `cf ic delete <container>`).
    The container must be stopped before it can be deleted, unless the `force` query
    parameter is set to true.'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3//containers/{name_or_id}
  tags: Containers,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/ibm-cloud/containersname-or-id-delete-openapi.md
- name: IBM Containers Bind a public IP address to a single container
  x-api-slug: ibm-containers
  description: 'This endpoint binds an available public IP address to a single container
    (corresponding IBM Containers command: `cf ic ip bind <ip_adress> <container>`).
    After a container is bound to a public IP address, it can be accessed at `https://<public_ip_adress>:<public_port>`.'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3//containers/{name_or_id}/floating-ips/{ip}/bind
  tags: Containers,Name,Floating-ips,Ip,Bind
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/ibm-cloud/containersname-or-idfloatingipsipbind-post-openapi.md
- name: IBM Containers Unbind a public IP address from a container
  x-api-slug: ibm-containers
  description: 'This endpoint unbinds a public IP address from a container (corresponding
    IBM Containers command: `cf ic ip unbind <ip_adress> <container>`). The container
    that is unbound from the IP address will not be accessible from the internet anymore.
    The public IP address will be further allocated to the space and can be used to
    be bound to other containers.'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3//containers/{name_or_id}/floating-ips/{ip}/unbind
  tags: Containers,Name,Floating-ips,Ip,Unbind
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/ibm-cloud/containersname-or-idfloatingipsipunbind-post-openapi.md
- name: IBM Containers Inspect a single container
  x-api-slug: ibm-containers
  description: 'This endpoint retrieves detailed information about a single container
    (corresponding IBM Containers command: `cf ic inspect <container>`).'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3//containers/{name_or_id}/json
  tags: Containers,Name,Json
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/ibm-cloud/containersname-or-idjson-get-openapi.md
- name: IBM Containers Pause a single container
  x-api-slug: ibm-containers
  description: 'Pause all processes in a running single container with a given container
    ID or name (corresponding IBM Containers command: `cf ic pause <container>`).'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3//containers/{name_or_id}/pause
  tags: Containers,Name,Pause
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/ibm-cloud/containersname-or-idpause-post-openapi.md
- name: IBM Containers Rename a single container
  x-api-slug: ibm-containers
  description: 'Change the current name of an existing single container that is identified
    by the container ID or name (corresponding IBM Containers command: `cf ic rename
    <old_name> <new_name>`).'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3//containers/{name_or_id}/rename
  tags: Containers,Name,Rename
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/ibm-cloud/containersname-or-idrename-post-openapi.md
- name: IBM Containers Restart a single container
  x-api-slug: ibm-containers
  description: 'Restart a container with a given container ID or name (corresponding
    IBM Containers command: `cf ic restart <container>`).'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3//containers/{name_or_id}/restart
  tags: Containers,Name,Restart
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/ibm-cloud/containersname-or-idrestart-post-openapi.md
- name: IBM Containers Start a single container
  x-api-slug: ibm-containers
  description: 'Start a single container with a given container name or ID (corresponding
    IBM Containers command: `cf ic start <container>`).'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3//containers/{name_or_id}/start
  tags: Containers,Name,Start
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/ibm-cloud/containersname-or-idstart-post-openapi.md
- name: IBM Containers Stop a single container
  x-api-slug: ibm-containers
  description: 'Stop a single container with a given container name or ID (corresponding
    IBM Containers command: `cf ic stop <container>`).'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3//containers/{name_or_id}/stop
  tags: Containers,Name,Stop
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/ibm-cloud/containersname-or-idstop-post-openapi.md
- name: IBM Containers Unpause a single container
  x-api-slug: ibm-containers
  description: 'Unpause all processes that are currently stopped inside a single containers
    with a given container ID or name (corresponding IBM Containers command: `cf ic
    unpause <container>`).'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3//containers/{name_or_id}/unpause
  tags: Containers,Name,Unpause
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/ibm-cloud/containersname-or-idunpause-post-openapi.md
- name: IBM Containers Inspect a Docker image in private Bluemix registry
  x-api-slug: ibm-containers
  description: 'This endpoint returns detailed information about a Docker image that
    is stored in the private Bluemix registry of an organization (corresponding IBM
    Containers command: `cf ic inspect <image_name_or_id>`).'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3//images/{name_or_id}/json
  tags: Images,Name,Json
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/ibm-cloud/imagesname-or-idjson-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/ibm-cloud/imagesname-or-idjson-get-openapi.md
- name: IBM Containers Retrieve the namespace of an organization.
  x-api-slug: ibm-containers
  description: 'This endpoint retrieves the namespace that was set for the organization
    that owns the current space (corresponding IBM Containers command: `cf ic namespace
    get`).'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3//registry/namespaces
  tags: Registry,Namespaces
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/ibm-cloud/registrynamespaces-get-openapi.md
- name: IBM Containers Check the availability of a namespace
  x-api-slug: ibm-containers
  description: "This endpoint checks whether a namespace is available in Bluemix and
    can be used to set up the private Docker images registry for an organization.
    When a HTTP code `201 Ok` is returned, the namespace is already assigned to another
    organization in Bluemix and cannot be used. When a HTTP code `404 Not found` is
    returned, the namespace can be used for your organization. \n\n Consider the following
    rules when choosing a namespace for your organization: \n\n- Every organization
    can have one namespace at a time only \n- The namespace must be unique in Bluemix.
    \n- The namespace can be 4-30 characters long. \n- The namespace must start with
    at least one letter or number. \n- The namespace can only contain lowercase letters,
    numbers or underscores (_)."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3//registry/namespaces/{namespace}
  tags: Registry,Namespaces,Namespace
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/ibm-cloud/registrynamespacesnamespace-get-openapi.md
- name: IBM Containers Set a namespace for your private Bluemix registry.
  x-api-slug: ibm-containers
  description: "Set up your own Docker images registry in Bluemix by defining a namespace
    for your organization (corresponding IBM Containers command: `cf ic namespace
    set <namespace>`). The namespace is used to generate a unique URL to your private
    Bluemix registry. In your private registry you store all Docker images that you
    want to share across your organization. To create a container from an image, you
    must first push the image to your registry. \n\n The namespace cannot be changed
    after is has been set. Consider the following rules to choose a namespace for
    your organization: \n\n- Every organization can have one namespace at a time only
    \n- The namespace must be unique in Bluemix. \n- The namespace can be 4-30 characters
    long. \n- The namespace must start with at least one letter or number. \n- The
    namespace can only contain lowercase letters, numbers or underscores (_)."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3//registry/namespaces/{namespace}
  tags: Registry,Namespaces,Namespace
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/ibm-cloud/registrynamespacesnamespace-put-openapi.md
- name: IBM Containers Delete a file share
  x-api-slug: ibm-containers
  description: "This endpoint deletes a file share from a space (corresponding IBM
    Containers command: `cf ic volume fs-rm FSNAME`).\n\n Before you can delete a
    file share, all mounted volumes must be deleted first. To delete a volume, run
    `cf ic volume rm VOLNAME` or call the `DELETE /volumes/{name}` API endpoint. \n\n
    **Note:** To delete a file share you must have been granted organization developer
    rights."
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3//volumes/fs/{name}
  tags: Volumes,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/ibm-cloud/volumesfsname-delete-openapi.md
- name: IBM Containers Inspect a file share
  x-api-slug: ibm-containers
  description: 'This endpoint returns detailed information about a file share (corresponding
    IBM Containers command: `cf ic volume fs-inspect FSNAME`).'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3//volumes/fs/{name}/json
  tags: Volumes,Name,Json
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/ibm-cloud/volumesfsnamejson-get-openapi.md
- name: IBM Containers Delete a volume
  x-api-slug: ibm-containers
  description: 'Delete a volume with a given name from a space (corresponding IBM
    Containers command: `cf ic volume rm VOLNAME`). To delete a volume, all mounted
    containers must be unmounted first. After the volume is deleted, the data that
    are stored in the volume are lost.'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3//volumes/{name}
  tags: Volumes,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/ibm-cloud/volumesname-delete-openapi.md
- name: IBM Containers Share a volume with another space
  x-api-slug: ibm-containers
  description: This endpoint provisions an existing volume that was created in one
    space to another space within the same organization. Single containers and container
    groups in each space can read and write to the shared volume. The volume remains
    owned by the original space it was created in, including management and billing.
    For example, the volume can be deleted from the original space only.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3//volumes/{name}
  tags: Volumes,Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/ibm-cloud/volumesname-post-openapi.md
- name: IBM Containers Retrieve detailed information about a volume.
  x-api-slug: ibm-containers
  description: 'Retrieve a detailed list of information about a volume that is identified
    by the volume name (corresponding IBM Containers command: `cf ic volume inspect
    VOLNAME`).'
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3//volumes/{name}/json
  tags: Volumes,Name,Json
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/ibm-cloud/volumesnamejson-get-openapi.md
- name: IBM Containers
  x-api-slug: ibm-containers
  description: The IBM Cloud has been built to help you solve problems and advance
    opportunities in a world flush with data. Whether it&rsquo;s data you possess,
    data outside your firewall, or data that&rsquo;s coming, the IBM Cloud helps you
    protect it, move it, integrate it and unlock intelligence from it &mdash; giving
    you what it takes to prevail in a competitive market.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/28560-ibm-containers.jpg
  humanURL: https://www.ibm.com/cloud/
  baseURL: https://containers-api.ng.bluemix.net//v3
  tags: Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/ibm-cloud/openapi.md
x-common:
- type: x-blog
  url: https://www.ibm.com/blogs/bluemix/
- type: x-crunchbase
  url: https://crunchbase.com/organization/product/ibm-bluemix
- type: x-documentation
  url: https://console.bluemix.net/docs/
- type: x-github
  url: https://github.com/IBM-Cloud
- type: x-twitter
  url: https://twitter.com/IBMcloud
- type: x-website
  url: https://www.ibm.com/cloud/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---