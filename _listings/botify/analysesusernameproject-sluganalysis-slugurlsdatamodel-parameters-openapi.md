---
swagger: "2.0"
x-collection-name: Botify
x-complete: 0
info:
  title: Botify Parameters Analyses Username Project Slug Analysis Slug Urls Datamodel
  description: Parameters analyses username project slug analysis slug urls datamodel.
  version: 1.0.0
host: api.botify.com
basePath: /v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /analyses/{username}/{project_slug}:
    get:
      summary: Get Analyses Username Project Slug
      description: Get analyses username project slug.
      operationId: getAnalysesUsernameProjectSlug
      x-api-path-slug: analysesusernameproject-slug-get
      parameters:
      - in: query
        name: only_success
        description: Return only successfully finished analyses
      - in: query
        name: page
        description: Page Number
      - in: query
        name: size
        description: Page Size
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Username
      - Project
      - Slug
    parameters:
      summary: Parameters Analyses Username Project Slug
      description: Parameters analyses username project slug.
      operationId: parametersAnalysesUsernameProjectSlug
      x-api-path-slug: analysesusernameproject-slug-parameters
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Username
      - Project
      - Slug
  /analyses/{username}/{project_slug}/{analysis_slug}:
    get:
      summary: Get Analyses Username Project Slug Analysis Slug
      description: Get analyses username project slug analysis slug.
      operationId: getAnalysesUsernameProjectSlugAnalysisSlug
      x-api-path-slug: analysesusernameproject-sluganalysis-slug-get
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Username
      - Project
      - Slug
      - Analysis
      - Slug
    parameters:
      summary: Parameters Analyses Username Project Slug Analysis Slug
      description: Parameters analyses username project slug analysis slug.
      operationId: parametersAnalysesUsernameProjectSlugAnalysisSlug
      x-api-path-slug: analysesusernameproject-sluganalysis-slug-parameters
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Username
      - Project
      - Slug
      - Analysis
      - Slug
  /analyses/{username}/{project_slug}/{analysis_slug}/crawl_statistics:
    get:
      summary: Get Analyses Username Project Slug Analysis Slug Crawl Statistics
      description: Get analyses username project slug analysis slug crawl statistics.
      operationId: getAnalysesUsernameProjectSlugAnalysisSlugCrawlStatistics
      x-api-path-slug: analysesusernameproject-sluganalysis-slugcrawl-statistics-get
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Username
      - Project
      - Slug
      - Analysis
      - Slug
      - Crawl
      - Statistics
    parameters:
      summary: Parameters Analyses Username Project Slug Analysis Slug Crawl Statistics
      description: Parameters analyses username project slug analysis slug crawl statistics.
      operationId: parametersAnalysesUsernameProjectSlugAnalysisSlugCrawlStatistics
      x-api-path-slug: analysesusernameproject-sluganalysis-slugcrawl-statistics-parameters
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Username
      - Project
      - Slug
      - Analysis
      - Slug
      - Crawl
      - Statistics
  /analyses/{username}/{project_slug}/{analysis_slug}/crawl_statistics/time:
    get:
      summary: Get Analyses Username Project Slug Analysis Slug Crawl Statistics Time
      description: Return crawl statistics grouped by time frequency (1 min, 5 mins
        or 60 min) for an analysis
      operationId: getAnalysesUsernameProjectSlugAnalysisSlugCrawlStatisticsTime
      x-api-path-slug: analysesusernameproject-sluganalysis-slugcrawl-statisticstime-get
      parameters:
      - in: query
        name: frequency
        description: Aggregation frequency
      - in: query
        name: limit
        description: max number of elements to retrieve
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Username
      - Project
      - Slug
      - Analysis
      - Slug
      - Crawl
      - Statistics
      - Time
    parameters:
      summary: Parameters Analyses Username Project Slug Analysis Slug Crawl Statistics
        Time
      description: Parameters analyses username project slug analysis slug crawl statistics
        time.
      operationId: parametersAnalysesUsernameProjectSlugAnalysisSlugCrawlStatisticsTime
      x-api-path-slug: analysesusernameproject-sluganalysis-slugcrawl-statisticstime-parameters
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Username
      - Project
      - Slug
      - Analysis
      - Slug
      - Crawl
      - Statistics
      - Time
  /analyses/{username}/{project_slug}/{analysis_slug}/crawl_statistics/urls/{list_type}:
    get:
      summary: Get Analyses Username Project Slug Analysis Slug Crawl Statistics Urls
        List Type
      description: Return a list of 1000 latest URLs crawled (all crawled URLs or
        only URLS with HTTP errors)
      operationId: getAnalysesUsernameProjectSlugAnalysisSlugCrawlStatisticsUrlsListType
      x-api-path-slug: analysesusernameproject-sluganalysis-slugcrawl-statisticsurlslist-type-get
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Username
      - Project
      - Slug
      - Analysis
      - Slug
      - Crawl
      - Statistics
      - Urls
      - List
      - Type
    parameters:
      summary: Parameters Analyses Username Project Slug Analysis Slug Crawl Statistics
        Urls List Type
      description: Parameters analyses username project slug analysis slug crawl statistics
        urls list type.
      operationId: parametersAnalysesUsernameProjectSlugAnalysisSlugCrawlStatisticsUrlsListType
      x-api-path-slug: analysesusernameproject-sluganalysis-slugcrawl-statisticsurlslist-type-parameters
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Username
      - Project
      - Slug
      - Analysis
      - Slug
      - Crawl
      - Statistics
      - Urls
      - List
      - Type
  /analyses/{username}/{project_slug}/{analysis_slug}/features/ganalytics/orphan_urls/{medium}/{source}:
    get:
      summary: Get Analyses Username Project Slug Analysis Slug Features Ganalytics
        Orphan Urls Medium Source
      description: 'Legacy    List of Orphan URLs. URLs which generated visits from
        the selected source according to Google Analytics data, but were not crawled
        with by the Botify crawler (either because no links to them were found on
        the website, or because the crawler was not allowed to follow these links
        according to the project settings).   For a search engine (medium: origanic;
        sources: all, aol, ask, baidu, bing, google, naver, yahoo, yandex) or a social
        network (medium: social; sources: all, facebook, google+, linkedin, pinterest,
        reddit, tumblr, twitter)'
      operationId: getAnalysesUsernameProjectSlugAnalysisSlugFeaturesGanalyticsOrphanUrlsMediumSource
      x-api-path-slug: analysesusernameproject-sluganalysis-slugfeaturesganalyticsorphan-urlsmediumsource-get
      parameters:
      - in: query
        name: page
        description: Page Number
      - in: query
        name: size
        description: Page Size
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Username
      - Project
      - Slug
      - Analysis
      - Slug
      - Features
      - Ganalytics
      - Orphan
      - Urls
      - Medium
      - Source
    parameters:
      summary: Parameters Analyses Username Project Slug Analysis Slug Features Ganalytics
        Orphan Urls Medium Source
      description: Parameters analyses username project slug analysis slug features
        ganalytics orphan urls medium source.
      operationId: parametersAnalysesUsernameProjectSlugAnalysisSlugFeaturesGanalyticsOrphanUrlsMediumSource
      x-api-path-slug: analysesusernameproject-sluganalysis-slugfeaturesganalyticsorphan-urlsmediumsource-parameters
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Username
      - Project
      - Slug
      - Analysis
      - Slug
      - Features
      - Ganalytics
      - Orphan
      - Urls
      - Medium
      - Source
  /analyses/{username}/{project_slug}/{analysis_slug}/features/links/percentiles:
    get:
      summary: Get Analyses Username Project Slug Analysis Slug Features Links Percentiles
      description: Get analyses username project slug analysis slug features links
        percentiles.
      operationId: getAnalysesUsernameProjectSlugAnalysisSlugFeaturesLinksPercentiles
      x-api-path-slug: analysesusernameproject-sluganalysis-slugfeatureslinkspercentiles-get
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Username
      - Project
      - Slug
      - Analysis
      - Slug
      - Features
      - Links
      - Percentiles
    parameters:
      summary: Parameters Analyses Username Project Slug Analysis Slug Features Links
        Percentiles
      description: Parameters analyses username project slug analysis slug features
        links percentiles.
      operationId: parametersAnalysesUsernameProjectSlugAnalysisSlugFeaturesLinksPercentiles
      x-api-path-slug: analysesusernameproject-sluganalysis-slugfeatureslinkspercentiles-parameters
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Username
      - Project
      - Slug
      - Analysis
      - Slug
      - Features
      - Links
      - Percentiles
  /analyses/{username}/{project_slug}/{analysis_slug}/features/pagerank/lost:
    get:
      summary: Get Analyses Username Project Slug Analysis Slug Features Pagerank
        Lost
      description: Get analyses username project slug analysis slug features pagerank
        lost.
      operationId: getAnalysesUsernameProjectSlugAnalysisSlugFeaturesPagerankLost
      x-api-path-slug: analysesusernameproject-sluganalysis-slugfeaturespageranklost-get
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Username
      - Project
      - Slug
      - Analysis
      - Slug
      - Features
      - Pagerank
      - Lost
    parameters:
      summary: Parameters Analyses Username Project Slug Analysis Slug Features Pagerank
        Lost
      description: Parameters analyses username project slug analysis slug features
        pagerank lost.
      operationId: parametersAnalysesUsernameProjectSlugAnalysisSlugFeaturesPagerankLost
      x-api-path-slug: analysesusernameproject-sluganalysis-slugfeaturespageranklost-parameters
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Username
      - Project
      - Slug
      - Analysis
      - Slug
      - Features
      - Pagerank
      - Lost
  /analyses/{username}/{project_slug}/{analysis_slug}/features/sitemaps/report:
    get:
      summary: Get Analyses Username Project Slug Analysis Slug Features Sitemaps
        Report
      description: Get global information of the sitemaps found (sitemaps indexes,
        invalid sitemaps urls, etc.)
      operationId: getAnalysesUsernameProjectSlugAnalysisSlugFeaturesSitemapsReport
      x-api-path-slug: analysesusernameproject-sluganalysis-slugfeaturessitemapsreport-get
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Username
      - Project
      - Slug
      - Analysis
      - Slug
      - Features
      - Sitemaps
      - Report
    parameters:
      summary: Parameters Analyses Username Project Slug Analysis Slug Features Sitemaps
        Report
      description: Parameters analyses username project slug analysis slug features
        sitemaps report.
      operationId: parametersAnalysesUsernameProjectSlugAnalysisSlugFeaturesSitemapsReport
      x-api-path-slug: analysesusernameproject-sluganalysis-slugfeaturessitemapsreport-parameters
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Username
      - Project
      - Slug
      - Analysis
      - Slug
      - Features
      - Sitemaps
      - Report
  /analyses/{username}/{project_slug}/{analysis_slug}/features/sitemaps/samples/out_of_config:
    get:
      summary: Get Analyses Username Project Slug Analysis Slug Features Sitemaps
        Samples Out Of Config
      description: Sample list of URLs which were found in your sitemaps but outside
        of the crawl perimeter defined for the project, for instance domain/subdomain
        or protocol (HTTP/HTTPS) not allowed in the crawl settings.
      operationId: getAnalysesUsernameProjectSlugAnalysisSlugFeaturesSitemapsSamplesOutOfConfig
      x-api-path-slug: analysesusernameproject-sluganalysis-slugfeaturessitemapssamplesout-of-config-get
      parameters:
      - in: query
        name: page
        description: Page Number
      - in: query
        name: size
        description: Page Size
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Username
      - Project
      - Slug
      - Analysis
      - Slug
      - Features
      - Sitemaps
      - Samples
      - Out
      - Of
      - Config
    parameters:
      summary: Parameters Analyses Username Project Slug Analysis Slug Features Sitemaps
        Samples Out Of Config
      description: Parameters analyses username project slug analysis slug features
        sitemaps samples out of config.
      operationId: parametersAnalysesUsernameProjectSlugAnalysisSlugFeaturesSitemapsSamplesOutOfConfig
      x-api-path-slug: analysesusernameproject-sluganalysis-slugfeaturessitemapssamplesout-of-config-parameters
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Username
      - Project
      - Slug
      - Analysis
      - Slug
      - Features
      - Sitemaps
      - Samples
      - Out
      - Of
      - Config
  /analyses/{username}/{project_slug}/{analysis_slug}/features/sitemaps/samples/sitemap_only:
    get:
      summary: Get Analyses Username Project Slug Analysis Slug Features Sitemaps
        Samples Sitemap Only
      description: Sample list of URLs which were found in your sitemaps, within the
        project allowed scope (allowed domains/subdomains/protocols), but not found
        by the Botify crawler.
      operationId: getAnalysesUsernameProjectSlugAnalysisSlugFeaturesSitemapsSamplesSitemapOnly
      x-api-path-slug: analysesusernameproject-sluganalysis-slugfeaturessitemapssamplessitemap-only-get
      parameters:
      - in: query
        name: page
        description: Page Number
      - in: query
        name: size
        description: Page Size
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Username
      - Project
      - Slug
      - Analysis
      - Slug
      - Features
      - Sitemaps
      - Samples
      - Sitemap
      - Only
    parameters:
      summary: Parameters Analyses Username Project Slug Analysis Slug Features Sitemaps
        Samples Sitemap Only
      description: Parameters analyses username project slug analysis slug features
        sitemaps samples sitemap only.
      operationId: parametersAnalysesUsernameProjectSlugAnalysisSlugFeaturesSitemapsSamplesSitemapOnly
      x-api-path-slug: analysesusernameproject-sluganalysis-slugfeaturessitemapssamplessitemap-only-parameters
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Username
      - Project
      - Slug
      - Analysis
      - Slug
      - Features
      - Sitemaps
      - Samples
      - Sitemap
      - Only
  /analyses/{username}/{project_slug}/{analysis_slug}/features/top_domains/domains:
    get:
      summary: Get Analyses Username Project Slug Analysis Slug Features Top Domains
        Domains
      description: Get analyses username project slug analysis slug features top domains
        domains.
      operationId: getAnalysesUsernameProjectSlugAnalysisSlugFeaturesTopDomainsDomains
      x-api-path-slug: analysesusernameproject-sluganalysis-slugfeaturestop-domainsdomains-get
      parameters:
      - in: query
        name: page
        description: Page Number
      - in: query
        name: size
        description: Page Size
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Username
      - Project
      - Slug
      - Analysis
      - Slug
      - Features
      - Top
      - Domains
      - Domains
    parameters:
      summary: Parameters Analyses Username Project Slug Analysis Slug Features Top
        Domains Domains
      description: Parameters analyses username project slug analysis slug features
        top domains domains.
      operationId: parametersAnalysesUsernameProjectSlugAnalysisSlugFeaturesTopDomainsDomains
      x-api-path-slug: analysesusernameproject-sluganalysis-slugfeaturestop-domainsdomains-parameters
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Username
      - Project
      - Slug
      - Analysis
      - Slug
      - Features
      - Top
      - Domains
      - Domains
  /analyses/{username}/{project_slug}/{analysis_slug}/features/top_domains/subdomains:
    get:
      summary: Get Analyses Username Project Slug Analysis Slug Features Top Domains
        Subdomains
      description: Get analyses username project slug analysis slug features top domains
        subdomains.
      operationId: getAnalysesUsernameProjectSlugAnalysisSlugFeaturesTopDomainsSubdomains
      x-api-path-slug: analysesusernameproject-sluganalysis-slugfeaturestop-domainssubdomains-get
      parameters:
      - in: query
        name: page
        description: Page Number
      - in: query
        name: size
        description: Page Size
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Username
      - Project
      - Slug
      - Analysis
      - Slug
      - Features
      - Top
      - Domains
      - Subdomains
    parameters:
      summary: Parameters Analyses Username Project Slug Analysis Slug Features Top
        Domains Subdomains
      description: Parameters analyses username project slug analysis slug features
        top domains subdomains.
      operationId: parametersAnalysesUsernameProjectSlugAnalysisSlugFeaturesTopDomainsSubdomains
      x-api-path-slug: analysesusernameproject-sluganalysis-slugfeaturestop-domainssubdomains-parameters
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Username
      - Project
      - Slug
      - Analysis
      - Slug
      - Features
      - Top
      - Domains
      - Subdomains
  /analyses/{username}/{project_slug}/{analysis_slug}/features/visits/orphan_urls/{medium}/{source}:
    get:
      summary: Get Analyses Username Project Slug Analysis Slug Features Visits Orphan
        Urls Medium Source
      description: 'List of Orphan URLs. URLs which generated visits from the selected
        source according to Google Analytics data, but were not crawled with by the
        Botify crawler (either because no links to them were found on the website,
        or because the crawler was not allowed to follow these links according to
        the project settings).   For a search engine (medium: origanic; sources: all,
        aol, ask, baidu, bing, google, naver, yahoo, yandex) or a social network (medium:
        social; sources: all, facebook, google+, linkedin, pinterest, reddit, tumblr,
        twitter)'
      operationId: getAnalysesUsernameProjectSlugAnalysisSlugFeaturesVisitsOrphanUrlsMediumSource
      x-api-path-slug: analysesusernameproject-sluganalysis-slugfeaturesvisitsorphan-urlsmediumsource-get
      parameters:
      - in: query
        name: page
        description: Page Number
      - in: query
        name: size
        description: Page Size
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Username
      - Project
      - Slug
      - Analysis
      - Slug
      - Features
      - Visits
      - Orphan
      - Urls
      - Medium
      - Source
    parameters:
      summary: Parameters Analyses Username Project Slug Analysis Slug Features Visits
        Orphan Urls Medium Source
      description: Parameters analyses username project slug analysis slug features
        visits orphan urls medium source.
      operationId: parametersAnalysesUsernameProjectSlugAnalysisSlugFeaturesVisitsOrphanUrlsMediumSource
      x-api-path-slug: analysesusernameproject-sluganalysis-slugfeaturesvisitsorphan-urlsmediumsource-parameters
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Username
      - Project
      - Slug
      - Analysis
      - Slug
      - Features
      - Visits
      - Orphan
      - Urls
      - Medium
      - Source
  /analyses/{username}/{project_slug}/{analysis_slug}/urls:
    parameters:
      summary: Parameters Analyses Username Project Slug Analysis Slug Urls
      description: Parameters analyses username project slug analysis slug urls.
      operationId: parametersAnalysesUsernameProjectSlugAnalysisSlugUrls
      x-api-path-slug: analysesusernameproject-sluganalysis-slugurls-parameters
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Username
      - Project
      - Slug
      - Analysis
      - Slug
      - Urls
    post:
      summary: Post Analyses Username Project Slug Analysis Slug Urls
      description: Post analyses username project slug analysis slug urls.
      operationId: postAnalysesUsernameProjectSlugAnalysisSlugUrls
      x-api-path-slug: analysesusernameproject-sluganalysis-slugurls-post
      parameters:
      - in: query
        name: area
        description: Analysis context
      - in: query
        name: page
        description: Page Number
      - in: query
        name: size
        description: Page Size
      - in: body
        name: UrlsQuery
        description: Urls query
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Username
      - Project
      - Slug
      - Analysis
      - Slug
      - Urls
  /analyses/{username}/{project_slug}/{analysis_slug}/urls/aggs:
    parameters:
      summary: Parameters Analyses Username Project Slug Analysis Slug Urls Aggs
      description: Parameters analyses username project slug analysis slug urls aggs.
      operationId: parametersAnalysesUsernameProjectSlugAnalysisSlugUrlsAggs
      x-api-path-slug: analysesusernameproject-sluganalysis-slugurlsaggs-parameters
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Username
      - Project
      - Slug
      - Analysis
      - Slug
      - Urls
      - Aggs
    post:
      summary: Post Analyses Username Project Slug Analysis Slug Urls Aggs
      description: Post analyses username project slug analysis slug urls aggs.
      operationId: postAnalysesUsernameProjectSlugAnalysisSlugUrlsAggs
      x-api-path-slug: analysesusernameproject-sluganalysis-slugurlsaggs-post
      parameters:
      - in: query
        name: area
        description: Analysis context
      - in: body
        name: UrlsAggsQueries
        description: UrlsAggs queries
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Username
      - Project
      - Slug
      - Analysis
      - Slug
      - Urls
      - Aggs
  /analyses/{username}/{project_slug}/{analysis_slug}/urls/datamodel:
    get:
      summary: Get Analyses Username Project Slug Analysis Slug Urls Datamodel
      description: Get analyses username project slug analysis slug urls datamodel.
      operationId: getAnalysesUsernameProjectSlugAnalysisSlugUrlsDatamodel
      x-api-path-slug: analysesusernameproject-sluganalysis-slugurlsdatamodel-get
      parameters:
      - in: query
        name: area
        description: Analysis context
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Username
      - Project
      - Slug
      - Analysis
      - Slug
      - Urls
      - Datamodel
    parameters:
      summary: Parameters Analyses Username Project Slug Analysis Slug Urls Datamodel
      description: Parameters analyses username project slug analysis slug urls datamodel.
      operationId: parametersAnalysesUsernameProjectSlugAnalysisSlugUrlsDatamodel
      x-api-path-slug: analysesusernameproject-sluganalysis-slugurlsdatamodel-parameters
      responses:
        200:
          description: OK
      tags:
      - Analyses
      - Username
      - Project
      - Slug
      - Analysis
      - Slug
      - Urls
      - Datamodel
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