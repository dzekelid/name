swagger: "2.0"
x-collection-name: Amadeus
x-complete: 1
info:
  title: Amadeus
  description: amadeus-api-is-a-toolkit-designed-for-travel-agencies-who-want-to-develop-their-own-travel-products-rather-than-using-offtheshelf-solutions--with-this-tool-you-can-build-your-very-own-customised-applications-that-link-in-a-stable-and-secure-dialogue-with-our-global-distribution-system-gds-
  contact:
    name: Amadeus Innovation and Research
    url: https://sandbox.amadeus.com
  version: 1.0.0
host: api.sandbox.amadeus.com
basePath: /v1.2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /airports/autocomplete:
    get:
      summary: Get Airports Autocomplete
      description: "Using the term parameter and given the start of any word in an
        airport's official name, a city name, or the start of an IATA code, this API
        provides the full name and IATA location code of the city or airport, for
        use in flight searches. Only major cities and civilian airports with several
        commercial flights per week are included by default. The response provides
        up to 20 possible matches, sorted by importance, in a JQuery UI Autocomplete
        compatible format. This sample implementation using JQuery UI may help. This
        API uses data from the OpenTravelData project.\n \nBy only using the country
        parameter, this API is also able to find all the IATA location codes associated
        with a country. Both term and country parameters can be used together to filter
        the results accordingly.          \n\nThe value returned is the IATA location
        code. The label returned is always in UTF-8 format, with the airport official
        name (which is often in the native language), in the format of English City
        Name (if not already included in the airport name)."
      operationId: getAirportsAutocomplete
      x-api-path-slug: airportsautocomplete-get
      parameters:
      - in: query
        name: all_airports
        description: Boolean to include or not all airports, no matter their traffic
          rank
      - in: query
        name: country
        description: Identified a country based of a ISO 3166-1 alpha-2 code
      - in: query
        name: term
        description: Search keyword that should represent the start of a word in a
          city or airport name
      responses:
        200:
          description: OK
      tags:
      - Airlines
      - Airports
      - Autocomplete