---
swagger: "2.0"
x-collection-name: New Relic
x-complete: 0
info:
  title: New Relic Get Applications Application  Metrics Data. Format
  version: 1.0.0
  description: "This API endpoint returns a list of values for each of the requested
    metrics. The list of available metrics\ncan be returned using the Metric Name
    API endpoint.\n\nMetric data can be filtered by a number of parameters, including
    multiple names and values, and by time range.\nMetric names and values will be
    matched intelligently in the background.\n\nYou can also retrieve a summarized
    data point across the entire time range selected by using the summarize\nparameter.\n\nSee
    our documentation for a discussion on \noutput pagination,  time range \nrelated
    considerations, and for examples of requesting and using metric values."
basePath: v2/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /applications/{application_id}/hosts/{host_id}/metrics/data.{format}:
    get:
      summary: Get Applications Application  Hosts Host  Metrics Data. Format
      description: "This API endpoint returns a list of values for each of the requested
        metrics. The list of available metrics\ncan be returned using the Metric Name
        API endpoint.\n\nMetric data can be filtered by a number of parameters, including
        multiple names and values, and by time range.\nMetric names and values will
        be matched intelligently in the background.\n\nYou can also retrieve a summarized
        data point across the entire time range selected by using the summarize\nparameter.\n\nSee
        our documentation for a discussion on \noutput pagination,  time range \nrelated
        considerations, and for examples of requesting and using metric values."
      operationId: getApplicationsApplicationHostsHostMetricsData.Format
      x-api-path-slug: applicationsapplication-idhostshost-idmetricsdata-format-get
      parameters:
      - in: path
        name: application_id
        description: Application ID
        type: integer
      - in: query
        name: from
        description: Retrieve metrics after this time
        type: time
      - in: path
        name: host_id
        description: Application Host ID
        type: integer
      - in: query
        name: names
        description: Retrieve specific metrics by name
        type: array
      - in: query
        name: period
        description: Period of timeslices in seconds
        type: integer
      - in: query
        name: raw
        description: Return unformatted raw values
        type: boolean
      - in: query
        name: summarize
        description: Summarize the data
        type: boolean
      - in: query
        name: to
        description: Retrieve metrics before this time
        type: time
      - in: query
        name: values
        description: Retrieve specific metric values
        type: array
      responses:
        200:
          description: OK
      tags:
      - Applications
      - Application
      - ""
      - Hosts
      - Host
      - ""
      - Metrics
      - Data.
      - Format
  /applications/{application_id}/instances/{instance_id}/metrics/data.{format}:
    get:
      summary: Get Applications Application  Instances Instance  Metrics Data. Format
      description: "This API endpoint returns a list of values for each of the requested
        metrics. The list of available metrics\ncan be returned using the Metric Name
        API endpoint.\n\nMetric data can be filtered by a number of parameters, including
        multiple names and values, and by time range.\nMetric names and values will
        be matched intelligently in the background.\n\nYou can also retrieve a summarized
        data point across the entire time range selected by using the summarize\nparameter.\n\nSee
        our documentation for a discussion on \noutput pagination,  time range \nrelated
        considerations, and for examples of requesting and using metric values."
      operationId: getApplicationsApplicationInstancesInstanceMetricsData.Format
      x-api-path-slug: applicationsapplication-idinstancesinstance-idmetricsdata-format-get
      parameters:
      - in: path
        name: application_id
        description: Application ID
        type: integer
      - in: query
        name: from
        description: Retrieve metrics after this time
        type: time
      - in: path
        name: instance_id
        description: Application Instance ID
        type: integer
      - in: query
        name: names
        description: Retrieve specific metrics by name
        type: array
      - in: query
        name: period
        description: Period of timeslices in seconds
        type: integer
      - in: query
        name: raw
        description: Return unformatted raw values
        type: boolean
      - in: query
        name: summarize
        description: Summarize the data
        type: boolean
      - in: query
        name: to
        description: Retrieve metrics before this time
        type: time
      - in: query
        name: values
        description: Retrieve specific metric values
        type: array
      responses:
        200:
          description: OK
      tags:
      - Applications
      - Application
      - ""
      - Instances
      - Instance
      - ""
      - Metrics
      - Data.
      - Format
  /applications/{application_id}/metrics/data.{format}:
    get:
      summary: Get Applications Application  Metrics Data. Format
      description: "This API endpoint returns a list of values for each of the requested
        metrics. The list of available metrics\ncan be returned using the Metric Name
        API endpoint.\n\nMetric data can be filtered by a number of parameters, including
        multiple names and values, and by time range.\nMetric names and values will
        be matched intelligently in the background.\n\nYou can also retrieve a summarized
        data point across the entire time range selected by using the summarize\nparameter.\n\nSee
        our documentation for a discussion on \noutput pagination,  time range \nrelated
        considerations, and for examples of requesting and using metric values."
      operationId: getApplicationsApplicationMetricsData.Format
      x-api-path-slug: applicationsapplication-idmetricsdata-format-get
      parameters:
      - in: path
        name: application_id
        description: Application ID
        type: integer
      - in: query
        name: from
        description: Retrieve metrics after this time
        type: time
      - in: query
        name: names
        description: Retrieve specific metrics by name
        type: array
      - in: query
        name: period
        description: Period of timeslices in seconds
        type: integer
      - in: query
        name: raw
        description: Return unformatted raw values
        type: boolean
      - in: query
        name: summarize
        description: Summarize the data
        type: boolean
      - in: query
        name: to
        description: Retrieve metrics before this time
        type: time
      - in: query
        name: values
        description: Retrieve specific metric values
        type: array
      responses:
        200:
          description: OK
      tags:
      - Applications
      - Application
      - ""
      - Metrics
      - Data.
      - Format
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