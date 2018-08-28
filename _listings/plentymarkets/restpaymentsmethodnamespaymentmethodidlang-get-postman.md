{
  "info": {
    "name": "Plentymarkets Gets a payment method name by id and lang",
    "_postman_id": "e8d136d7-0c9a-48f7-beff-f5086028d9b8",
    "description": "Gets a payment method name by id and lang. The ID and the requested lang of the payment method must be specified.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "List",
      "item": [
        {
          "id": "925d409f-446d-492f-9459-cddc58722de2",
          "name": "getRestPaymentsMethodnamesPaymentmethod",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "rest/payments/methodNames/:paymentMethodId"
              ],
              "query": [
                {
                  "key": "itemsPerPage",
                  "value": "%7B%7D",
                  "disabled": false
                },
                {
                  "key": "page",
                  "value": "%7B%7D",
                  "disabled": false
                }
              ],
              "variable": [
                {
                  "id": "paymentMethodId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "List all payment method names for a payment method id. The payment method id must be specified."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "489e4712-5cfa-43f8-b0f8-38bf32a1e3e6"
            }
          ]
        }
      ]
    },
    {
      "name": "S",
      "item": [
        {
          "id": "e6f1a2a1-3ebd-4998-9088-87d490363fb1",
          "name": "getRestPaymentsMethodnamesPaymentmethodLang",
          "request": {
            "url": {
              "protocol": "http",
              "host": "example.com",
              "path": [
                "rest/payments/methodNames/:paymentMethodId/:lang"
              ],
              "variable": [
                {
                  "id": "lang",
                  "value": "{}",
                  "type": "string"
                },
                {
                  "id": "paymentMethodId",
                  "value": "{}",
                  "type": "string"
                }
              ]
            },
            "method": "GET",
            "header": [
              {
                "key": "Accept",
                "value": "*/*",
                "disabled": false
              }
            ],
            "body": {
              "mode": "raw"
            },
            "description": "Gets a payment method name by id and lang. The ID and the requested lang of the payment method must be specified."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3dfc0cd0-6952-4bd2-8084-e4c751b73c8b"
            }
          ]
        }
      ]
    }
  ]
}