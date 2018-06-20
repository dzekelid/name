---
name: Wordnik
x-slug: wordnik
description: Wordnik is an online English dictionary and language resource that provides
  dictionary and thesaurus content, some of it based on print dictionaries such as
  the Century Dictionary, the American Heritage Dictionary, WordNet, and GCIDE. Wordnik
  has collected a corpus of billions of words which it uses to display example sentences,
  allowing it to provide information on a much larger set of words than a typical
  dictionary.
image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2708-wordnik.jpg
x-kinRank: "8"
x-alexaRank: "46540"
tags: Name
created: "2018-06-20"
modified: "2018-06-20"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/wordnik/apis.md
specificationVersion: "0.14"
apis:
- name: Wordnik Authenticates a User
  x-api-slug: wordnik
  description: Authenticates a user.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2708-wordnik.jpg
  humanURL: http://wordnik.com
  baseURL: https://api.wordnik.com//v4//account.json/authenticate/{username}
  tags: Account,Authenticate,Username
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/wordnik/account-jsonauthenticateusername-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/wordnik/account-jsonauthenticateusername-get-openapi.md
- name: Wordnik Authenticates a user
  x-api-slug: wordnik
  description: Authenticates a user.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2708-wordnik.jpg
  humanURL: http://wordnik.com
  baseURL: https://api.wordnik.com//v4//account.json/authenticate/{username}
  tags: Account,Authenticate,Username
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/wordnik/account-jsonauthenticateusername-post-openapi.md
- name: Wordnik
  x-api-slug: wordnik
  description: The Wordnik API lets you request definitions, example sentences, spelling
    suggestions, related words like synonyms and antonyms, phrases containing a given
    word, word autocompletion, random words, words of the day, and much more.
  image: http://kinlane-productions.s3.amazonaws.com/screen-capture-api/2708-wordnik.jpg
  humanURL: http://wordnik.com
  baseURL: https://api.wordnik.com//v4
  tags: Name
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/name/master/_listings/wordnik/openapi.md
x-common:
- type: x-crunchbase
  url: https://crunchbase.com/organization/wordnik
- type: x-developer
  url: http://developer.wordnik.com/
- type: x-documentation
  url: http://developer.wordnik.com/docs.html
- type: x-email
  url: feedback@wordnik.com
- type: x-email
  url: support@wordnik.com
- type: x-email
  url: privacy@wordnik.com
- type: x-email
  url: dmca@wordnik.com
- type: x-github
  url: https://github.com/wordnik
- type: x-twitter
  url: https://twitter.com/wordnik
- type: x-website
  url: http://wordnik.com
- type: x-website
  url: https://www.wordnik.com/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---