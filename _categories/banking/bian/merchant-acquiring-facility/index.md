---
layout: api-single
title: BIAN Banking APIs - Merchant Acquiring Facility
parent-title: BIAN APIs
description: Banking API Standards - APIs - Merchant Acquiring Facility
keywords: 
duration: 
type: document
order: 2
parent: /categories/banking/bian
api-logo: /dist/images/logos/bian_logo.svg
api-summary: This service domain orchestrates the activities related to Merchant fulfillment, Merchant Account maintenance, Merchant transactional activities and settlement, including the billing of merchant fees and charges
api-example-use: The Acquiring Bank signs up Merchants for accepting Card Payments and opens Merchant Accounts for them
api-published-by: Bianuser06 Team
---
<script id="api-spec" type="application/json">
{
  "swagger": "2.0",
  "info": {
    "version": "1.0.0",
    "title": "Merchant Acquiring Facility",
    "description": "Orchestrates the activities related to Merchant fulfillment, Merchant Account maintenance, etc"
  },
  "host": "bianorg.azure-api.net",
  "basePath": "/sd-mchnt-aqrng-fclty/v1",
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
    "/merchant-acquiring-facility/merchant-acquiring-facility-fulfillment-arrangement/initiation": {
      "post": {
        "tags": [
          "initiate"
        ],
        "summary": "Initiate Merchant Acquiring Facility",
        "description": "Initiate Merchant Acquiring Facility",
        "operationId": "initiateMerchantAcquiringFacilityFulfillmentArrangement",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "in": "body",
            "name": "body",
            "description": "Initiate a new merchant acquiring facility",
            "required": true,
            "schema": {
              "type": "object",
              "properties": {
                "productServiceReference": {
                  "type": "string",
                  "example": "PSRE32429",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "customerReference": {
                  "type": "string",
                  "example": "CURE3242",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier             \n"
                },
                "partyReference": {
                  "type": "string",
                  "example": "PARE3002",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "bankBranchLocationReference": {
                  "type": "string",
                  "example": "BBLR4222",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
                },
                "accountCurrency": {
                  "type": "string",
                  "example": "USD",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "merchantAcquiringFacilityStatus": {
                  "type": "string",
                  "example": "Active",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "merchantAcquiringFacilityLimits": {
                  "type": "string",
                  "example": "SpendLimits",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount  \n"
                },
                "merchantAcquiringFacilityAccountReference": {
                  "type": "string",
                  "example": "MAFR9399",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
                },
                "merchantAcquiringFacilityOperationalTerms": {
                  "type": "string",
                  "example": "Active",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "merchantAcquiringFacilityFeeConfiguration": {
                  "type": "string",
                  "example": "PenaltyRates",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Rate \n"
                },
                "taxReference": {
                  "type": "string",
                  "example": "TXRE3030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier   \n"
                }
              }
            }
          }
        ],
        "responses": {
          "201": {
            "description": "Created",
            "schema": {
              "type": "object",
              "properties": {
                "productInstanceReference": {
                  "type": "string",
                  "example": "PIRE2030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier \n"
                },
                "productServiceReference": {
                  "type": "string",
                  "example": "SERE32429",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "customerReference": {
                  "type": "string",
                  "example": "CURE3242",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier             \n"
                },
                "partyReference": {
                  "type": "string",
                  "example": "PARE3002",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "bankBranchLocationReference": {
                  "type": "string",
                  "example": "BBLR4222",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
                },
                "accountCurrency": {
                  "type": "string",
                  "example": "USD",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text \n"
                },
                "merchantAcquiringFacilityStatus": {
                  "type": "string",
                  "example": "Active",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "merchantAcquiringFacilityLimits": {
                  "type": "string",
                  "example": "SpendLimits",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount  \n"
                },
                "merchantAcquiringFacilityAccountReference": {
                  "type": "string",
                  "example": "MAFR9399",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
                },
                "merchantAcquiringFacilityOperationalTerms": {
                  "type": "string",
                  "example": "Active",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "merchantAcquiringFacilityFeeConfiguration": {
                  "type": "string",
                  "example": "PenaltyRates",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Rate \n"
                },
                "taxReference": {
                  "type": "string",
                  "example": "TXRE3030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier \n"
                }
              }
            }
          }
        }
      }
    },
    "/merchant-acquiring-facility/merchant-acquiring-facility-fulfillment-arrangement/{cr-reference-id}/updation": {
      "put": {
        "tags": [
          "update"
        ],
        "summary": "Update Merchant Acquiring Facility",
        "description": "Update the options/settings for a merchant acquiring facility",
        "operationId": "updateMerchantAcquiringFacilityFulfillmentArrangement",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Product Instance Reference",
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
                "productServiceReference": {
                  "type": "string",
                  "example": "PSRE32429",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "customerReference": {
                  "type": "string",
                  "example": "CURE3242",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier             \n"
                },
                "partyReference": {
                  "type": "string",
                  "example": "PARE3002",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "bankBranchLocationReference": {
                  "type": "string",
                  "example": "BBLR4222",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
                },
                "accountCurrency": {
                  "type": "string",
                  "example": "USD",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "merchantAcquiringFacilityStatus": {
                  "type": "string",
                  "example": "Active",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "merchantAcquiringFacilityLimits": {
                  "type": "string",
                  "example": "SpendLimits",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount  \n"
                },
                "merchantAcquiringFacilityAccountReference": {
                  "type": "string",
                  "example": "MAFR9399",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
                },
                "merchantAcquiringFacilityOperationalTerms": {
                  "type": "string",
                  "example": "Active",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "merchantAcquiringFacilityFeeConfiguration": {
                  "type": "string",
                  "example": "PenaltyRates",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Rate \n"
                },
                "taxReference": {
                  "type": "string",
                  "example": "TXRE3030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier   \n"
                }
              }
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "schema": {
              "type": "object",
              "properties": {
                "productInstanceReference": {
                  "type": "string",
                  "example": "PIRE2030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier \n"
                },
                "productServiceReference": {
                  "type": "string",
                  "example": "SERE32429",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "customerReference": {
                  "type": "string",
                  "example": "CURE3242",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier             \n"
                },
                "partyReference": {
                  "type": "string",
                  "example": "PARE3002",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "bankBranchLocationReference": {
                  "type": "string",
                  "example": "BBLR4222",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
                },
                "accountCurrency": {
                  "type": "string",
                  "example": "USD",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text \n"
                },
                "merchantAcquiringFacilityStatus": {
                  "type": "string",
                  "example": "Active",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "merchantAcquiringFacilityLimits": {
                  "type": "string",
                  "example": "SpendLimits",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount  \n"
                },
                "merchantAcquiringFacilityAccountReference": {
                  "type": "string",
                  "example": "MAFR9399",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
                },
                "merchantAcquiringFacilityOperationalTerms": {
                  "type": "string",
                  "example": "Active",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "merchantAcquiringFacilityFeeConfiguration": {
                  "type": "string",
                  "example": "PenaltyRates",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Rate \n"
                },
                "taxReference": {
                  "type": "string",
                  "example": "TXRE3030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier \n"
                }
              }
            }
          }
        }
      }
    },
    "/merchant-acquiring-facility/merchant-acquiring-facility-fulfillment-arrangement/{cr-reference-id}/recording": {
      "post": {
        "tags": [
          "record"
        ],
        "summary": "Record feedback",
        "description": "Record feedback/activity against a merchant acquiring facility",
        "operationId": "recordMerchantAcquiringFacilityFulfillmentArrangement",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Product Instance Reference",
            "required": true,
            "type": "string"
          },
          {
            "in": "body",
            "name": "Merchant Acquiring",
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
                  "example": "2018-08-28T09:00:00",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime \n"
                },
                "empolyeeBusinessUnitReference": {
                  "type": "string",
                  "example": "EBUR6798",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier       \n"
                }
              }
            }
          }
        ],
        "responses": {
          "201": {
            "description": "Created",
            "schema": {
              "type": "object",
              "properties": {
                "recordingRecordReference": {
                  "type": "string",
                  "example": "RRR2030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
                },
                "recordingRecordStatus": {
                  "type": "string",
                  "example": "Applied",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text      \n"
                }
              }
            }
          }
        }
      }
    },
    "/merchant-acquiring-facility/merchant-acquiring-facility-fulfillment-arrangement/{cr-reference-id}/clearings/{bq-reference-id}/execution": {
      "put": {
        "tags": [
          "execute"
        ],
        "summary": "Execute merchant facility transactions",
        "description": "Process merchant facility transactions",
        "operationId": "executeMerchantAcquiringFacilityFulfillmentArrangementclearing",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Product Instance Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Merchant Acquiring Clearing Task Reference",
            "required": true,
            "type": "string"
          },
          {
            "in": "body",
            "name": "body",
            "description": "Execute Merchant Acquiring request payload",
            "required": true,
            "schema": {
              "type": "object",
              "properties": {
                "cardTransactionRecordReference": {
                  "type": "string",
                  "example": "CTRR9292",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionProductInstanceReference": {
                  "type": "string",
                  "example": "CTPI8390",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionNetworkReference": {
                  "type": "string",
                  "example": "CTNR3030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionIssuingBankReference": {
                  "type": "string",
                  "example": "CTIB3293",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionMerchantAcquiringBankReference": {
                  "type": "string",
                  "example": "CTMA0393",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionType": {
                  "type": "string",
                  "example": "Debit",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text             \n"
                },
                "cardTransactionCurrency": {
                  "type": "string",
                  "example": "USD",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "cardTransactionAmountType": {
                  "type": "string",
                  "example": "OriginalAmount",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "cardTransactionAmount": {
                  "type": "string",
                  "example": "$500",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount\n"
                },
                "cardTransactionMerchantReference": {
                  "type": "string",
                  "example": "CTMR3022",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionLocationReference": {
                  "type": "string",
                  "example": "CTLR4344",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionProductServiceReference": {
                  "type": "string",
                  "example": "CTSR2244",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionDateTime": {
                  "type": "string",
                  "example": "2018-12-07:T09:00:00",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
                },
                "cardTransactionFXConversionCharge": {
                  "type": "string",
                  "example": "$20",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount  \n"
                },
                "cardTransactionInterchargeFee": {
                  "type": "string",
                  "example": "$5",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount\n"
                },
                "cardTransactionAuthorizationRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary        \n",
                  "properties": {}
                },
                "merchantAcquiringClearingTaskRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary      \n",
                  "properties": {}
                }
              }
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "schema": {
              "type": "object",
              "properties": {
                "merchantAcquiringClearingTaskReference": {
                  "type": "string",
                  "example": "MACR3198",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
                },
                "productInstanceReference": {
                  "type": "string",
                  "example": "LPIR2030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionRecordReference": {
                  "type": "string",
                  "example": "CTRR9292",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionProductInstanceReference": {
                  "type": "string",
                  "example": "CTPI8390",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionNetworkReference": {
                  "type": "string",
                  "example": "CTNR3030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionIssuingBankReference": {
                  "type": "string",
                  "example": "CTIB3293",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionMerchantAcquiringBankReference": {
                  "type": "string",
                  "example": "CTMA0393",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionType": {
                  "type": "string",
                  "example": "Debit",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text             \n"
                },
                "cardTransactionCurrency": {
                  "type": "string",
                  "example": "USD",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "cardTransactionAmountType": {
                  "type": "string",
                  "example": "OriginalAmount",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "cardTransactionAmount": {
                  "type": "string",
                  "example": "$500",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount\n"
                },
                "cardTransactionMerchantReference": {
                  "type": "string",
                  "example": "CTMR3022",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionLocationReference": {
                  "type": "string",
                  "example": "CTLR4344",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionProductServiceReference": {
                  "type": "string",
                  "example": "CTSR2244",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionDateTime": {
                  "type": "string",
                  "example": "2018-12-07:T09:00:00",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
                },
                "cardTransactionFXConversionCharge": {
                  "type": "string",
                  "example": "$20",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount  \n"
                },
                "cardTransactionInterchargeFee": {
                  "type": "string",
                  "example": "$5",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount\n"
                },
                "cardTransactionAuthorizationRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary        \n",
                  "properties": {}
                },
                "merchantAcquiringClearingTaskRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
                  "properties": {}
                }
              }
            }
          }
        }
      }
    },
    "/merchant-acquiring-facility/merchant-acquiring-facility-fulfillment-arrangement/{cr-reference-id}/clearings/execution": {
      "post": {
        "tags": [
          "execute"
        ],
        "summary": "Execute merchant facility transactions",
        "description": "Process merchant facility transactions",
        "operationId": "executeMerchantAcquiringFacilityFulfillmentArrangementclearings",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Product Instance Reference",
            "required": true,
            "type": "string"
          },
          {
            "in": "body",
            "name": "body",
            "description": "Execute merchant facility request payload",
            "required": true,
            "schema": {
              "type": "object",
              "properties": {
                "cardTransactionRecordReference": {
                  "type": "string",
                  "example": "CTRR9292",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionProductInstanceReference": {
                  "type": "string",
                  "example": "CTPI8390",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionNetworkReference": {
                  "type": "string",
                  "example": "CTNR3030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionIssuingBankReference": {
                  "type": "string",
                  "example": "CTIB3293",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionMerchantAcquiringBankReference": {
                  "type": "string",
                  "example": "CTMA0393",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionType": {
                  "type": "string",
                  "example": "Debit",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text             \n"
                },
                "cardTransactionCurrency": {
                  "type": "string",
                  "example": "USD",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "cardTransactionAmountType": {
                  "type": "string",
                  "example": "OriginalAmount",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "cardTransactionAmount": {
                  "type": "string",
                  "example": "$500",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount\n"
                },
                "cardTransactionMerchantReference": {
                  "type": "string",
                  "example": "CTMR3022",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionLocationReference": {
                  "type": "string",
                  "example": "CTLR4344",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionProductServiceReference": {
                  "type": "string",
                  "example": "CTSR2244",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionDateTime": {
                  "type": "string",
                  "example": "2018-12-07:T09:00:00",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
                },
                "cardTransactionFXConversionCharge": {
                  "type": "string",
                  "example": "$20",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount  \n"
                },
                "cardTransactionInterchargeFee": {
                  "type": "string",
                  "example": "$5",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount\n"
                },
                "cardTransactionAuthorizationRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary        \n",
                  "properties": {}
                },
                "merchantAcquiringClearingTaskRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary      \n",
                  "properties": {}
                }
              }
            }
          }
        ],
        "responses": {
          "201": {
            "description": "Created",
            "schema": {
              "type": "object",
              "properties": {
                "merchantAcquiringClearingTaskReference": {
                  "type": "string",
                  "example": "MACR3198",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
                },
                "productInstanceReference": {
                  "type": "string",
                  "example": "LPIR2030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionRecordReference": {
                  "type": "string",
                  "example": "CTRR9292",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionProductInstanceReference": {
                  "type": "string",
                  "example": "CTPI8390",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionNetworkReference": {
                  "type": "string",
                  "example": "CTNR3030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionIssuingBankReference": {
                  "type": "string",
                  "example": "CTIB3293",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionMerchantAcquiringBankReference": {
                  "type": "string",
                  "example": "CTMA0393",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionType": {
                  "type": "string",
                  "example": "Debit",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text             \n"
                },
                "cardTransactionCurrency": {
                  "type": "string",
                  "example": "USD",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "cardTransactionAmountType": {
                  "type": "string",
                  "example": "OriginalAmount",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "cardTransactionAmount": {
                  "type": "string",
                  "example": "$500",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount\n"
                },
                "cardTransactionMerchantReference": {
                  "type": "string",
                  "example": "CTMR3022",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionLocationReference": {
                  "type": "string",
                  "example": "CTLR4344",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionProductServiceReference": {
                  "type": "string",
                  "example": "CTSR2244",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionDateTime": {
                  "type": "string",
                  "example": "2018-12-07:T09:00:00",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
                },
                "cardTransactionFXConversionCharge": {
                  "type": "string",
                  "example": "$20",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount  \n"
                },
                "cardTransactionInterchargeFee": {
                  "type": "string",
                  "example": "$5",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount\n"
                },
                "cardTransactionAuthorizationRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary        \n",
                  "properties": {}
                },
                "merchantAcquiringClearingTaskRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
                  "properties": {}
                }
              }
            }
          }
        }
      }
    },
    "/merchant-acquiring-facility/merchant-acquiring-facility-fulfillment-arrangement/{cr-reference-id}/chargebacks/{bq-reference-id}/execution": {
      "put": {
        "tags": [
          "execute"
        ],
        "summary": "Execute merchant facility chargebacks and adjustments",
        "description": "Process merchant facility chargebacks and adjustments",
        "operationId": "executeMerchantAcquiringFacilityFulfillmentArrangementChargeback",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Product Instance Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Merchant Acquiring Chargeback Task Reference",
            "required": true,
            "type": "string"
          },
          {
            "in": "body",
            "name": "body",
            "description": "Execute Merchant Acquiring chargebacks request payload",
            "required": true,
            "schema": {
              "type": "object",
              "properties": {
                "chargebackInstruction": {
                  "type": "string",
                  "example": "AmountDetailed",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text      \n"
                },
                "cardTransactionRecordReference": {
                  "type": "string",
                  "example": "CTRR9292",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionProductInstanceReference": {
                  "type": "string",
                  "example": "CTPI8390",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionNetworkReference": {
                  "type": "string",
                  "example": "CTNR3030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionIssuingBankReference": {
                  "type": "string",
                  "example": "CTIB3293",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionMerchantAcquiringBankReference": {
                  "type": "string",
                  "example": "CTMA0393",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionType": {
                  "type": "string",
                  "example": "Debit",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text             \n"
                },
                "cardTransactionCurrency": {
                  "type": "string",
                  "example": "USD",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "cardTransactionAmountType": {
                  "type": "string",
                  "example": "OriginalAmount",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "cardTransactionAmount": {
                  "type": "string",
                  "example": "$500",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount\n"
                },
                "cardTransactionMerchantReference": {
                  "type": "string",
                  "example": "CTMR3022",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionLocationReference": {
                  "type": "string",
                  "example": "CTLR4344",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionProductServiceReference": {
                  "type": "string",
                  "example": "CTSR2244",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionDateTime": {
                  "type": "string",
                  "example": "2018-12-07:T09:00:00",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
                },
                "cardTransactionFXConversionCharge": {
                  "type": "string",
                  "example": "$20",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount  \n"
                },
                "cardTransactionInterchargeFee": {
                  "type": "string",
                  "example": "$5",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount\n"
                },
                "cardTransactionAuthorizationRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary        \n",
                  "properties": {}
                },
                "merchantAcquiringChargebackTaskRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
                  "properties": {}
                }
              }
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "schema": {
              "type": "object",
              "properties": {
                "merchantAcquiringChargebackTaskReference": {
                  "type": "string",
                  "example": "MACB2001",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
                },
                "productInstanceReference": {
                  "type": "string",
                  "example": "LPIR2030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "chargebackInstruction": {
                  "type": "string",
                  "example": "AmountDetailed",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text      \n"
                },
                "cardTransactionRecordReference": {
                  "type": "string",
                  "example": "CTRR9292",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionProductInstanceReference": {
                  "type": "string",
                  "example": "CTPI8390",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionNetworkReference": {
                  "type": "string",
                  "example": "CTNR3030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionIssuingBankReference": {
                  "type": "string",
                  "example": "CTIB3293",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionMerchantAcquiringBankReference": {
                  "type": "string",
                  "example": "CTMA0393",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionType": {
                  "type": "string",
                  "example": "Debit",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text             \n"
                },
                "cardTransactionCurrency": {
                  "type": "string",
                  "example": "USD",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "cardTransactionAmountType": {
                  "type": "string",
                  "example": "OriginalAmount",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "cardTransactionAmount": {
                  "type": "string",
                  "example": "$500",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount\n"
                },
                "cardTransactionMerchantReference": {
                  "type": "string",
                  "example": "CTMR3022",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionLocationReference": {
                  "type": "string",
                  "example": "CTLR4344",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionProductServiceReference": {
                  "type": "string",
                  "example": "CTSR2244",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionDateTime": {
                  "type": "string",
                  "example": "2018-12-07:T09:00:00",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
                },
                "cardTransactionFXConversionCharge": {
                  "type": "string",
                  "example": "$20",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount  \n"
                },
                "cardTransactionInterchargeFee": {
                  "type": "string",
                  "example": "$5",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount\n"
                },
                "cardTransactionAuthorizationRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary        \n",
                  "properties": {}
                },
                "merchantAcquiringChargebackTaskRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary  \n",
                  "properties": {}
                }
              }
            }
          }
        }
      }
    },
    "/merchant-acquiring-facility/merchant-acquiring-facility-fulfillment-arrangement/{cr-reference-id}/chargebacks/execution": {
      "post": {
        "tags": [
          "execute"
        ],
        "summary": "Process merchant facility chargebacks and adjustments",
        "description": "Process merchant facility chargebacks and adjustments",
        "operationId": "executeMerchantAcquiringFacilityFulfillmentArrangementChargebacks",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Product Instance Reference",
            "required": true,
            "type": "string"
          },
          {
            "in": "body",
            "name": "body",
            "description": "Execute merchant facility chargeback request payload",
            "required": true,
            "schema": {
              "type": "object",
              "properties": {
                "chargebackInstruction": {
                  "type": "string",
                  "example": "AmountDetailed",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text      \n"
                },
                "cardTransactionRecordReference": {
                  "type": "string",
                  "example": "CTRR9292",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionProductInstanceReference": {
                  "type": "string",
                  "example": "CTPI8390",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionNetworkReference": {
                  "type": "string",
                  "example": "CTNR3030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionIssuingBankReference": {
                  "type": "string",
                  "example": "CTIB3293",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionMerchantAcquiringBankReference": {
                  "type": "string",
                  "example": "CTMA0393",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionType": {
                  "type": "string",
                  "example": "Debit",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text             \n"
                },
                "cardTransactionCurrency": {
                  "type": "string",
                  "example": "USD",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "cardTransactionAmountType": {
                  "type": "string",
                  "example": "OriginalAmount",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "cardTransactionAmount": {
                  "type": "string",
                  "example": "$500",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount\n"
                },
                "cardTransactionMerchantReference": {
                  "type": "string",
                  "example": "CTMR3022",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionLocationReference": {
                  "type": "string",
                  "example": "CTLR4344",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionProductServiceReference": {
                  "type": "string",
                  "example": "CTSR2244",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionDateTime": {
                  "type": "string",
                  "example": "2018-12-07:T09:00:00",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
                },
                "cardTransactionFXConversionCharge": {
                  "type": "string",
                  "example": "$20",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount  \n"
                },
                "cardTransactionInterchargeFee": {
                  "type": "string",
                  "example": "$5",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount\n"
                },
                "cardTransactionAuthorizationRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary        \n",
                  "properties": {}
                },
                "merchantAcquiringChargebackTaskRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
                  "properties": {}
                }
              }
            }
          }
        ],
        "responses": {
          "201": {
            "description": "Created",
            "schema": {
              "type": "object",
              "properties": {
                "merchantAcquiringChargebackTaskReference": {
                  "type": "string",
                  "example": "MACB2001",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
                },
                "productInstanceReference": {
                  "type": "string",
                  "example": "LPIR2030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "chargebackInstruction": {
                  "type": "string",
                  "example": "AmountDetailed",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text      \n"
                },
                "cardTransactionRecordReference": {
                  "type": "string",
                  "example": "CTRR9292",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionProductInstanceReference": {
                  "type": "string",
                  "example": "CTPI8390",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionNetworkReference": {
                  "type": "string",
                  "example": "CTNR3030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionIssuingBankReference": {
                  "type": "string",
                  "example": "CTIB3293",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionMerchantAcquiringBankReference": {
                  "type": "string",
                  "example": "CTMA0393",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionType": {
                  "type": "string",
                  "example": "Debit",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text             \n"
                },
                "cardTransactionCurrency": {
                  "type": "string",
                  "example": "USD",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "cardTransactionAmountType": {
                  "type": "string",
                  "example": "OriginalAmount",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "cardTransactionAmount": {
                  "type": "string",
                  "example": "$500",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount\n"
                },
                "cardTransactionMerchantReference": {
                  "type": "string",
                  "example": "CTMR3022",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionLocationReference": {
                  "type": "string",
                  "example": "CTLR4344",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionProductServiceReference": {
                  "type": "string",
                  "example": "CTSR2244",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionDateTime": {
                  "type": "string",
                  "example": "2018-12-07:T09:00:00",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
                },
                "cardTransactionFXConversionCharge": {
                  "type": "string",
                  "example": "$20",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount  \n"
                },
                "cardTransactionInterchargeFee": {
                  "type": "string",
                  "example": "$5",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount\n"
                },
                "cardTransactionAuthorizationRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary        \n",
                  "properties": {}
                },
                "merchantAcquiringChargebackTaskRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary  \n",
                  "properties": {}
                }
              }
            }
          }
        }
      }
    },
    "/merchant-acquiring-facility/merchant-acquiring-facility-fulfillment-arrangement/{cr-reference-id}/settlements/{bq-reference-id}/execution": {
      "put": {
        "tags": [
          "execute"
        ],
        "summary": "execute merchant facility settlement",
        "description": "Process merchant facility settlement",
        "operationId": "executeMerchantAcquiringFacilityFulfillmentArrangementSettlement",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Product Instance Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Merchant Acquiring Settlement Task  Reference",
            "required": true,
            "type": "string"
          },
          {
            "in": "body",
            "name": "body",
            "description": "Execute Merchant Acquiring settlement request payload",
            "required": true,
            "schema": {
              "type": "object",
              "properties": {
                "merchantAcquiringFacilityAccountReference": {
                  "type": "string",
                  "example": "MAFR9399",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "participantMerchantAcquirerBankReference": {
                  "type": "string",
                  "example": "PMAB3427",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "participantIssuerBankReference": {
                  "type": "string",
                  "example": "PIBR3218",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardFinancialSettlementServicePaymentAdviceRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary  \n",
                  "properties": {}
                },
                "participantPaymentTransaction": {
                  "type": "string",
                  "example": "Details",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "participantAcquirerBankSettlementAccountStatement": {
                  "type": "string",
                  "example": "Statement",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text      \n"
                },
                "merchantAcquiringSettlementTaskRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
                  "properties": {}
                }
              }
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "schema": {
              "type": "object",
              "properties": {
                "merchantAcquiringSettlementTaskReference": {
                  "type": "string",
                  "example": "MASR3056",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
                },
                "productInstanceReference": {
                  "type": "string",
                  "example": "LPIR2030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "merchantAcquiringFacilityAccountReference": {
                  "type": "string",
                  "example": "MAFR9399",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "participantMerchantAcquirerBankReference": {
                  "type": "string",
                  "example": "PMAB3427",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "participantIssuerBankReference": {
                  "type": "string",
                  "example": "PIBR3218",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardFinancialSettlementServicePaymentAdviceRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary  \n",
                  "properties": {}
                },
                "participantPaymentTransaction": {
                  "type": "string",
                  "example": "Details",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "participantAcquirerBankSettlementAccountStatement": {
                  "type": "string",
                  "example": "Statement",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text      \n"
                },
                "merchantAcquiringSettlementTaskRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
                  "properties": {}
                }
              }
            }
          }
        }
      }
    },
    "/merchant-acquiring-facility/merchant-acquiring-facility-fulfillment-arrangement/{cr-reference-id}/settlements/execution": {
      "post": {
        "tags": [
          "execute"
        ],
        "summary": "execute merchant facility settlement",
        "description": "Process merchant facility settlement",
        "operationId": "executeMerchantAcquiringFacilityFulfillmentArrangementSettlements",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Product Instance Reference",
            "required": true,
            "type": "string"
          },
          {
            "in": "body",
            "name": "body",
            "description": "Execute merchant facility settlement request payload",
            "required": true,
            "schema": {
              "type": "object",
              "properties": {
                "merchantAcquiringFacilityAccountReference": {
                  "type": "string",
                  "example": "MAFR9399",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "participantMerchantAcquirerBankReference": {
                  "type": "string",
                  "example": "PMAB3427",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "participantIssuerBankReference": {
                  "type": "string",
                  "example": "PIBR3218",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardFinancialSettlementServicePaymentAdviceRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary  \n",
                  "properties": {}
                },
                "participantPaymentTransaction": {
                  "type": "string",
                  "example": "Details",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "participantAcquirerBankSettlementAccountStatement": {
                  "type": "string",
                  "example": "Statement",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text      \n"
                },
                "merchantAcquiringSettlementTaskRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
                  "properties": {}
                }
              }
            }
          }
        ],
        "responses": {
          "201": {
            "description": "Created",
            "schema": {
              "type": "object",
              "properties": {
                "merchantAcquiringSettlementTaskReference": {
                  "type": "string",
                  "example": "MASR3056",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
                },
                "productInstanceReference": {
                  "type": "string",
                  "example": "LPIR2030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "merchantAcquiringFacilityAccountReference": {
                  "type": "string",
                  "example": "MAFR9399",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "participantMerchantAcquirerBankReference": {
                  "type": "string",
                  "example": "PMAB3427",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "participantIssuerBankReference": {
                  "type": "string",
                  "example": "PIBR3218",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardFinancialSettlementServicePaymentAdviceRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary  \n",
                  "properties": {}
                },
                "participantPaymentTransaction": {
                  "type": "string",
                  "example": "Details",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "participantAcquirerBankSettlementAccountStatement": {
                  "type": "string",
                  "example": "Statement",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text      \n"
                },
                "merchantAcquiringSettlementTaskRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
                  "properties": {}
                }
              }
            }
          }
        }
      }
    },
    "/merchant-acquiring-facility/merchant-acquiring-facility-fulfillment-arrangement/{cr-reference-id}/requisition": {
      "put": {
        "tags": [
          "request"
        ],
        "summary": "Request manual intervention requests on the facility",
        "description": "Process manual intervention requests on the facility",
        "operationId": "requestMerchantAcquiringFacilityFulfillmentArrangementUpdate",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Product Instance Reference",
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
                "productServiceReference": {
                  "type": "string",
                  "example": "PSRE32429",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "customerReference": {
                  "type": "string",
                  "example": "CURE3242",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier             \n"
                },
                "partyReference": {
                  "type": "string",
                  "example": "PARE3002",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "bankBranchLocationReference": {
                  "type": "string",
                  "example": "BBLR4222",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
                },
                "accountCurrency": {
                  "type": "string",
                  "example": "USD",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "merchantAcquiringFacilityStatus": {
                  "type": "string",
                  "example": "Active",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "merchantAcquiringFacilityLimits": {
                  "type": "string",
                  "example": "SpendLimits",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount  \n"
                },
                "merchantAcquiringFacilityAccountReference": {
                  "type": "string",
                  "example": "MAFR9399",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
                },
                "merchantAcquiringFacilityOperationalTerms": {
                  "type": "string",
                  "example": "Active",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "merchantAcquiringFacilityFeeConfiguration": {
                  "type": "string",
                  "example": "PenaltyRates",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Rate \n"
                },
                "taxReference": {
                  "type": "string",
                  "example": "TXRE3030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier   \n"
                }
              }
            }
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "schema": {
              "type": "object",
              "properties": {
                "productInstanceReference": {
                  "type": "string",
                  "example": "PIRE2030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier \n"
                },
                "productServiceReference": {
                  "type": "string",
                  "example": "SERE32429",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "customerReference": {
                  "type": "string",
                  "example": "CURE3242",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier             \n"
                },
                "partyReference": {
                  "type": "string",
                  "example": "PARE3002",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "bankBranchLocationReference": {
                  "type": "string",
                  "example": "BBLR4222",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
                },
                "accountCurrency": {
                  "type": "string",
                  "example": "USD",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text \n"
                },
                "merchantAcquiringFacilityStatus": {
                  "type": "string",
                  "example": "Active",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "merchantAcquiringFacilityLimits": {
                  "type": "string",
                  "example": "SpendLimits",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount  \n"
                },
                "merchantAcquiringFacilityAccountReference": {
                  "type": "string",
                  "example": "MAFR9399",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
                },
                "merchantAcquiringFacilityOperationalTerms": {
                  "type": "string",
                  "example": "Active",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "merchantAcquiringFacilityFeeConfiguration": {
                  "type": "string",
                  "example": "PenaltyRates",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Rate \n"
                },
                "taxReference": {
                  "type": "string",
                  "example": "TXRE3030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier \n"
                }
              }
            }
          }
        }
      }
    },
    "/merchant-acquiring-facility/merchant-acquiring-facility-fulfillment-arrangement/requisition": {
      "post": {
        "tags": [
          "request"
        ],
        "summary": "Request manual intervention requests on the facility",
        "description": "Process manual intervention requests on the facility",
        "operationId": "requestMerchantAcquiringFacilityFulfillmentArrangementCreate",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "in": "body",
            "name": "Merchant Acquiring",
            "required": true,
            "schema": {
              "type": "object",
              "properties": {
                "productServiceReference": {
                  "type": "string",
                  "example": "PSRE32429",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "customerReference": {
                  "type": "string",
                  "example": "CURE3242",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier             \n"
                },
                "partyReference": {
                  "type": "string",
                  "example": "PARE3002",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "bankBranchLocationReference": {
                  "type": "string",
                  "example": "BBLR4222",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
                },
                "accountCurrency": {
                  "type": "string",
                  "example": "USD",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "merchantAcquiringFacilityStatus": {
                  "type": "string",
                  "example": "Active",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "merchantAcquiringFacilityLimits": {
                  "type": "string",
                  "example": "SpendLimits",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount  \n"
                },
                "merchantAcquiringFacilityAccountReference": {
                  "type": "string",
                  "example": "MAFR9399",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
                },
                "merchantAcquiringFacilityOperationalTerms": {
                  "type": "string",
                  "example": "Active",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "merchantAcquiringFacilityFeeConfiguration": {
                  "type": "string",
                  "example": "PenaltyRates",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Rate \n"
                },
                "taxReference": {
                  "type": "string",
                  "example": "TXRE3030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier   \n"
                }
              }
            }
          }
        ],
        "responses": {
          "201": {
            "description": "Created",
            "schema": {
              "type": "object",
              "properties": {
                "productInstanceReference": {
                  "type": "string",
                  "example": "PIRE2030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier \n"
                },
                "productServiceReference": {
                  "type": "string",
                  "example": "SERE32429",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "customerReference": {
                  "type": "string",
                  "example": "CURE3242",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier             \n"
                },
                "partyReference": {
                  "type": "string",
                  "example": "PARE3002",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "bankBranchLocationReference": {
                  "type": "string",
                  "example": "BBLR4222",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
                },
                "accountCurrency": {
                  "type": "string",
                  "example": "USD",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text \n"
                },
                "merchantAcquiringFacilityStatus": {
                  "type": "string",
                  "example": "Active",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "merchantAcquiringFacilityLimits": {
                  "type": "string",
                  "example": "SpendLimits",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount  \n"
                },
                "merchantAcquiringFacilityAccountReference": {
                  "type": "string",
                  "example": "MAFR9399",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
                },
                "merchantAcquiringFacilityOperationalTerms": {
                  "type": "string",
                  "example": "Active",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "merchantAcquiringFacilityFeeConfiguration": {
                  "type": "string",
                  "example": "PenaltyRates",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Rate \n"
                },
                "taxReference": {
                  "type": "string",
                  "example": "TXRE3030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier \n"
                }
              }
            }
          }
        }
      }
    },
    "/merchant-acquiring-facility/merchant-acquiring-facility-fulfillment-arrangement/": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve CR Ids",
        "operationId": "retrieveMerchantAcquiringFacilityReferenceIds",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "collection-filter",
            "in": "query",
            "description": "Filter to refine the result set. ex- 'customerReference = 43563'",
            "required": false,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "schema": {
              "type": "array",
              "items": {
                "type": "string"
              },
              "example": [
                "CRR4533",
                "CRR5323"
              ]
            }
          }
        }
      }
    },
    "/merchant-acquiring-facility/merchant-acquiring-facility-fulfillment-arrangement/behavior-qualifiers/": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve BQ names.",
        "operationId": "retrieveMerchantAcquiringFacilityQualifiers",
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
                "FacilityTerms",
                "Account",
                "Clearing",
                "Chargeback",
                "Settlement",
                "Fees",
                "Reports"
              ]
            }
          }
        }
      }
    },
    "/merchant-acquiring-facility/merchant-acquiring-facility-fulfillment-arrangement/{cr-reference-id}/{behavior-qualifier}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve BQ Ids.",
        "operationId": "retrieveMerchantAcquiringFacilityReferenceId",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Product Instance Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "behavior-qualifier",
            "in": "path",
            "description": "Behavior Qualifier Name. ex- clearing",
            "required": true,
            "type": "string"
          },
          {
            "name": "collection-filter",
            "in": "query",
            "description": "Filter to refine the result set. ex- cardTransactionType=CTT1",
            "required": false,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "schema": {
              "type": "array",
              "items": {
                "type": "string"
              },
              "example": [
                "BQR34252",
                "BQR346234",
                "BQR43633"
              ]
            }
          }
        }
      }
    },
    "/merchant-acquiring-facility/merchant-acquiring-facility-fulfillment-arrangement/{cr-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve Master Control Records",
        "operationId": "retrieveMerchantAcquiringFacilityMaster",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Product Instance Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "schema": {
              "type": "object",
              "properties": {
                "productInstanceReference": {
                  "type": "string",
                  "example": "PIRE2030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier \n"
                },
                "productServiceReference": {
                  "type": "string",
                  "example": "SERE32429",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "customerReference": {
                  "type": "string",
                  "example": "CURE3242",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier             \n"
                },
                "partyReference": {
                  "type": "string",
                  "example": "PARE3002",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "bankBranchLocationReference": {
                  "type": "string",
                  "example": "BBLR4222",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
                },
                "accountCurrency": {
                  "type": "string",
                  "example": "USD",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text \n"
                },
                "merchantAcquiringFacilityStatus": {
                  "type": "string",
                  "example": "Active",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "merchantAcquiringFacilityLimits": {
                  "type": "string",
                  "example": "SpendLimits",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount  \n"
                },
                "merchantAcquiringFacilityAccountReference": {
                  "type": "string",
                  "example": "MAFR9399",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
                },
                "merchantAcquiringFacilityOperationalTerms": {
                  "type": "string",
                  "example": "Active",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "merchantAcquiringFacilityFeeConfiguration": {
                  "type": "string",
                  "example": "PenaltyRates",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Rate \n"
                },
                "taxReference": {
                  "type": "string",
                  "example": "TXRE3030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier \n"
                }
              }
            }
          }
        }
      },
      "delete": {
        "tags": [
          "terminate"
        ],
        "summary": "Termination of a merchant facility",
        "operationId": "terminateMerchantAcquiringFacilityFulfillmentArrangement",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Product Instance Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "204": {
            "description": "No Content"
          }
        }
      }
    },
    "/merchant-acquiring-facility/merchant-acquiring-facility-fulfillment-arrangement/{cr-reference-id}/facilityterms/{bq-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve Facility Terms attributes.",
        "operationId": "retrieveMerchantAcquiringFacilityFacilityTerms",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Product Instance Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Merchant Acquiring Facility Operational Terms Access Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "schema": {
              "type": "object",
              "properties": {
                "merchantAcquiringFacilityOperationalTermsAccessReference": {
                  "type": "string",
                  "example": "MATR7221",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
                },
                "productInstanceReference": {
                  "type": "string",
                  "example": "LPIR2030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "merchantAcquiringFacilityOperationalTerms": {
                  "type": "string",
                  "example": "Active",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text      \n"
                },
                "merchantAcquiringFacilityOperationalTermsAccessRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
                  "properties": {}
                }
              }
            }
          }
        }
      }
    },
    "/merchant-acquiring-facility/merchant-acquiring-facility-fulfillment-arrangement/{cr-reference-id}/accounts/{bq-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve Account BQ attributes.",
        "operationId": "retrieveMerchantAcquiringFacilityFulfillmentArrangementAccount",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Product Instance Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Merchant Acquiring Account Access Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "schema": {
              "type": "object",
              "properties": {
                "merchantAcquiringAccountAccessReference": {
                  "type": "string",
                  "example": "MAAR3398",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
                },
                "productInstanceReference": {
                  "type": "string",
                  "example": "LPIR2030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "merchantAcquiringFacilityAccountReference": {
                  "type": "string",
                  "example": "MAFR9399",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "merchantAcquiringAccountPostingPurpose": {
                  "type": "string",
                  "example": "Fees",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "merchantAcquiringAccountPostingAmount": {
                  "type": "string",
                  "example": "Credit",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount\n"
                },
                "merchantAcquiringAccountPostingValueDate": {
                  "type": "string",
                  "example": "09-07-2018",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Date      \n"
                },
                "merchantAcquiringAccountPostingResult": {
                  "type": "string",
                  "example": "Success",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text      \n"
                },
                "merchantAcquiringAccountAccessRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary  \n",
                  "properties": {}
                }
              }
            }
          }
        }
      }
    },
    "/merchant-acquiring-facility/merchant-acquiring-facility-fulfillment-arrangement/{cr-reference-id}/clearings/{bq-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve Clearing attributes.",
        "operationId": "retrieveMerchantAcquiringFacilityFulfillmentArrangementClearing",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Product Instance Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Merchant Acquiring Clearing Task Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "schema": {
              "type": "object",
              "properties": {
                "merchantAcquiringClearingTaskReference": {
                  "type": "string",
                  "example": "MACR3198",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
                },
                "productInstanceReference": {
                  "type": "string",
                  "example": "LPIR2030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionRecordReference": {
                  "type": "string",
                  "example": "CTRR9292",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionProductInstanceReference": {
                  "type": "string",
                  "example": "CTPI8390",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionNetworkReference": {
                  "type": "string",
                  "example": "CTNR3030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionIssuingBankReference": {
                  "type": "string",
                  "example": "CTIB3293",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionMerchantAcquiringBankReference": {
                  "type": "string",
                  "example": "CTMA0393",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionType": {
                  "type": "string",
                  "example": "Debit",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text             \n"
                },
                "cardTransactionCurrency": {
                  "type": "string",
                  "example": "USD",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "cardTransactionAmountType": {
                  "type": "string",
                  "example": "OriginalAmount",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "cardTransactionAmount": {
                  "type": "string",
                  "example": "$500",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount\n"
                },
                "cardTransactionMerchantReference": {
                  "type": "string",
                  "example": "CTMR3022",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionLocationReference": {
                  "type": "string",
                  "example": "CTLR4344",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionProductServiceReference": {
                  "type": "string",
                  "example": "CTSR2244",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionDateTime": {
                  "type": "string",
                  "example": "2018-12-07:T09:00:00",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
                },
                "cardTransactionFXConversionCharge": {
                  "type": "string",
                  "example": "$20",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount  \n"
                },
                "cardTransactionInterchargeFee": {
                  "type": "string",
                  "example": "$5",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount\n"
                },
                "cardTransactionAuthorizationRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary        \n",
                  "properties": {}
                },
                "merchantAcquiringClearingTaskRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
                  "properties": {}
                }
              }
            }
          }
        }
      }
    },
    "/merchant-acquiring-facility/merchant-acquiring-facility-fulfillment-arrangement/{cr-reference-id}/chargebacks/{bq-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve Chargeback attributes.",
        "operationId": "retrieveMerchantAcquiringFacilityFulfillmentArrangementChargeback",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Product Instance Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Merchant Acquiring Chargeback Task Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "schema": {
              "type": "object",
              "properties": {
                "merchantAcquiringChargebackTaskReference": {
                  "type": "string",
                  "example": "MACB2001",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
                },
                "productInstanceReference": {
                  "type": "string",
                  "example": "LPIR2030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "chargebackInstruction": {
                  "type": "string",
                  "example": "AmountDetailed",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text      \n"
                },
                "cardTransactionRecordReference": {
                  "type": "string",
                  "example": "CTRR9292",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionProductInstanceReference": {
                  "type": "string",
                  "example": "CTPI8390",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionNetworkReference": {
                  "type": "string",
                  "example": "CTNR3030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionIssuingBankReference": {
                  "type": "string",
                  "example": "CTIB3293",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionMerchantAcquiringBankReference": {
                  "type": "string",
                  "example": "CTMA0393",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionType": {
                  "type": "string",
                  "example": "Debit",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text             \n"
                },
                "cardTransactionCurrency": {
                  "type": "string",
                  "example": "USD",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "cardTransactionAmountType": {
                  "type": "string",
                  "example": "OriginalAmount",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "cardTransactionAmount": {
                  "type": "string",
                  "example": "$500",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount\n"
                },
                "cardTransactionMerchantReference": {
                  "type": "string",
                  "example": "CTMR3022",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionLocationReference": {
                  "type": "string",
                  "example": "CTLR4344",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionProductServiceReference": {
                  "type": "string",
                  "example": "CTSR2244",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardTransactionDateTime": {
                  "type": "string",
                  "example": "2018-12-07:T09:00:00",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
                },
                "cardTransactionFXConversionCharge": {
                  "type": "string",
                  "example": "$20",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount  \n"
                },
                "cardTransactionInterchargeFee": {
                  "type": "string",
                  "example": "$5",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount\n"
                },
                "cardTransactionAuthorizationRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary        \n",
                  "properties": {}
                },
                "merchantAcquiringChargebackTaskRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary  \n",
                  "properties": {}
                }
              }
            }
          }
        }
      }
    },
    "/merchant-acquiring-facility/merchant-acquiring-facility-fulfillment-arrangement/{cr-reference-id}/settlements/{bq-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve Settlement attributes.",
        "operationId": "retrieveMerchantAcquiringFacilityFulfillmentArrangementSettlement",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Product Instance Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Merchant Acquiring Settlement Task Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "schema": {
              "type": "object",
              "properties": {
                "merchantAcquiringSettlementTaskReference": {
                  "type": "string",
                  "example": "MASR3056",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
                },
                "productInstanceReference": {
                  "type": "string",
                  "example": "LPIR2030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "merchantAcquiringFacilityAccountReference": {
                  "type": "string",
                  "example": "MAFR9399",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "participantMerchantAcquirerBankReference": {
                  "type": "string",
                  "example": "PMAB3427",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "participantIssuerBankReference": {
                  "type": "string",
                  "example": "PIBR3218",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "cardFinancialSettlementServicePaymentAdviceRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary  \n",
                  "properties": {}
                },
                "participantPaymentTransaction": {
                  "type": "string",
                  "example": "Details",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "participantAcquirerBankSettlementAccountStatement": {
                  "type": "string",
                  "example": "Statement",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text      \n"
                },
                "merchantAcquiringSettlementTaskRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
                  "properties": {}
                }
              }
            }
          }
        }
      }
    },
    "/merchant-acquiring-facility/merchant-acquiring-facility-fulfillment-arrangement/{cr-reference-id}/fees/{bq-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve Fees attributes.",
        "operationId": "retrieveMerchantAcquiringFacilityFulfillmentArrangementFees",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Product Instance Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Merchant Acquiring Fee Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "schema": {
              "type": "object",
              "properties": {
                "merchantAcquiringFeeReference": {
                  "type": "string",
                  "example": "MAFE9321",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "productInstanceReference": {
                  "type": "string",
                  "example": "LPIR2030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "merchantAcquiringFeeConfiguration": {
                  "type": "string",
                  "example": "ApplicableFee",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "merchantAcquiringFeeType": {
                  "type": "string",
                  "example": "Monthy",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text  \n"
                },
                "merchantAcquiringFeeCharge": {
                  "type": "string",
                  "example": "$5",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount\n"
                },
                "merchantAcquiringDateTime": {
                  "type": "string",
                  "example": "2018-08-28T09:00:00",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
                },
                "merchantAcquiringFeeProjectionsCommitments": {
                  "type": "string",
                  "example": "Anticipated",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                }
              }
            }
          }
        }
      }
    },
    "/merchant-acquiring-facility/merchant-acquiring-facility-fulfillment-arrangement/{cr-reference-id}/reports/{bq-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve Reports attributes.",
        "operationId": "retrieveMerchantAcquiringFacilityFulfillmentArrangementReports",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Product Instance Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Statement Instance Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "OK",
            "schema": {
              "type": "object",
              "properties": {
                "productInstanceReference": {
                  "type": "string",
                  "example": "LPIR2030",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "statementInstanceReference": {
                  "type": "string",
                  "example": "SIRE9321",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
                },
                "statementType": {
                  "type": "string",
                  "example": "Balance",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "statementTransactionType": {
                  "type": "string",
                  "example": "Card",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "statementPeriod": {
                  "type": "string",
                  "example": "2018-07-01 To 2018-07-31",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Duration\n"
                },
                "transactionRecordReference": {
                  "type": "string",
                  "example": "TRRE3902",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "transactionType": {
                  "type": "string",
                  "example": "Debit",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "transactionPrincipleAmount": {
                  "type": "string",
                  "example": "$50",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount\n"
                },
                "transactionCounterparty": {
                  "type": "string",
                  "example": "Payee",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text  \n"
                },
                "transactionObligation": {
                  "type": "string",
                  "example": "PurchasedService",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
                },
                "transactionDateTime": {
                  "type": "string",
                  "example": "2018-08-28T09:00:00",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime      \n"
                },
                "statementInstanceRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
                  "properties": {}
                }
              }
            }
          }
        }
      }
    }
  },
  "definitions": {
    "MerchantAcquiring": {
      "type": "object",
      "properties": {
        "productServiceReference": {
          "type": "string",
          "example": "PSRE32429",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "customerReference": {
          "type": "string",
          "example": "CURE3242",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier             \n"
        },
        "partyReference": {
          "type": "string",
          "example": "PARE3002",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "bankBranchLocationReference": {
          "type": "string",
          "example": "BBLR4222",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
        },
        "accountCurrency": {
          "type": "string",
          "example": "USD",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "merchantAcquiringFacilityStatus": {
          "type": "string",
          "example": "Active",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "merchantAcquiringFacilityLimits": {
          "type": "string",
          "example": "SpendLimits",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount  \n"
        },
        "merchantAcquiringFacilityAccountReference": {
          "type": "string",
          "example": "MAFR9399",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
        },
        "merchantAcquiringFacilityOperationalTerms": {
          "type": "string",
          "example": "Active",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "merchantAcquiringFacilityFeeConfiguration": {
          "type": "string",
          "example": "PenaltyRates",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Rate \n"
        },
        "taxReference": {
          "type": "string",
          "example": "TXRE3030",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier   \n"
        }
      }
    },
    "MerchantAcquiringWithRoot": {
      "type": "object",
      "properties": {
        "productInstanceReference": {
          "type": "string",
          "example": "PIRE2030",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier \n"
        },
        "productServiceReference": {
          "type": "string",
          "example": "SERE32429",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "customerReference": {
          "type": "string",
          "example": "CURE3242",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier             \n"
        },
        "partyReference": {
          "type": "string",
          "example": "PARE3002",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "bankBranchLocationReference": {
          "type": "string",
          "example": "BBLR4222",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
        },
        "accountCurrency": {
          "type": "string",
          "example": "USD",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text \n"
        },
        "merchantAcquiringFacilityStatus": {
          "type": "string",
          "example": "Active",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "merchantAcquiringFacilityLimits": {
          "type": "string",
          "example": "SpendLimits",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount  \n"
        },
        "merchantAcquiringFacilityAccountReference": {
          "type": "string",
          "example": "MAFR9399",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
        },
        "merchantAcquiringFacilityOperationalTerms": {
          "type": "string",
          "example": "Active",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "merchantAcquiringFacilityFeeConfiguration": {
          "type": "string",
          "example": "PenaltyRates",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Rate \n"
        },
        "taxReference": {
          "type": "string",
          "example": "TXRE3030",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier \n"
        }
      }
    },
    "MerchantAcquiringRecordRequest": {
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
          "example": "2018-08-28T09:00:00",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime \n"
        },
        "empolyeeBusinessUnitReference": {
          "type": "string",
          "example": "EBUR6798",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier       \n"
        }
      }
    },
    "MerchantAcquiringRecordResponse": {
      "type": "object",
      "properties": {
        "recordingRecordReference": {
          "type": "string",
          "example": "RRR2030",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
        },
        "recordingRecordStatus": {
          "type": "string",
          "example": "Applied",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text      \n"
        }
      }
    },
    "FacilityTermsWithIdAndRoot": {
      "type": "object",
      "properties": {
        "merchantAcquiringFacilityOperationalTermsAccessReference": {
          "type": "string",
          "example": "MATR7221",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
        },
        "productInstanceReference": {
          "type": "string",
          "example": "LPIR2030",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "merchantAcquiringFacilityOperationalTerms": {
          "type": "string",
          "example": "Active",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text      \n"
        },
        "merchantAcquiringFacilityOperationalTermsAccessRecord": {
          "type": "object",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
          "properties": {}
        }
      }
    },
    "AccountWithIdAndRoot": {
      "type": "object",
      "properties": {
        "merchantAcquiringAccountAccessReference": {
          "type": "string",
          "example": "MAAR3398",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
        },
        "productInstanceReference": {
          "type": "string",
          "example": "LPIR2030",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "merchantAcquiringFacilityAccountReference": {
          "type": "string",
          "example": "MAFR9399",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "merchantAcquiringAccountPostingPurpose": {
          "type": "string",
          "example": "Fees",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "merchantAcquiringAccountPostingAmount": {
          "type": "string",
          "example": "Credit",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount\n"
        },
        "merchantAcquiringAccountPostingValueDate": {
          "type": "string",
          "example": "09-07-2018",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Date      \n"
        },
        "merchantAcquiringAccountPostingResult": {
          "type": "string",
          "example": "Success",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text      \n"
        },
        "merchantAcquiringAccountAccessRecord": {
          "type": "object",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary  \n",
          "properties": {}
        }
      }
    },
    "Clearing": {
      "type": "object",
      "properties": {
        "cardTransactionRecordReference": {
          "type": "string",
          "example": "CTRR9292",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "cardTransactionProductInstanceReference": {
          "type": "string",
          "example": "CTPI8390",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "cardTransactionNetworkReference": {
          "type": "string",
          "example": "CTNR3030",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "cardTransactionIssuingBankReference": {
          "type": "string",
          "example": "CTIB3293",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "cardTransactionMerchantAcquiringBankReference": {
          "type": "string",
          "example": "CTMA0393",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "cardTransactionType": {
          "type": "string",
          "example": "Debit",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text             \n"
        },
        "cardTransactionCurrency": {
          "type": "string",
          "example": "USD",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "cardTransactionAmountType": {
          "type": "string",
          "example": "OriginalAmount",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "cardTransactionAmount": {
          "type": "string",
          "example": "$500",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount\n"
        },
        "cardTransactionMerchantReference": {
          "type": "string",
          "example": "CTMR3022",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "cardTransactionLocationReference": {
          "type": "string",
          "example": "CTLR4344",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "cardTransactionProductServiceReference": {
          "type": "string",
          "example": "CTSR2244",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "cardTransactionDateTime": {
          "type": "string",
          "example": "2018-12-07:T09:00:00",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
        },
        "cardTransactionFXConversionCharge": {
          "type": "string",
          "example": "$20",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount  \n"
        },
        "cardTransactionInterchargeFee": {
          "type": "string",
          "example": "$5",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount\n"
        },
        "cardTransactionAuthorizationRecord": {
          "type": "object",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary        \n",
          "properties": {}
        },
        "merchantAcquiringClearingTaskRecord": {
          "type": "object",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary      \n",
          "properties": {}
        }
      }
    },
    "ClearingWithIdAndRoot": {
      "type": "object",
      "properties": {
        "merchantAcquiringClearingTaskReference": {
          "type": "string",
          "example": "MACR3198",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
        },
        "productInstanceReference": {
          "type": "string",
          "example": "LPIR2030",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "cardTransactionRecordReference": {
          "type": "string",
          "example": "CTRR9292",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "cardTransactionProductInstanceReference": {
          "type": "string",
          "example": "CTPI8390",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "cardTransactionNetworkReference": {
          "type": "string",
          "example": "CTNR3030",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "cardTransactionIssuingBankReference": {
          "type": "string",
          "example": "CTIB3293",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "cardTransactionMerchantAcquiringBankReference": {
          "type": "string",
          "example": "CTMA0393",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "cardTransactionType": {
          "type": "string",
          "example": "Debit",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text             \n"
        },
        "cardTransactionCurrency": {
          "type": "string",
          "example": "USD",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "cardTransactionAmountType": {
          "type": "string",
          "example": "OriginalAmount",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "cardTransactionAmount": {
          "type": "string",
          "example": "$500",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount\n"
        },
        "cardTransactionMerchantReference": {
          "type": "string",
          "example": "CTMR3022",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "cardTransactionLocationReference": {
          "type": "string",
          "example": "CTLR4344",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "cardTransactionProductServiceReference": {
          "type": "string",
          "example": "CTSR2244",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "cardTransactionDateTime": {
          "type": "string",
          "example": "2018-12-07:T09:00:00",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
        },
        "cardTransactionFXConversionCharge": {
          "type": "string",
          "example": "$20",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount  \n"
        },
        "cardTransactionInterchargeFee": {
          "type": "string",
          "example": "$5",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount\n"
        },
        "cardTransactionAuthorizationRecord": {
          "type": "object",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary        \n",
          "properties": {}
        },
        "merchantAcquiringClearingTaskRecord": {
          "type": "object",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
          "properties": {}
        }
      }
    },
    "Chargeback": {
      "type": "object",
      "properties": {
        "chargebackInstruction": {
          "type": "string",
          "example": "AmountDetailed",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text      \n"
        },
        "cardTransactionRecordReference": {
          "type": "string",
          "example": "CTRR9292",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "cardTransactionProductInstanceReference": {
          "type": "string",
          "example": "CTPI8390",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "cardTransactionNetworkReference": {
          "type": "string",
          "example": "CTNR3030",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "cardTransactionIssuingBankReference": {
          "type": "string",
          "example": "CTIB3293",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "cardTransactionMerchantAcquiringBankReference": {
          "type": "string",
          "example": "CTMA0393",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "cardTransactionType": {
          "type": "string",
          "example": "Debit",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text             \n"
        },
        "cardTransactionCurrency": {
          "type": "string",
          "example": "USD",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "cardTransactionAmountType": {
          "type": "string",
          "example": "OriginalAmount",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "cardTransactionAmount": {
          "type": "string",
          "example": "$500",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount\n"
        },
        "cardTransactionMerchantReference": {
          "type": "string",
          "example": "CTMR3022",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "cardTransactionLocationReference": {
          "type": "string",
          "example": "CTLR4344",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "cardTransactionProductServiceReference": {
          "type": "string",
          "example": "CTSR2244",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "cardTransactionDateTime": {
          "type": "string",
          "example": "2018-12-07:T09:00:00",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
        },
        "cardTransactionFXConversionCharge": {
          "type": "string",
          "example": "$20",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount  \n"
        },
        "cardTransactionInterchargeFee": {
          "type": "string",
          "example": "$5",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount\n"
        },
        "cardTransactionAuthorizationRecord": {
          "type": "object",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary        \n",
          "properties": {}
        },
        "merchantAcquiringChargebackTaskRecord": {
          "type": "object",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
          "properties": {}
        }
      }
    },
    "ChargebackWithIdAndRoot": {
      "type": "object",
      "properties": {
        "merchantAcquiringChargebackTaskReference": {
          "type": "string",
          "example": "MACB2001",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
        },
        "productInstanceReference": {
          "type": "string",
          "example": "LPIR2030",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "chargebackInstruction": {
          "type": "string",
          "example": "AmountDetailed",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text      \n"
        },
        "cardTransactionRecordReference": {
          "type": "string",
          "example": "CTRR9292",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "cardTransactionProductInstanceReference": {
          "type": "string",
          "example": "CTPI8390",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "cardTransactionNetworkReference": {
          "type": "string",
          "example": "CTNR3030",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "cardTransactionIssuingBankReference": {
          "type": "string",
          "example": "CTIB3293",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "cardTransactionMerchantAcquiringBankReference": {
          "type": "string",
          "example": "CTMA0393",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "cardTransactionType": {
          "type": "string",
          "example": "Debit",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text             \n"
        },
        "cardTransactionCurrency": {
          "type": "string",
          "example": "USD",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "cardTransactionAmountType": {
          "type": "string",
          "example": "OriginalAmount",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "cardTransactionAmount": {
          "type": "string",
          "example": "$500",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount\n"
        },
        "cardTransactionMerchantReference": {
          "type": "string",
          "example": "CTMR3022",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "cardTransactionLocationReference": {
          "type": "string",
          "example": "CTLR4344",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "cardTransactionProductServiceReference": {
          "type": "string",
          "example": "CTSR2244",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "cardTransactionDateTime": {
          "type": "string",
          "example": "2018-12-07:T09:00:00",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
        },
        "cardTransactionFXConversionCharge": {
          "type": "string",
          "example": "$20",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount  \n"
        },
        "cardTransactionInterchargeFee": {
          "type": "string",
          "example": "$5",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount\n"
        },
        "cardTransactionAuthorizationRecord": {
          "type": "object",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary        \n",
          "properties": {}
        },
        "merchantAcquiringChargebackTaskRecord": {
          "type": "object",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary  \n",
          "properties": {}
        }
      }
    },
    "Settlement": {
      "type": "object",
      "properties": {
        "merchantAcquiringFacilityAccountReference": {
          "type": "string",
          "example": "MAFR9399",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "participantMerchantAcquirerBankReference": {
          "type": "string",
          "example": "PMAB3427",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "participantIssuerBankReference": {
          "type": "string",
          "example": "PIBR3218",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "cardFinancialSettlementServicePaymentAdviceRecord": {
          "type": "object",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary  \n",
          "properties": {}
        },
        "participantPaymentTransaction": {
          "type": "string",
          "example": "Details",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "participantAcquirerBankSettlementAccountStatement": {
          "type": "string",
          "example": "Statement",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text      \n"
        },
        "merchantAcquiringSettlementTaskRecord": {
          "type": "object",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
          "properties": {}
        }
      }
    },
    "SettlementWithIdAndRoot": {
      "type": "object",
      "properties": {
        "merchantAcquiringSettlementTaskReference": {
          "type": "string",
          "example": "MASR3056",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier  \n"
        },
        "productInstanceReference": {
          "type": "string",
          "example": "LPIR2030",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "merchantAcquiringFacilityAccountReference": {
          "type": "string",
          "example": "MAFR9399",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "participantMerchantAcquirerBankReference": {
          "type": "string",
          "example": "PMAB3427",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "participantIssuerBankReference": {
          "type": "string",
          "example": "PIBR3218",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "cardFinancialSettlementServicePaymentAdviceRecord": {
          "type": "object",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary  \n",
          "properties": {}
        },
        "participantPaymentTransaction": {
          "type": "string",
          "example": "Details",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "participantAcquirerBankSettlementAccountStatement": {
          "type": "string",
          "example": "Statement",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text      \n"
        },
        "merchantAcquiringSettlementTaskRecord": {
          "type": "object",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
          "properties": {}
        }
      }
    },
    "FeesWithIdAndRoot": {
      "type": "object",
      "properties": {
        "merchantAcquiringFeeReference": {
          "type": "string",
          "example": "MAFE9321",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "productInstanceReference": {
          "type": "string",
          "example": "LPIR2030",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "merchantAcquiringFeeConfiguration": {
          "type": "string",
          "example": "ApplicableFee",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "merchantAcquiringFeeType": {
          "type": "string",
          "example": "Monthy",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text  \n"
        },
        "merchantAcquiringFeeCharge": {
          "type": "string",
          "example": "$5",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount\n"
        },
        "merchantAcquiringDateTime": {
          "type": "string",
          "example": "2018-08-28T09:00:00",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
        },
        "merchantAcquiringFeeProjectionsCommitments": {
          "type": "string",
          "example": "Anticipated",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        }
      }
    },
    "ReportsWithIdAndRoot": {
      "type": "object",
      "properties": {
        "productInstanceReference": {
          "type": "string",
          "example": "LPIR2030",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "statementInstanceReference": {
          "type": "string",
          "example": "SIRE9321",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier      \n"
        },
        "statementType": {
          "type": "string",
          "example": "Balance",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "statementTransactionType": {
          "type": "string",
          "example": "Card",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "statementPeriod": {
          "type": "string",
          "example": "2018-07-01 To 2018-07-31",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Duration\n"
        },
        "transactionRecordReference": {
          "type": "string",
          "example": "TRRE3902",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "transactionType": {
          "type": "string",
          "example": "Debit",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "transactionPrincipleAmount": {
          "type": "string",
          "example": "$50",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Amount\n"
        },
        "transactionCounterparty": {
          "type": "string",
          "example": "Payee",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text  \n"
        },
        "transactionObligation": {
          "type": "string",
          "example": "PurchasedService",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text    \n"
        },
        "transactionDateTime": {
          "type": "string",
          "example": "2018-08-28T09:00:00",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime      \n"
        },
        "statementInstanceRecord": {
          "type": "object",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
          "properties": {}
        }
      }
    }
  }
}
</script>