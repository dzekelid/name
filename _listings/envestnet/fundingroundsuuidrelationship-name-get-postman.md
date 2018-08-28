{
  "info": {
    "name": "Crunch Base Get Funding Rounds Relationships",
    "_postman_id": "a3a4c07c-2134-4607-bf23-6d6a247787fa",
    "description": "Get Funding Rounds Relationships",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Acquisitions",
      "item": [
        {
          "id": "e5921d10-162c-46b5-9dce-c81e02b00fe9",
          "name": "acquistions",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.crunchbase.com",
              "path": [
                "v",
                "3",
                "acquisitions/:uuid"
              ],
              "query": [
                {
                  "key": "user_key",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "uuid",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Pull from Acquisition"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bc143bf3-53dc-410f-b4c8-d9633beafc50"
            }
          ]
        },
        {
          "id": "dfb09fa1-953e-49cb-8306-08b1fc3c1095",
          "name": "acquisitionsRelationships",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.crunchbase.com",
              "path": [
                "v",
                "3",
                "acquisitions/:uuid/:relationship_name"
              ],
              "query": [
                {
                  "key": "page",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "sort_order",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "relationship_name",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "uuid",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get Acquisitions Relationships"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4592db42-3273-4cc5-bc88-fd8ff5827f4c"
            }
          ]
        }
      ]
    },
    {
      "name": "Categories",
      "item": [
        {
          "id": "21112085-f352-47df-aa68-c2394345fb68",
          "name": "categories",
          "request": {
            "url": "http://api.crunchbase.com/v/3/categories?page=%7B%7D&sort_order=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get Categories"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "7f2b0250-229d-46d9-ae55-8e3a311d360a"
            }
          ]
        }
      ]
    },
    {
      "name": "Funding",
      "item": [
        {
          "id": "e3f962e7-6e70-4f6c-9831-58d1da9cdd73",
          "name": "fundingRounds",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.crunchbase.com",
              "path": [
                "v",
                "3",
                "funding-rounds/:uuid"
              ],
              "query": [
                {
                  "key": "user_key",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "uuid",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets funding rounds by UUID"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "bf9ec79a-bdd7-4dc3-ab0c-917107225914"
            }
          ]
        },
        {
          "id": "ff5e5bc4-8519-4336-a766-f3a61338cdb1",
          "name": "fundingRoundRelationships",
          "request": {
            "url": {
              "protocol": "http",
              "host": "api.crunchbase.com",
              "path": [
                "v",
                "3",
                "funding-rounds/:uuid/:relationship_name"
              ],
              "query": [
                {
                  "key": "page",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "sort_order",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "relationship_name",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "uuid",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Get Funding Rounds Relationships"
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "504d75b7-4653-4229-b3e2-ec43f85ab9f1"
            }
          ]
        }
      ]
    }
  ]
}