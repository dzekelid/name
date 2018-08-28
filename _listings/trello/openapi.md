swagger: "2.0"
x-collection-name: Trello
x-complete: 1
info:
  title: Trello
  description: this-document-describes-the-rest-api-of-trello-as-published-by-trello-com---a-hrefhttpstrello-comdocsindex-html-target-blankofficial-documentationa--a-hrefhttpstrello-comdocsapi-target-blankthe-html-pages-that-were-scraped-in-order-to-generate-this-specification-a
  termsOfService: https://trello.com/legal
  contact:
    name: Trello
    url: https://trello.com/home
  version: "1.0"
host: trello.com
basePath: /1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /boards/{idBoard}/name:
    put:
      summary: Put Boards Name
      description: Put boards name.
      operationId: updateBoardsNameByIdBoard
      x-api-path-slug: boardsidboardname-put
      parameters:
      - in: body
        name: body
        description: Attributes of Boards Name to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idBoard
        description: board_id
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Boards
      - Name
  /cards/{idCard}/checklist/{idChecklist}/checkItem/{idCheckItem}/name:
    put:
      summary: Put Cards Checklist Checkitem Checkitem Name
      description: Put cards checklist checkitem checkitem name.
      operationId: updateCardsChecklistCheckItemNameByIdCardByIdChecklistByIdCheckItem
      x-api-path-slug: cardsidcardchecklistidchecklistcheckitemidcheckitemname-put
      parameters:
      - in: body
        name: body
        description: Attributes of Cards Checklist Check Item Name to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: path
        name: idCheckItem
        description: idCheckItem
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Checklist
      - Checkitem
      - Checkitem
      - Name
  /cards/{idCard}/name:
    put:
      summary: Put Cards Name
      description: Put cards name.
      operationId: updateCardsNameByIdCard
      x-api-path-slug: cardsidcardname-put
      parameters:
      - in: body
        name: body
        description: Attributes of Cards Name to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idCard
        description: card id or shortlink
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Cards
      - Name
  /checklists/{idChecklist}/name:
    put:
      summary: Put Checklists Name
      description: Put checklists name.
      operationId: updateChecklistsNameByIdChecklist
      x-api-path-slug: checklistsidchecklistname-put
      parameters:
      - in: body
        name: body
        description: Attributes of Checklists Name to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idChecklist
        description: idChecklist
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Checklists
      - Name
  /labels/{idLabel}/name:
    put:
      summary: Put Labels Label Name
      description: Put labels label name.
      operationId: updateLabelsNameByIdLabel
      x-api-path-slug: labelsidlabelname-put
      parameters:
      - in: body
        name: body
        description: Attributes of Labels Name to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idLabel
        description: idLabel
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Labels
      - Label
      - Name
  /lists/{idList}/name:
    put:
      summary: Put Lists List Name
      description: Put lists list name.
      operationId: updateListsNameByIdList
      x-api-path-slug: listsidlistname-put
      parameters:
      - in: body
        name: body
        description: Attributes of Lists Name to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idList
        description: idList
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Lists
      - List
      - Name
  /members/{idMember}/savedSearches/{idSavedSearch}/name:
    put:
      summary: Put Members Savedsearches Savedsearch Name
      description: Put members savedsearches savedsearch name.
      operationId: updateMembersSavedSearchesNameByIdMemberByIdSavedSearch
      x-api-path-slug: membersidmembersavedsearchesidsavedsearchname-put
      parameters:
      - in: body
        name: body
        description: Attributes of Members Saved Searches Name to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idMember
        description: idMember or username
      - in: path
        name: idSavedSearch
        description: idSavedSearch
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Members
      - Savedsearches
      - Savedsearch
      - Name
  /organizations/{idOrg}/name:
    put:
      summary: Put Organizations Name
      description: Put organizations name.
      operationId: updateOrganizationsNameByIdOrg
      x-api-path-slug: organizationsidorgname-put
      parameters:
      - in: body
        name: body
        description: Attributes of Organizations Name to be updated
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: idOrg
        description: idOrg or name
      - in: query
        name: key
        description: Generate your application key
      - in: query
        name: token
        description: Getting a token from a user
      responses:
        200:
          description: OK
      tags:
      - Organizations
      - Name