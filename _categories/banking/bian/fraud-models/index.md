---
layout: api-single
title: Fraud Models
parent-title: BIAN APIs
description: Banking API Standards - APIs - Fraud Models
keywords: 
duration: 
type: api
standard: bian
order: 4
parent: /categories/banking/bian
api-logo: /dist/images/logos/bian_logo.svg
api-summary: This service domain develops and maintains a portfolio of fraud detection models. It support the use of these models in different production contexts and refines the models in response to new and changing exposures
api-example-use: Financial engineers develop and refine a portfolio of fraud scanner and detection models for deployment across the bank
api-published-by: Bianuser06 Team
---
<script id="api-spec" type="application/json">
{
  "swagger": "2.0",
  "info": {
    "version": "1.0.1",
    "title": "Fraud Models",
    "description": "This service domain develops and maintains a portfolio of fraud detection models"
  },
  "host": "bianorg.azure-api.net",
  "basePath": "/sd-fraud-models/v1",
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
    "/fraud-models/fraud-model-specification/{cr-reference-id}/designs/{bq-reference-id}/updation": {
      "put": {
        "tags": [
          "update"
        ],
        "summary": "Request for updates to an existing fraud model",
        "description": "Update  Request updates/amendments to an existing fraud model,",
        "operationId": "updateFraudModelSpecificationDesign",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Fraud Model Model Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Fraud Model Model Design Task Reference",
            "required": true,
            "type": "string"
          },
          {
            "in": "body",
            "name": "body",
            "description": "Design Request Payload",
            "required": true,
            "schema": {
              "type": "object",
              "properties": {
                "fraudModelModel": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: this is the executable model specificaion\n"
                },
                "fraudModelModelDesignTaskRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n general-info: details/tracking the design activity\n",
                  "properties": {}
                },
                "customerMarketDataServiceReference": {
                  "type": "string",
                  "example": "CDSR715154",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: service providers of example market research and production data\n"
                },
                "customerMarketDataReference": {
                  "type": "string",
                  "example": "CDR790746",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: example market research/production data file\n"
                },
                "productServiceActivityReportReference": {
                  "type": "string",
                  "example": "PARR721644",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: internal bank activity report - used for development \n"
                },
                "productServiceActivityReport": {
                  "type": "object",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n general-info: data file/report of production activity\n",
                  "properties": {}
                },
                "fraudModelModelType": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Fraud Model Model Type\n"
                },
                "fraudModelModelUsage": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: records number of production deployments and frequency of execution\n"
                },
                "fraudModelModelImpact": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: reported impact/accuracy of model\n"
                },
                "fraudModelModelFeedbackRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n general-info: user provided feedback/suggestions\n",
                  "properties": {}
                },
                "fraudModelModelSpecification": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: design - inputs, calculations, outputs \n"
                },
                "fraudModelModelOperationalRequirements": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: defines operational and technical requirements\n"
                },
                "fraudModelModelAllowedUsage": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: defines when/where model can be used\n"
                },
                "fraudModelModelUsageGuidelines": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: guidance on usage and result interpretation\n"
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
                "fraudModelModelReference": {
                  "type": "string",
                  "example": "FMMR773227",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: this is the master reference\n"
                },
                "fraudModelModel": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: this is the executable model specificaion\n"
                },
                "fraudModelModelDesignTaskReference": {
                  "type": "string",
                  "example": "FMMDTR756034",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: reference to design activity\n"
                },
                "fraudModelModelDesignTaskRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n general-info: details/tracking the design activity\n",
                  "properties": {}
                },
                "customerMarketDataServiceReference": {
                  "type": "string",
                  "example": "CDSR715154",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: service providers of example market research and production data\n"
                },
                "customerMarketDataReference": {
                  "type": "string",
                  "example": "CDR790746",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: example market research/production data file\n"
                },
                "productServiceActivityReportReference": {
                  "type": "string",
                  "example": "PARR721644",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: internal bank activity report - used for development \n"
                },
                "productServiceActivityReport": {
                  "type": "object",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n general-info: data file/report of production activity\n",
                  "properties": {}
                },
                "fraudModelModelType": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Fraud Model Model Type\n"
                },
                "fraudModelModelUsage": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: records number of production deployments and frequency of execution\n"
                },
                "fraudModelModelImpact": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: reported impact/accuracy of model\n"
                },
                "fraudModelModelFeedbackRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n general-info: user provided feedback/suggestions\n",
                  "properties": {}
                },
                "fraudModelModelSpecification": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: design - inputs, calculations, outputs \n"
                },
                "fraudModelModelOperationalRequirements": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: defines operational and technical requirements\n"
                },
                "fraudModelModelAllowedUsage": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: defines when/where model can be used\n"
                },
                "fraudModelModelUsageGuidelines": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: guidance on usage and result interpretation\n"
                }
              }
            }
          }
        }
      }
    },
    "/fraud-models/fraud-model-specification/{cr-reference-id}/recording": {
      "post": {
        "tags": [
          "record"
        ],
        "summary": "Record feedback about the use/performance of a fraud model",
        "description": "To record use/activity and results for a fraud model,",
        "operationId": "recordFraudModelSpecificationRecord",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Fraud Model Model Reference",
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
                  "example": "RRR4678",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "recordingRecordStatus": {
                  "type": "string",
                  "example": "active",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                }
              }
            }
          }
        }
      }
    },
    "/fraud-models/fraud-model-specification/{cr-reference-id}/deployments/{bq-reference-id}/requisition": {
      "put": {
        "tags": [
          "request"
        ],
        "summary": "Request access to a fraud model algorithm/specification",
        "description": "Request  Request access to a fraud model specification (for use),",
        "operationId": "requestFraudModelSpecificationDeploymentUpdate",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Fraud Model Model Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Fraud Model Model Deployment Task Reference",
            "required": true,
            "type": "string"
          },
          {
            "in": "body",
            "name": "body",
            "description": "Deployment  request payload",
            "required": true,
            "schema": {
              "type": "object",
              "properties": {
                "fraudModelModel": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: this is the executable model specificaion\n"
                },
                "fraudModelModelDeploymentTaskRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n general-info: details/tracking the deployment activity\n",
                  "properties": {}
                },
                "employeeBusinessUnitReference": {
                  "type": "string",
                  "example": "ER769585",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: the unit requesting the deployment\n"
                },
                "fraudModelModelVersion": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Fraud Model Model Version\n"
                },
                "fraudModelModelDeploymentStatus": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: tracks completion of deployment actions\n"
                },
                "fraudModelModelUsage": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: records number of production deployments\n"
                },
                "fraudModelModelDeploymentTaskResult": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Fraud Model Model Deployment Task Result\n"
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
                "fraudModelModelReference": {
                  "type": "string",
                  "example": "FMMR773227",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: this is the master reference\n"
                },
                "fraudModelModel": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: this is the executable model specificaion\n"
                },
                "fraudModelModelDeploymentTaskReference": {
                  "type": "string",
                  "example": "FMMDTR756034",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: reference to deployment task\n"
                },
                "fraudModelModelDeploymentTaskRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n general-info: details/tracking the deployment activity\n",
                  "properties": {}
                },
                "employeeBusinessUnitReference": {
                  "type": "string",
                  "example": "ER769585",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: the unit requesting the deployment\n"
                },
                "fraudModelModelVersion": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Fraud Model Model Version\n"
                },
                "fraudModelModelDeploymentStatus": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: tracks completion of deployment actions\n"
                },
                "fraudModelModelUsage": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: records number of production deployments\n"
                },
                "fraudModelModelDeploymentTaskResult": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Fraud Model Model Deployment Task Result\n"
                }
              }
            }
          }
        }
      }
    },
    "/fraud-models/fraud-model-specification/{cr-reference-id}/deployments/requisition": {
      "post": {
        "tags": [
          "request"
        ],
        "summary": "Request access to a fraud model algorithm/specification",
        "description": "Request  Request access to a fraud model specification (for use),",
        "operationId": "requestFraudModelSpecificationDeploymentCreate",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Fraud Model Model Reference",
            "required": true,
            "type": "string"
          },
          {
            "in": "body",
            "name": "body",
            "description": "Deployment  Request Payload",
            "required": true,
            "schema": {
              "type": "object",
              "properties": {
                "fraudModelModel": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: this is the executable model specificaion\n"
                },
                "fraudModelModelDeploymentTaskRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n general-info: details/tracking the deployment activity\n",
                  "properties": {}
                },
                "employeeBusinessUnitReference": {
                  "type": "string",
                  "example": "ER769585",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: the unit requesting the deployment\n"
                },
                "fraudModelModelVersion": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Fraud Model Model Version\n"
                },
                "fraudModelModelDeploymentStatus": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: tracks completion of deployment actions\n"
                },
                "fraudModelModelUsage": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: records number of production deployments\n"
                },
                "fraudModelModelDeploymentTaskResult": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Fraud Model Model Deployment Task Result\n"
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
                "fraudModelModelReference": {
                  "type": "string",
                  "example": "FMMR773227",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: this is the master reference\n"
                },
                "fraudModelModel": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: this is the executable model specificaion\n"
                },
                "fraudModelModelDeploymentTaskReference": {
                  "type": "string",
                  "example": "FMMDTR756034",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: reference to deployment task\n"
                },
                "fraudModelModelDeploymentTaskRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n general-info: details/tracking the deployment activity\n",
                  "properties": {}
                },
                "employeeBusinessUnitReference": {
                  "type": "string",
                  "example": "ER769585",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: the unit requesting the deployment\n"
                },
                "fraudModelModelVersion": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Fraud Model Model Version\n"
                },
                "fraudModelModelDeploymentStatus": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: tracks completion of deployment actions\n"
                },
                "fraudModelModelUsage": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: records number of production deployments\n"
                },
                "fraudModelModelDeploymentTaskResult": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Fraud Model Model Deployment Task Result\n"
                }
              }
            }
          }
        }
      }
    },
    "/fraud-models/fraud-model-specification": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve CR Ids",
        "operationId": "RetrieveFraudModelsReferenceIds",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "collection-filter",
            "in": "query",
            "description": "Filter to refine the result set. ex- fraudModelModelStatus =  suspended",
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
                "ID726464",
                "ID7264642"
              ]
            }
          }
        }
      }
    },
    "/fraud-models/fraud-model-specification/behavior-qualifiers/": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve BQ names",
        "operationId": "RetrieveFraudModelsBehaviorQualifiers",
        "produces": [
          "application/json"
        ],
        "parameters": [],
        "responses": {
          "200": {
            "description": "OK",
            "schema": {
              "type": "array",
              "items": {
                "type": "string"
              },
              "example": [
                "Design",
                "Testing",
                "Compliance",
                "Implementation",
                "Deployment"
              ]
            }
          }
        }
      }
    },
    "/fraud-models/fraud-model-specification/{cr-reference-id}/{behavior-qualifier}/": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve Behavior Qualifier Reference Ids",
        "operationId": "RetrieveFraudModelsBehaviorQualifierReferenceIds",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Fraud Model Model Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "behavior-qualifier",
            "in": "path",
            "description": "Behavior Qualifier Name. ex- design",
            "required": true,
            "type": "string"
          },
          {
            "name": "collection-filter",
            "in": "query",
            "description": "Filter to refine the result set. ex- fraudModelModelType = TYPE1",
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
                "BQID1",
                "BQID2"
              ]
            }
          }
        }
      }
    },
    "/fraud-models/fraud-model-specification/{cr-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve a Fraud Models Record",
        "description": "Retrieve a Fraud Models Record",
        "operationId": "retrieveFraudModels",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Fraud Model Model Reference",
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
                "fraudModelPortfolioRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n general-info: record of all models usage and performance statistics\n",
                  "properties": {}
                },
                "fraudModelModelReference": {
                  "type": "string",
                  "example": "FMR772612",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: this is the master reference\n"
                },
                "fraudModelModelType": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Fraud Model Model Type\n"
                },
                "fraudModelModelPurpose": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: defines fraud detection/analysis/insights provided\n"
                },
                "fraudModelModelStatus": {
                  "type": "string",
                  "example": "suspended",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: e.g. under development, in-force, suspended\n"
                },
                "fraudModelModelUsage": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: records number of production deployments and frequency of execution\n"
                },
                "fraudModelModelImpact": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: records impact/accuracy of model insights\n"
                },
                "fraudModelModelBudget": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: records time/effort on design/development by version/date\n"
                },
                "fraudModelModelVersion": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: release version of available model\n"
                },
                "fraudModelModel": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: this is the executable model specificaion\n"
                }
              }
            }
          }
        }
      }
    },
    "/fraud-models/fraud-model-specification/{cr-reference-id}/designs/{bq-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve a Fraud Models Design Record",
        "description": "Retrieve a Fraud Models Design Record",
        "operationId": "retrieveFraudModelsDesign",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Fraud Model Model Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Fraud Model Model Design Task Reference",
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
                "fraudModelModelReference": {
                  "type": "string",
                  "example": "FMMR773227",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: this is the master reference\n"
                },
                "fraudModelModel": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: this is the executable model specificaion\n"
                },
                "fraudModelModelDesignTaskReference": {
                  "type": "string",
                  "example": "FMMDTR756034",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: reference to design activity\n"
                },
                "fraudModelModelDesignTaskRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n general-info: details/tracking the design activity\n",
                  "properties": {}
                },
                "customerMarketDataServiceReference": {
                  "type": "string",
                  "example": "CDSR715154",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: service providers of example market research and production data\n"
                },
                "customerMarketDataReference": {
                  "type": "string",
                  "example": "CDR790746",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: example market research/production data file\n"
                },
                "productServiceActivityReportReference": {
                  "type": "string",
                  "example": "PARR721644",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: internal bank activity report - used for development \n"
                },
                "productServiceActivityReport": {
                  "type": "object",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n general-info: data file/report of production activity\n",
                  "properties": {}
                },
                "fraudModelModelType": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Fraud Model Model Type\n"
                },
                "fraudModelModelUsage": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: records number of production deployments and frequency of execution\n"
                },
                "fraudModelModelImpact": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: reported impact/accuracy of model\n"
                },
                "fraudModelModelFeedbackRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n general-info: user provided feedback/suggestions\n",
                  "properties": {}
                },
                "fraudModelModelSpecification": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: design - inputs, calculations, outputs \n"
                },
                "fraudModelModelOperationalRequirements": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: defines operational and technical requirements\n"
                },
                "fraudModelModelAllowedUsage": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: defines when/where model can be used\n"
                },
                "fraudModelModelUsageGuidelines": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: guidance on usage and result interpretation\n"
                }
              }
            }
          }
        }
      }
    },
    "/fraud-models/fraud-model-specification/{cr-reference-id}/testings/{bq-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve a Fraud Models Testing Record",
        "description": "Retrieve a Fraud Models Testing Record",
        "operationId": "retrieveFraudModelsTesting",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Fraud Model Model Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Fraud Model Model Testing Task Reference",
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
                "fraudModelModelReference": {
                  "type": "string",
                  "example": "FMMR773227",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: this is the master reference\n"
                },
                "fraudModelModel": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: this is the executable model specificaion\n"
                },
                "fraudModelModelTestingTaskReference": {
                  "type": "string",
                  "example": "FMMTTR725964",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: reference to testing activity\n"
                },
                "fraudModelModelTestingTaskRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n general-info: details/tracking the testing activity\n",
                  "properties": {}
                },
                "fraudModelModelType": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Fraud Model Model Type\n"
                },
                "fraudModelModelTestReference": {
                  "type": "string",
                  "example": "FMMTR747177",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: Fraud Model Model Test Reference\n"
                },
                "fraudModelModelTestType": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: unit, integration, load, acceptance etc.\n"
                },
                "fraudModelModelTestHarnessReference": {
                  "type": "string",
                  "example": "FMMTHR728981",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: testing environment\n"
                },
                "fraudModelModelTestResult": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: errors result in further design/implementation\n"
                }
              }
            }
          }
        }
      }
    },
    "/fraud-models/fraud-model-specification/{cr-reference-id}/compliances/{bq-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve a Fraud Models Compliance Record",
        "description": "Retrieve a Fraud Models Compliance Record",
        "operationId": "retrieveFraudModelsCompliance",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Fraud Model Model Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Fraud Model Model Compliance Task Reference",
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
                "fraudModelModelReference": {
                  "type": "string",
                  "example": "FMMR773227",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: this is the master reference\n"
                },
                "fraudModelModel": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: this is the executable model specificaion\n"
                },
                "fraudModelModelComplianceTaskReference": {
                  "type": "string",
                  "example": "FMMCTR715433",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: reference to compliance checking activity\n"
                },
                "fraudModelModelComplianceTaskRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n general-info: details/tracking the compliance checking activity\n",
                  "properties": {}
                },
                "fraudModelModelType": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Fraud Model Model Type\n"
                },
                "complianceTestReference": {
                  "type": "string",
                  "example": "FMMCTR715433",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: Compliance Test Reference\n"
                },
                "complianceTestType": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Compliance Test Type\n"
                },
                "complianceTestResult": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: failure results in further design/development\n"
                }
              }
            }
          }
        }
      }
    },
    "/fraud-models/fraud-model-specification/{cr-reference-id}/implementations/{bq-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve a Fraud Models Implementation Record",
        "description": "Retrieve a Fraud Models Implementation Record",
        "operationId": "retrieveFraudModelsImplementation",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Fraud Model Model Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Fraud Model Model Implementation Task Reference",
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
                "fraudModelModelReference": {
                  "type": "string",
                  "example": "FMMR773227",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: this is the master reference\n"
                },
                "fraudModelModel": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: this is the executable model specificaion\n"
                },
                "fraudModelModelImplementationTaskReference": {
                  "type": "string",
                  "example": "FMMITR768246",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: reference to implementation activity\n"
                },
                "fraudModelModelImplementationTaskRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n general-info: details/tracking the implementation activity\n",
                  "properties": {}
                },
                "fraudModelModelType": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Fraud Model Model Type\n"
                },
                "fraudModelModelDevelopmentTaskReference": {
                  "type": "string",
                  "example": "FMMDTR756034",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: Fraud Model Model Development Task Reference\n"
                },
                "fraudModelModelDevelopmentTaskDescription": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Fraud Model Model Development Task Description\n"
                },
                "fraudModelModelDevelopmentTaskBudget": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: time/effort planned/actual\n"
                },
                "fraudModelModelDevelopmentTaskOrganization": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Fraud Model Model Development Task Organization\n"
                },
                "fraudModelModelDevelopmentTaskStatus": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Fraud Model Model Development Task Status\n"
                },
                "fraudModelModelDevelopmentTaskDeliverable": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Fraud Model Model Development Task Deliverable\n"
                },
                "fraudModelModelStatus": {
                  "type": "string",
                  "example": "suspended",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: e.g. under development, in-force, suspended\n"
                }
              }
            }
          }
        }
      }
    },
    "/fraud-models/fraud-model-specification/{cr-reference-id}/deployments/{bq-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve a Fraud Models Deployment Record",
        "description": "Retrieve a Fraud Models Deployment Record",
        "operationId": "retrieveFraudModelsDeployment",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Fraud Model Model Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Fraud Model Model Deployment Task Reference",
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
                "fraudModelModelReference": {
                  "type": "string",
                  "example": "FMMR773227",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: this is the master reference\n"
                },
                "fraudModelModel": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: this is the executable model specificaion\n"
                },
                "fraudModelModelDeploymentTaskReference": {
                  "type": "string",
                  "example": "FMMDTR756034",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: reference to deployment task\n"
                },
                "fraudModelModelDeploymentTaskRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n general-info: details/tracking the deployment activity\n",
                  "properties": {}
                },
                "employeeBusinessUnitReference": {
                  "type": "string",
                  "example": "ER769585",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: the unit requesting the deployment\n"
                },
                "fraudModelModelVersion": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Fraud Model Model Version\n"
                },
                "fraudModelModelDeploymentStatus": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: tracks completion of deployment actions\n"
                },
                "fraudModelModelUsage": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: records number of production deployments\n"
                },
                "fraudModelModelDeploymentTaskResult": {
                  "type": "string",
                  "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Fraud Model Model Deployment Task Result\n"
                }
              }
            }
          }
        }
      }
    }
  },
  "definitions": {
    "FraudModelsModelWithIdAndRoot": {
      "type": "object",
      "properties": {
        "fraudModelPortfolioRecord": {
          "type": "object",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n general-info: record of all models usage and performance statistics\n",
          "properties": {}
        },
        "fraudModelModelReference": {
          "type": "string",
          "example": "FMR772612",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: this is the master reference\n"
        },
        "fraudModelModelType": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Fraud Model Model Type\n"
        },
        "fraudModelModelPurpose": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: defines fraud detection/analysis/insights provided\n"
        },
        "fraudModelModelStatus": {
          "type": "string",
          "example": "suspended",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: e.g. under development, in-force, suspended\n"
        },
        "fraudModelModelUsage": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: records number of production deployments and frequency of execution\n"
        },
        "fraudModelModelImpact": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: records impact/accuracy of model insights\n"
        },
        "fraudModelModelBudget": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: records time/effort on design/development by version/date\n"
        },
        "fraudModelModelVersion": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: release version of available model\n"
        },
        "fraudModelModel": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: this is the executable model specificaion\n"
        }
      }
    },
    "FraudModelsDesignWithIdAndRoot": {
      "type": "object",
      "properties": {
        "fraudModelModelReference": {
          "type": "string",
          "example": "FMMR773227",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: this is the master reference\n"
        },
        "fraudModelModel": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: this is the executable model specificaion\n"
        },
        "fraudModelModelDesignTaskReference": {
          "type": "string",
          "example": "FMMDTR756034",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: reference to design activity\n"
        },
        "fraudModelModelDesignTaskRecord": {
          "type": "object",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n general-info: details/tracking the design activity\n",
          "properties": {}
        },
        "customerMarketDataServiceReference": {
          "type": "string",
          "example": "CDSR715154",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: service providers of example market research and production data\n"
        },
        "customerMarketDataReference": {
          "type": "string",
          "example": "CDR790746",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: example market research/production data file\n"
        },
        "productServiceActivityReportReference": {
          "type": "string",
          "example": "PARR721644",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: internal bank activity report - used for development \n"
        },
        "productServiceActivityReport": {
          "type": "object",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n general-info: data file/report of production activity\n",
          "properties": {}
        },
        "fraudModelModelType": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Fraud Model Model Type\n"
        },
        "fraudModelModelUsage": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: records number of production deployments and frequency of execution\n"
        },
        "fraudModelModelImpact": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: reported impact/accuracy of model\n"
        },
        "fraudModelModelFeedbackRecord": {
          "type": "object",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n general-info: user provided feedback/suggestions\n",
          "properties": {}
        },
        "fraudModelModelSpecification": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: design - inputs, calculations, outputs \n"
        },
        "fraudModelModelOperationalRequirements": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: defines operational and technical requirements\n"
        },
        "fraudModelModelAllowedUsage": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: defines when/where model can be used\n"
        },
        "fraudModelModelUsageGuidelines": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: guidance on usage and result interpretation\n"
        }
      }
    },
    "FraudModelsTestingWithIdAndRoot": {
      "type": "object",
      "properties": {
        "fraudModelModelReference": {
          "type": "string",
          "example": "FMMR773227",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: this is the master reference\n"
        },
        "fraudModelModel": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: this is the executable model specificaion\n"
        },
        "fraudModelModelTestingTaskReference": {
          "type": "string",
          "example": "FMMTTR725964",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: reference to testing activity\n"
        },
        "fraudModelModelTestingTaskRecord": {
          "type": "object",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n general-info: details/tracking the testing activity\n",
          "properties": {}
        },
        "fraudModelModelType": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Fraud Model Model Type\n"
        },
        "fraudModelModelTestReference": {
          "type": "string",
          "example": "FMMTR747177",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: Fraud Model Model Test Reference\n"
        },
        "fraudModelModelTestType": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: unit, integration, load, acceptance etc.\n"
        },
        "fraudModelModelTestHarnessReference": {
          "type": "string",
          "example": "FMMTHR728981",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: testing environment\n"
        },
        "fraudModelModelTestResult": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: errors result in further design/implementation\n"
        }
      }
    },
    "FraudModelsComplianceWithIdAndRoot": {
      "type": "object",
      "properties": {
        "fraudModelModelReference": {
          "type": "string",
          "example": "FMMR773227",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: this is the master reference\n"
        },
        "fraudModelModel": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: this is the executable model specificaion\n"
        },
        "fraudModelModelComplianceTaskReference": {
          "type": "string",
          "example": "FMMCTR715433",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: reference to compliance checking activity\n"
        },
        "fraudModelModelComplianceTaskRecord": {
          "type": "object",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n general-info: details/tracking the compliance checking activity\n",
          "properties": {}
        },
        "fraudModelModelType": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Fraud Model Model Type\n"
        },
        "complianceTestReference": {
          "type": "string",
          "example": "FMMCTR715433",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: Compliance Test Reference\n"
        },
        "complianceTestType": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Compliance Test Type\n"
        },
        "complianceTestResult": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: failure results in further design/development\n"
        }
      }
    },
    "FraudModelsImplementationWithIdAndRoot": {
      "type": "object",
      "properties": {
        "fraudModelModelReference": {
          "type": "string",
          "example": "FMMR773227",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: this is the master reference\n"
        },
        "fraudModelModel": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: this is the executable model specificaion\n"
        },
        "fraudModelModelImplementationTaskReference": {
          "type": "string",
          "example": "FMMITR768246",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: reference to implementation activity\n"
        },
        "fraudModelModelImplementationTaskRecord": {
          "type": "object",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n general-info: details/tracking the implementation activity\n",
          "properties": {}
        },
        "fraudModelModelType": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Fraud Model Model Type\n"
        },
        "fraudModelModelDevelopmentTaskReference": {
          "type": "string",
          "example": "FMMDTR756034",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: Fraud Model Model Development Task Reference\n"
        },
        "fraudModelModelDevelopmentTaskDescription": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Fraud Model Model Development Task Description\n"
        },
        "fraudModelModelDevelopmentTaskBudget": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: time/effort planned/actual\n"
        },
        "fraudModelModelDevelopmentTaskOrganization": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Fraud Model Model Development Task Organization\n"
        },
        "fraudModelModelDevelopmentTaskStatus": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Fraud Model Model Development Task Status\n"
        },
        "fraudModelModelDevelopmentTaskDeliverable": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Fraud Model Model Development Task Deliverable\n"
        },
        "fraudModelModelStatus": {
          "type": "string",
          "example": "suspended",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: e.g. under development, in-force, suspended\n"
        }
      }
    },
    "FraudModelsDeploymentWithIdAndRoot": {
      "type": "object",
      "properties": {
        "fraudModelModelReference": {
          "type": "string",
          "example": "FMMR773227",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: this is the master reference\n"
        },
        "fraudModelModel": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: this is the executable model specificaion\n"
        },
        "fraudModelModelDeploymentTaskReference": {
          "type": "string",
          "example": "FMMDTR756034",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: reference to deployment task\n"
        },
        "fraudModelModelDeploymentTaskRecord": {
          "type": "object",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n general-info: details/tracking the deployment activity\n",
          "properties": {}
        },
        "employeeBusinessUnitReference": {
          "type": "string",
          "example": "ER769585",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: the unit requesting the deployment\n"
        },
        "fraudModelModelVersion": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Fraud Model Model Version\n"
        },
        "fraudModelModelDeploymentStatus": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: tracks completion of deployment actions\n"
        },
        "fraudModelModelUsage": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: records number of production deployments\n"
        },
        "fraudModelModelDeploymentTaskResult": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Fraud Model Model Deployment Task Result\n"
        }
      }
    },
    "FraudModelsDesignBase": {
      "type": "object",
      "properties": {
        "fraudModelModel": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: this is the executable model specificaion\n"
        },
        "fraudModelModelDesignTaskRecord": {
          "type": "object",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n general-info: details/tracking the design activity\n",
          "properties": {}
        },
        "customerMarketDataServiceReference": {
          "type": "string",
          "example": "CDSR715154",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: service providers of example market research and production data\n"
        },
        "customerMarketDataReference": {
          "type": "string",
          "example": "CDR790746",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: example market research/production data file\n"
        },
        "productServiceActivityReportReference": {
          "type": "string",
          "example": "PARR721644",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: internal bank activity report - used for development \n"
        },
        "productServiceActivityReport": {
          "type": "object",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n general-info: data file/report of production activity\n",
          "properties": {}
        },
        "fraudModelModelType": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Fraud Model Model Type\n"
        },
        "fraudModelModelUsage": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: records number of production deployments and frequency of execution\n"
        },
        "fraudModelModelImpact": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: reported impact/accuracy of model\n"
        },
        "fraudModelModelFeedbackRecord": {
          "type": "object",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n general-info: user provided feedback/suggestions\n",
          "properties": {}
        },
        "fraudModelModelSpecification": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: design - inputs, calculations, outputs \n"
        },
        "fraudModelModelOperationalRequirements": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: defines operational and technical requirements\n"
        },
        "fraudModelModelAllowedUsage": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: defines when/where model can be used\n"
        },
        "fraudModelModelUsageGuidelines": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: guidance on usage and result interpretation\n"
        }
      }
    },
    "FraudModelsDeploymentBase": {
      "type": "object",
      "properties": {
        "fraudModelModel": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: this is the executable model specificaion\n"
        },
        "fraudModelModelDeploymentTaskRecord": {
          "type": "object",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n general-info: details/tracking the deployment activity\n",
          "properties": {}
        },
        "employeeBusinessUnitReference": {
          "type": "string",
          "example": "ER769585",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n general-info: the unit requesting the deployment\n"
        },
        "fraudModelModelVersion": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Fraud Model Model Version\n"
        },
        "fraudModelModelDeploymentStatus": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: tracks completion of deployment actions\n"
        },
        "fraudModelModelUsage": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: records number of production deployments\n"
        },
        "fraudModelModelDeploymentTaskResult": {
          "type": "string",
          "description": "`status: Not Mapped`\n core-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n general-info: Fraud Model Model Deployment Task Result\n"
        }
      }
    },
    "FraudModelRecordRequest": {
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
      }
    },
    "FraudModelRecordResponse": {
      "type": "object",
      "properties": {
        "recordingRecordReference": {
          "type": "string",
          "example": "RRR4678",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "recordingRecordStatus": {
          "type": "string",
          "example": "active",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        }
      }
    }
  }
}
</script>