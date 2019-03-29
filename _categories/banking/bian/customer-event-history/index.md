---
layout: api-single
title: Customer Event History
parent-title: BIAN APIs
description: Banking API Standards - APIs - Customer Event History
keywords: 
duration: 
type: api
standard: bian
order: 4
parent: /categories/banking/bian
api-logo: /dist/images/logos/bian_logo.svg
api-summary: This service domain captures, classifies and stores relationship, servicing and product fulfillment related customer events. In addition to servicing and product transaction details, the log can capture life/relationship events that are revealed during customer exchanges.
api-example-use: A customer contacts the call center to enquire about account transactions and during the dialogue the servicing representative detects a life event (e.g. the customer is moving house). The contact details and life event are captured in the customer history.
api-published-by: bianuser02 team
---
<script id="api-spec" type="application/json">
{
  "swagger": "2.0",
  "info": {
    "version": "1.0.0",
    "title": "Customer Event History",
    "description": "This service domain captures, classifies and stores relationship, servicing and product fulfillment."
  },
  "host": "bianorg.azure-api.net",
  "basePath": "/sd-customer-event-hi/v1",
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
    "/customer-event-history/customer-event-log/{cr-reference-id}/updation": {
      "put": {
        "tags": [
          "update"
        ],
        "summary": "Update a Customer Event History record",
        "operationId": "updateCustomerEventLog",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Event Log Reference",
            "required": true,
            "type": "string"
          },
          {
            "in": "body",
            "name": "body",
            "description": "Update control record request payload",
            "required": true,
            "schema": {
              "type": "object",
              "properties": {
                "customerEventLog": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n",
                  "properties": {}
                },
                "customerReference": {
                  "type": "string",
                  "example": "CR764656",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                }
              },
              "example": {
                "customerEventLog": "{}",
                "customerReference": "CR764656"
              }
            }
          }
        ],
        "responses": {
          "200": {
            "description": "Successfully Updated Customer Event History record",
            "schema": {
              "type": "object",
              "properties": {
                "customerEventLogReference": {
                  "type": "string",
                  "example": "CELR736464",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerEventLog": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n",
                  "properties": {}
                },
                "customerReference": {
                  "type": "string",
                  "example": "CR764656",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                }
              },
              "example": {
                "customerEventLog": "{}",
                "customerEventLogReference": "CELR736464",
                "customerReference": "CR764656"
              }
            }
          }
        }
      }
    },
    "/customer-event-history/customer-event-log/{cr-reference-id}/relationships/{bq-reference-id}/recording": {
      "post": {
        "tags": [
          "record"
        ],
        "summary": "Record a customer relationship event",
        "description": "Record a customer relationship event",
        "operationId": "recordCustomerEventLogCustomerRelationshipEvent",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Event Log Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Customer Relationship Event Reference",
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
                "customerRelationshipEventType": {
                  "type": "string",
                  "example": "advisory",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "employeeUnitReference": {
                  "type": "string",
                  "example": "EUR736465",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerRelationshipEventRecord": {
                  "type": "object",
                  "example": "captured information/details in the log",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
                  "properties": {}
                },
                "customerRelationshipEventAction": {
                  "type": "string",
                  "example": "agreed follow-up activity",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "dateTimeLocation": {
                  "type": "string",
                  "example": "2018-03-28 12:30:00 CST Dallas USA",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
                }
              },
              "example": {
                "customerRelationshipEventRecord": "captured information/details in the log",
                "customerRelationshipEventType": "advisory",
                "employeeUnitReference": "EUR736465",
                "customerRelationshipEventAction": "agreed follow-up activity",
                "dateTimeLocation": "2018-03-28 12:30:00 CST Dallas USA"
              }
            }
          }
        ],
        "responses": {
          "201": {
            "description": "Successfully Created a customer relationship event record",
            "schema": {
              "type": "object",
              "properties": {
                "recordingRecordReference": {
                  "type": "string",
                  "example": "RRR123",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerRelationshipEventResult": {
                  "type": "string",
                  "example": "successful",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                }
              },
              "example": {
                "recordingRecordReference": "RRR123",
                "customerRelationshipEventResult": "successful"
              }
            }
          }
        }
      }
    },
    "/customer-event-history/customer-event-log/{cr-reference-id}/sales/{bq-reference-id}/recording": {
      "post": {
        "tags": [
          "record"
        ],
        "summary": "Record a customer sales event",
        "description": "Record a customer sales event",
        "operationId": "recordCustomerEventLogSalesEvent",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Event Log Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Customer Sales Event Reference",
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
                "customerSalesEventType": {
                  "type": "string",
                  "example": "solicited",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "employeeUnitReference": {
                  "type": "string",
                  "example": "EUR7236464",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "productServiceType": {
                  "type": "string",
                  "example": "Product Service Type",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "leadOpportunityReference": {
                  "type": "string",
                  "example": "LOR736464",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerSalesEventRecord": {
                  "type": "object",
                  "example": "captured information/details in the log",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
                  "properties": {}
                },
                "commissionAgreementReference": {
                  "type": "string",
                  "example": "CAR736464",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "dateTimeLocation": {
                  "type": "string",
                  "example": "2018-03-28 12:30:00 CST Dallas USA",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
                }
              },
              "example": {
                "customerSalesEventRecord": "captured information/details in the log",
                "customerSalesEventType": "solicited",
                "employeeUnitReference": "EUR7236464",
                "dateTimeLocation": "2018-03-28 12:30:00 CST Dallas USA",
                "commissionAgreementReference": "CAR736464",
                "leadOpportunityReference": "LOR736464",
                "productServiceType": "Product Service Type"
              }
            }
          }
        ],
        "responses": {
          "201": {
            "description": "Successfully Created a customer sales event record",
            "schema": {
              "type": "object",
              "properties": {
                "recordingRecordReference": {
                  "type": "string",
                  "example": "RRR123",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerSalesEventResult": {
                  "type": "string",
                  "example": "successful",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                }
              },
              "example": {
                "recordingRecordReference": "RRR123",
                "customerSalesEventResult": "successful"
              }
            }
          }
        }
      }
    },
    "/customer-event-history/customer-event-log/{cr-reference-id}/servicings/{bq-reference-id}/recording": {
      "post": {
        "tags": [
          "record"
        ],
        "summary": "Record a customer servicing event",
        "description": "Record a customer servicing event",
        "operationId": "recordCustomerEventLogServicingEvent",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Event Log Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Customer Servicing Event Reference",
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
                "customerServicingEventType": {
                  "type": "string",
                  "example": "assisted",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerContactDialogueRecordReference": {
                  "type": "string",
                  "example": "CDRR736464",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "accessedProductService": {
                  "type": "string",
                  "example": "referenced products/services",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "channelDeviceType": {
                  "type": "string",
                  "example": "device type",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "contactPurpose": {
                  "type": "string",
                  "example": "purpose for contact",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "contactResult": {
                  "type": "string",
                  "example": "successful",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "employeeUnit Reference": {
                  "type": "string",
                  "example": "EUR63544",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerServicingEventRecord": {
                  "type": "object",
                  "example": "captured information/details in the log",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
                  "properties": {}
                },
                "dateTimeLocation": {
                  "type": "string",
                  "example": "2018-03-28 12:30:00 CST Dallas USA",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
                }
              },
              "example": {
                "channelDeviceType": "device type",
                "accessedProductService": "referenced products/services",
                "dateTimeLocation": "2018-03-28 12:30:00 CST Dallas USA",
                "customerContactDialogueRecordReference": "CDRR736464",
                "employeeUnit Reference": "EUR63544",
                "customerServicingEventRecord": "captured information/details in the log",
                "contactResult": "successful",
                "customerServicingEventType": "assisted",
                "contactPurpose": "purpose for contact"
              }
            }
          }
        ],
        "responses": {
          "201": {
            "description": "Successfully Created a customer servicing event record",
            "schema": {
              "type": "object",
              "properties": {
                "recordingRecordReference": {
                  "type": "string",
                  "example": "RRR123",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerServicingEventResult": {
                  "type": "string",
                  "example": "successful",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                }
              },
              "example": {
                "customerServicingEventResult": "successful",
                "recordingRecordReference": "RRR123"
              }
            }
          }
        }
      }
    },
    "/customer-event-history/customer-event-log/{cr-reference-id}/product-services/{bq-reference-id}/recording": {
      "post": {
        "tags": [
          "record"
        ],
        "summary": "Record a customer product servicing/alert event",
        "description": "Record a customer product servicing/alert event",
        "operationId": "recordCustomerEventLogProductServiceEvent/Alert",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Event Log Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Customer Product Event Reference",
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
                "productInstanceReference": {
                  "type": "string",
                  "example": "PIR726454",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "productActionEventType": {
                  "type": "string",
                  "example": "payment initiation",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "productActionEventDescription": {
                  "type": "string",
                  "example": "details of action is available",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "productActionEventResult": {
                  "type": "string",
                  "example": "successful",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "employeeUnitReference": {
                  "type": "string",
                  "example": "EUR7236454",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerProductServiceEventRecord": {
                  "type": "object",
                  "example": "captured information/details in the log",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
                  "properties": {}
                },
                "dateTimeLocation": {
                  "type": "string",
                  "example": "2018-03-28 12:30:00 CST Dallas USA",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
                }
              },
              "example": {
                "productActionEventType": "payment initiation",
                "productInstanceReference": "PIR726454",
                "employeeUnitReference": "EUR7236454",
                "dateTimeLocation": "2018-03-28 12:30:00 CST Dallas USA",
                "productActionEventDescription": "details of action is available",
                "customerProductServiceEventRecord": "captured information/details in the log",
                "productActionEventResult": "successful"
              }
            }
          }
        ],
        "responses": {
          "201": {
            "description": "Successfully Created a customer product-services/alert event record",
            "schema": {
              "type": "object",
              "properties": {
                "recordingRecordReference": {
                  "type": "string",
                  "example": "RRR123",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerProductServiceEventResult": {
                  "type": "string",
                  "example": "successful",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                }
              },
              "example": {
                "customerProductServiceEventResult": "successful",
                "recordingRecordReference": "RRR123"
              }
            }
          }
        }
      }
    },
    "/customer-event-history/customer-event-log/{cr-reference-id}/frauds/{bq-reference-id}/recording": {
      "post": {
        "tags": [
          "record"
        ],
        "summary": "Record a customer Fraud event",
        "description": "Record a customer Fraud event",
        "operationId": "recordCustomerEventLogFraudEvent",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Event Log Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Customer Fraud Event Reference",
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
                "customerFraudCaseEventType": {
                  "type": "string",
                  "example": "stolen card",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerContactDialogueRecordReference": {
                  "type": "string",
                  "example": "CDRR737464",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "accessedProductService": {
                  "type": "string",
                  "example": "referenced products/services if provided",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "employeeUnitReference": {
                  "type": "string",
                  "example": "EUR736464",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "fraudCaseReference": {
                  "type": "string",
                  "example": "FCR736474",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "dateTimeLocation": {
                  "type": "string",
                  "example": "2018-03-28 12:30:00 CST Dallas USA",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
                }
              },
              "example": {
                "accessedProductService": "referenced products/services if provided",
                "employeeUnitReference": "EUR736464",
                "customerFraudCaseEventType": "stolen card",
                "fraudCaseReference": "FCR736474",
                "dateTimeLocation": "2018-03-28 12:30:00 CST Dallas USA",
                "customerContactDialogueRecordReference": "CDRR737464"
              }
            }
          }
        ],
        "responses": {
          "201": {
            "description": "Successfully Created a customer fraud event record",
            "schema": {
              "type": "object",
              "properties": {
                "recordingRecordReference": {
                  "type": "string",
                  "example": "RRR123",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerFraudEventResult": {
                  "type": "string",
                  "example": "successful",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                }
              },
              "example": {
                "recordingRecordReference": "RRR123",
                "customerFraudEventResult": "successful"
              }
            }
          }
        }
      }
    },
    "/customer-event-history/customer-event-log/{cr-reference-id}/lives/{bq-reference-id}/recording": {
      "post": {
        "tags": [
          "record"
        ],
        "summary": "Record a customer life event",
        "description": "Record a customer life event",
        "operationId": "recordCustomerEventLogLifeEvent",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Event Log Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Customer Life Event Reference",
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
                "customerLifeEventType": {
                  "type": "string",
                  "example": "relocation",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerContactReference": {
                  "type": "string",
                  "example": "CCR736464",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "employeeUnitReference": {
                  "type": "string",
                  "example": "EUR736464",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerLifeEventRecord": {
                  "type": "object",
                  "example": "captured information/details in the log",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
                  "properties": {}
                },
                "customerLifeEventVerificationStatus": {
                  "type": "string",
                  "example": true,
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "dateTimeLocation": {
                  "type": "string",
                  "example": "2018-03-28 12:30:00 CST Dallas USA",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
                }
              },
              "example": {
                "employeeUnitReference": "EUR736464",
                "customerLifeEventRecord": "captured information/details in the log",
                "dateTimeLocation": "2018-03-28 12:30:00 CST Dallas USA",
                "customerContactReference": "CCR736464",
                "customerLifeEventVerificationStatus": true,
                "customerLifeEventType": "relocation"
              }
            }
          }
        ],
        "responses": {
          "201": {
            "description": "Successfully Created a customer life event record",
            "schema": {
              "type": "object",
              "properties": {
                "recordingRecordReference": {
                  "type": "string",
                  "example": "RRR123",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerLifeEventResult": {
                  "type": "string",
                  "example": "successful",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                }
              },
              "example": {
                "recordingRecordReference": "RRR123",
                "customerLifeEventResult": "successful"
              }
            }
          }
        }
      }
    },
    "/customer-event-history/customer-event-log": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve Customer Event History Control Record IDs available within the Service Domain.",
        "operationId": "RetrieveCustomerEventHistoryReferenceIds",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "collection-filter",
            "in": "query",
            "description": "Filter to refine the result set. ex- 'customeReference == CR123'",
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
                "CELR123",
                "CELR345"
              ]
            }
          }
        }
      }
    },
    "/customer-event-history/customer-event-log/behavior-qualifiers": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve all Behaviour Qualifier names in the Current Account Service Domain.",
        "operationId": "RetrieveCurrentAccountBehaviorQualifiers",
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
                "relationship",
                "sales",
                "servicing",
                "product-service",
                "fraud",
                "life"
              ]
            }
          }
        }
      }
    },
    "/customer-event-history/customer-event-log/{cr-reference-id}/{behavior-qualifier}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve Behaviour Qualifier Reference IDs of the given Behavior Qulifier.",
        "operationId": "RetrieveBehaviorQualifierReferenceIds",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Event Log Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "behavior-qualifier",
            "in": "path",
            "description": "Behavior Qualifier Name. ex- relationship",
            "required": true,
            "type": "string"
          },
          {
            "name": "collection-filter",
            "in": "query",
            "description": "Filter to refine the result set. ex- 'employeeUnitReference == \"EUR736464\"'",
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
                "CRER345",
                "CRER789",
                "CRER456"
              ]
            }
          }
        }
      }
    },
    "/customer-event-history/customer-event-log/{cr-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve a customer event log report",
        "operationId": "retrieveCustomerEventLog",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Event Log Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "Successfully retrieved customer event log report",
            "schema": {
              "type": "object",
              "properties": {
                "customerEventLogReference": {
                  "type": "string",
                  "example": "CELR736464",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerEventLog": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n",
                  "properties": {}
                },
                "customerReference": {
                  "type": "string",
                  "example": "CR764656",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                }
              },
              "example": {
                "customerEventLog": "{}",
                "customerEventLogReference": "CELR736464",
                "customerReference": "CR764656"
              }
            }
          }
        }
      }
    },
    "/customer-event-history/customer-event-log/{cr-reference-id}/relationships/{bq-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve customer event log relationships record",
        "operationId": "retrieveRelationships",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Event Log Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Customer Relationship Event Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "Successfully Retrieved customer event log relationships record",
            "schema": {
              "type": "object",
              "properties": {
                "customerEventLogReference": {
                  "type": "string",
                  "example": "CELR7546464",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerRelationshipEventReference": {
                  "type": "string",
                  "example": "CRER73464565",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerRelationshipEventType": {
                  "type": "string",
                  "example": "advisory",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "employeeUnitReference": {
                  "type": "string",
                  "example": "EUR736465",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerRelationshipEventRecord": {
                  "type": "object",
                  "example": "captured information/details in the log",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
                  "properties": {}
                },
                "customerRelationshipEventAction": {
                  "type": "string",
                  "example": "agreed follow-up activity",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "dateTimeLocation": {
                  "type": "string",
                  "example": "2018-03-28 12:30:00 CST Dallas USA",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
                },
                "customerRelationshipEventResult": {
                  "type": "string",
                  "example": "successful",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                }
              },
              "example": {
                "customerRelationshipEventRecord": "captured information/details in the log",
                "customerRelationshipEventType": "advisory",
                "customerEventLogReference": "CELR7546464",
                "employeeUnitReference": "EUR736465",
                "customerRelationshipEventAction": "agreed follow-up activity",
                "dateTimeLocation": "2018-03-28 12:30:00 CST Dallas USA",
                "customerRelationshipEventReference": "CRER73464565",
                "customerRelationshipEventResult": "successful"
              }
            }
          }
        }
      }
    },
    "/customer-event-history/customer-event-log/{cr-reference-id}/sales/{bq-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve customer event log sales record",
        "operationId": "retrieveSales",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Event Log Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Customer Sales Event Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "Successfully Retrieved customer event log sales record",
            "schema": {
              "type": "object",
              "properties": {
                "customerEventLogReference": {
                  "type": "string",
                  "example": "CELR7634646",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerSalesEventReference": {
                  "type": "string",
                  "example": "CSER7354646",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerSalesEventType": {
                  "type": "string",
                  "example": "solicited",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "employeeUnitReference": {
                  "type": "string",
                  "example": "EUR7236464",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "productServiceType": {
                  "type": "string",
                  "example": "Product Service Type",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "leadOpportunityReference": {
                  "type": "string",
                  "example": "LOR736464",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerSalesEventRecord": {
                  "type": "object",
                  "example": "captured information/details in the log",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
                  "properties": {}
                },
                "commissionAgreementReference": {
                  "type": "string",
                  "example": "CAR736464",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "dateTimeLocation": {
                  "type": "string",
                  "example": "2018-03-28 12:30:00 CST Dallas USA",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
                },
                "customerSalesEventResult": {
                  "type": "string",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                }
              },
              "example": {
                "customerSalesEventRecord": "captured information/details in the log",
                "customerSalesEventType": "solicited",
                "customerEventLogReference": "CELR7634646",
                "employeeUnitReference": "EUR7236464",
                "dateTimeLocation": "2018-03-28 12:30:00 CST Dallas USA",
                "customerSalesEventReference": "CSER7354646",
                "commissionAgreementReference": "CAR736464",
                "leadOpportunityReference": "LOR736464",
                "customerSalesEventResult": "customerSalesEventResult",
                "productServiceType": "Product Service Type"
              }
            }
          }
        }
      }
    },
    "/customer-event-history/customer-event-log/{cr-reference-id}/servicings/{bq-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve customer event log servicing record",
        "operationId": "retrieveServicing",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Event Log Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Customer Servicing Event Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "Successfully Retrieved customer event log servicing record",
            "schema": {
              "type": "object",
              "properties": {
                "customerEventLogReference": {
                  "type": "string",
                  "example": "CELR726464",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerServicingEventReference": {
                  "type": "string",
                  "example": "CSER735454",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerServicingEventType": {
                  "type": "string",
                  "example": "assisted",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerContactDialogueRecordReference": {
                  "type": "string",
                  "example": "CDRR736464",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "accessedProductService": {
                  "type": "string",
                  "example": "referenced products/services",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "channelDeviceType": {
                  "type": "string",
                  "example": "device type",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "contactPurpose": {
                  "type": "string",
                  "example": "purpose for contact",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "contactResult": {
                  "type": "string",
                  "example": "successful",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "employeeUnit Reference": {
                  "type": "string",
                  "example": "EUR63544",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerServicingEventRecord": {
                  "type": "object",
                  "example": "captured information/details in the log",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
                  "properties": {}
                },
                "dateTimeLocation": {
                  "type": "string",
                  "example": "2018-03-28 12:30:00 CST Dallas USA",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
                },
                "customerServicingEventResult": {
                  "type": "string",
                  "example": "successful",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                }
              },
              "example": {
                "channelDeviceType": "device type",
                "accessedProductService": "referenced products/services",
                "customerEventLogReference": "CELR726464",
                "customerServicingEventReference": "CSER735454",
                "dateTimeLocation": "2018-03-28 12:30:00 CST Dallas USA",
                "customerServicingEventResult": "successful",
                "customerContactDialogueRecordReference": "CDRR736464",
                "employeeUnit Reference": "EUR63544",
                "customerServicingEventRecord": "captured information/details in the log",
                "contactResult": "successful",
                "customerServicingEventType": "assisted",
                "contactPurpose": "purpose for contact"
              }
            }
          }
        }
      }
    },
    "/customer-event-history/customer-event-log/{cr-reference-id}/product-services/{bq-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve customer event log product-service record",
        "operationId": "retrieveProductService",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Event Log Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Customer Product Event Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "Successfully Retrieved customer event log product-service record",
            "schema": {
              "type": "object",
              "properties": {
                "customerEventLogReference": {
                  "type": "string",
                  "example": "CELR736464",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerProductEventReference": {
                  "type": "string",
                  "example": "CPER7364646",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "productInstanceReference": {
                  "type": "string",
                  "example": "PIR726454",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "productActionEventType": {
                  "type": "string",
                  "example": "payment initiation",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "productActionEventDescription": {
                  "type": "string",
                  "example": "details of action is available",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "productActionEventResult": {
                  "type": "string",
                  "example": "successful",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "employeeUnitReference": {
                  "type": "string",
                  "example": "EUR7236454",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerProductServiceEventRecord": {
                  "type": "object",
                  "example": "captured information/details in the log",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
                  "properties": {}
                },
                "dateTimeLocation": {
                  "type": "string",
                  "example": "2018-03-28 12:30:00 CST Dallas USA",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
                },
                "customerProductServiceEventResult": {
                  "type": "string",
                  "example": "successful",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                }
              },
              "example": {
                "productActionEventType": "payment initiation",
                "productInstanceReference": "PIR726454",
                "customerProductServiceEventResult": "successful",
                "customerEventLogReference": "CELR736464",
                "employeeUnitReference": "EUR7236454",
                "dateTimeLocation": "2018-03-28 12:30:00 CST Dallas USA",
                "customerProductEventReference": "CPER7364646",
                "productActionEventDescription": "details of action is available",
                "customerProductServiceEventRecord": "captured information/details in the log",
                "productActionEventResult": "successful"
              }
            }
          }
        }
      }
    },
    "/customer-event-history/customer-event-log/{cr-reference-id}/frauds/{bq-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve customer event log fraud event record",
        "operationId": "retrieveFraud",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Event Log Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Customer Fraud Event Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "Successfully Retrieved customer event log fraud event record",
            "schema": {
              "type": "object",
              "properties": {
                "customerEventLogReference": {
                  "type": "string",
                  "example": "CELR735464",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerFraudEventReference": {
                  "type": "string",
                  "example": "CFER7364645",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerFraudCaseEventType": {
                  "type": "string",
                  "example": "stolen card",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerContactDialogueRecordReference": {
                  "type": "string",
                  "example": "CDRR737464",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "accessedProductService": {
                  "type": "string",
                  "example": "referenced products/services if provided",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "employeeUnitReference": {
                  "type": "string",
                  "example": "EUR736464",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "fraudCaseReference": {
                  "type": "string",
                  "example": "FCR736474",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "dateTimeLocation": {
                  "type": "string",
                  "example": "2018-03-28 12:30:00 CST Dallas USA",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
                },
                "customerFraudEventResult": {
                  "type": "string",
                  "example": "successful",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                }
              },
              "example": {
                "customerFraudEventReference": "CFER7364645",
                "accessedProductService": "referenced products/services if provided",
                "customerEventLogReference": "CELR735464",
                "employeeUnitReference": "EUR736464",
                "customerFraudCaseEventType": "stolen card",
                "fraudCaseReference": "FCR736474",
                "dateTimeLocation": "2018-03-28 12:30:00 CST Dallas USA",
                "customerContactDialogueRecordReference": "CDRR737464",
                "customerFraudEventResult": "successful"
              }
            }
          }
        }
      }
    },
    "/customer-event-history/customer-event-log/{cr-reference-id}/lives/{bq-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve customer event log life event record",
        "operationId": "retrieveLife",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Event Log Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Customer Life Event Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "Successfully Retrieved customer event log life event record",
            "schema": {
              "type": "object",
              "properties": {
                "customerEventLogReference": {
                  "type": "string",
                  "example": "CELR736464",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerLifeEventReference": {
                  "type": "string",
                  "example": "CLER646474",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerLifeEventType": {
                  "type": "string",
                  "example": "relocation",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "customerContactReference": {
                  "type": "string",
                  "example": "CCR736464",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "employeeUnitReference": {
                  "type": "string",
                  "example": "EUR736464",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerLifeEventRecord": {
                  "type": "object",
                  "example": "captured information/details in the log",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
                  "properties": {}
                },
                "customerLifeEventVerificationStatus": {
                  "type": "string",
                  "example": true,
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "dateTimeLocation": {
                  "type": "string",
                  "example": "2018-03-28 12:30:00 CST Dallas USA",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
                }
              },
              "example": {
                "customerEventLogReference": "CELR736464",
                "employeeUnitReference": "EUR736464",
                "customerLifeEventRecord": "captured information/details in the log",
                "dateTimeLocation": "2018-03-28 12:30:00 CST Dallas USA",
                "customerContactReference": "CCR736464",
                "customerLifeEventReference": "CLER646474",
                "customerLifeEventVerificationStatus": true,
                "customerLifeEventType": "relocation"
              }
            }
          }
        }
      }
    }
  },
  "definitions": {
    "EventLogBase": {
      "type": "object",
      "properties": {
        "customerEventLog": {
          "type": "object",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n",
          "properties": {}
        },
        "customerReference": {
          "type": "string",
          "example": "CR764656",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        }
      },
      "example": {
        "customerEventLog": "{}",
        "customerReference": "CR764656"
      }
    },
    "EventLogBaseWithID": {
      "type": "object",
      "properties": {
        "customerEventLogReference": {
          "type": "string",
          "example": "CELR736464",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerEventLog": {
          "type": "object",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n",
          "properties": {}
        },
        "customerReference": {
          "type": "string",
          "example": "CR764656",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        }
      },
      "example": {
        "customerEventLog": "{}",
        "customerEventLogReference": "CELR736464",
        "customerReference": "CR764656"
      }
    },
    "RelationshipBase": {
      "type": "object",
      "properties": {
        "customerRelationshipEventType": {
          "type": "string",
          "example": "advisory",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "employeeUnitReference": {
          "type": "string",
          "example": "EUR736465",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerRelationshipEventRecord": {
          "type": "object",
          "example": "captured information/details in the log",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
          "properties": {}
        },
        "customerRelationshipEventAction": {
          "type": "string",
          "example": "agreed follow-up activity",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "dateTimeLocation": {
          "type": "string",
          "example": "2018-03-28 12:30:00 CST Dallas USA",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
        }
      },
      "example": {
        "customerRelationshipEventRecord": "captured information/details in the log",
        "customerRelationshipEventType": "advisory",
        "employeeUnitReference": "EUR736465",
        "customerRelationshipEventAction": "agreed follow-up activity",
        "dateTimeLocation": "2018-03-28 12:30:00 CST Dallas USA"
      }
    },
    "RelationshipBaseWithIdAndStatus": {
      "type": "object",
      "properties": {
        "customerEventLogReference": {
          "type": "string",
          "example": "CELR7546464",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerRelationshipEventReference": {
          "type": "string",
          "example": "CRER73464565",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerRelationshipEventType": {
          "type": "string",
          "example": "advisory",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "employeeUnitReference": {
          "type": "string",
          "example": "EUR736465",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerRelationshipEventRecord": {
          "type": "object",
          "example": "captured information/details in the log",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
          "properties": {}
        },
        "customerRelationshipEventAction": {
          "type": "string",
          "example": "agreed follow-up activity",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "dateTimeLocation": {
          "type": "string",
          "example": "2018-03-28 12:30:00 CST Dallas USA",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
        },
        "customerRelationshipEventResult": {
          "type": "string",
          "example": "successful",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        }
      },
      "example": {
        "customerRelationshipEventRecord": "captured information/details in the log",
        "customerRelationshipEventType": "advisory",
        "customerEventLogReference": "CELR7546464",
        "employeeUnitReference": "EUR736465",
        "customerRelationshipEventAction": "agreed follow-up activity",
        "dateTimeLocation": "2018-03-28 12:30:00 CST Dallas USA",
        "customerRelationshipEventReference": "CRER73464565",
        "customerRelationshipEventResult": "successful"
      }
    },
    "RelationshipRecordResponse": {
      "type": "object",
      "properties": {
        "recordingRecordReference": {
          "type": "string",
          "example": "RRR123",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerRelationshipEventResult": {
          "type": "string",
          "example": "successful",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        }
      },
      "example": {
        "recordingRecordReference": "RRR123",
        "customerRelationshipEventResult": "successful"
      }
    },
    "SalesBase": {
      "type": "object",
      "properties": {
        "customerSalesEventType": {
          "type": "string",
          "example": "solicited",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "employeeUnitReference": {
          "type": "string",
          "example": "EUR7236464",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "productServiceType": {
          "type": "string",
          "example": "Product Service Type",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "leadOpportunityReference": {
          "type": "string",
          "example": "LOR736464",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerSalesEventRecord": {
          "type": "object",
          "example": "captured information/details in the log",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
          "properties": {}
        },
        "commissionAgreementReference": {
          "type": "string",
          "example": "CAR736464",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "dateTimeLocation": {
          "type": "string",
          "example": "2018-03-28 12:30:00 CST Dallas USA",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
        }
      },
      "example": {
        "customerSalesEventRecord": "captured information/details in the log",
        "customerSalesEventType": "solicited",
        "employeeUnitReference": "EUR7236464",
        "dateTimeLocation": "2018-03-28 12:30:00 CST Dallas USA",
        "commissionAgreementReference": "CAR736464",
        "leadOpportunityReference": "LOR736464",
        "productServiceType": "Product Service Type"
      }
    },
    "SalesBaseWithIdAndStatus": {
      "type": "object",
      "properties": {
        "customerEventLogReference": {
          "type": "string",
          "example": "CELR7634646",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerSalesEventReference": {
          "type": "string",
          "example": "CSER7354646",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerSalesEventType": {
          "type": "string",
          "example": "solicited",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "employeeUnitReference": {
          "type": "string",
          "example": "EUR7236464",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "productServiceType": {
          "type": "string",
          "example": "Product Service Type",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "leadOpportunityReference": {
          "type": "string",
          "example": "LOR736464",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerSalesEventRecord": {
          "type": "object",
          "example": "captured information/details in the log",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
          "properties": {}
        },
        "commissionAgreementReference": {
          "type": "string",
          "example": "CAR736464",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "dateTimeLocation": {
          "type": "string",
          "example": "2018-03-28 12:30:00 CST Dallas USA",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
        },
        "customerSalesEventResult": {
          "type": "string",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        }
      },
      "example": {
        "customerSalesEventRecord": "captured information/details in the log",
        "customerSalesEventType": "solicited",
        "customerEventLogReference": "CELR7634646",
        "employeeUnitReference": "EUR7236464",
        "dateTimeLocation": "2018-03-28 12:30:00 CST Dallas USA",
        "customerSalesEventReference": "CSER7354646",
        "commissionAgreementReference": "CAR736464",
        "leadOpportunityReference": "LOR736464",
        "customerSalesEventResult": "customerSalesEventResult",
        "productServiceType": "Product Service Type"
      }
    },
    "SalesRecordResponse": {
      "type": "object",
      "properties": {
        "recordingRecordReference": {
          "type": "string",
          "example": "RRR123",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerSalesEventResult": {
          "type": "string",
          "example": "successful",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        }
      },
      "example": {
        "recordingRecordReference": "RRR123",
        "customerSalesEventResult": "successful"
      }
    },
    "ServicingBase": {
      "type": "object",
      "properties": {
        "customerServicingEventType": {
          "type": "string",
          "example": "assisted",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "customerContactDialogueRecordReference": {
          "type": "string",
          "example": "CDRR736464",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "accessedProductService": {
          "type": "string",
          "example": "referenced products/services",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "channelDeviceType": {
          "type": "string",
          "example": "device type",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "contactPurpose": {
          "type": "string",
          "example": "purpose for contact",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "contactResult": {
          "type": "string",
          "example": "successful",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "employeeUnit Reference": {
          "type": "string",
          "example": "EUR63544",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerServicingEventRecord": {
          "type": "object",
          "example": "captured information/details in the log",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
          "properties": {}
        },
        "dateTimeLocation": {
          "type": "string",
          "example": "2018-03-28 12:30:00 CST Dallas USA",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
        }
      },
      "example": {
        "channelDeviceType": "device type",
        "accessedProductService": "referenced products/services",
        "dateTimeLocation": "2018-03-28 12:30:00 CST Dallas USA",
        "customerContactDialogueRecordReference": "CDRR736464",
        "employeeUnit Reference": "EUR63544",
        "customerServicingEventRecord": "captured information/details in the log",
        "contactResult": "successful",
        "customerServicingEventType": "assisted",
        "contactPurpose": "purpose for contact"
      }
    },
    "ServicingBaseWithIdAndStatus": {
      "type": "object",
      "properties": {
        "customerEventLogReference": {
          "type": "string",
          "example": "CELR726464",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerServicingEventReference": {
          "type": "string",
          "example": "CSER735454",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerServicingEventType": {
          "type": "string",
          "example": "assisted",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "customerContactDialogueRecordReference": {
          "type": "string",
          "example": "CDRR736464",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "accessedProductService": {
          "type": "string",
          "example": "referenced products/services",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "channelDeviceType": {
          "type": "string",
          "example": "device type",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "contactPurpose": {
          "type": "string",
          "example": "purpose for contact",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "contactResult": {
          "type": "string",
          "example": "successful",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "employeeUnit Reference": {
          "type": "string",
          "example": "EUR63544",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerServicingEventRecord": {
          "type": "object",
          "example": "captured information/details in the log",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
          "properties": {}
        },
        "dateTimeLocation": {
          "type": "string",
          "example": "2018-03-28 12:30:00 CST Dallas USA",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
        },
        "customerServicingEventResult": {
          "type": "string",
          "example": "successful",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        }
      },
      "example": {
        "channelDeviceType": "device type",
        "accessedProductService": "referenced products/services",
        "customerEventLogReference": "CELR726464",
        "customerServicingEventReference": "CSER735454",
        "dateTimeLocation": "2018-03-28 12:30:00 CST Dallas USA",
        "customerServicingEventResult": "successful",
        "customerContactDialogueRecordReference": "CDRR736464",
        "employeeUnit Reference": "EUR63544",
        "customerServicingEventRecord": "captured information/details in the log",
        "contactResult": "successful",
        "customerServicingEventType": "assisted",
        "contactPurpose": "purpose for contact"
      }
    },
    "ServicingRecordResponse": {
      "type": "object",
      "properties": {
        "recordingRecordReference": {
          "type": "string",
          "example": "RRR123",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerServicingEventResult": {
          "type": "string",
          "example": "successful",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        }
      },
      "example": {
        "customerServicingEventResult": "successful",
        "recordingRecordReference": "RRR123"
      }
    },
    "ProductServiceBase": {
      "type": "object",
      "properties": {
        "productInstanceReference": {
          "type": "string",
          "example": "PIR726454",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "productActionEventType": {
          "type": "string",
          "example": "payment initiation",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "productActionEventDescription": {
          "type": "string",
          "example": "details of action is available",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "productActionEventResult": {
          "type": "string",
          "example": "successful",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "employeeUnitReference": {
          "type": "string",
          "example": "EUR7236454",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerProductServiceEventRecord": {
          "type": "object",
          "example": "captured information/details in the log",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
          "properties": {}
        },
        "dateTimeLocation": {
          "type": "string",
          "example": "2018-03-28 12:30:00 CST Dallas USA",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
        }
      },
      "example": {
        "productActionEventType": "payment initiation",
        "productInstanceReference": "PIR726454",
        "employeeUnitReference": "EUR7236454",
        "dateTimeLocation": "2018-03-28 12:30:00 CST Dallas USA",
        "productActionEventDescription": "details of action is available",
        "customerProductServiceEventRecord": "captured information/details in the log",
        "productActionEventResult": "successful"
      }
    },
    "ProductServiceBaseWithIdAndStatus": {
      "type": "object",
      "properties": {
        "customerEventLogReference": {
          "type": "string",
          "example": "CELR736464",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerProductEventReference": {
          "type": "string",
          "example": "CPER7364646",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "productInstanceReference": {
          "type": "string",
          "example": "PIR726454",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "productActionEventType": {
          "type": "string",
          "example": "payment initiation",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "productActionEventDescription": {
          "type": "string",
          "example": "details of action is available",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "productActionEventResult": {
          "type": "string",
          "example": "successful",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "employeeUnitReference": {
          "type": "string",
          "example": "EUR7236454",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerProductServiceEventRecord": {
          "type": "object",
          "example": "captured information/details in the log",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
          "properties": {}
        },
        "dateTimeLocation": {
          "type": "string",
          "example": "2018-03-28 12:30:00 CST Dallas USA",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
        },
        "customerProductServiceEventResult": {
          "type": "string",
          "example": "successful",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        }
      },
      "example": {
        "productActionEventType": "payment initiation",
        "productInstanceReference": "PIR726454",
        "customerProductServiceEventResult": "successful",
        "customerEventLogReference": "CELR736464",
        "employeeUnitReference": "EUR7236454",
        "dateTimeLocation": "2018-03-28 12:30:00 CST Dallas USA",
        "customerProductEventReference": "CPER7364646",
        "productActionEventDescription": "details of action is available",
        "customerProductServiceEventRecord": "captured information/details in the log",
        "productActionEventResult": "successful"
      }
    },
    "ProductServiceRecordResponse": {
      "type": "object",
      "properties": {
        "recordingRecordReference": {
          "type": "string",
          "example": "RRR123",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerProductServiceEventResult": {
          "type": "string",
          "example": "successful",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        }
      },
      "example": {
        "customerProductServiceEventResult": "successful",
        "recordingRecordReference": "RRR123"
      }
    },
    "FraudBase": {
      "type": "object",
      "properties": {
        "customerFraudCaseEventType": {
          "type": "string",
          "example": "stolen card",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "customerContactDialogueRecordReference": {
          "type": "string",
          "example": "CDRR737464",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "accessedProductService": {
          "type": "string",
          "example": "referenced products/services if provided",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "employeeUnitReference": {
          "type": "string",
          "example": "EUR736464",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "fraudCaseReference": {
          "type": "string",
          "example": "FCR736474",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "dateTimeLocation": {
          "type": "string",
          "example": "2018-03-28 12:30:00 CST Dallas USA",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
        }
      },
      "example": {
        "accessedProductService": "referenced products/services if provided",
        "employeeUnitReference": "EUR736464",
        "customerFraudCaseEventType": "stolen card",
        "fraudCaseReference": "FCR736474",
        "dateTimeLocation": "2018-03-28 12:30:00 CST Dallas USA",
        "customerContactDialogueRecordReference": "CDRR737464"
      }
    },
    "FraudBaseWithIdAndStatus": {
      "type": "object",
      "properties": {
        "customerEventLogReference": {
          "type": "string",
          "example": "CELR735464",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerFraudEventReference": {
          "type": "string",
          "example": "CFER7364645",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerFraudCaseEventType": {
          "type": "string",
          "example": "stolen card",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "customerContactDialogueRecordReference": {
          "type": "string",
          "example": "CDRR737464",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "accessedProductService": {
          "type": "string",
          "example": "referenced products/services if provided",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "employeeUnitReference": {
          "type": "string",
          "example": "EUR736464",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "fraudCaseReference": {
          "type": "string",
          "example": "FCR736474",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "dateTimeLocation": {
          "type": "string",
          "example": "2018-03-28 12:30:00 CST Dallas USA",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
        },
        "customerFraudEventResult": {
          "type": "string",
          "example": "successful",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        }
      },
      "example": {
        "customerFraudEventReference": "CFER7364645",
        "accessedProductService": "referenced products/services if provided",
        "customerEventLogReference": "CELR735464",
        "employeeUnitReference": "EUR736464",
        "customerFraudCaseEventType": "stolen card",
        "fraudCaseReference": "FCR736474",
        "dateTimeLocation": "2018-03-28 12:30:00 CST Dallas USA",
        "customerContactDialogueRecordReference": "CDRR737464",
        "customerFraudEventResult": "successful"
      }
    },
    "FraudRecordResponse": {
      "type": "object",
      "properties": {
        "recordingRecordReference": {
          "type": "string",
          "example": "RRR123",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerFraudEventResult": {
          "type": "string",
          "example": "successful",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        }
      },
      "example": {
        "recordingRecordReference": "RRR123",
        "customerFraudEventResult": "successful"
      }
    },
    "LifeBase": {
      "type": "object",
      "properties": {
        "customerLifeEventType": {
          "type": "string",
          "example": "relocation",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "customerContactReference": {
          "type": "string",
          "example": "CCR736464",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "employeeUnitReference": {
          "type": "string",
          "example": "EUR736464",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerLifeEventRecord": {
          "type": "object",
          "example": "captured information/details in the log",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
          "properties": {}
        },
        "customerLifeEventVerificationStatus": {
          "type": "string",
          "example": true,
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "dateTimeLocation": {
          "type": "string",
          "example": "2018-03-28 12:30:00 CST Dallas USA",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
        }
      },
      "example": {
        "employeeUnitReference": "EUR736464",
        "customerLifeEventRecord": "captured information/details in the log",
        "dateTimeLocation": "2018-03-28 12:30:00 CST Dallas USA",
        "customerContactReference": "CCR736464",
        "customerLifeEventVerificationStatus": true,
        "customerLifeEventType": "relocation"
      }
    },
    "LifeBaseWithIdAndStatus": {
      "type": "object",
      "properties": {
        "customerEventLogReference": {
          "type": "string",
          "example": "CELR736464",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerLifeEventReference": {
          "type": "string",
          "example": "CLER646474",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerLifeEventType": {
          "type": "string",
          "example": "relocation",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "customerContactReference": {
          "type": "string",
          "example": "CCR736464",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "employeeUnitReference": {
          "type": "string",
          "example": "EUR736464",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerLifeEventRecord": {
          "type": "object",
          "example": "captured information/details in the log",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
          "properties": {}
        },
        "customerLifeEventVerificationStatus": {
          "type": "string",
          "example": true,
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "dateTimeLocation": {
          "type": "string",
          "example": "2018-03-28 12:30:00 CST Dallas USA",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
        }
      },
      "example": {
        "customerEventLogReference": "CELR736464",
        "employeeUnitReference": "EUR736464",
        "customerLifeEventRecord": "captured information/details in the log",
        "dateTimeLocation": "2018-03-28 12:30:00 CST Dallas USA",
        "customerContactReference": "CCR736464",
        "customerLifeEventReference": "CLER646474",
        "customerLifeEventVerificationStatus": true,
        "customerLifeEventType": "relocation"
      }
    },
    "LifeRecordResponse": {
      "type": "object",
      "properties": {
        "recordingRecordReference": {
          "type": "string",
          "example": "RRR123",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerLifeEventResult": {
          "type": "string",
          "example": "successful",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        }
      },
      "example": {
        "recordingRecordReference": "RRR123",
        "customerLifeEventResult": "successful"
      }
    }
  },
  "parameters": {
    "controlRecordReference": {
      "name": "cr-reference-id",
      "in": "path",
      "description": "Customer Event Log Reference",
      "required": true,
      "type": "string"
    }
  }
}
</script>