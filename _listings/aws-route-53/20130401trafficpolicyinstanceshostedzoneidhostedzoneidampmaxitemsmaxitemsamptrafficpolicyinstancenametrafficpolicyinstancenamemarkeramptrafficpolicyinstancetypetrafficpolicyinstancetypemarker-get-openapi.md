---
swagger: "2.0"
x-collection-name: AWS Route 53
x-complete: 0
info:
  title: AWS Route 53 API List Traffic Policy Instances By Hosted Zone
  version: 1.0.0
  description: 'Gets information about the traffic policy instances that you created
    in a specifiedhosted zone.NoteAfter you submit an UpdateTrafficPolicyInstance
    request, there''s a briefdelay while Amazon Route 53 creates the resource record
    sets that are specified in the traffic policydefinition. For more information,
    see the State response element.Send a GET request to the /Amazon Route 53 APIversion/trafficpolicyinstance
    resource and include the ID of the hostedzone.Amazon Route 53 returns a maximum
    of 100 items in each response. If you have a lot of trafficpolicy instances, you
    can use the MaxItems parameter to list them in groups of upto 100.The response
    includes four values that help you navigate from one group ofMaxItems traffic
    policy instances to the next:             IsTruncated               If the value
    of IsTruncated in the response is true, there aremore traffic policy instances
    associated with the current AWS account.If IsTruncated is false, this response
    includes the lasttraffic policy instance that is associated with the current account.             MaxItems           The
    value that you specified for the MaxItems parameter in the requestthat produced
    the current response.                  TrafficPolicyInstanceNameMarker and TrafficPolicyInstanceTypeMarker               If
    IsTruncated is true, these two values in the responserepresent the first traffic
    policy instance in the next group of MaxItemstraffic policy instances. To list
    more traffic policy instances, make another call toListTrafficPolicyInstancesByHostedZone,
    and specify these values in thecorresponding request parameters.If IsTruncated
    is false, all three elements are omittedfrom the response.'
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /2013-04-01/delegationset:
    post:
      summary: Create Reusable Delegation Set
      description: Creates a delegation set (a group of four name servers) that can
        be reused by multiplehosted zones. If a hosted zoned ID is specified, CreateReusableDelegationSetmarks
        the delegation set associated with that zone as reusableSend a POST request
        to the /2013-04-01/delegationset resource. The request body must include a
        document with a CreateReusableDelegationSetRequest element.NoteA reusable
        delegation set can't be associated with a private hosted zone/For more information,
        including a procedure on how to create and configure a reusabledelegation
        set (also known as white label name servers), see Configuring White Label
        NameServers.
      operationId: createreusabledelegationset
      x-api-path-slug: 20130401delegationset-post
      parameters:
      - in: body
        name: CallerReference
        description: A unique string that identifies the request, and that allows
          you to retry failedCreateReusableDelegationSet requests without the risk
          of executing theoperation twice
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: CreateReusableDelegationSetRequest
        description: Root level tag for the CreateReusableDelegationSetRequest parameters
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: HostedZoneId
        description: If you want to mark the delegation set for an existing hosted
          zone as reusable, the IDfor that hosted zone
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Reusable Delegation Sets
  /2013-04-01/hostedzone:
    post:
      summary: Create Hosted Zone
      description: Creates a new public hosted zone, used to specify how the Domain
        Name System (DNS)routes traffic on the Internet for a domain, such as example.com,
        and its subdomains. ImportantPublic hosted zones can't be converted to a private
        hosted zone or vice versa.Instead, create a new hosted zone with the same
        name and create new resource recordsets.Send a POST request to the /2013-04-01/hostedzone
        resource. The request body must include a documentwith a CreateHostedZoneRequest
        element. The response returns theCreateHostedZoneResponse element containing
        metadata about the hostedzone.Fore more information about charges for hosted
        zones, see Amazon Route 53 Pricing.Note the following:You can't create a hosted
        zone for a top-level domain (TLD).Amazon Route 53 automatically creates a
        default SOA record and four NS records for the zone.For more information about
        SOA and NS records, see NS and SOA Records that Amazon Route 53 Creates for
        a Hosted Zone in the Amazon Route 53 Developer Guide.If your domain is registered
        with a registrar other than Amazon Route 53, you must update thename servers
        with your registrar to make Amazon Route 53 your DNS service. For more information,
        seeConfiguring Amazon Route 53 as your DNSService in the Amazon Route 53 Developer's
        Guide.After creating a zone, its initial status is PENDING. This means that
        itis not yet available on all DNS servers. The status of the zone changes
        to INSYNCwhen the NS and SOA records are available on all Amazon Route 53
        DNS servers. When trying to create a hosted zone using a reusable delegation
        set, specify anoptional DelegationSetId, and Amazon Route 53 would assign
        those 4 NS records for the zone, instead ofallotting a new one.
      operationId: createhostedzone
      x-api-path-slug: 20130401hostedzone-post
      parameters:
      - in: body
        name: CallerReference
        description: A unique string that identifies the request and that allows failedCreateHostedZone
          requests to be retried without the risk of executing theoperation twice
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: CreateHostedZoneRequest
        description: Root level tag for the CreateHostedZoneRequest parameters
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: Default
        description: None
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: DelegationSetId
        description: If you want to associate a reusable delegation set with this
          hosted zone, the ID thatAmazon Route 53 assigned to the reusable delegation
          set when you created it
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: HostedZoneConfig
        description: (Optional) A complex type that contains an optional comment about
          your hosted zone
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: Name
        description: The name of the domain
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: Parent
        description: CreatedHostedZoneRequest
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: VPC
        description: The VPC that you want your hosted zone to be associated with
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Hosted Zones
  ? /2013-04-01/hostedzone/Id/rrset&amp;identifier=StartRecordIdentifier&amp;maxitems=MaxItems?name=StartRecordName&amp;type=StartRecordType
  : get:
      summary: List Resource Record Sets
      description: 'Lists the resource record sets in a specified hosted zone.            ListResourceRecordSets
        returns up to 100 resource record sets at a time in ASCII order, beginning
        at a position specified by the name and type elements. The action sorts results
        first by DNS name with the labels reversed, for example:            com.example.www.         Note
        the trailing dot, which can change the sort order in some circumstances.When
        multiple records have the same DNS name, the action sorts results by the record
        type.You can use the name and type elements to adjust the beginning position
        of the list of resource record sets returned:If you do not specify Name or
        TypeThe results begin with the first resource record set that the hosted zone
        contains.If you specify Name but not TypeThe results begin with the first
        resource record set in the list whose name is greater than or equal to Name.If
        you specify Type but not NameAmazon Route 53 returns the InvalidInput error.If
        you specify both Name and TypeThe results begin with the first resource record
        set in the list whose name is greater than or equal to Name, and whose type
        is greater than or equal to Type.This action returns the most current version
        of the records. This includes records that are PENDING, and that are not yet
        available on all Amazon Route 53 DNS servers.To ensure that you get an accurate
        listing of the resource record sets for a hosted zone at a point in time,
        do not submit a ChangeResourceRecordSets request while you''re paging through
        the results of a ListResourceRecordSets request. If you do, some pages may
        display results without the latest changes while other pages display results
        with the latest changes.'
      operationId: listresourcerecordsets
      x-api-path-slug: 20130401hostedzoneidrrsetampidentifierstartrecordidentifierampmaxitemsmaxitemsnamestartrecordnameamptypestartrecordtype-get
      parameters:
      - in: path
        name: Id
        description: The ID of the hosted zone that contains the resource record sets
          that you want toget
        type: string
      responses:
        200:
          description: OK
      tags:
      - Resource Record Sets
  /2013-04-01/hostedzone/Id/rrset/:
    post:
      summary: Change Resource Record Sets
      description: 'Create, change, update, or delete authoritative DNS information
        on all Amazon Route 53 servers.Send a POST request to:             /2013-04-01/hostedzone/Amazon
        Route 53 hosted ZoneID/rrset resource. The request body must include a document
        with aChangeResourceRecordSetsRequest element. The request body contains a
        list ofchange items, known as a change batch. Change batches are considered
        transactional changes.When using the Amazon Route 53 API to change resource
        record sets, Amazon Route 53 either makes all or none of thechanges in a change
        batch request. This ensures that Amazon Route 53 never partially implements
        theintended changes to the resource record sets in a hosted zone. For example,
        a change batch request that deletes the CNAME record forwww.example.com and
        creates an alias resource record set for www.example.com. Amazon Route 53
        deletesthe first resource record set and creates the second resource record
        set in a singleoperation. If either the DELETE or the CREATE action fails,
        thenboth changes (plus any other changes in the batch) fail, and the original
        CNAMErecord continues to exist.ImportantDue to the nature of transactional
        changes, you can''t delete the same resourcerecord set more than once in a
        single change batch. If you attempt to delete the same changebatch more than
        once, Amazon Route 53 returns an InvalidChangeBatch error.NoteTo create resource
        record sets for complex routing configurations, use either thetraffic flow
        visual editor in the Amazon Route 53 console or the API actions for traffic
        policies andtraffic policy instances. Save the configuration as a traffic
        policy, then associate thetraffic policy with one or more domain names (such
        as example.com) or subdomain names (suchas www.example.com), in the same hosted
        zone or in multiple hosted zones. You can roll backthe updates if the new
        configuration isn''t performing as expected. For more information, seeUsing
        Traffic Flow to Route DNSTraffic in the Amazon Route 53 Developer Guide.Use
        ChangeResourceRecordsSetsRequest to perform the following actions:                  CREATE:
        Creates a resource record set that has the specified values.                  DELETE:
        Deletes an existing resource record set that has the specified values.                  UPSERT:
        If a resource record set does not already exist, AWS createsit. If a resource
        set does exist, Amazon Route 53 updates it with the values in the request.
        The values that you need to include in the request depend on the type of resource
        record set that you''re creating, deleting, or updating:            Basic
        resource record sets (excluding alias, failover, geolocation, latency, and
        weighted resource record sets)                           Name                                 Type                                 TTL                           Failover,
        geolocation, latency, or weighted resource record sets (excluding alias resource
        record sets)                           Name                                 Type                                 TTL                                 SetIdentifier                           Alias
        resource record sets (including failover alias, geolocation alias, latency
        alias, and weighted alias resource record sets)                           Name                                 Type                                 AliasTarget
        (includes DNSName, EvaluateTargetHealth, and HostedZoneId)                  SetIdentifier
        (for failover, geolocation, latency, and weighted resource record sets)When
        you submit a ChangeResourceRecordSets request, Amazon Route 53 propagates
        your changes to all of the Amazon Route 53 authoritative DNS servers. While
        your changes are propagating, GetChange returns a status of PENDING. When
        propagation is complete, GetChange returns a status of INSYNC. Changes generally
        propagate to all Amazon Route 53 name servers in a few minutes. In rare circumstances,
        propagation can take up to 30 minutes. For more information, see GetChange       For
        information about the limits on a ChangeResourceRecordSets request, see Limits
        in the Amazon Route 53 Developer Guide.'
      operationId: changeresourcerecordsets
      x-api-path-slug: 20130401hostedzoneidrrset-post
      parameters:
      - in: body
        name: ChangeBatch
        description: A complex type that contains an optional comment and the Changeselement
        schema:
          $ref: '#/definitions/holder'
      - in: body
        name: ChangeResourceRecordSetsRequest
        description: Root level tag for the ChangeResourceRecordSetsRequest parameters
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: Id
        description: The ID of the hosted zone that contains the resource record sets
          that you want tochange
        type: string
      responses:
        200:
          description: OK
      tags:
      - Changes
  /2013-04-01/hostedzonesbyname?dnsname=DNSName&amp;hostedzoneid=HostedZoneId&amp;maxitems=MaxItems:
    get:
      summary: List Hosted Zones By Name
      description: 'Retrieves a list of your hosted zones in lexicographic order.
        Send a GETrequest to the /2013-04-01/hostedzonesbyname resource. The response
        includes aHostedZones child element for each hosted zone created by the current
        AWSaccount.             ListHostedZonesByName sorts hosted zones by name with
        the labels reversed.For example:                  com.example.www.               Note
        the trailing dot, which can change the sort order in some circumstances.If
        the domain name includes escape characters or Punycode,ListHostedZonesByName
        alphabetizes the domain name using the escaped orPunycoded value, which is
        the format that Amazon Route 53 saves in its database. For example, to createa
        hosted zone for example.com, specify ex\344mple.com for the domain name.ListHostedZonesByName
        alphabetizes it as:                  com.ex\344mple.               The labels
        are reversed and alphabetized using the escaped value. For more informationabout
        valid domain name formats, including internationalized domain names, see DNS
        Domain Name Format in theAmazon Route 53 Developer Guide.Amazon Route 53 returns
        up to 100 items in each response. If you have a lot of hosted zones, usethe
        MaxItems parameter to list them in groups of up to 100. The response includesvalues
        that help navigate from one group of MaxItems hosted zones to thenext:The
        DNSName and HostedZoneId elements in the responsecontain the values, if any,
        specified for the dnsname andhostedzoneid parameters in the request that produced
        the currentresponse.The MaxItems element in the response contains the value,
        if any, thatyou specified for the maxitems parameter in the request that produced
        thecurrent response.If the value of IsTruncated in the response is true, there
        are morehosted zones associated with the current AWS account. If IsTruncated
        is false, this response includes the last hosted zonethat is associated with
        the current account. The NextDNSName element andNextHostedZoneId elements
        are omitted from the response.The NextDNSName and NextHostedZoneId elements
        in theresponse contain the domain name and the hosted zone ID of the next
        hosted zone that isassociated with the current AWS account. If you want to
        list more hosted zones, makeanother call to ListHostedZonesByName, and specify
        the value ofNextDNSName and NextHostedZoneId in the dnsnameand hostedzoneid
        parameters, respectively.'
      operationId: listhostedzonesbyname
      x-api-path-slug: 20130401hostedzonesbynamednsnamednsnameamphostedzoneidhostedzoneidampmaxitemsmaxitems-get
      parameters:
      - in: path
        name: dnsname
        description: (Optional) For your first request to ListHostedZonesByName, include
          thednsname parameter only if you want to specify the name of the first hosted
          zonein the response
        type: string
      responses:
        200:
          description: OK
      tags:
      - Hosted Zones
  ? /2013-04-01/testdnsanswer&amp;edns0clientsubnetip=EDNS0ClientSubnetIP&amp;edns0clientsubnetmask=EDNS0ClientSubnetMask?hostedzoneid=HostedZoneId&amp;recordname=RecordName&amp;recordtype=RecordType&amp;resolverip=ResolverIP
  : get:
      summary: Test D N S Answer
      description: Gets the value that Amazon Route 53 returns in response to a DNS
        request for a specified record name and type. You can optionally specify the
        IP address of a DNS resolver, an EDNS0 client subnet IP address, and a subnet
        mask.
      operationId: testdnsanswer
      x-api-path-slug: 20130401testdnsanswerampedns0clientsubnetipedns0clientsubnetipampedns0clientsubnetmaskedns0clientsubnetmaskhostedzoneidhostedzoneidamprecordnamerecordnameamprecordtyperecordtypeampresolveripresolverip-get
      parameters:
      - in: path
        name: edns0clientsubnetip
        description: If the resolver that you specified for resolverip supports EDNS0,
          specify the IP address of a client in the applicable location
        type: string
      responses:
        200:
          description: OK
      tags:
      - DNS
  ? /2013-04-01/trafficpolicyinstances/hostedzone?id=HostedZoneId&amp;maxitems=MaxItems&amp;trafficpolicyinstancename=TrafficPolicyInstanceNameMarker&amp;trafficpolicyinstancetype=TrafficPolicyInstanceTypeMarker
  : get:
      summary: List Traffic Policy Instances By Hosted Zone
      description: 'Gets information about the traffic policy instances that you created
        in a specifiedhosted zone.NoteAfter you submit an UpdateTrafficPolicyInstance
        request, there''s a briefdelay while Amazon Route 53 creates the resource
        record sets that are specified in the traffic policydefinition. For more information,
        see the State response element.Send a GET request to the /Amazon Route 53
        APIversion/trafficpolicyinstance resource and include the ID of the hostedzone.Amazon
        Route 53 returns a maximum of 100 items in each response. If you have a lot
        of trafficpolicy instances, you can use the MaxItems parameter to list them
        in groups of upto 100.The response includes four values that help you navigate
        from one group ofMaxItems traffic policy instances to the next:             IsTruncated               If
        the value of IsTruncated in the response is true, there aremore traffic policy
        instances associated with the current AWS account.If IsTruncated is false,
        this response includes the lasttraffic policy instance that is associated
        with the current account.             MaxItems           The value that you
        specified for the MaxItems parameter in the requestthat produced the current
        response.                  TrafficPolicyInstanceNameMarker and TrafficPolicyInstanceTypeMarker               If
        IsTruncated is true, these two values in the responserepresent the first traffic
        policy instance in the next group of MaxItemstraffic policy instances. To
        list more traffic policy instances, make another call toListTrafficPolicyInstancesByHostedZone,
        and specify these values in thecorresponding request parameters.If IsTruncated
        is false, all three elements are omittedfrom the response.'
      operationId: listtrafficpolicyinstancesbyhostedzone
      x-api-path-slug: 20130401trafficpolicyinstanceshostedzoneidhostedzoneidampmaxitemsmaxitemsamptrafficpolicyinstancenametrafficpolicyinstancenamemarkeramptrafficpolicyinstancetypetrafficpolicyinstancetypemarker-get
      parameters:
      - in: path
        name: id
        description: The ID of the hosted zone for which you want to list traffic
          policyinstances
        type: string
      responses:
        200:
          description: OK
      tags:
      - Traffic Policies
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