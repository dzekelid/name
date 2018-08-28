{
  "info": {
    "name": "AWS CloudSearch List Domain Names",
    "_postman_id": "67a4b3ef-601e-41c3-b9c8-c15d553a8cd2",
    "description": "Lists all search domains owned by an account.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Tags",
      "item": [
        {
          "id": "594cba13-51a5-462d-97d4-2bced5c57e7f",
          "name": "AddTags",
          "request": {
            "url": "http://example.com/api/?Action=AddTags?Base=Base&InternalException=InternalException&LimitExceededException=LimitExceededException&ValidationException=ValidationException",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Attaches resource tags to an\n Amazon CloudSearch domain."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "4d7233bf-8ba1-458c-8443-74f688c857b5"
            }
          ]
        }
      ]
    },
    {
      "name": "Suggesters",
      "item": [
        {
          "id": "7cc91581-9579-4a8b-9257-c48e5334c1d6",
          "name": "BuildSuggesters",
          "request": {
            "url": "http://example.com/api/?Action=BuildSuggesters?DomainName=DomainName",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Indexes the search suggestions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "ec8e8da3-1f8d-44e5-8f2d-a05ca0750cf2"
            }
          ]
        },
        {
          "id": "c6adf832-6e41-49f5-8f0b-6283ea9c4fa1",
          "name": "DefineSuggester",
          "request": {
            "url": "http://example.com/api/?Action=DefineSuggester?DomainName=DomainName&Suggester=Suggester",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Configures a suggester for a domain."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "06b8a425-2cfc-4cf5-b31c-ae2e71f74f7a"
            }
          ]
        },
        {
          "id": "bf36adc1-bc02-43e9-a940-17f3c3d2af64",
          "name": "DeleteSuggester",
          "request": {
            "url": "http://example.com/api/?Action=DeleteSuggester?DomainName=DomainName&SuggesterName=SuggesterName",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes a suggester."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "559e44fc-2477-478a-97c5-6090df4589ae"
            }
          ]
        },
        {
          "id": "891bbf76-73e1-4cad-8aa0-4b42d21bf82e",
          "name": "DescribeSuggesters",
          "request": {
            "url": "http://example.com/api/?Action=DescribeSuggesters?Deployed=Deployed&DomainName=DomainName&SuggesterNames.member.N=SuggesterNames.member.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets the suggesters configured for a domain."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "917c1bbd-ada9-40e5-a5f3-55d627f52cb1"
            }
          ]
        }
      ]
    },
    {
      "name": "Domains",
      "item": [
        {
          "id": "71e5fc18-5bf9-4b21-bc80-7d0fb3e123ee",
          "name": "CreateDomain",
          "request": {
            "url": "http://example.com/api/?Action=CreateDomain?DomainName=DomainName",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Creates a new search domain."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3d0e8748-618b-4371-b1f4-89b4cdd5d17a"
            }
          ]
        },
        {
          "id": "8810bd64-b04a-4cb9-97a3-f32f82cbf013",
          "name": "DeleteDomain",
          "request": {
            "url": "http://example.com/api/?Action=DeleteDomain?DomainName=DomainName",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Permanently deletes a search domain and all of its data."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "66132add-1294-4d2b-bc05-9b953ba978d2"
            }
          ]
        },
        {
          "id": "48be4d05-2528-4a04-8535-1067c8ed83a9",
          "name": "DescribeDomains",
          "request": {
            "url": "http://example.com/api/?Action=DescribeDomains?DomainNames.member.N=DomainNames.member.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets information about the search domains owned by this account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3a2e33a6-43d0-4408-8cb4-e3369f22b8f3"
            }
          ]
        },
        {
          "id": "81ee302a-881c-4a27-9ceb-20f54b2f8f2e",
          "name": "ListDomainNames",
          "request": {
            "url": "http://example.com/api/?Action=ListDomainNames?DomainNames=DomainNames",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Lists all search domains owned by an account."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6c4728cd-f6e0-47ff-840f-f99c0459f9c3"
            }
          ]
        }
      ]
    },
    {
      "name": "Analysis Scheme",
      "item": [
        {
          "id": "8c93d4d2-8514-4370-ae26-dd3723ae39bf",
          "name": "DefineAnalysisScheme",
          "request": {
            "url": "http://example.com/api/?Action=DefineAnalysisScheme?AnalysisScheme=AnalysisScheme&DomainName=DomainName",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Configures an analysis scheme that can be applied to a text or text-array field to define language-specific text processing options."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "6978f025-894e-4337-a774-47d34eb699df"
            }
          ]
        },
        {
          "id": "97e7f64c-a4f6-4d00-8b68-e832942bf214",
          "name": "DeleteAnalysisScheme",
          "request": {
            "url": "http://example.com/api/?Action=DeleteAnalysisScheme?AnalysisSchemeName=AnalysisSchemeName&DomainName=DomainName",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Deletes an analysis scheme."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "cdd520e4-b548-4881-bf48-516029354fc1"
            }
          ]
        },
        {
          "id": "2f667fd2-faf5-4aa6-96e0-68db6fa5e748",
          "name": "DescribeAnalysisSchemes",
          "request": {
            "url": "http://example.com/api/?Action=DescribeAnalysisSchemes?AnalysisSchemeNames.member.N=AnalysisSchemeNames.member.N&Deployed=Deployed&DomainName=DomainName",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets the analysis schemes configured for a domain."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "811f1ff8-99cb-4d40-824b-c0b34b7a2f28"
            }
          ]
        }
      ]
    },
    {
      "name": "Expressions",
      "item": [
        {
          "id": "0655ce98-fdea-40c0-8c9d-d25e4ad773f1",
          "name": "DefineExpression",
          "request": {
            "url": "http://example.com/api/?Action=DefineExpression?DomainName=DomainName&Expression=Expression",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Configures an Expression  for the search domain."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "1e7f2541-c0eb-4f7a-9fcf-44b7dc260619"
            }
          ]
        },
        {
          "id": "dd883cdb-3bd7-4d8a-8570-1e759637fb6f",
          "name": "DeleteExpression",
          "request": {
            "url": "http://example.com/api/?Action=DeleteExpression?DomainName=DomainName&ExpressionName=ExpressionName",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Removes an \n  Expression\n  from the search domain."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "339eccac-130d-4890-a47d-96cec63280dc"
            }
          ]
        },
        {
          "id": "ee69cbff-21a8-4665-9699-30f94f9b145d",
          "name": "DescribeExpressions",
          "request": {
            "url": "http://example.com/api/?Action=DescribeExpressions?Deployed=Deployed&DomainName=DomainName&ExpressionNames.member.N=ExpressionNames.member.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets the expressions configured for the search domain."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "f148ca87-3994-4cb4-82fe-a850ab1a64d2"
            }
          ]
        }
      ]
    },
    {
      "name": "Index Fields",
      "item": [
        {
          "id": "41d7c455-a4e0-45de-83e3-3d8837a9b9ac",
          "name": "DefineIndexField",
          "request": {
            "url": "http://example.com/api/?Action=DefineIndexField?DomainName=DomainName&IndexField=IndexField",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Configures an ndexField  for the search domain."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "a9974d40-e246-4d4d-bd0d-98d12312c11f"
            }
          ]
        },
        {
          "id": "276fd53c-2d50-4aea-bca4-47ca3bf48ee4",
          "name": "DeleteIndexField",
          "request": {
            "url": "http://example.com/api/?Action=DeleteIndexField?DomainName=DomainName&IndexFieldName=IndexFieldName",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Removes an \n  IndexField\n  from the search domain."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "389146dc-6355-4315-aaa5-13634def917d"
            }
          ]
        },
        {
          "id": "bcf5b243-4233-4889-bebd-06fc08a3a279",
          "name": "DescribeIndexFields",
          "request": {
            "url": "http://example.com/api/?Action=DescribeIndexFields?Deployed=Deployed&DomainName=DomainName&FieldNames.member.N=FieldNames.member.N",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets information about the index fields configured for the search domain."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "557b9377-f116-43bf-840c-9b2b01b7c4ba"
            }
          ]
        }
      ]
    },
    {
      "name": "Availability Options",
      "item": [
        {
          "id": "cac013ac-4293-4a2f-8570-fd7e2425f872",
          "name": "DescribeAvailabilityOptions",
          "request": {
            "url": "http://example.com/api/?Action=DescribeAvailabilityOptions?Deployed=Deployed&DomainName=DomainName",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets the availability options configured for a domain."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "3a4e5e69-c611-44ef-b069-7b7fbcc57eca"
            }
          ]
        }
      ]
    },
    {
      "name": "Scaling Parameters",
      "item": [
        {
          "id": "0d08a253-ff76-43ab-8e7e-974deb3dc291",
          "name": "DescribeScalingParameters",
          "request": {
            "url": "http://example.com/api/?Action=DescribeScalingParameters?DomainName=DomainName",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets the scaling parameters configured for a domain."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "d5043568-0730-42a2-9317-cc0511cb7006"
            }
          ]
        }
      ]
    },
    {
      "name": "Service Access Policies",
      "item": [
        {
          "id": "f48618b4-8b0a-4fb9-8cf3-9c40f368fd4d",
          "name": "DescribeServiceAccessPolicies",
          "request": {
            "url": "http://example.com/api/?Action=DescribeServiceAccessPolicies?Deployed=Deployed&DomainName=DomainName",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Gets information about the access policies that control access to the domain's document and search endpoints."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "16881464-37ad-46e9-b440-371f53253ec6"
            }
          ]
        }
      ]
    },
    {
      "name": "Index Documents",
      "item": [
        {
          "id": "9d5a3951-fa53-4d2d-9d2b-02bb0caa1206",
          "name": "IndexDocuments",
          "request": {
            "url": "http://example.com/api/?Action=IndexDocuments?DomainName=DomainName",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Tells the search domain to start indexing its documents using the latest indexing options."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "af426659-e912-4136-b8e6-080222cd30af"
            }
          ]
        }
      ]
    }
  ]
}