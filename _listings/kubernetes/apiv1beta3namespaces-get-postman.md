{
  "info": {
    "name": "Kubernetes Get Namespaces",
    "_postman_id": "4c84e515-86ac-4c5c-885a-20dd69484670",
    "description": "List objects of kind namespace.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Endpoints",
      "item": [
        {
          "id": "67ae6ec2-9e7a-493c-8fc9-4b53be4664f5",
          "name": "listEndpoints",
          "request": {
            "url": "http:///api/v1beta3/127.0.0.1:6443/api/v1beta3/endpoints",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "List objects of kind endpoints."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "eae87629-d02e-4735-a32a-e8641cd4471c"
            }
          ]
        }
      ]
    },
    {
      "name": "Events",
      "item": [
        {
          "id": "dc60fcae-7d97-4ae6-89ff-65242938a968",
          "name": "listEvent",
          "request": {
            "url": "http:///api/v1beta3/127.0.0.1:6443/api/v1beta3/events",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "List objects of kind event."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d9a77c90-06e1-4a7c-a453-0ffbf028c3bf"
            }
          ]
        }
      ]
    },
    {
      "name": "Limitranges",
      "item": [
        {
          "id": "14a8449f-abb3-40c0-b70a-a3ccd7ada178",
          "name": "listLimitRange",
          "request": {
            "url": "http:///api/v1beta3/127.0.0.1:6443/api/v1beta3/limitranges",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "List objects of kind limitrange."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "42f4c191-6a65-4d2b-8e15-c0d8a753c3e3"
            }
          ]
        }
      ]
    },
    {
      "name": "Namespaces",
      "item": [
        {
          "id": "93ff70f2-263b-49fa-8f39-70da0922fed3",
          "name": "listNamespace",
          "request": {
            "url": "http:///api/v1beta3/127.0.0.1:6443/api/v1beta3/namespaces",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "List objects of kind namespace."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f16ef743-b093-470d-9cb9-6b47552f8113"
            }
          ]
        }
      ]
    }
  ]
}