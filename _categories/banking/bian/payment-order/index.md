---
layout: api-single
title: Payment Order
parent-title: BIAN APIs
description: Banking API Standards - APIs - Payment Order
keywords: 
duration: 
type: api
standard: bian
order: 1
parent: /categories/banking/bian
api-logo: /dist/images/logos/bian_logo.svg
api-summary: This service domain handles the bank-side processing of funds transfers, making the necessary bank and regulatory checks on the involved parties and applying their payment preferences where appropriate
api-example-use: A customer transaction results in the generation of a payment order to transfer funds to an account in another bank
api-published-by: Bianuser05 Team
---
<script id="api-spec" type="application/json">
{
  "swagger": "2.0",
  "info": {
    "version": "1.0.0",
    "title": "Payment Order",
    "description": "Handles the bank-side processing of funds transfers"
  },
  "host": "bianorg.azure-api.net",
  "basePath": "/sd-payment-order/v1",
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
  "paths": {
    "/payment-order/payment-order-procedure/{cr-reference-id}/updation": {
      "put": {
        "tags": [
          "update"
        ],
        "summary": "Update Payment order",
        "description": "Update/amend details of an active payment order transaction",
        "operationId": "updatePaymentOrderProcedure",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Payment Order Request Reference",
            "required": true,
            "type": "string"
          },
          {
            "in": "body",
            "name": "body",
            "description": "Update Control record payload",
            "required": true,
            "schema": {
              "type": "object",
              "properties": {
                "paymentOrderUpdateDescription": {
                  "type": "string",
                  "example": "ChangePaymentOrder",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                },
                "paymentOrderInitiatorReference": {
                  "type": "string",
                  "example": "POIR1234",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payerReference": {
                  "type": "string",
                  "example": "PYRE5345",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payerBankReference": {
                  "type": "string",
                  "example": "PYBR1093",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payerProductInstanceReference": {
                  "type": "string",
                  "example": "payer account number",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payeeReference": {
                  "type": "string",
                  "example": "PAEE5007",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payeeProductInstanceReference": {
                  "type": "string",
                  "example": "PPIR3456",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payeeBankReference": {
                  "type": "string",
                  "example": "PEBR2783",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "amount": {
                  "type": "string",
                  "example": "$5000",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount    \n"
                },
                "currency": {
                  "type": "string",
                  "example": "USD",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                },
                "dateType": {
                  "type": "string",
                  "example": "Order",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                },
                "date": {
                  "type": "string",
                  "example": "2018-08-28T00:00:00Z",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Date      \n"
                },
                "paymentMechanism": {
                  "type": "string",
                  "example": "ACH",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Name    \n"
                }
              },
              "example": {
                "date": "2018-08-28T00:00:00Z",
                "payerProductInstanceReference": "payer account number",
                "amount": "$5000",
                "paymentOrderUpdateDescription": "ChangePaymentOrder",
                "paymentOrderInitiatorReference": "POIR1234",
                "payeeReference": "PAEE5007",
                "payeeProductInstanceReference": "PPIR3456",
                "payerBankReference": "PYBR1093",
                "payeeBankReference": "PEBR2783",
                "dateType": "Order",
                "payerReference": "PYRE5345",
                "currency": "USD",
                "paymentMechanism": "ACH"
              }
            }
          }
        ],
        "responses": {
          "200": {
            "description": "Successfully updated payment order transaction.",
            "schema": {
              "type": "object",
              "properties": {
                "paymentOrderRequestReference": {
                  "type": "string",
                  "example": "PDRE9408",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "paymentOrderUpdateReference": {
                  "type": "string",
                  "example": "POUR7676",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "paymentOrderUpdateDescription": {
                  "type": "string",
                  "example": "ChangePaymentOrder",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                },
                "paymentOrderInitiatorReference": {
                  "type": "string",
                  "example": "POIR1234",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payerReference": {
                  "type": "string",
                  "example": "PYRE5345",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payerBankReference": {
                  "type": "string",
                  "example": "PYBR1093",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier    \n"
                },
                "payerProductInstanceReference": {
                  "type": "string",
                  "example": "payer account number",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payeeReference": {
                  "type": "string",
                  "example": "PAEE5007",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payeeProductInstanceReference": {
                  "type": "string",
                  "example": "PPIR3456",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payeeBankReference": {
                  "type": "string",
                  "example": "PEBR2783",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "amount": {
                  "type": "string",
                  "example": "$5000",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount    \n"
                },
                "currency": {
                  "type": "string",
                  "example": "USD",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                },
                "dateType": {
                  "type": "string",
                  "example": "Order",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                },
                "date": {
                  "type": "string",
                  "example": "2018-08-28",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Date    \n"
                },
                "paymentMechanism": {
                  "type": "string",
                  "example": "ACH",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Name    \n"
                },
                "paymentOrderUpdateResult": {
                  "type": "string",
                  "example": "Success",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                }
              },
              "example": {
                "date": "2018-08-28",
                "payerProductInstanceReference": "payer account number",
                "amount": "$5000",
                "paymentOrderUpdateDescription": "ChangePaymentOrder",
                "paymentOrderInitiatorReference": "POIR1234",
                "payeeReference": "PAEE5007",
                "payeeProductInstanceReference": "PPIR3456",
                "payerBankReference": "PYBR1093",
                "payeeBankReference": "PEBR2783",
                "paymentOrderUpdateReference": "POUR7676",
                "paymentOrderUpdateResult": "Success",
                "dateType": "Order",
                "payerReference": "PYRE5345",
                "currency": "USD",
                "paymentOrderRequestReference": "PDRE9408",
                "paymentMechanism": "ACH"
              }
            }
          }
        }
      }
    },
    "/payment-order/payment-order-procedure/{cr-reference-id}/recording": {
      "post": {
        "tags": [
          "record"
        ],
        "summary": "Record feedback",
        "description": "Record feedback/activity against payment order activity/processing",
        "operationId": "recordPaymentOrderProcedure",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Payment Order Request Reference",
            "required": true,
            "type": "integer"
          },
          {
            "in": "body",
            "name": "body",
            "description": "Record Control record payload",
            "required": true,
            "schema": {
              "type": "object",
              "properties": {
                "recordingRecordType": {
                  "type": "string",
                  "example": "BehaviorModelPerformanceFeedback",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                },
                "recordingRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary    \n",
                  "properties": {}
                },
                "recordingRecordDateTime": {
                  "type": "string",
                  "example": "2018-08-28T09:00:00Z",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime    \n"
                },
                "empolyeeBusinessUnitReference": {
                  "type": "string",
                  "example": "EBUR6798",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                }
              },
              "example": {
                "recordingRecordType": "BehaviorModelPerformanceFeedback",
                "empolyeeBusinessUnitReference": "EBUR6798",
                "recordingRecordDateTime": "2018-08-28T09:00:00Z",
                "recordingRecord": "{}"
              }
            }
          }
        ],
        "responses": {
          "201": {
            "description": "Successfully created new Record.",
            "schema": {
              "type": "object",
              "properties": {
                "recordingRecordReference": {
                  "type": "string",
                  "example": "CRRR3456",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "recordingRecordStatus": {
                  "type": "string",
                  "example": "Applied",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                }
              },
              "example": {
                "recordingRecordReference": "CRRR3456",
                "recordingRecordStatus": "Applied"
              }
            }
          }
        }
      }
    },
    "/payment-order/payment-order-procedure/{cr-reference-id}/execution": {
      "put": {
        "tags": [
          "execute"
        ],
        "summary": "Update payment order",
        "description": "Update a payment order execution record",
        "operationId": "executePaymentOrderProcedureUpdate",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Payment Order Request Reference",
            "required": true,
            "type": "string"
          },
          {
            "in": "body",
            "name": "body",
            "description": "Execute Control record payload",
            "required": true,
            "schema": {
              "type": "object",
              "properties": {
                "paymentOrderInitiatorReference": {
                  "type": "string",
                  "example": "source",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payerReference": {
                  "type": "string",
                  "example": "PA7753535",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier    \n"
                },
                "payerBankReference": {
                  "type": "string",
                  "example": "PRIR5859",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier    \n"
                },
                "payerProductInstanceReference": {
                  "type": "string",
                  "example": "PERR3438",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier    \n"
                },
                "payeeReference": {
                  "type": "string",
                  "example": "POPR72354",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier    \n"
                },
                "payeeProductInstanceReference": {
                  "type": "string",
                  "example": "PI73453145",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier    \n"
                },
                "payeeBankReference": {
                  "type": "string",
                  "example": "PEIR5859",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier    \n"
                },
                "amount": {
                  "type": "string",
                  "example": "$2000",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount    \n"
                },
                "currency": {
                  "type": "string",
                  "example": "USD",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                },
                "dateType": {
                  "type": "string",
                  "example": "interest bearing",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                },
                "date": {
                  "type": "string",
                  "example": "09-07-2018",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Date    \n"
                },
                "paymentMechanismReference": {
                  "type": "string",
                  "example": "SWIFT",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier    \n"
                },
                "paymentMechanismType": {
                  "type": "string",
                  "example": "Mechanism Type",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                },
                "paymentMechanismProperties": {
                  "type": "string",
                  "example": "specific payment instructions",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                }
              },
              "example": {
                "date": "09-07-2018",
                "payerProductInstanceReference": "PERR3438",
                "amount": "$2000",
                "paymentOrderInitiatorReference": "source",
                "payeeReference": "POPR72354",
                "payeeProductInstanceReference": "PI73453145",
                "payerBankReference": "PRIR5859",
                "payeeBankReference": "PEIR5859",
                "paymentMechanismType": "Mechanism Type",
                "paymentMechanismProperties": "specific payment instructions",
                "dateType": "interest bearing",
                "payerReference": "PA7753535",
                "currency": "USD",
                "paymentMechanismReference": "SWIFT"
              }
            }
          }
        ],
        "responses": {
          "200": {
            "description": "Successfully updated payment order execution record.",
            "schema": {
              "type": "object",
              "properties": {
                "paymentOrderRequestReference": {
                  "type": "string",
                  "example": "CR7735345",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "paymentOrderInitiatorReference": {
                  "type": "string",
                  "example": "source",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payerReference": {
                  "type": "string",
                  "example": "PA7753535",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payerBankReference": {
                  "type": "string",
                  "example": "PRIR5859",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payerProductInstanceReference": {
                  "type": "string",
                  "example": "PERR3438",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payeeReference": {
                  "type": "string",
                  "example": "POPR72354",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payeeProductInstanceReference": {
                  "type": "string",
                  "example": "PI73453145",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payeeBankReference": {
                  "type": "string",
                  "example": "PEIR5859",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "amount": {
                  "type": "string",
                  "example": "$2000",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount    \n"
                },
                "currency": {
                  "type": "string",
                  "example": "USD",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text      \n"
                },
                "dateType": {
                  "type": "string",
                  "example": "interest bearing",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text      \n"
                },
                "date": {
                  "type": "string",
                  "example": "09-07-2018",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Date      \n"
                },
                "paymentMechanismReference": {
                  "type": "string",
                  "example": "SWIFT",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier    \n"
                },
                "paymentMechanismType": {
                  "type": "string",
                  "example": "Mechanism Type",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                },
                "paymentMechanismProperties": {
                  "type": "string",
                  "example": "specific payment instructions",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                }
              },
              "example": {
                "date": "09-07-2018",
                "payerProductInstanceReference": "PERR3438",
                "amount": "$2000",
                "paymentOrderInitiatorReference": "source",
                "payeeReference": "POPR72354",
                "payeeProductInstanceReference": "PI73453145",
                "payerBankReference": "PRIR5859",
                "payeeBankReference": "PEIR5859",
                "paymentMechanismType": "Mechanism Type",
                "paymentMechanismProperties": "specific payment instructions",
                "dateType": "interest bearing",
                "payerReference": "PA7753535",
                "currency": "USD",
                "paymentOrderRequestReference": "CR7735345",
                "paymentMechanismReference": "SWIFT"
              }
            }
          }
        }
      }
    },
    "/payment-order/payment-order-procedure/execution": {
      "post": {
        "tags": [
          "execute"
        ],
        "summary": "Create payment order",
        "description": "Create a new payment order execution record",
        "operationId": "executePaymentOrderProcedureCreate",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "in": "body",
            "name": "body",
            "description": "Execute Control record payload",
            "required": true,
            "schema": {
              "type": "object",
              "properties": {
                "paymentOrderInitiatorReference": {
                  "type": "string",
                  "example": "source",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payerReference": {
                  "type": "string",
                  "example": "PA7753535",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier    \n"
                },
                "payerBankReference": {
                  "type": "string",
                  "example": "PRIR5859",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier    \n"
                },
                "payerProductInstanceReference": {
                  "type": "string",
                  "example": "PERR3438",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier    \n"
                },
                "payeeReference": {
                  "type": "string",
                  "example": "POPR72354",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier    \n"
                },
                "payeeProductInstanceReference": {
                  "type": "string",
                  "example": "PI73453145",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier    \n"
                },
                "payeeBankReference": {
                  "type": "string",
                  "example": "PEIR5859",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier    \n"
                },
                "amount": {
                  "type": "string",
                  "example": "$2000",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount    \n"
                },
                "currency": {
                  "type": "string",
                  "example": "USD",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                },
                "dateType": {
                  "type": "string",
                  "example": "interest bearing",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                },
                "date": {
                  "type": "string",
                  "example": "09-07-2018",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Date    \n"
                },
                "paymentMechanismReference": {
                  "type": "string",
                  "example": "SWIFT",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier    \n"
                },
                "paymentMechanismType": {
                  "type": "string",
                  "example": "Mechanism Type",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                },
                "paymentMechanismProperties": {
                  "type": "string",
                  "example": "specific payment instructions",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                }
              },
              "example": {
                "date": "09-07-2018",
                "payerProductInstanceReference": "PERR3438",
                "amount": "$2000",
                "paymentOrderInitiatorReference": "source",
                "payeeReference": "POPR72354",
                "payeeProductInstanceReference": "PI73453145",
                "payerBankReference": "PRIR5859",
                "payeeBankReference": "PEIR5859",
                "paymentMechanismType": "Mechanism Type",
                "paymentMechanismProperties": "specific payment instructions",
                "dateType": "interest bearing",
                "payerReference": "PA7753535",
                "currency": "USD",
                "paymentMechanismReference": "SWIFT"
              }
            }
          }
        ],
        "responses": {
          "201": {
            "description": "Successfully created payment order execution record",
            "schema": {
              "type": "object",
              "properties": {
                "paymentOrderRequestReference": {
                  "type": "string",
                  "example": "CR7735345",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "paymentOrderInitiatorReference": {
                  "type": "string",
                  "example": "source",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payerReference": {
                  "type": "string",
                  "example": "PA7753535",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payerBankReference": {
                  "type": "string",
                  "example": "PRIR5859",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payerProductInstanceReference": {
                  "type": "string",
                  "example": "PERR3438",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payeeReference": {
                  "type": "string",
                  "example": "POPR72354",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payeeProductInstanceReference": {
                  "type": "string",
                  "example": "PI73453145",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payeeBankReference": {
                  "type": "string",
                  "example": "PEIR5859",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "amount": {
                  "type": "string",
                  "example": "$2000",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount    \n"
                },
                "currency": {
                  "type": "string",
                  "example": "USD",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text      \n"
                },
                "dateType": {
                  "type": "string",
                  "example": "interest bearing",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text      \n"
                },
                "date": {
                  "type": "string",
                  "example": "09-07-2018",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Date      \n"
                },
                "paymentMechanismReference": {
                  "type": "string",
                  "example": "SWIFT",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier    \n"
                },
                "paymentMechanismType": {
                  "type": "string",
                  "example": "Mechanism Type",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                },
                "paymentMechanismProperties": {
                  "type": "string",
                  "example": "specific payment instructions",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                }
              },
              "example": {
                "date": "09-07-2018",
                "payerProductInstanceReference": "PERR3438",
                "amount": "$2000",
                "paymentOrderInitiatorReference": "source",
                "payeeReference": "POPR72354",
                "payeeProductInstanceReference": "PI73453145",
                "payerBankReference": "PRIR5859",
                "payeeBankReference": "PEIR5859",
                "paymentMechanismType": "Mechanism Type",
                "paymentMechanismProperties": "specific payment instructions",
                "dateType": "interest bearing",
                "payerReference": "PA7753535",
                "currency": "USD",
                "paymentOrderRequestReference": "CR7735345",
                "paymentMechanismReference": "SWIFT"
              }
            }
          }
        }
      }
    },
    "/payment-order/payment-order-procedure/": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve CR Ids",
        "operationId": "RetrievePaymentOrderReferenceIds",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "collection-filter",
            "in": "query",
            "description": "Filter to refine the result set. ex- 'amount > 200000'",
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
                "PORR123",
                "PORR345"
              ]
            }
          }
        }
      }
    },
    "/payment-order/payment-order-procedure/behavior-qualifiers/": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve BQ names",
        "operationId": "RetrievePaymentOrderBehaviorQualifiers",
        "produces": [
          "application/json"
        ],
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
                "order",
                "compliance",
                "update",
                "execution",
                "reporting"
              ]
            }
          }
        }
      }
    },
    "/payment-order/payment-order-procedure/{cr-reference-id}/{behavior-qualifier}/": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve BQ Ids",
        "operationId": "RetrieveBehaviorQualifierReferenceIds",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Payment Order Request Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "behavior-qualifier",
            "in": "path",
            "description": "Behavior Qualifier Name. ex- order",
            "required": true,
            "type": "string"
          },
          {
            "name": "collection-filter",
            "in": "query",
            "description": "Filter to refine the result set. ex- 'amount > $5000'",
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
                "POR123",
                "POR345"
              ]
            }
          }
        }
      }
    },
    "/payment-order/payment-order-procedure/{cr-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve Payment order details",
        "description": "Retrieve a payment order transaction report",
        "operationId": "retrievePaymentOrderProcedure",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Payment Order Request Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "Successfully retrieved payment order transaction record report.",
            "schema": {
              "type": "object",
              "properties": {
                "paymentOrderRequestReference": {
                  "type": "string",
                  "example": "PORR4545",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "paymentOrderInitiatorReference": {
                  "type": "string",
                  "example": "POIR4545",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payerReference": {
                  "type": "string",
                  "example": "PYRE4545",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payerBankReference": {
                  "type": "string",
                  "example": "PBRE4545",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payerProductInstanceReference": {
                  "type": "string",
                  "example": "PPRE4545",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payeeReference": {
                  "type": "string",
                  "example": "PTRE4545",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payeeProductInstanceReference": {
                  "type": "string",
                  "example": "PTRE4545",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payeeBankReference": {
                  "type": "string",
                  "example": "PTRE4545",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "amount": {
                  "type": "string",
                  "example": "$5000",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount    \n"
                },
                "currency": {
                  "type": "string",
                  "example": "USD",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                },
                "dateType": {
                  "type": "string",
                  "example": "order",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                },
                "date": {
                  "type": "string",
                  "example": "2018-09-07",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Date    \n"
                },
                "paymentMechanismReference": {
                  "type": "string",
                  "example": "ACH",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier    \n"
                },
                "paymentMechanismType": {
                  "type": "string",
                  "example": "Type",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text      \n"
                },
                "paymentMechanismProperties": {
                  "type": "string",
                  "example": "specific payment instructions",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                }
              },
              "example": {
                "date": "2018-09-07",
                "payerProductInstanceReference": "PPRE4545",
                "amount": "$5000",
                "paymentOrderInitiatorReference": "POIR4545",
                "payeeReference": "PTRE4545",
                "payeeProductInstanceReference": "PTRE4545",
                "payerBankReference": "PBRE4545",
                "payeeBankReference": "PTRE4545",
                "paymentMechanismType": "Type",
                "paymentMechanismProperties": "specific payment instructions",
                "dateType": "order",
                "payerReference": "PYRE4545",
                "currency": "USD",
                "paymentOrderRequestReference": "PORR4545",
                "paymentMechanismReference": "ACH"
              }
            }
          }
        }
      }
    },
    "/payment-order/payment-order-procedure/{cr-reference-id}/compliances/{bq-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve compliance reporting",
        "description": "Retrieve a payment order compliance report",
        "operationId": "retrievePaymentOrderComplianceProcedure",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Payment Order Request Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Payment Oder Compliance Check Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "Successfully retrieved payment order compliance report.",
            "schema": {
              "type": "object",
              "properties": {
                "paymentOrderRequestReference": {
                  "type": "string",
                  "example": "PDRE9408",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "paymentOderComplianceCheckReference": {
                  "type": "string",
                  "example": "POCC7262342",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payerReference": {
                  "type": "string",
                  "example": "PYRE5345",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payeeReference": {
                  "type": "string",
                  "example": "PAEE5007",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "amount": {
                  "type": "string",
                  "example": "$5000",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount    \n"
                },
                "currency": {
                  "type": "string",
                  "example": "USD",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                },
                "paymentOrderComplianceCheckType": {
                  "type": "string",
                  "example": "Check Type",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                },
                "paymentOrderComplianceCheckResult": {
                  "type": "string",
                  "example": "Success",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                }
              },
              "example": {
                "paymentOrderComplianceCheckType": "Check Type",
                "amount": "$5000",
                "payeeReference": "PAEE5007",
                "paymentOderComplianceCheckReference": "POCC7262342",
                "payerReference": "PYRE5345",
                "currency": "USD",
                "paymentOrderComplianceCheckResult": "Success",
                "paymentOrderRequestReference": "PDRE9408"
              }
            }
          }
        }
      }
    },
    "/payment-order/payment-order-procedure/{cr-reference-id}/orders/{bq-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve processing report",
        "description": "Retrieve a payment order processing report",
        "operationId": "retrievePaymentOrderOrderProcedure",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Payment Order Request Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Payment Order Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "Successfully retrieved payment order processing report.",
            "schema": {
              "type": "object",
              "properties": {
                "paymentOrderRequestReference": {
                  "type": "string",
                  "example": "PDRE9408",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "paymentOrderReference": {
                  "type": "string",
                  "example": "PDRE9408",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "paymentOrderStatus": {
                  "type": "string",
                  "example": "authorization",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                },
                "interestedParties": {
                  "type": "string",
                  "example": "authorizing",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                },
                "productInstanceReference": {
                  "type": "string",
                  "example": "for default settlement instructions",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "paymentExecutionReference": {
                  "type": "string",
                  "example": "PER723475324",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "settlementInstructions": {
                  "type": "string",
                  "example": "can be defined as part of the payment or determined at execution",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                }
              },
              "example": {
                "paymentExecutionReference": "PER723475324",
                "productInstanceReference": "for default settlement instructions",
                "settlementInstructions": "can be defined as part of the payment or determined at execution",
                "paymentOrderStatus": "authorization",
                "interestedParties": "authorizing",
                "paymentOrderRequestReference": "PDRE9408",
                "paymentOrderReference": "PDRE9408"
              }
            }
          }
        }
      }
    },
    "/payment-order/payment-order-procedure/{cr-reference-id}/updates/{bq-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve update reporting",
        "description": "Retrieve a payment order processing update report",
        "operationId": "retrievePaymentOrderUpdateProcedure",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Payment Order Request Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Payment Order Update Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "Successfully retrieved payment order processing update report.",
            "schema": {
              "type": "object",
              "properties": {
                "paymentOrderRequestReference": {
                  "type": "string",
                  "example": "PDRE9408",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "paymentOrderUpdateReference": {
                  "type": "string",
                  "example": "POUR7676",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "paymentOrderUpdateDescription": {
                  "type": "string",
                  "example": "ChangePaymentOrder",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                },
                "paymentOrderInitiatorReference": {
                  "type": "string",
                  "example": "POIR1234",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payerReference": {
                  "type": "string",
                  "example": "PYRE5345",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payerBankReference": {
                  "type": "string",
                  "example": "PYBR1093",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier    \n"
                },
                "payerProductInstanceReference": {
                  "type": "string",
                  "example": "payer account number",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payeeReference": {
                  "type": "string",
                  "example": "PAEE5007",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payeeProductInstanceReference": {
                  "type": "string",
                  "example": "PPIR3456",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payeeBankReference": {
                  "type": "string",
                  "example": "PEBR2783",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "amount": {
                  "type": "string",
                  "example": "$5000",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount    \n"
                },
                "currency": {
                  "type": "string",
                  "example": "USD",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                },
                "dateType": {
                  "type": "string",
                  "example": "Order",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                },
                "date": {
                  "type": "string",
                  "example": "2018-08-28",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Date    \n"
                },
                "paymentMechanism": {
                  "type": "string",
                  "example": "ACH",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Name    \n"
                },
                "paymentOrderUpdateResult": {
                  "type": "string",
                  "example": "Success",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                }
              },
              "example": {
                "date": "2018-08-28",
                "payerProductInstanceReference": "payer account number",
                "amount": "$5000",
                "paymentOrderUpdateDescription": "ChangePaymentOrder",
                "paymentOrderInitiatorReference": "POIR1234",
                "payeeReference": "PAEE5007",
                "payeeProductInstanceReference": "PPIR3456",
                "payerBankReference": "PYBR1093",
                "payeeBankReference": "PEBR2783",
                "paymentOrderUpdateReference": "POUR7676",
                "paymentOrderUpdateResult": "Success",
                "dateType": "Order",
                "payerReference": "PYRE5345",
                "currency": "USD",
                "paymentOrderRequestReference": "PDRE9408",
                "paymentMechanism": "ACH"
              }
            }
          }
        }
      }
    },
    "/payment-order/payment-order-procedure/{cr-reference-id}/executions/{bq-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve execution reporting",
        "description": "Retrieve a payment order payment execution report",
        "operationId": "retrievePaymentOrderPaymentExecutionProcedure",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Payment Order Request Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Payment Execution Transaction Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "Successfully retrieved payment order execution report.",
            "schema": {
              "type": "object",
              "properties": {
                "paymentExecutionServiceReference": {
                  "type": "string",
                  "example": "PESR3434",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "paymentExecutionServiceStatus": {
                  "type": "string",
                  "example": "Initiated",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                },
                "paymentOrderRequestReference": {
                  "type": "string",
                  "example": "PESR3434",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "paymentOrderReference": {
                  "type": "string",
                  "example": "POR72345324",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "paymentExecutionTransactionReference": {
                  "type": "string",
                  "example": "PTRE4545",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "paymentOrder": {
                  "type": "string",
                  "example": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary    \n"
                }
              },
              "example": {
                "paymentOrder": "object",
                "paymentExecutionServiceStatus": "Initiated",
                "paymentExecutionTransactionReference": "PTRE4545",
                "paymentOrderRequestReference": "PESR3434",
                "paymentExecutionServiceReference": "PESR3434",
                "paymentOrderReference": "POR72345324"
              }
            }
          }
        }
      }
    },
    "/payment-order/payment-order-procedure/{cr-reference-id}/reportings/{bq-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve reporting",
        "description": "Retrieve a payment order reporting",
        "operationId": "retrievePaymentOrderReportingProcedure",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Payment Order Request Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Payment Order Reporting Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "Successfully retrieved payment order reporting report.",
            "schema": {
              "type": "object",
              "properties": {
                "paymentOrderRequestReference": {
                  "type": "string",
                  "example": "PDRE9456",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "paymentOrderReportingReference": {
                  "type": "string",
                  "example": "PDRE9408",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "paymentOrderInitiatorReference": {
                  "type": "string",
                  "example": "POIR4949",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payerReference": {
                  "type": "string",
                  "example": "PYRE5345",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payerBankReference": {
                  "type": "string",
                  "example": "PYBR1093",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payerProductInstanceReference": {
                  "type": "string",
                  "example": "PPIR2467",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payeeReference": {
                  "type": "string",
                  "example": "PAEE5007",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payeeProductInstanceReference": {
                  "type": "string",
                  "example": "PARR6400",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "payeeBankReference": {
                  "type": "string",
                  "example": "PEBR2783",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "amount": {
                  "type": "string",
                  "example": "$5000",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount    \n"
                },
                "currency": {
                  "type": "string",
                  "example": "USD",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                },
                "dateType": {
                  "type": "string",
                  "example": "Order",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                },
                "date": {
                  "type": "string",
                  "example": "2018-08-28T00:00:00Z",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Date    \n"
                },
                "paymentMechanism": {
                  "type": "string",
                  "example": "NEFT",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Name    \n"
                },
                "paymentOrderStatus": {
                  "type": "string",
                  "example": "Initiated",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                }
              },
              "example": {
                "date": "2018-08-28T00:00:00Z",
                "payerProductInstanceReference": "PPIR2467",
                "amount": "$5000",
                "paymentOrderInitiatorReference": "POIR4949",
                "payeeReference": "PAEE5007",
                "payeeProductInstanceReference": "PARR6400",
                "payerBankReference": "PYBR1093",
                "payeeBankReference": "PEBR2783",
                "dateType": "Order",
                "payerReference": "PYRE5345",
                "paymentOrderStatus": "Initiated",
                "currency": "USD",
                "paymentOrderRequestReference": "PDRE9456",
                "paymentOrderReportingReference": "PDRE9408",
                "paymentMechanism": "NEFT"
              }
            }
          }
        }
      }
    }
  },
  "definitions": {
    "MasterOrderRecordBase": {
      "type": "object",
      "properties": {
        "paymentOrderInitiatorReference": {
          "type": "string",
          "example": "source",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "payerReference": {
          "type": "string",
          "example": "PA7753535",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier    \n"
        },
        "payerBankReference": {
          "type": "string",
          "example": "PRIR5859",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier    \n"
        },
        "payerProductInstanceReference": {
          "type": "string",
          "example": "PERR3438",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier    \n"
        },
        "payeeReference": {
          "type": "string",
          "example": "POPR72354",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier    \n"
        },
        "payeeProductInstanceReference": {
          "type": "string",
          "example": "PI73453145",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier    \n"
        },
        "payeeBankReference": {
          "type": "string",
          "example": "PEIR5859",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier    \n"
        },
        "amount": {
          "type": "string",
          "example": "$2000",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount    \n"
        },
        "currency": {
          "type": "string",
          "example": "USD",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
        },
        "dateType": {
          "type": "string",
          "example": "interest bearing",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
        },
        "date": {
          "type": "string",
          "example": "09-07-2018",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Date    \n"
        },
        "paymentMechanismReference": {
          "type": "string",
          "example": "SWIFT",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier    \n"
        },
        "paymentMechanismType": {
          "type": "string",
          "example": "Mechanism Type",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
        },
        "paymentMechanismProperties": {
          "type": "string",
          "example": "specific payment instructions",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
        }
      },
      "example": {
        "date": "09-07-2018",
        "payerProductInstanceReference": "PERR3438",
        "amount": "$2000",
        "paymentOrderInitiatorReference": "source",
        "payeeReference": "POPR72354",
        "payeeProductInstanceReference": "PI73453145",
        "payerBankReference": "PRIR5859",
        "payeeBankReference": "PEIR5859",
        "paymentMechanismType": "Mechanism Type",
        "paymentMechanismProperties": "specific payment instructions",
        "dateType": "interest bearing",
        "payerReference": "PA7753535",
        "currency": "USD",
        "paymentMechanismReference": "SWIFT"
      }
    },
    "MasterOrderRecordBaseWithRoot": {
      "type": "object",
      "properties": {
        "paymentOrderRequestReference": {
          "type": "string",
          "example": "CR7735345",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "paymentOrderInitiatorReference": {
          "type": "string",
          "example": "source",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "payerReference": {
          "type": "string",
          "example": "PA7753535",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "payerBankReference": {
          "type": "string",
          "example": "PRIR5859",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "payerProductInstanceReference": {
          "type": "string",
          "example": "PERR3438",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "payeeReference": {
          "type": "string",
          "example": "POPR72354",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "payeeProductInstanceReference": {
          "type": "string",
          "example": "PI73453145",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "payeeBankReference": {
          "type": "string",
          "example": "PEIR5859",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "amount": {
          "type": "string",
          "example": "$2000",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount    \n"
        },
        "currency": {
          "type": "string",
          "example": "USD",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text      \n"
        },
        "dateType": {
          "type": "string",
          "example": "interest bearing",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text      \n"
        },
        "date": {
          "type": "string",
          "example": "09-07-2018",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Date      \n"
        },
        "paymentMechanismReference": {
          "type": "string",
          "example": "SWIFT",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier    \n"
        },
        "paymentMechanismType": {
          "type": "string",
          "example": "Mechanism Type",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
        },
        "paymentMechanismProperties": {
          "type": "string",
          "example": "specific payment instructions",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
        }
      },
      "example": {
        "date": "09-07-2018",
        "payerProductInstanceReference": "PERR3438",
        "amount": "$2000",
        "paymentOrderInitiatorReference": "source",
        "payeeReference": "POPR72354",
        "payeeProductInstanceReference": "PI73453145",
        "payerBankReference": "PRIR5859",
        "payeeBankReference": "PEIR5859",
        "paymentMechanismType": "Mechanism Type",
        "paymentMechanismProperties": "specific payment instructions",
        "dateType": "interest bearing",
        "payerReference": "PA7753535",
        "currency": "USD",
        "paymentOrderRequestReference": "CR7735345",
        "paymentMechanismReference": "SWIFT"
      }
    },
    "PaymentOrderComplianceBaseWithRootAndId": {
      "type": "object",
      "properties": {
        "paymentOrderRequestReference": {
          "type": "string",
          "example": "PDRE9408",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "paymentOderComplianceCheckReference": {
          "type": "string",
          "example": "POCC7262342",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "payerReference": {
          "type": "string",
          "example": "PYRE5345",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "payeeReference": {
          "type": "string",
          "example": "PAEE5007",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "amount": {
          "type": "string",
          "example": "$5000",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount    \n"
        },
        "currency": {
          "type": "string",
          "example": "USD",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
        },
        "paymentOrderComplianceCheckType": {
          "type": "string",
          "example": "Check Type",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
        },
        "paymentOrderComplianceCheckResult": {
          "type": "string",
          "example": "Success",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
        }
      },
      "example": {
        "paymentOrderComplianceCheckType": "Check Type",
        "amount": "$5000",
        "payeeReference": "PAEE5007",
        "paymentOderComplianceCheckReference": "POCC7262342",
        "payerReference": "PYRE5345",
        "currency": "USD",
        "paymentOrderComplianceCheckResult": "Success",
        "paymentOrderRequestReference": "PDRE9408"
      }
    },
    "PaymentOrderRecordRequest": {
      "type": "object",
      "properties": {
        "recordingRecordType": {
          "type": "string",
          "example": "BehaviorModelPerformanceFeedback",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
        },
        "recordingRecord": {
          "type": "object",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary    \n",
          "properties": {}
        },
        "recordingRecordDateTime": {
          "type": "string",
          "example": "2018-08-28T09:00:00Z",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime    \n"
        },
        "empolyeeBusinessUnitReference": {
          "type": "string",
          "example": "EBUR6798",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        }
      },
      "example": {
        "recordingRecordType": "BehaviorModelPerformanceFeedback",
        "empolyeeBusinessUnitReference": "EBUR6798",
        "recordingRecordDateTime": "2018-08-28T09:00:00Z",
        "recordingRecord": "{}"
      }
    },
    "PaymentOrderRecordResponse": {
      "type": "object",
      "properties": {
        "recordingRecordReference": {
          "type": "string",
          "example": "CRRR3456",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "recordingRecordStatus": {
          "type": "string",
          "example": "Applied",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
        }
      },
      "example": {
        "recordingRecordReference": "CRRR3456",
        "recordingRecordStatus": "Applied"
      }
    },
    "PaymentOrderOrderBaseWithRoot": {
      "type": "object",
      "properties": {
        "paymentOrderRequestReference": {
          "type": "string",
          "example": "PDRE9408",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "paymentOrderReference": {
          "type": "string",
          "example": "PDRE9408",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "paymentOrderStatus": {
          "type": "string",
          "example": "authorization",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
        },
        "interestedParties": {
          "type": "string",
          "example": "authorizing",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
        },
        "productInstanceReference": {
          "type": "string",
          "example": "for default settlement instructions",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "paymentExecutionReference": {
          "type": "string",
          "example": "PER723475324",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "settlementInstructions": {
          "type": "string",
          "example": "can be defined as part of the payment or determined at execution",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
        }
      },
      "example": {
        "paymentExecutionReference": "PER723475324",
        "productInstanceReference": "for default settlement instructions",
        "settlementInstructions": "can be defined as part of the payment or determined at execution",
        "paymentOrderStatus": "authorization",
        "interestedParties": "authorizing",
        "paymentOrderRequestReference": "PDRE9408",
        "paymentOrderReference": "PDRE9408"
      }
    },
    "PaymentOrderUpdateBase": {
      "type": "object",
      "properties": {
        "paymentOrderUpdateDescription": {
          "type": "string",
          "example": "ChangePaymentOrder",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
        },
        "paymentOrderInitiatorReference": {
          "type": "string",
          "example": "POIR1234",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "payerReference": {
          "type": "string",
          "example": "PYRE5345",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "payerBankReference": {
          "type": "string",
          "example": "PYBR1093",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "payerProductInstanceReference": {
          "type": "string",
          "example": "payer account number",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "payeeReference": {
          "type": "string",
          "example": "PAEE5007",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "payeeProductInstanceReference": {
          "type": "string",
          "example": "PPIR3456",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "payeeBankReference": {
          "type": "string",
          "example": "PEBR2783",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "amount": {
          "type": "string",
          "example": "$5000",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount    \n"
        },
        "currency": {
          "type": "string",
          "example": "USD",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
        },
        "dateType": {
          "type": "string",
          "example": "Order",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
        },
        "date": {
          "type": "string",
          "example": "2018-08-28T00:00:00Z",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Date      \n"
        },
        "paymentMechanism": {
          "type": "string",
          "example": "ACH",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Name    \n"
        }
      },
      "example": {
        "date": "2018-08-28T00:00:00Z",
        "payerProductInstanceReference": "payer account number",
        "amount": "$5000",
        "paymentOrderUpdateDescription": "ChangePaymentOrder",
        "paymentOrderInitiatorReference": "POIR1234",
        "payeeReference": "PAEE5007",
        "payeeProductInstanceReference": "PPIR3456",
        "payerBankReference": "PYBR1093",
        "payeeBankReference": "PEBR2783",
        "dateType": "Order",
        "payerReference": "PYRE5345",
        "currency": "USD",
        "paymentMechanism": "ACH"
      }
    },
    "PaymentOrderUpdateBaseWithRoot": {
      "type": "object",
      "properties": {
        "paymentOrderRequestReference": {
          "type": "string",
          "example": "PDRE9408",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "paymentOrderUpdateReference": {
          "type": "string",
          "example": "POUR7676",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "paymentOrderUpdateDescription": {
          "type": "string",
          "example": "ChangePaymentOrder",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
        },
        "paymentOrderInitiatorReference": {
          "type": "string",
          "example": "POIR1234",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "payerReference": {
          "type": "string",
          "example": "PYRE5345",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "payerBankReference": {
          "type": "string",
          "example": "PYBR1093",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier    \n"
        },
        "payerProductInstanceReference": {
          "type": "string",
          "example": "payer account number",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "payeeReference": {
          "type": "string",
          "example": "PAEE5007",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "payeeProductInstanceReference": {
          "type": "string",
          "example": "PPIR3456",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "payeeBankReference": {
          "type": "string",
          "example": "PEBR2783",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "amount": {
          "type": "string",
          "example": "$5000",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount    \n"
        },
        "currency": {
          "type": "string",
          "example": "USD",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
        },
        "dateType": {
          "type": "string",
          "example": "Order",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
        },
        "date": {
          "type": "string",
          "example": "2018-08-28",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Date    \n"
        },
        "paymentMechanism": {
          "type": "string",
          "example": "ACH",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Name    \n"
        },
        "paymentOrderUpdateResult": {
          "type": "string",
          "example": "Success",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
        }
      },
      "example": {
        "date": "2018-08-28",
        "payerProductInstanceReference": "payer account number",
        "amount": "$5000",
        "paymentOrderUpdateDescription": "ChangePaymentOrder",
        "paymentOrderInitiatorReference": "POIR1234",
        "payeeReference": "PAEE5007",
        "payeeProductInstanceReference": "PPIR3456",
        "payerBankReference": "PYBR1093",
        "payeeBankReference": "PEBR2783",
        "paymentOrderUpdateReference": "POUR7676",
        "paymentOrderUpdateResult": "Success",
        "dateType": "Order",
        "payerReference": "PYRE5345",
        "currency": "USD",
        "paymentOrderRequestReference": "PDRE9408",
        "paymentMechanism": "ACH"
      }
    },
    "PaymentExecutionBaseWithId": {
      "type": "object",
      "properties": {
        "paymentExecutionServiceReference": {
          "type": "string",
          "example": "PESR3434",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "paymentExecutionServiceStatus": {
          "type": "string",
          "example": "Initiated",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
        },
        "paymentOrderRequestReference": {
          "type": "string",
          "example": "PESR3434",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "paymentOrderReference": {
          "type": "string",
          "example": "POR72345324",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "paymentExecutionTransactionReference": {
          "type": "string",
          "example": "PTRE4545",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "paymentOrder": {
          "type": "string",
          "example": "object",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary    \n"
        }
      },
      "example": {
        "paymentOrder": "object",
        "paymentExecutionServiceStatus": "Initiated",
        "paymentExecutionTransactionReference": "PTRE4545",
        "paymentOrderRequestReference": "PESR3434",
        "paymentExecutionServiceReference": "PESR3434",
        "paymentOrderReference": "POR72345324"
      }
    },
    "PaymentOrderReportingBaseWithRoot": {
      "type": "object",
      "properties": {
        "paymentOrderRequestReference": {
          "type": "string",
          "example": "PDRE9456",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "paymentOrderReportingReference": {
          "type": "string",
          "example": "PDRE9408",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "paymentOrderInitiatorReference": {
          "type": "string",
          "example": "POIR4949",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "payerReference": {
          "type": "string",
          "example": "PYRE5345",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "payerBankReference": {
          "type": "string",
          "example": "PYBR1093",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "payerProductInstanceReference": {
          "type": "string",
          "example": "PPIR2467",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "payeeReference": {
          "type": "string",
          "example": "PAEE5007",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "payeeProductInstanceReference": {
          "type": "string",
          "example": "PARR6400",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "payeeBankReference": {
          "type": "string",
          "example": "PEBR2783",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "amount": {
          "type": "string",
          "example": "$5000",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount    \n"
        },
        "currency": {
          "type": "string",
          "example": "USD",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
        },
        "dateType": {
          "type": "string",
          "example": "Order",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
        },
        "date": {
          "type": "string",
          "example": "2018-08-28T00:00:00Z",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Date    \n"
        },
        "paymentMechanism": {
          "type": "string",
          "example": "NEFT",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Name    \n"
        },
        "paymentOrderStatus": {
          "type": "string",
          "example": "Initiated",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
        }
      },
      "example": {
        "date": "2018-08-28T00:00:00Z",
        "payerProductInstanceReference": "PPIR2467",
        "amount": "$5000",
        "paymentOrderInitiatorReference": "POIR4949",
        "payeeReference": "PAEE5007",
        "payeeProductInstanceReference": "PARR6400",
        "payerBankReference": "PYBR1093",
        "payeeBankReference": "PEBR2783",
        "dateType": "Order",
        "payerReference": "PYRE5345",
        "paymentOrderStatus": "Initiated",
        "currency": "USD",
        "paymentOrderRequestReference": "PDRE9456",
        "paymentOrderReportingReference": "PDRE9408",
        "paymentMechanism": "NEFT"
      }
    },
    "PaymentOrderRetrieveCapture": {
      "type": "object",
      "properties": {
        "paymentOrderRequestReference": {
          "type": "string",
          "example": "PORR4545",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "paymentOrderInitiatorReference": {
          "type": "string",
          "example": "POIR4545",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "payerReference": {
          "type": "string",
          "example": "PYRE4545",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "payerBankReference": {
          "type": "string",
          "example": "PBRE4545",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "payerProductInstanceReference": {
          "type": "string",
          "example": "PPRE4545",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "payeeReference": {
          "type": "string",
          "example": "PTRE4545",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "payeeProductInstanceReference": {
          "type": "string",
          "example": "PTRE4545",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "payeeBankReference": {
          "type": "string",
          "example": "PTRE4545",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "amount": {
          "type": "string",
          "example": "$5000",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount    \n"
        },
        "currency": {
          "type": "string",
          "example": "USD",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
        },
        "dateType": {
          "type": "string",
          "example": "order",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
        },
        "date": {
          "type": "string",
          "example": "2018-09-07",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Date    \n"
        },
        "paymentMechanismReference": {
          "type": "string",
          "example": "ACH",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier    \n"
        },
        "paymentMechanismType": {
          "type": "string",
          "example": "Type",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text      \n"
        },
        "paymentMechanismProperties": {
          "type": "string",
          "example": "specific payment instructions",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        }
      },
      "example": {
        "date": "2018-09-07",
        "payerProductInstanceReference": "PPRE4545",
        "amount": "$5000",
        "paymentOrderInitiatorReference": "POIR4545",
        "payeeReference": "PTRE4545",
        "payeeProductInstanceReference": "PTRE4545",
        "payerBankReference": "PBRE4545",
        "payeeBankReference": "PTRE4545",
        "paymentMechanismType": "Type",
        "paymentMechanismProperties": "specific payment instructions",
        "dateType": "order",
        "payerReference": "PYRE4545",
        "currency": "USD",
        "paymentOrderRequestReference": "PORR4545",
        "paymentMechanismReference": "ACH"
      }
    }
  }
}
</script>