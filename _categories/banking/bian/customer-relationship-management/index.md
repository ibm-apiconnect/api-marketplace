---
layout: api-single
title: Customer Relationship Management
parent-title: BIAN APIs
description: Banking API Standards - APIs - Customer Relationship Management
keywords: 
duration: 
type: api
standard: bian
order: 4
parent: /categories/banking/bian
api-logo: /dist/images/logos/bian_logo.svg
api-summary: This service domain develops and executes a customer plan to maintain and build a customer relationship. Activities include ongoing customer contact, tracking internal and external events and activity of interest and relevance, product and service matching and sales, processing ad-hoc queries.
api-example-use: A corporate customer relationship manager reviews recent activity for a customer and notices that levels of activity are trending lower. Possible external (market) and internal (servicing/ fulfillment) activities are reviewed for possible causes.
api-published-by: bianuser02 team
---
<script id="api-spec" type="application/json">
{
  "swagger": "2.0",
  "info": {
    "version": "1.0.0",
    "title": "Customer Relationship Management",
    "description": "This service domain develops, executes a customer plan to maintain and build a customer relationship"
  },
  "host": "bianorg.azure-api.net",
  "basePath": "/sd-customer-relation/v1",
  "securityDefinitions": {
    "apiKeyHeader": {
      "type": "apiKey",
      "name": "Ocp-Apim-Subscription-Key",
      "in": "header"
    }
  },
  "security": [
    {
      "apiKeyHeader": []
    }
  ],
  "schemes": [
    "https"
  ],
  "consumes": [
    "application/json"
  ],
  "produces": [
    "application/json"
  ],
  "paths": {
    "/customer-relationship-management/customer-relationship-management-plan/{cr-reference-id}/recording": {
      "post": {
        "tags": [
          "record"
        ],
        "summary": "Record information against a relationship managed activity",
        "description": "Record information against a relationship managed activity",
        "operationId": "recordCustomerRelationshipManagementPlan",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Relationship Plan Reference",
            "required": true,
            "type": "string"
          },
          {
            "in": "body",
            "name": "body",
            "description": "Record control record request payload",
            "required": true,
            "schema": {
              "type": "object",
              "properties": {
                "recordingRecordType": {
                  "type": "string",
                  "example": "Behavior model performance feedback",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "recordingRecord": {
                  "type": "object",
                  "example": "the feedback",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
                  "properties": {}
                },
                "recordingRecordDateTime": {
                  "type": "string",
                  "example": "2018-09-02",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
                },
                "employeeBusinessUnitReference": {
                  "type": "string",
                  "example": "EBU7623524",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                }
              },
              "example": {
                "recordingRecordType": "Behavior model performance feedback",
                "employeeBusinessUnitReference": "EBU7623524",
                "recordingRecordDateTime": "2018-09-02",
                "recordingRecord": "the feedback"
              }
            }
          }
        ],
        "responses": {
          "201": {
            "description": "A new record is created",
            "schema": {
              "type": "object",
              "properties": {
                "recordingRecordReference": {
                  "type": "string",
                  "example": "RRR59821735",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "recordingRecordStatus": {
                  "type": "string",
                  "example": "Applied",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                }
              },
              "example": {
                "recordingRecordReference": "RRR59821735",
                "recordingRecordStatus": "Applied"
              }
            }
          }
        }
      }
    },
    "/customer-relationship-management/customer-relationship-management-plan/{cr-reference-id}/requisition": {
      "put": {
        "tags": [
          "request"
        ],
        "summary": "Request relationship management support/troubleshooting assistance",
        "description": "Update an existing incident",
        "operationId": "requestCustomerRelationshipManagementPlanUpdate",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Relationship Plan Reference",
            "required": true,
            "type": "string"
          },
          {
            "in": "body",
            "name": "body",
            "required": true,
            "schema": {
              "type": "object",
              "properties": {
                "customerReference": {
                  "type": "string",
                  "example": "CR736235",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "employeeBusinessUnitReference": {
                  "type": "string",
                  "example": "EMP4678",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "productServiceActivityReference": {
                  "type": "string",
                  "example": "SAR72365425",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerIncidentType": {
                  "type": "string",
                  "example": "Customer Incident Type",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerIncidentDescription": {
                  "type": "string",
                  "example": "narrative of cause/impact",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerIncidentResolution": {
                  "type": "string",
                  "example": "narrative of resolution actions",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                }
              },
              "example": {
                "customerIncidentType": "Customer Incident Type",
                "customerIncidentResolution": "narrative of resolution actions",
                "employeeBusinessUnitReference": "EMP4678",
                "customerIncidentDescription": "narrative of cause/impact",
                "customerReference": "CR736235",
                "productServiceActivityReference": "SAR72365425"
              }
            }
          }
        ],
        "responses": {
          "200": {
            "description": "Successfully Updated Incident Record",
            "schema": {
              "type": "object",
              "properties": {
                "customerIncidentReference": {
                  "type": "string",
                  "example": "CIR7235244",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerRelationshipPlanReference": {
                  "type": "string",
                  "example": "CRPR72546",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerReference": {
                  "type": "string",
                  "example": "CR736235",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "employeeBusinessUnitReference": {
                  "type": "string",
                  "example": "EMP4678",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "productServiceActivityReference": {
                  "type": "string",
                  "example": "SAR72365425",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerIncidentType": {
                  "type": "string",
                  "example": "Customer Incident Type",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerIncidentDescription": {
                  "type": "string",
                  "example": "narrative of cause/impact",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerIncidentResolution": {
                  "type": "string",
                  "example": "narrative of resolution actions",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                }
              },
              "example": {
                "customerIncidentType": "Customer Incident Type",
                "customerIncidentResolution": "narrative of resolution actions",
                "employeeBusinessUnitReference": "EMP4678",
                "customerRelationshipPlanReference": "CRPR72546",
                "customerIncidentDescription": "narrative of cause/impact",
                "customerIncidentReference": "CIR7235244",
                "customerReference": "CR736235",
                "productServiceActivityReference": "SAR72365425"
              }
            }
          }
        }
      }
    },
    "/customer-relationship-management/customer-relationship-management-plan/requisition": {
      "post": {
        "tags": [
          "request"
        ],
        "summary": "Request relationship management support/troubleshooting assistance",
        "description": "Create new incident",
        "operationId": "requestCustomerRelationshipManagementPlanCreate",
        "parameters": [
          {
            "in": "body",
            "name": "body",
            "required": true,
            "schema": {
              "type": "object",
              "properties": {
                "customerReference": {
                  "type": "string",
                  "example": "CR736235",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "employeeBusinessUnitReference": {
                  "type": "string",
                  "example": "EMP4678",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "productServiceActivityReference": {
                  "type": "string",
                  "example": "SAR72365425",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerIncidentType": {
                  "type": "string",
                  "example": "Customer Incident Type",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerIncidentDescription": {
                  "type": "string",
                  "example": "narrative of cause/impact",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerIncidentResolution": {
                  "type": "string",
                  "example": "narrative of resolution actions",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                }
              },
              "example": {
                "customerIncidentType": "Customer Incident Type",
                "customerIncidentResolution": "narrative of resolution actions",
                "employeeBusinessUnitReference": "EMP4678",
                "customerIncidentDescription": "narrative of cause/impact",
                "customerReference": "CR736235",
                "productServiceActivityReference": "SAR72365425"
              }
            }
          }
        ],
        "responses": {
          "201": {
            "description": "Successfully Created New Incident Record",
            "schema": {
              "type": "object",
              "properties": {
                "customerIncidentReference": {
                  "type": "string",
                  "example": "CIR7235244",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerRelationshipPlanReference": {
                  "type": "string",
                  "example": "CRPR72546",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerReference": {
                  "type": "string",
                  "example": "CR736235",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "employeeBusinessUnitReference": {
                  "type": "string",
                  "example": "EMP4678",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "productServiceActivityReference": {
                  "type": "string",
                  "example": "SAR72365425",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerIncidentType": {
                  "type": "string",
                  "example": "Customer Incident Type",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerIncidentDescription": {
                  "type": "string",
                  "example": "narrative of cause/impact",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerIncidentResolution": {
                  "type": "string",
                  "example": "narrative of resolution actions",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                }
              },
              "example": {
                "customerIncidentType": "Customer Incident Type",
                "customerIncidentResolution": "narrative of resolution actions",
                "employeeBusinessUnitReference": "EMP4678",
                "customerRelationshipPlanReference": "CRPR72546",
                "customerIncidentDescription": "narrative of cause/impact",
                "customerIncidentReference": "CIR7235244",
                "customerReference": "CR736235",
                "productServiceActivityReference": "SAR72365425"
              }
            }
          }
        }
      }
    },
    "/customer-relationship-management/customer-relationship-management-plan": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve Customer Relationship Management Control Record Ids available within the Service Domain.",
        "operationId": "RetrieveCustomerRelationshipManagementReferenceIds",
        "parameters": [
          {
            "name": "collection-filter",
            "in": "query",
            "description": "Filter to refine the result set. ex- 'customerReference == \"CR763254\"'",
            "required": false,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "successful",
            "schema": {
              "type": "array",
              "items": {
                "type": "string"
              },
              "example": [
                "CRM123",
                "CRM345"
              ]
            }
          }
        }
      }
    },
    "/customer-relationship-management/customer-relationship-management-plan/behavior-qualifiers": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve all Behaviour Qualifier names in the Customer Relationship Management Service Domain.",
        "operationId": "RetrieveCustomerRelationshipManagementBehaviorQualifiers",
        "parameters": [],
        "responses": {
          "200": {
            "description": "successful",
            "schema": {
              "type": "array",
              "items": {
                "type": "string"
              },
              "example": [
                "development",
                "incident",
                "contact"
              ]
            }
          }
        }
      }
    },
    "/customer-relationship-management/customer-relationship-management-plan/{cr-reference-id}/{behavior-qualifier}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve Behaviour Qualifier Reference Ids of the given Behavior Qulifier.",
        "operationId": "RetrieveBehaviorQualifierReferenceIds",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Relationship Plan Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "behavior-qualifier",
            "in": "path",
            "description": "Behavior Qualifier Name. ex- development",
            "required": true,
            "type": "string"
          },
          {
            "name": "collection-filter",
            "in": "query",
            "description": "Filter to refine the result set. i.e. 'customerReference == \"CR763254\"'",
            "required": false,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "successful",
            "schema": {
              "type": "array",
              "items": {
                "type": "string"
              },
              "example": [
                "DEV345",
                "DEV789",
                "DEV456"
              ]
            }
          }
        }
      }
    },
    "/customer-relationship-management/customer-relationship-management-plan/{cr-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve Customer Relationship Management Relationship Plan Record",
        "operationId": "RetrieveCustomerRelationshipManagement",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Relationship Plan Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "Successfully Retrieved Customer Relationship Management Relationship Plan Record",
            "schema": {
              "type": "object",
              "properties": {
                "customerRelationshipPlanReference": {
                  "type": "string",
                  "example": "CRPR762542",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerRelationshipPlan": {
                  "type": "string",
                  "example": "details planned and actual product coverage and profitability and relationship development and trouble-shooting",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerReference": {
                  "type": "string",
                  "example": "CRM4658",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "employeeBusinessUnitReference": {
                  "type": "string",
                  "example": "EBU7264424",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerRelationshipRatingType": {
                  "type": "string",
                  "example": "credit",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerRelationshipRating": {
                  "type": "string",
                  "example": "customer Relationship Rating",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerInsightType": {
                  "type": "string",
                  "example": "retention candidate",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerInsightDescription": {
                  "type": "string",
                  "example": "Customer Insight Description",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerBudget": {
                  "type": "string",
                  "example": "arget income and allowed expenses/discounts",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerProductCoverage": {
                  "type": "string",
                  "example": "product/service coverage",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerProductUsage": {
                  "type": "string",
                  "example": "product activity",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerProductEligibilityProfile": {
                  "type": "string",
                  "example": "unsold/eligible products",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerSalesPlan": {
                  "type": "string",
                  "example": "target product sales and associated contact schedule",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerProfitability": {
                  "type": "string",
                  "example": "assessment of net business impact of relationship",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Measure\n"
                },
                "customerRelationshipContactHistory": {
                  "type": "string",
                  "example": "Customer Relationship Contact History",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                }
              },
              "example": {
                "customerProductUsage": "product activity",
                "customerRelationshipContactHistory": "Customer Relationship Contact History",
                "customerInsightType": "retention candidate",
                "customerBudget": "arget income and allowed expenses/discounts",
                "employeeBusinessUnitReference": "EBU7264424",
                "customerRelationshipPlanReference": "CRPR762542",
                "customerInsightDescription": "Customer Insight Description",
                "customerProductCoverage": "product/service coverage",
                "customerSalesPlan": "target product sales and associated contact schedule",
                "customerRelationshipPlan": "details planned and actual product coverage and profitability and relationship development and trouble-shooting",
                "customerReference": "CRM4658",
                "customerProfitability": "assessment of net business impact of relationship",
                "customerRelationshipRatingType": "credit",
                "customerRelationshipRating": "customer Relationship Rating",
                "customerProductEligibilityProfile": "unsold/eligible products"
              }
            }
          }
        }
      }
    },
    "/customer-relationship-management/customer-relationship-management-plan/{cr-reference-id}/developments/{bq-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve Customer Relationship Management Plan Development Record",
        "operationId": "retrieveDevelopment",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Relationship Plan Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Customer Development Task Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "Successful",
            "schema": {
              "type": "object",
              "properties": {
                "customerDevelopmentTaskReference": {
                  "type": "string",
                  "example": "CDTR346479",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerRelationshipPlanReference": {
                  "type": "string",
                  "example": "CRPR635479",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerDevelopmentTaskType": {
                  "type": "string",
                  "example": "up-sell",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerDevelopmentTaskDescription": {
                  "type": "string",
                  "example": "Customer Development Task Description",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerReference": {
                  "type": "string",
                  "example": "CR736464",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "employeeBusinessUnitReference": {
                  "type": "string",
                  "example": "EBU7454748",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerSalesPlan": {
                  "type": "string",
                  "example": "Customer Sales Plan",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerRelationshipContactReference": {
                  "type": "string",
                  "example": "CRCR726464",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerDevelopmentTaskResult": {
                  "type": "string",
                  "example": "Success",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                }
              },
              "example": {
                "employeeBusinessUnitReference": "EBU7454748",
                "customerRelationshipPlanReference": "CRPR635479",
                "customerDevelopmentTaskType": "up-sell",
                "customerDevelopmentTaskReference": "CDTR346479",
                "customerSalesPlan": "Customer Sales Plan",
                "customerDevelopmentTaskDescription": "Customer Development Task Description",
                "customerReference": "CR736464",
                "customerRelationshipContactReference": "CRCR726464",
                "customerDevelopmentTaskResult": "Success"
              }
            }
          }
        }
      }
    },
    "/customer-relationship-management/customer-relationship-management-plan/{cr-reference-id}/incidents/{bq-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve Customer Relationship Management Plan Incident Record",
        "operationId": "retrieveIncident",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Relationship Plan Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Customer Incident Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "Successfully Retrieved Customer Relationship Management Plan Incident Record",
            "schema": {
              "type": "object",
              "properties": {
                "customerIncidentReference": {
                  "type": "string",
                  "example": "CIR7235244",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerRelationshipPlanReference": {
                  "type": "string",
                  "example": "CRPR72546",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerReference": {
                  "type": "string",
                  "example": "CR736235",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "employeeBusinessUnitReference": {
                  "type": "string",
                  "example": "EMP4678",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "productServiceActivityReference": {
                  "type": "string",
                  "example": "SAR72365425",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerIncidentType": {
                  "type": "string",
                  "example": "Customer Incident Type",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerIncidentDescription": {
                  "type": "string",
                  "example": "narrative of cause/impact",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerIncidentResolution": {
                  "type": "string",
                  "example": "narrative of resolution actions",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                }
              },
              "example": {
                "customerIncidentType": "Customer Incident Type",
                "customerIncidentResolution": "narrative of resolution actions",
                "employeeBusinessUnitReference": "EMP4678",
                "customerRelationshipPlanReference": "CRPR72546",
                "customerIncidentDescription": "narrative of cause/impact",
                "customerIncidentReference": "CIR7235244",
                "customerReference": "CR736235",
                "productServiceActivityReference": "SAR72365425"
              }
            }
          }
        }
      }
    },
    "/customer-relationship-management/customer-relationship-management-plan/{cr-reference-id}/contacts/{bq-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve Customer Relationship Management Plan Contact Record",
        "operationId": "retrieveContact",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Relationship Plan Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Customer Relationship Plan Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "Successfully Retrieved Customer Relationship Management Plan Contact Record",
            "schema": {
              "type": "object",
              "properties": {
                "customerRelationshipPlanReference": {
                  "type": "string",
                  "example": "8Z232342",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerContactReference": {
                  "type": "string",
                  "example": "8Z232342",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerReference": {
                  "type": "string",
                  "example": "8Z232342",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerRelationshipContactHistory": {
                  "type": "string",
                  "example": "Customer Relationship Contact History",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerRelationshipContactSchedule": {
                  "type": "string",
                  "example": "CustomerRelationshipContact Schedule",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerRelationshipContactDateTimeLocation": {
                  "type": "string",
                  "example": "2018-09-02 16:34:00 EST New York USA",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
                },
                "employeeReference": {
                  "type": "string",
                  "example": "8Z232342",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerRelationshipContactType": {
                  "type": "string",
                  "example": "type/purpose of contact",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerRelationshipContactRecord": {
                  "type": "object",
                  "example": "log of contact",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
                  "properties": {}
                },
                "customerRelationshipContactResult": {
                  "type": "string",
                  "example": "Customer Relationship Contact Result",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                }
              },
              "example": {
                "customerRelationshipPlanReference": "8Z232342",
                "employeeReference": "8Z232342",
                "customerRelationshipContactSchedule": "CustomerRelationshipContact Schedule",
                "customerRelationshipContactType": "type/purpose of contact",
                "customerReference": "8Z232342",
                "customerRelationshipContactHistory": "Customer Relationship Contact History",
                "customerContactReference": "8Z232342",
                "customerRelationshipContactDateTimeLocation": "2018-09-02 16:34:00 EST New York USA",
                "customerRelationshipContactResult": "Customer Relationship Contact Result",
                "customerRelationshipContactRecord": "log of contact"
              }
            }
          }
        }
      }
    }
  },
  "definitions": {
    "DevelopmentBaseWithIdAndRoot": {
      "type": "object",
      "properties": {
        "customerDevelopmentTaskReference": {
          "type": "string",
          "example": "CDTR346479",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerRelationshipPlanReference": {
          "type": "string",
          "example": "CRPR635479",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerDevelopmentTaskType": {
          "type": "string",
          "example": "up-sell",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "customerDevelopmentTaskDescription": {
          "type": "string",
          "example": "Customer Development Task Description",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "customerReference": {
          "type": "string",
          "example": "CR736464",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "employeeBusinessUnitReference": {
          "type": "string",
          "example": "EBU7454748",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerSalesPlan": {
          "type": "string",
          "example": "Customer Sales Plan",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "customerRelationshipContactReference": {
          "type": "string",
          "example": "CRCR726464",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerDevelopmentTaskResult": {
          "type": "string",
          "example": "Success",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        }
      },
      "example": {
        "employeeBusinessUnitReference": "EBU7454748",
        "customerRelationshipPlanReference": "CRPR635479",
        "customerDevelopmentTaskType": "up-sell",
        "customerDevelopmentTaskReference": "CDTR346479",
        "customerSalesPlan": "Customer Sales Plan",
        "customerDevelopmentTaskDescription": "Customer Development Task Description",
        "customerReference": "CR736464",
        "customerRelationshipContactReference": "CRCR726464",
        "customerDevelopmentTaskResult": "Success"
      }
    },
    "ContactBaseWithIdAndRoot": {
      "type": "object",
      "properties": {
        "customerRelationshipPlanReference": {
          "type": "string",
          "example": "8Z232342",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerContactReference": {
          "type": "string",
          "example": "8Z232342",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerReference": {
          "type": "string",
          "example": "8Z232342",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerRelationshipContactHistory": {
          "type": "string",
          "example": "Customer Relationship Contact History",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "customerRelationshipContactSchedule": {
          "type": "string",
          "example": "CustomerRelationshipContact Schedule",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "customerRelationshipContactDateTimeLocation": {
          "type": "string",
          "example": "2018-09-02 16:34:00 EST New York USA",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
        },
        "employeeReference": {
          "type": "string",
          "example": "8Z232342",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerRelationshipContactType": {
          "type": "string",
          "example": "type/purpose of contact",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "customerRelationshipContactRecord": {
          "type": "object",
          "example": "log of contact",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
          "properties": {}
        },
        "customerRelationshipContactResult": {
          "type": "string",
          "example": "Customer Relationship Contact Result",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        }
      },
      "example": {
        "customerRelationshipPlanReference": "8Z232342",
        "employeeReference": "8Z232342",
        "customerRelationshipContactSchedule": "CustomerRelationshipContact Schedule",
        "customerRelationshipContactType": "type/purpose of contact",
        "customerReference": "8Z232342",
        "customerRelationshipContactHistory": "Customer Relationship Contact History",
        "customerContactReference": "8Z232342",
        "customerRelationshipContactDateTimeLocation": "2018-09-02 16:34:00 EST New York USA",
        "customerRelationshipContactResult": "Customer Relationship Contact Result",
        "customerRelationshipContactRecord": "log of contact"
      }
    },
    "RetrieveCustomerRelationshipManagementPlanResponse": {
      "type": "object",
      "properties": {
        "customerRelationshipPlanReference": {
          "type": "string",
          "example": "CRPR762542",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerRelationshipPlan": {
          "type": "string",
          "example": "details planned and actual product coverage and profitability and relationship development and trouble-shooting",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "customerReference": {
          "type": "string",
          "example": "CRM4658",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "employeeBusinessUnitReference": {
          "type": "string",
          "example": "EBU7264424",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerRelationshipRatingType": {
          "type": "string",
          "example": "credit",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "customerRelationshipRating": {
          "type": "string",
          "example": "customer Relationship Rating",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "customerInsightType": {
          "type": "string",
          "example": "retention candidate",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "customerInsightDescription": {
          "type": "string",
          "example": "Customer Insight Description",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "customerBudget": {
          "type": "string",
          "example": "arget income and allowed expenses/discounts",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "customerProductCoverage": {
          "type": "string",
          "example": "product/service coverage",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "customerProductUsage": {
          "type": "string",
          "example": "product activity",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "customerProductEligibilityProfile": {
          "type": "string",
          "example": "unsold/eligible products",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "customerSalesPlan": {
          "type": "string",
          "example": "target product sales and associated contact schedule",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "customerProfitability": {
          "type": "string",
          "example": "assessment of net business impact of relationship",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Measure\n"
        },
        "customerRelationshipContactHistory": {
          "type": "string",
          "example": "Customer Relationship Contact History",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        }
      },
      "example": {
        "customerProductUsage": "product activity",
        "customerRelationshipContactHistory": "Customer Relationship Contact History",
        "customerInsightType": "retention candidate",
        "customerBudget": "arget income and allowed expenses/discounts",
        "employeeBusinessUnitReference": "EBU7264424",
        "customerRelationshipPlanReference": "CRPR762542",
        "customerInsightDescription": "Customer Insight Description",
        "customerProductCoverage": "product/service coverage",
        "customerSalesPlan": "target product sales and associated contact schedule",
        "customerRelationshipPlan": "details planned and actual product coverage and profitability and relationship development and trouble-shooting",
        "customerReference": "CRM4658",
        "customerProfitability": "assessment of net business impact of relationship",
        "customerRelationshipRatingType": "credit",
        "customerRelationshipRating": "customer Relationship Rating",
        "customerProductEligibilityProfile": "unsold/eligible products"
      }
    },
    "RelationshipPlanRecordRequest": {
      "type": "object",
      "properties": {
        "recordingRecordType": {
          "type": "string",
          "example": "Behavior model performance feedback",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "recordingRecord": {
          "type": "object",
          "example": "the feedback",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
          "properties": {}
        },
        "recordingRecordDateTime": {
          "type": "string",
          "example": "2018-09-02",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
        },
        "employeeBusinessUnitReference": {
          "type": "string",
          "example": "EBU7623524",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        }
      },
      "example": {
        "recordingRecordType": "Behavior model performance feedback",
        "employeeBusinessUnitReference": "EBU7623524",
        "recordingRecordDateTime": "2018-09-02",
        "recordingRecord": "the feedback"
      }
    },
    "RelationshipPlanRecordResponse": {
      "type": "object",
      "properties": {
        "recordingRecordReference": {
          "type": "string",
          "example": "RRR59821735",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "recordingRecordStatus": {
          "type": "string",
          "example": "Applied",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        }
      },
      "example": {
        "recordingRecordReference": "RRR59821735",
        "recordingRecordStatus": "Applied"
      }
    },
    "IncidentBase": {
      "type": "object",
      "properties": {
        "customerReference": {
          "type": "string",
          "example": "CR736235",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "employeeBusinessUnitReference": {
          "type": "string",
          "example": "EMP4678",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "productServiceActivityReference": {
          "type": "string",
          "example": "SAR72365425",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerIncidentType": {
          "type": "string",
          "example": "Customer Incident Type",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "customerIncidentDescription": {
          "type": "string",
          "example": "narrative of cause/impact",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "customerIncidentResolution": {
          "type": "string",
          "example": "narrative of resolution actions",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        }
      },
      "example": {
        "customerIncidentType": "Customer Incident Type",
        "customerIncidentResolution": "narrative of resolution actions",
        "employeeBusinessUnitReference": "EMP4678",
        "customerIncidentDescription": "narrative of cause/impact",
        "customerReference": "CR736235",
        "productServiceActivityReference": "SAR72365425"
      }
    },
    "IncidentBaseWithIdAndRoot": {
      "type": "object",
      "properties": {
        "customerIncidentReference": {
          "type": "string",
          "example": "CIR7235244",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerRelationshipPlanReference": {
          "type": "string",
          "example": "CRPR72546",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerReference": {
          "type": "string",
          "example": "CR736235",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "employeeBusinessUnitReference": {
          "type": "string",
          "example": "EMP4678",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "productServiceActivityReference": {
          "type": "string",
          "example": "SAR72365425",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerIncidentType": {
          "type": "string",
          "example": "Customer Incident Type",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "customerIncidentDescription": {
          "type": "string",
          "example": "narrative of cause/impact",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "customerIncidentResolution": {
          "type": "string",
          "example": "narrative of resolution actions",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        }
      },
      "example": {
        "customerIncidentType": "Customer Incident Type",
        "customerIncidentResolution": "narrative of resolution actions",
        "employeeBusinessUnitReference": "EMP4678",
        "customerRelationshipPlanReference": "CRPR72546",
        "customerIncidentDescription": "narrative of cause/impact",
        "customerIncidentReference": "CIR7235244",
        "customerReference": "CR736235",
        "productServiceActivityReference": "SAR72365425"
      }
    }
  }
}
</script>