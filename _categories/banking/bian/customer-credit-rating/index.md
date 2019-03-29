---
layout: api-single
title: Customer Credit Rating
parent-title: BIAN APIs
description: Banking API Standards - APIs - Customer Credit Rating
keywords: 
duration: 
type: api
standard: bian
order: 4
parent: /categories/banking/bian
api-logo: /dist/images/logos/bian_logo.svg
api-summary: This service domain maintains and administers the bank's credit assessment for customers based on consolidated internal data and optionally by referencing external credit agency reports
api-example-use: A customer calls the contact center wishing to know what mortgage offers they are eligible for. The customer servicing representative (CSR) uses the customer's internal credit assessment as one input to reference the Product Directory to retrieve the details of available products and terms.
api-published-by: bianuser02 team
---
<script id="api-spec" type="application/json">
{
  "swagger": "2.0",
  "info": {
    "version": "1.0.0",
    "title": "Customer Credit Rating",
    "description": "This service domain maintains and administers the bank's credit assessment for customers."
  },
  "host": "bianorg.azure-api.net",
  "basePath": "/sd-customer-credit-r/v1",
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
    "/customer-credit-rating/customer-credit-rating-measurement/{cr-reference-id}/alerts/recording": {
      "post": {
        "tags": [
          "record"
        ],
        "summary": "Record information against Customer Credit Rating alert",
        "operationId": "recordCustomerCreditRatingMeasurementAlert",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Credit Rating Assessment Reference",
            "required": true,
            "type": "string"
          },
          {
            "in": "body",
            "name": "body",
            "description": "Customer Credit Rating Alert Request Payload",
            "required": false,
            "schema": {
              "type": "object",
              "properties": {
                "customerReference": {
                  "type": "string",
                  "example": "CR564",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerCreditRatingAssessmentReference": {
                  "type": "string",
                  "example": "CCRAR232342",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "productInstanceReference": {
                  "type": "string",
                  "example": "PIR7676",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "employeeBusinessUnitReference": {
                  "type": "string",
                  "example": "EBUR5567",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerCreditAlertType": {
                  "type": "string",
                  "example": "CCAT678",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerCreditAlertDescription": {
                  "type": "string",
                  "example": "Alert",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "dateTime": {
                  "type": "string",
                  "example": "2018-09-06T09:00:00",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
                }
              },
              "example": {
                "dateTime": "2018-09-06T09:00:00",
                "productInstanceReference": "PIR7676",
                "employeeBusinessUnitReference": "EBUR5567",
                "customerReference": "CR564",
                "customerCreditAlertDescription": "Alert",
                "customerCreditRatingAssessmentReference": "CCRAR232342",
                "customerCreditAlertType": "CCAT678"
              }
            }
          }
        ],
        "responses": {
          "201": {
            "description": "Created a Customer Credit Rating Alert record successfully",
            "schema": {
              "type": "object",
              "properties": {
                "customerCreditAlertReference": {
                  "type": "string",
                  "example": "CCAR2342",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "recordingRecordStatus": {
                  "type": "string",
                  "example": "Applied",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                }
              },
              "example": {
                "customerCreditAlertReference": "CCAR2342",
                "recordingRecordStatus": "Applied"
              }
            }
          }
        }
      }
    },
    "/customer-credit-rating/customer-credit-rating-measurement/{cr-reference-id}/recording": {
      "post": {
        "tags": [
          "record"
        ],
        "summary": "Record information against Customer Credit Rating assessment",
        "operationId": "recordCustomerCreditRatingMeasurement",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Credit Rating Assessment Reference",
            "required": true,
            "type": "string"
          },
          {
            "in": "body",
            "name": "body",
            "description": "Record Request Payload",
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
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
                  "properties": {}
                },
                "recordingRecordDateTime": {
                  "type": "string",
                  "example": "2018-09-06T09:00:00",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
                },
                "employeeBusinessUnitReference": {
                  "type": "string",
                  "example": "REF456",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                }
              },
              "example": {
                "recordingRecordType": "Behavior model performance feedback",
                "employeeBusinessUnitReference": "REF456",
                "recordingRecordDateTime": "2018-09-06T09:00:00",
                "recordingRecord": "{}"
              }
            }
          }
        ],
        "responses": {
          "201": {
            "description": "Created a Customer Credit Rating record successfully",
            "schema": {
              "type": "object",
              "properties": {
                "recordingRecordReference": {
                  "type": "string",
                  "example": "RRR4678",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "recordingRecordStatus": {
                  "type": "string",
                  "example": "Applied",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                }
              },
              "example": {
                "recordingRecordReference": "RRR4678",
                "recordingRecordStatus": "Applied"
              }
            }
          }
        }
      }
    },
    "/customer-credit-rating/customer-credit-rating-measurement/{cr-reference-id}/requisition": {
      "put": {
        "tags": [
          "request"
        ],
        "summary": "update Request to undertake credit view refresh/reworking",
        "operationId": "requestCustomerCreditRatingMeasurementUpdate",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Credit Rating Assessment Reference",
            "required": true,
            "type": "string"
          },
          {
            "in": "body",
            "name": "body",
            "description": "Customer Credit Assessment Request Payload",
            "required": true,
            "schema": {
              "properties": {
                "customerCreditRatingAssessment": {
                  "type": "string",
                  "example": "internal bank credit rating/assessment",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerBehaviorModel": {
                  "type": "string",
                  "example": "model2",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "ratingAgencyCreditReportReference": {
                  "type": "string",
                  "example": "RACRR538",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "internalCreditAnalysisReportReference": {
                  "type": "string",
                  "example": "ICARR980",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerReference": {
                  "type": "string",
                  "example": "CR1234",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerCreditRatingAssessmentType": {
                  "type": "string",
                  "example": "corporate",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerCreditRatingNarrative": {
                  "type": "string",
                  "example": "structured report outlining basis for rating",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerCreditRatingSchedule": {
                  "type": "string",
                  "example": "update schedule",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                }
              },
              "example": {
                "customerCreditRatingSchedule": "update schedule",
                "customerCreditRatingAssessment": "internal bank credit rating/assessment",
                "internalCreditAnalysisReportReference": "ICARR980",
                "ratingAgencyCreditReportReference": "RACRR538",
                "customerReference": "CR1234",
                "customerCreditRatingNarrative": "structured report outlining basis for rating",
                "customerCreditRatingAssessmentType": "corporate",
                "customerBehaviorModel": "model2"
              }
            }
          }
        ],
        "responses": {
          "200": {
            "description": "Updated a Customer Credit Rating record successfully",
            "schema": {
              "properties": {
                "customerCreditRatingAssessmentReference": {
                  "type": "string",
                  "example": "CCRAR232342",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerCreditRatingAssessment": {
                  "type": "string",
                  "example": "internal bank credit rating/assessment",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerBehaviorModel": {
                  "type": "string",
                  "example": "model2",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "ratingAgencyCreditReportReference": {
                  "type": "string",
                  "example": "RRCRR436",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "internalCreditAnalysisReportReference": {
                  "type": "string",
                  "example": "ICARR9090",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerReference": {
                  "type": "string",
                  "example": "CR437",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerCreditRatingAssessmentType": {
                  "type": "string",
                  "example": "corporate",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerCreditRatingNarrative": {
                  "type": "string",
                  "example": "structured report outlining basis for rating",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerCreditRatingSchedule": {
                  "type": "string",
                  "example": "update schedule",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                }
              },
              "example": {
                "customerCreditRatingSchedule": "update schedule",
                "customerCreditRatingAssessment": "internal bank credit rating/assessment",
                "internalCreditAnalysisReportReference": "ICARR9090",
                "ratingAgencyCreditReportReference": "RRCRR436",
                "customerReference": "CR437",
                "customerCreditRatingNarrative": "structured report outlining basis for rating",
                "customerCreditRatingAssessmentType": "corporate",
                "customerCreditRatingAssessmentReference": "CCRAR232342",
                "customerBehaviorModel": "model2"
              }
            }
          }
        }
      }
    },
    "/customer-credit-rating/customer-credit-rating-measurement/requisition": {
      "post": {
        "tags": [
          "request"
        ],
        "summary": "Create Request to undertake credit view refresh/reworking",
        "operationId": "requestCustomerCreditRatingMeasurementCreate",
        "parameters": [
          {
            "in": "body",
            "name": "body",
            "description": "Customer Credit Assessment Request Payload",
            "required": true,
            "schema": {
              "properties": {
                "customerCreditRatingAssessment": {
                  "type": "string",
                  "example": "internal bank credit rating/assessment",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerBehaviorModel": {
                  "type": "string",
                  "example": "model2",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "ratingAgencyCreditReportReference": {
                  "type": "string",
                  "example": "RACRR538",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "internalCreditAnalysisReportReference": {
                  "type": "string",
                  "example": "ICARR980",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerReference": {
                  "type": "string",
                  "example": "CR1234",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerCreditRatingAssessmentType": {
                  "type": "string",
                  "example": "corporate",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerCreditRatingNarrative": {
                  "type": "string",
                  "example": "structured report outlining basis for rating",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerCreditRatingSchedule": {
                  "type": "string",
                  "example": "update schedule",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                }
              },
              "example": {
                "customerCreditRatingSchedule": "update schedule",
                "customerCreditRatingAssessment": "internal bank credit rating/assessment",
                "internalCreditAnalysisReportReference": "ICARR980",
                "ratingAgencyCreditReportReference": "RACRR538",
                "customerReference": "CR1234",
                "customerCreditRatingNarrative": "structured report outlining basis for rating",
                "customerCreditRatingAssessmentType": "corporate",
                "customerBehaviorModel": "model2"
              }
            }
          }
        ],
        "responses": {
          "201": {
            "description": "Created a Customer Credit Rating record successfully",
            "schema": {
              "properties": {
                "customerCreditRatingAssessmentReference": {
                  "type": "string",
                  "example": "CCRAR232342",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerCreditRatingAssessment": {
                  "type": "string",
                  "example": "internal bank credit rating/assessment",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerBehaviorModel": {
                  "type": "string",
                  "example": "model2",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "ratingAgencyCreditReportReference": {
                  "type": "string",
                  "example": "RRCRR436",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "internalCreditAnalysisReportReference": {
                  "type": "string",
                  "example": "ICARR9090",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerReference": {
                  "type": "string",
                  "example": "CR437",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerCreditRatingAssessmentType": {
                  "type": "string",
                  "example": "corporate",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerCreditRatingNarrative": {
                  "type": "string",
                  "example": "structured report outlining basis for rating",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerCreditRatingSchedule": {
                  "type": "string",
                  "example": "update schedule",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                }
              },
              "example": {
                "customerCreditRatingSchedule": "update schedule",
                "customerCreditRatingAssessment": "internal bank credit rating/assessment",
                "internalCreditAnalysisReportReference": "ICARR9090",
                "ratingAgencyCreditReportReference": "RRCRR436",
                "customerReference": "CR437",
                "customerCreditRatingNarrative": "structured report outlining basis for rating",
                "customerCreditRatingAssessmentType": "corporate",
                "customerCreditRatingAssessmentReference": "CCRAR232342",
                "customerBehaviorModel": "model2"
              }
            }
          }
        }
      }
    },
    "/customer-credit-rating/customer-credit-rating-measurement": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve Customer Credit Rating  Control Record Ids available within the Service Domain.",
        "operationId": "retrieveCustomerCreditRatingMeasurementReferenceIds",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "collection-filter",
            "in": "query",
            "description": "Filter to refine the result set. ex- 'customerBehaviorModel = CBM123'",
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
                "CCR123",
                "CCR345"
              ]
            }
          }
        }
      }
    },
    "/customer-credit-rating/customer-credit-rating-measurement/behavior-qualifiers": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve all Behaviour Qualifier names in Customer Credit Rating Domain.",
        "operationId": "retrieveCustomerCreditRatingMeasurementBehaviorQualifiers",
        "produces": [
          "application/json"
        ],
        "parameters": [],
        "responses": {
          "200": {
            "description": "Retrieved all Behaviour Qualifier names in Customer Credit Rating Domain successfully",
            "schema": {
              "type": "array",
              "items": {
                "type": "string"
              },
              "example": [
                "external-rating",
                "internal-analysis"
              ]
            }
          }
        }
      }
    },
    "/customer-credit-rating/customer-credit-rating-measurement/{cr-reference-id}/{behavior-qualifier}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve Behaviour Qualifier Reference Ids of a given Behavior Qulifier.",
        "operationId": "RetrieveBehaviorQualifierReferenceIds",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Credit Rating Assessment Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "behavior-qualifier",
            "in": "path",
            "description": "Behavior Qualifier Name. ex- external-rating",
            "required": true,
            "type": "string"
          },
          {
            "name": "collection-filter",
            "in": "query",
            "description": "Filter to refine the result set. ex- 'ratingAgencyCreditReportType = type-1'",
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
                "ER345",
                "ER789",
                "ER456"
              ]
            }
          }
        }
      }
    },
    "/customer-credit-rating/customer-credit-rating-measurement/{cr-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Customer Credit Rating Assessment record",
        "operationId": "retrieveCustomerCreditRatingMeasurement",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Credit Rating Assessment Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "Retrieved Customer Credit Rating Assessment record successfully",
            "schema": {
              "properties": {
                "customerCreditRatingAssessmentReference": {
                  "type": "string",
                  "example": "CCRAR232342",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerCreditRatingAssessment": {
                  "type": "string",
                  "example": "internal bank credit rating/assessment",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerBehaviorModel": {
                  "type": "string",
                  "example": "model2",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "ratingAgencyCreditReportReference": {
                  "type": "string",
                  "example": "RRCRR436",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "internalCreditAnalysisReportReference": {
                  "type": "string",
                  "example": "ICARR9090",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerReference": {
                  "type": "string",
                  "example": "CR437",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerCreditRatingAssessmentType": {
                  "type": "string",
                  "example": "corporate",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerCreditRatingNarrative": {
                  "type": "string",
                  "example": "structured report outlining basis for rating",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerCreditRatingSchedule": {
                  "type": "string",
                  "example": "update schedule",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                }
              },
              "example": {
                "customerCreditRatingSchedule": "update schedule",
                "customerCreditRatingAssessment": "internal bank credit rating/assessment",
                "internalCreditAnalysisReportReference": "ICARR9090",
                "ratingAgencyCreditReportReference": "RRCRR436",
                "customerReference": "CR437",
                "customerCreditRatingNarrative": "structured report outlining basis for rating",
                "customerCreditRatingAssessmentType": "corporate",
                "customerCreditRatingAssessmentReference": "CCRAR232342",
                "customerBehaviorModel": "model2"
              }
            }
          }
        }
      }
    },
    "/customer-credit-rating/customer-credit-rating-measurement/{cr-reference-id}/alerts/{bq-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve Alerts Behaviour Qualifier with all its' attributes.",
        "operationId": "Retrievealerts",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Credit Rating Assessment Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Rating Agency Credit Report Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "Retrieved Customer Credit Alerts record successfully",
            "schema": {
              "properties": {
                "customerCreditAlertReference": {
                  "type": "string",
                  "example": "CCRAR232342",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerReference": {
                  "type": "string",
                  "example": "CCRAR232342",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerCreditRatingAssessmentReference": {
                  "type": "string",
                  "example": "CCRAR232342",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "productInstanceReference": {
                  "type": "string",
                  "example": "CCRAR232342",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "employeeBusinessUnitReference": {
                  "type": "string",
                  "example": "CCRAR232342",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerCreditAlertType": {
                  "type": "string",
                  "example": "CCRAR232342",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerCreditAlertDescription": {
                  "type": "string",
                  "example": "Customer Credit Alert",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "dateTime": {
                  "type": "string",
                  "example": "2018-09-06T09:00:00",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
                }
              },
              "example": {
                "dateTime": "2018-09-06T09:00:00",
                "productInstanceReference": "CCRAR232342",
                "employeeBusinessUnitReference": "CCRAR232342",
                "customerReference": "CCRAR232342",
                "customerCreditAlertDescription": "Customer Credit Alert",
                "customerCreditAlertReference": "CCRAR232342",
                "customerCreditRatingAssessmentReference": "CCRAR232342",
                "customerCreditAlertType": "CCRAR232342"
              }
            }
          }
        }
      }
    },
    "/customer-credit-rating/customer-credit-rating-measurement/{cr-reference-id}/external-ratings/{bq-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve External Rating Behaviour Qualifier with all its' attributes.",
        "operationId": "Retrieveexternalratings",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Credit Rating Assessment Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Rating Agency Credit Report Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "Retrieved Customer Credit External Rating record successfully",
            "schema": {
              "properties": {
                "customerCreditRatingAssessmentReference": {
                  "type": "string",
                  "example": "CCRAR232342",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "ratingAgencyReference": {
                  "type": "string",
                  "example": "RAR888",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "ratingAgencyAccessServiceSessionReference": {
                  "type": "string",
                  "example": "RAASSR237",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "ratingAgencyAccessSchedule": {
                  "type": "string",
                  "example": "service availability",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerReference": {
                  "type": "string",
                  "example": "CR568",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "ratingAgencyCreditReportType": {
                  "type": "string",
                  "example": "long/short form report",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Code\n"
                },
                "ratingAgencyCreditReportReference": {
                  "type": "string",
                  "example": "RACRR432",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "ratingAgencyCreditReport": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
                  "properties": {}
                },
                "ratingAgengyCreditReportDateTime": {
                  "type": "string",
                  "example": "2018-09-06T09:00:00",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
                }
              },
              "example": {
                "ratingAgencyCreditReportType": "long/short form report",
                "ratingAgencyCreditReport": "{}",
                "ratingAgengyCreditReportDateTime": "2018-09-06T09:00:00",
                "ratingAgencyCreditReportReference": "RACRR432",
                "customerReference": "CR568",
                "ratingAgencyAccessServiceSessionReference": "RAASSR237",
                "ratingAgencyAccessSchedule": "service availability",
                "customerCreditRatingAssessmentReference": "CCRAR232342",
                "ratingAgencyReference": "RAR888"
              }
            }
          }
        }
      }
    },
    "/customer-credit-rating/customer-credit-rating-measurement/{cr-reference-id}/internal-analysis/{bq-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve Internal Analysis Behaviour Qualifier with all its' attributes.",
        "operationId": "Retrieveinternalanalysis",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Credit Rating Assessment Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Internal Credit Analysis Report Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "Retrieved Customer Credit Internal Analysis record successfully",
            "schema": {
              "type": "object",
              "properties": {
                "customerCreditRatingAssessmentReference": {
                  "type": "string",
                  "example": "CCRAR232342",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "internalCreditAnalysisReportReference": {
                  "type": "string",
                  "example": "ICARR23476",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "productServiceActivityReportReference": {
                  "type": "string",
                  "example": "PSARR4567",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "productServiceActivityReport": {
                  "type": "string",
                  "example": "PSAR132",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n"
                },
                "customerReference": {
                  "type": "string",
                  "example": "CR987",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerBehaviorModel": {
                  "type": "string",
                  "example": "CBM777",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "internalCreditAnalysisReportType": {
                  "type": "string",
                  "example": "ICART23476",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Code\n"
                },
                "internalCreditAnalysisReport": {
                  "type": "string",
                  "example": "ICAR23476",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n"
                },
                "internalCreditAnalysisReportDateTime": {
                  "type": "string",
                  "example": "2018-09-06T09:00:00",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
                }
              },
              "example": {
                "internalCreditAnalysisReport": "ICAR23476",
                "internalCreditAnalysisReportDateTime": "2018-09-06T09:00:00",
                "internalCreditAnalysisReportReference": "ICARR23476",
                "internalCreditAnalysisReportType": "ICART23476",
                "customerReference": "CR987",
                "customerCreditRatingAssessmentReference": "CCRAR232342",
                "productServiceActivityReportReference": "PSARR4567",
                "customerBehaviorModel": "CBM777",
                "productServiceActivityReport": "PSAR132"
              }
            }
          }
        }
      }
    }
  },
  "definitions": {
    "CreditRatingAlerts": {
      "properties": {
        "customerCreditAlertReference": {
          "type": "string",
          "example": "CCRAR232342",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerReference": {
          "type": "string",
          "example": "CCRAR232342",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerCreditRatingAssessmentReference": {
          "type": "string",
          "example": "CCRAR232342",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "productInstanceReference": {
          "type": "string",
          "example": "CCRAR232342",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "employeeBusinessUnitReference": {
          "type": "string",
          "example": "CCRAR232342",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerCreditAlertType": {
          "type": "string",
          "example": "CCRAR232342",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "customerCreditAlertDescription": {
          "type": "string",
          "example": "Customer Credit Alert",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "dateTime": {
          "type": "string",
          "example": "2018-09-06T09:00:00",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
        }
      },
      "example": {
        "dateTime": "2018-09-06T09:00:00",
        "productInstanceReference": "CCRAR232342",
        "employeeBusinessUnitReference": "CCRAR232342",
        "customerReference": "CCRAR232342",
        "customerCreditAlertDescription": "Customer Credit Alert",
        "customerCreditAlertReference": "CCRAR232342",
        "customerCreditRatingAssessmentReference": "CCRAR232342",
        "customerCreditAlertType": "CCRAR232342"
      }
    },
    "CreditRatingExternalRating": {
      "properties": {
        "customerCreditRatingAssessmentReference": {
          "type": "string",
          "example": "CCRAR232342",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "ratingAgencyReference": {
          "type": "string",
          "example": "RAR888",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "ratingAgencyAccessServiceSessionReference": {
          "type": "string",
          "example": "RAASSR237",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "ratingAgencyAccessSchedule": {
          "type": "string",
          "example": "service availability",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "customerReference": {
          "type": "string",
          "example": "CR568",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "ratingAgencyCreditReportType": {
          "type": "string",
          "example": "long/short form report",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Code\n"
        },
        "ratingAgencyCreditReportReference": {
          "type": "string",
          "example": "RACRR432",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "ratingAgencyCreditReport": {
          "type": "object",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
          "properties": {}
        },
        "ratingAgengyCreditReportDateTime": {
          "type": "string",
          "example": "2018-09-06T09:00:00",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
        }
      },
      "example": {
        "ratingAgencyCreditReportType": "long/short form report",
        "ratingAgencyCreditReport": "{}",
        "ratingAgengyCreditReportDateTime": "2018-09-06T09:00:00",
        "ratingAgencyCreditReportReference": "RACRR432",
        "customerReference": "CR568",
        "ratingAgencyAccessServiceSessionReference": "RAASSR237",
        "ratingAgencyAccessSchedule": "service availability",
        "customerCreditRatingAssessmentReference": "CCRAR232342",
        "ratingAgencyReference": "RAR888"
      }
    },
    "CreditRatingInternalAnalysisBase": {
      "type": "object",
      "properties": {
        "customerCreditRatingAssessmentReference": {
          "type": "string",
          "example": "CCRAR232342",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "internalCreditAnalysisReportReference": {
          "type": "string",
          "example": "ICARR23476",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "productServiceActivityReportReference": {
          "type": "string",
          "example": "PSARR4567",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "productServiceActivityReport": {
          "type": "string",
          "example": "PSAR132",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n"
        },
        "customerReference": {
          "type": "string",
          "example": "CR987",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerBehaviorModel": {
          "type": "string",
          "example": "CBM777",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "internalCreditAnalysisReportType": {
          "type": "string",
          "example": "ICART23476",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Code\n"
        },
        "internalCreditAnalysisReport": {
          "type": "string",
          "example": "ICAR23476",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n"
        },
        "internalCreditAnalysisReportDateTime": {
          "type": "string",
          "example": "2018-09-06T09:00:00",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
        }
      },
      "example": {
        "internalCreditAnalysisReport": "ICAR23476",
        "internalCreditAnalysisReportDateTime": "2018-09-06T09:00:00",
        "internalCreditAnalysisReportReference": "ICARR23476",
        "internalCreditAnalysisReportType": "ICART23476",
        "customerReference": "CR987",
        "customerCreditRatingAssessmentReference": "CCRAR232342",
        "productServiceActivityReportReference": "PSARR4567",
        "customerBehaviorModel": "CBM777",
        "productServiceActivityReport": "PSAR132"
      }
    },
    "CreditRatingBaseWithId": {
      "properties": {
        "customerCreditRatingAssessmentReference": {
          "type": "string",
          "example": "CCRAR232342",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerCreditRatingAssessment": {
          "type": "string",
          "example": "internal bank credit rating/assessment",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "customerBehaviorModel": {
          "type": "string",
          "example": "model2",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "ratingAgencyCreditReportReference": {
          "type": "string",
          "example": "RRCRR436",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "internalCreditAnalysisReportReference": {
          "type": "string",
          "example": "ICARR9090",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerReference": {
          "type": "string",
          "example": "CR437",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerCreditRatingAssessmentType": {
          "type": "string",
          "example": "corporate",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "customerCreditRatingNarrative": {
          "type": "string",
          "example": "structured report outlining basis for rating",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "customerCreditRatingSchedule": {
          "type": "string",
          "example": "update schedule",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        }
      },
      "example": {
        "customerCreditRatingSchedule": "update schedule",
        "customerCreditRatingAssessment": "internal bank credit rating/assessment",
        "internalCreditAnalysisReportReference": "ICARR9090",
        "ratingAgencyCreditReportReference": "RRCRR436",
        "customerReference": "CR437",
        "customerCreditRatingNarrative": "structured report outlining basis for rating",
        "customerCreditRatingAssessmentType": "corporate",
        "customerCreditRatingAssessmentReference": "CCRAR232342",
        "customerBehaviorModel": "model2"
      }
    },
    "AlertRecordRequest": {
      "type": "object",
      "properties": {
        "customerReference": {
          "type": "string",
          "example": "CR564",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerCreditRatingAssessmentReference": {
          "type": "string",
          "example": "CCRAR232342",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "productInstanceReference": {
          "type": "string",
          "example": "PIR7676",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "employeeBusinessUnitReference": {
          "type": "string",
          "example": "EBUR5567",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerCreditAlertType": {
          "type": "string",
          "example": "CCAT678",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "customerCreditAlertDescription": {
          "type": "string",
          "example": "Alert",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "dateTime": {
          "type": "string",
          "example": "2018-09-06T09:00:00",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
        }
      },
      "example": {
        "dateTime": "2018-09-06T09:00:00",
        "productInstanceReference": "PIR7676",
        "employeeBusinessUnitReference": "EBUR5567",
        "customerReference": "CR564",
        "customerCreditAlertDescription": "Alert",
        "customerCreditRatingAssessmentReference": "CCRAR232342",
        "customerCreditAlertType": "CCAT678"
      }
    },
    "AlertRecordResponse": {
      "type": "object",
      "properties": {
        "customerCreditAlertReference": {
          "type": "string",
          "example": "CCAR2342",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "recordingRecordStatus": {
          "type": "string",
          "example": "Applied",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        }
      },
      "example": {
        "customerCreditAlertReference": "CCAR2342",
        "recordingRecordStatus": "Applied"
      }
    },
    "CreditRatingBase": {
      "properties": {
        "customerCreditRatingAssessment": {
          "type": "string",
          "example": "internal bank credit rating/assessment",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "customerBehaviorModel": {
          "type": "string",
          "example": "model2",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "ratingAgencyCreditReportReference": {
          "type": "string",
          "example": "RACRR538",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "internalCreditAnalysisReportReference": {
          "type": "string",
          "example": "ICARR980",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerReference": {
          "type": "string",
          "example": "CR1234",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerCreditRatingAssessmentType": {
          "type": "string",
          "example": "corporate",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "customerCreditRatingNarrative": {
          "type": "string",
          "example": "structured report outlining basis for rating",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "customerCreditRatingSchedule": {
          "type": "string",
          "example": "update schedule",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        }
      },
      "example": {
        "customerCreditRatingSchedule": "update schedule",
        "customerCreditRatingAssessment": "internal bank credit rating/assessment",
        "internalCreditAnalysisReportReference": "ICARR980",
        "ratingAgencyCreditReportReference": "RACRR538",
        "customerReference": "CR1234",
        "customerCreditRatingNarrative": "structured report outlining basis for rating",
        "customerCreditRatingAssessmentType": "corporate",
        "customerBehaviorModel": "model2"
      }
    },
    "CreditRatingRecordRequest": {
      "type": "object",
      "properties": {
        "recordingRecordType": {
          "type": "string",
          "example": "Behavior model performance feedback",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "recordingRecord": {
          "type": "object",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
          "properties": {}
        },
        "recordingRecordDateTime": {
          "type": "string",
          "example": "2018-09-06T09:00:00",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
        },
        "employeeBusinessUnitReference": {
          "type": "string",
          "example": "REF456",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        }
      },
      "example": {
        "recordingRecordType": "Behavior model performance feedback",
        "employeeBusinessUnitReference": "REF456",
        "recordingRecordDateTime": "2018-09-06T09:00:00",
        "recordingRecord": "{}"
      }
    },
    "CreditRatingRecordResponse": {
      "type": "object",
      "properties": {
        "recordingRecordReference": {
          "type": "string",
          "example": "RRR4678",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "recordingRecordStatus": {
          "type": "string",
          "example": "Applied",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        }
      },
      "example": {
        "recordingRecordReference": "RRR4678",
        "recordingRecordStatus": "Applied"
      }
    }
  }
}
</script>