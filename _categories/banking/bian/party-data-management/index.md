---
layout: api-single
title: Party Data Management
parent-title: BIAN APIs
description: Banking API Standards - APIs - Party Data Management
keywords: 
duration: 
type: api
standard: bian
order: 3
parent: /categories/banking/bian
api-logo: /dist/images/logos/bian_logo.svg
api-summary: This service domain maintains details of the legal entity structure of the party including dependents and associations for individuals and ownership/subsidiary structures for corporations.
api-example-use: Party legal entity details are checked for the financial booking of a major loan.
api-published-by: bianuser02 team
---
<script id="api-spec" type="application/json">
{
  "swagger": "2.0",
  "info": {
    "version": "1.0.0",
    "title": "Party Data Management",
    "description": "This service domain maintains details of the legal entity structure of the party. "
  },
  "host": "bianorg.azure-api.net",
  "basePath": "/sd-party-data-manage/v1",
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
    "/party-data-management/party-directory-entry/{cr-reference-id}/references/{bq-reference-id}/updation": {
      "put": {
        "tags": [
          "update"
        ],
        "summary": "Update an existing party reference",
        "operationId": "updatePartyDirectoryReference",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Party Directory Entry Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Reference Directory Entry Reference",
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
                "legalEntityReference": {
                  "type": "string",
                  "example": "47654676",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_yagFILl5EeOpCN0IL2Swqw)\ngeneral-info: Legal Entity\n"
                },
                "legalEntityOfficialName": {
                  "type": "string",
                  "example": "Entity Official Name",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_E7L5qcTGEeChad0JzLk7QA_-1556021177/elements/_E7VDkMTGEeChad0JzLk7QA_151261734)\ngeneral-info: Legal Entity Official Name\n"
                },
                "legalEntityType": {
                  "type": "string",
                  "example": "T2",
                  "description": "`status: Registered`\n iso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_zJK20OVaEeG_peKHD7roXg_-1787384341)\n general-info: Legal Entity Type\n"
                },
                "sectorsofOperation": {
                  "type": "string",
                  "example": "Sectors of Operation",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_FNqJssTGEeChad0JzLk7QA_-694813541)\ngeneral-info: Sectors of Operation\n"
                },
                "registeredAddress": {
                  "type": "string",
                  "example": "Address",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_w8TGEeChad0JzLk7QA_1650940768/elements/_FNg_xcTGEeChad0JzLk7QA_1331688362)\ngeneral-info: Registered Address\n"
                },
                "headquartersLocation": {
                  "type": "string",
                  "example": "Headquarters Location",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_z2I6YGx5EeKmZJ0Ago--9g_239738909)\ngeneral-info: Headquarters Location\n"
                },
                "dateofIncorporation": {
                  "type": "string",
                  "example": "08/08/2018",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_FNqJsMTGEeChad0JzLk7QA_-992959099)\ngeneral-info: Date Of InCorporation\n"
                },
                "jurisdictionofIncorporation": {
                  "type": "string",
                  "example": "Jurisdiction of Incorporation",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_w8TGEeChad0JzLk7QA_1650940768/elements/__-cVZ2IiEeGD28DQaMef-g)\ngeneral-info: Jurisdiction of Incorporation\n"
                },
                "registrationAuthority": {
                  "type": "string",
                  "example": "Registration Authority",
                  "description": "`status: Provisionally Registered`\nbian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).RegistraftionAuthority\ngeneral-info: Registration Authority\n"
                },
                "primaryRegulator": {
                  "type": "string",
                  "example": "Primary Regulator",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FI4-csTGEeChad0JzLk7QA_-1972046907/elements/_I8jqIHQzEeKIFpWttHerUA_2136525583)\ngeneral-info: Primary Regulator\n"
                },
                "taxIdentifier": {
                  "type": "string",
                  "example": "Tax Identifier",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_FEHzNcTGEeChad0JzLk7QA_-1792766550)\ngeneral-info: Tax Identifier\n"
                },
                "contactRole": {
                  "type": "string",
                  "example": "contact Role",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_YaxeYNTxEeO8xr27LwkIFw)\ngeneral-info: Contact Role\n"
                },
                "contactAddressDetails": {
                  "type": "string",
                  "example": "Contact Address Details",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\ngeneral-info: Contact Address Details\n"
                }
              },
              "example": {
                "dateofIncorporation": "08/08/2018",
                "legalEntityReference": "47654676",
                "headquartersLocation": "Headquarters Location",
                "taxIdentifier": "Tax Identifier",
                "jurisdictionofIncorporation": "Jurisdiction of Incorporation",
                "contactAddressDetails": "Contact Address Details",
                "sectorsofOperation": "Sectors of Operation",
                "primaryRegulator": "Primary Regulator",
                "registeredAddress": "Address",
                "registrationAuthority": "Registration Authority",
                "legalEntityOfficialName": "Entity Official Name",
                "legalEntityType": "T2",
                "contactRole": "contact Role"
              }
            }
          }
        ],
        "responses": {
          "200": {
            "description": "successful",
            "schema": {
              "type": "object",
              "properties": {
                "partyDirectoryEntryReference": {
                  "type": "string",
                  "example": "47654676",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "referenceDirectoryEntryReference": {
                  "type": "string",
                  "example": "47654676",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "legalEntityReference": {
                  "type": "string",
                  "example": "47654676",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_yagFILl5EeOpCN0IL2Swqw)\ngeneral-info: Legal Entity\n"
                },
                "legalEntityOfficialName": {
                  "type": "string",
                  "example": "Entity Official Name",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_E7L5qcTGEeChad0JzLk7QA_-1556021177/elements/_E7VDkMTGEeChad0JzLk7QA_151261734)\ngeneral-info: Entity Official Name\n"
                },
                "legalEntityType": {
                  "type": "string",
                  "example": "T2",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_zJK20OVaEeG_peKHD7roXg_-1787384341)\ngeneral-info: Legal Entity Type\n"
                },
                "sectorsofOperation": {
                  "type": "string",
                  "example": "Sectors of Operation",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_FNqJssTGEeChad0JzLk7QA_-694813541)\ngeneral-info: Sectors of Operation\n"
                },
                "registeredAddress": {
                  "type": "string",
                  "example": "Address",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_w8TGEeChad0JzLk7QA_1650940768/elements/_FNg_xcTGEeChad0JzLk7QA_1331688362)\ngeneral-info: Registered Address\n"
                },
                "headquartersLocation": {
                  "type": "string",
                  "example": "Headquarters Location",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_z2I6YGx5EeKmZJ0Ago--9g_239738909)\ngeneral-info: Headquarters Location\n"
                },
                "dateofIncorporation": {
                  "type": "string",
                  "example": "08/08/2018",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_FNqJsMTGEeChad0JzLk7QA_-992959099)\ngeneral-info: Date Of InCorporation\n"
                },
                "jurisdictionofIncorporation": {
                  "type": "string",
                  "example": "Jurisdiction of Incorporation",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_w8TGEeChad0JzLk7QA_1650940768/elements/__-cVZ2IiEeGD28DQaMef-g)\ngeneral-info: Jurisdiction of Incorporation\n"
                },
                "registrationAuthority": {
                  "type": "string",
                  "example": "Registration Authority",
                  "description": "`status: Provisionally Registered`\n bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).RegistraftionAuthority\ngeneral-info: Registration Authority\n"
                },
                "primaryRegulator": {
                  "type": "string",
                  "example": "Primary Regulator",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FI4-csTGEeChad0JzLk7QA_-1972046907/elements/_I8jqIHQzEeKIFpWttHerUA_2136525583)\ngeneral-info: Primary Regulator\n"
                },
                "taxIdentifier": {
                  "type": "string",
                  "example": "Tax Identifier",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_FEHzNcTGEeChad0JzLk7QA_-1792766550)\ngeneral-info: Tax Identifier\n"
                },
                "contactRole": {
                  "type": "string",
                  "example": "contact Role",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_YaxeYNTxEeO8xr27LwkIFw)\ngeneral-info: Contact Role\n"
                },
                "contactAddressDetails": {
                  "type": "string",
                  "example": "Contact Address Details",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\ngeneral-info: Contact Address Details\n"
                }
              },
              "example": {
                "dateofIncorporation": "08/08/2018",
                "referenceDirectoryEntryReference": "47654676",
                "legalEntityReference": "47654676",
                "headquartersLocation": "Headquarters Location",
                "taxIdentifier": "Tax Identifier",
                "jurisdictionofIncorporation": "Jurisdiction of Incorporation",
                "partyDirectoryEntryReference": "47654676",
                "contactAddressDetails": "Contact Address Details",
                "sectorsofOperation": "Sectors of Operation",
                "primaryRegulator": "Primary Regulator",
                "registeredAddress": "Address",
                "registrationAuthority": "Registration Authority",
                "legalEntityOfficialName": "Entity Official Name",
                "legalEntityType": "T2",
                "contactRole": "contact Role"
              }
            }
          }
        }
      }
    },
    "/party-data-management/party-directory-entry/{cr-reference-id}/profiles/{bq-reference-id}/updation": {
      "put": {
        "tags": [
          "update"
        ],
        "summary": "Update an existing party profile",
        "operationId": "updatePartyDirectoryProfile",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Party Directory Entry Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Profile Directory Entry Reference",
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
                "organizationCapitalization": {
                  "type": "string",
                  "example": "Organization Capitalization",
                  "description": "`status: Provisionally Registered`\n bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.Capitalisation\n   general-info: Organization Capitalization\n \n"
                },
                "organizationDebtLevel": {
                  "type": "string",
                  "example": "Organization Debt Level",
                  "description": "`status: Provisionally Registered`\n  bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.DebtLevel\n   general-info: Organization Debt Level\n"
                },
                "organizationEconomicIntent": {
                  "type": "string",
                  "example": "Organization Economic Intent",
                  "description": "`status: Provisionally Registered`\n  bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.EconomicIntent\n    general-info: Organization Economic Intent\n"
                },
                "organizationGrowthRate": {
                  "type": "string",
                  "example": "Organization Growth Rate",
                  "description": "`status: Provisionally Registered`\n  bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.GrowthRate\n  general-info: Organization Growth Rate\n"
                },
                "organizationProfitabilityStocks": {
                  "type": "string",
                  "example": "Organization Profitability Stocks",
                  "description": "`status: Provisionally Registered`\n bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.GrowthRate\n  general-info: Organization Profitability/Stocks\n"
                },
                "organizationRevenueTurnover": {
                  "type": "string",
                  "example": "Organization Revenue  Turnover",
                  "description": "`status: Provisionally Registered`\n bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.Revenue\n  general-info: Organization Revenue/Turnover\n"
                }
              },
              "example": {
                "organizationDebtLevel": "Organization Debt Level",
                "organizationCapitalization": "Organization Capitalization",
                "organizationEconomicIntent": "Organization Economic Intent",
                "organizationGrowthRate": "Organization Growth Rate",
                "organizationRevenueTurnover": "Organization Revenue  Turnover",
                "organizationProfitabilityStocks": "Organization Profitability Stocks"
              }
            }
          }
        ],
        "responses": {
          "200": {
            "description": "successful",
            "schema": {
              "type": "object",
              "properties": {
                "partyDirectoryEntryReference": {
                  "type": "string",
                  "example": "Organization Capitalization",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "profileDirectoryEntryReference": {
                  "type": "string",
                  "example": "Organization Capitalization",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "organizationCapitalization": {
                  "type": "string",
                  "example": "Organization Capitalization",
                  "description": "`status: Provisionally Registered`\nbian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.Capitalisation\n  general-info: Organization Capitalization\n  \n"
                },
                "organizationDebtLevel": {
                  "type": "string",
                  "example": "Organization Debt Level",
                  "description": "`status: Provisonally Registered`\n  bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.DebtLevel\n   general-info: Organization Debt Level\n  \n"
                },
                "organizationEconomicIntent": {
                  "type": "string",
                  "example": "Organization Economic Intent",
                  "description": "`status: Provisionally Registered`\nbian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.EconomicIntent\n  general-info: Organization Economic Intent\n  \n"
                },
                "organizationGrowthRate": {
                  "type": "string",
                  "example": "Organization Growth Rate",
                  "description": "`status: Provisionally Registered`\n bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.GrowthRate\n   general-info: Organization Growth Rate\n   \n \n"
                },
                "organizationProfitabilityStocks": {
                  "type": "string",
                  "example": "Organization Profitability Stocks",
                  "description": "`status: Provisionally Registered`\n bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.GrowthRate\n general-info: Organization Profitability/Stocks\n \n"
                },
                "organizationRevenueTurnover": {
                  "type": "string",
                  "example": "Organization Revenue  Turnover",
                  "description": "`status: Provisionally Regsitered`\n  bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.Revenue\n    general-info: Organization Revenue/Turnover\n"
                }
              },
              "example": {
                "organizationDebtLevel": "Organization Debt Level",
                "organizationCapitalization": "Organization Capitalization",
                "profileDirectoryEntryReference": "Organization Capitalization",
                "organizationEconomicIntent": "Organization Economic Intent",
                "organizationGrowthRate": "Organization Growth Rate",
                "organizationRevenueTurnover": "Organization Revenue  Turnover",
                "partyDirectoryEntryReference": "Organization Capitalization",
                "organizationProfitabilityStocks": "Organization Profitability Stocks"
              }
            }
          }
        }
      }
    },
    "/party-data-management/party-directory-entry/{cr-reference-id}/association/{bq-reference-id}/updation": {
      "put": {
        "tags": [
          "update"
        ],
        "summary": "Update an existing party association",
        "operationId": "updatePartyDirectoryAssociation",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Party Directory Entry Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Association Directory Entry Reference",
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
                "legalEntityAssociationReference": {
                  "type": "string",
                  "example": "47654676",
                  "description": "`status: Provisionally Registered`\nbian-reference: PartyRegistryEntry.RegisteredParty(as RolePlayer).Role.PartyRelationship\n general-info: Legal Entity Association Reference (company or individual)\n"
                },
                "legalEntityAssociationType": {
                  "type": "string",
                  "example": "L2",
                  "description": "`status: Provisionally Registered`\n general-info: Legal Entity Association Reference (company or individual)\n   general-info: Legal Entity Association Type (corporate or familial)\n"
                },
                "legalEntityAssociationObligation": {
                  "type": "string",
                  "example": "Association Obligation",
                  "description": "`status: Provisionally Registered`\nbian-reference: PartyRegistryEntry.RegisteredParty(as RolePlayer).Role.PartyRelationship.RelationshipAgreement.Obligation\ngeneral-info: Legal Entity Association Obligation (e.g. shareholder, director, guardian, guarantor)\n"
                },
                "parentLegalEntityReference": {
                  "type": "string",
                  "example": "47654676",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_yagFILl5EeOpCN0IL2Swqw)\ngeneral-info: Parent Legal Entity\n"
                },
                "subsidiaryLegalEntityReference": {
                  "type": "string",
                  "example": "47654676",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_yagFILl5EeOpCN0IL2Swqw)\ngeneral-info: Subsidiary Legal Entity Reference\n"
                },
                "shareholdingProfile": {
                  "type": "string",
                  "example": "shareholding Profile",
                  "description": "`status: Provisionally Registered`\nbian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).ShareholderRegister\ngeneral-info: Shareholding Profile (lists major shareholders and shareholdings of significance) \n"
                }
              },
              "example": {
                "legalEntityAssociationType": "L2",
                "subsidiaryLegalEntityReference": "47654676",
                "legalEntityAssociationObligation": "Association Obligation",
                "shareholdingProfile": "shareholding Profile",
                "legalEntityAssociationReference": "47654676",
                "parentLegalEntityReference": "47654676"
              }
            }
          }
        ],
        "responses": {
          "200": {
            "description": "successful",
            "schema": {
              "type": "object",
              "properties": {
                "partyDirectoryEntryReference": {
                  "type": "string",
                  "example": "47654676",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "associationDirectoryEntryReference": {
                  "type": "string",
                  "example": "47654676",
                  "description": "`status: Not Mapped\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "legalEntityAssociationReference": {
                  "type": "string",
                  "example": "47654676",
                  "description": "`status: Provisionally Registered`\nbian-reference: PartyRegistryEntry.RegisteredParty(as RolePlayer).Role.PartyRelationship\ngeneral-info: Legal Entity Association Reference (company or individual)\n"
                },
                "legalEntityAssociationType": {
                  "type": "string",
                  "example": "L2",
                  "description": "`status: Provisionally Registered`\n  bian-reference: PartyRegistryEntry.RegisteredParty(as RolePlayer).Role.PartyRelationship.PartyRelationshipType\n  general-info: Legal Entity Association Type (corporate or familial)\n"
                },
                "legalEntityAssociationObligation": {
                  "type": "string",
                  "example": "Association Obligation",
                  "description": "`status: Provisionally Registered`\nbian-reference: PartyRegistryEntry.RegisteredParty(as RolePlayer).Role.PartyRelationship.RelationshipAgreement.Obligation\n general-info: Legal Entity Association Obligation (e.g. shareholder, director, guardian, guarantor)\n"
                },
                "parentLegalEntityReference": {
                  "type": "string",
                  "example": "47654676",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_yagFILl5EeOpCN0IL2Swqw)\ngeneral-info: Parent Legal Entity\n"
                },
                "subsidiaryLegalEntityReference": {
                  "type": "string",
                  "example": "47654676",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_yagFILl5EeOpCN0IL2Swqw)\ngeneral-info: Subsidiary Legal Entity Reference\n"
                },
                "shareholdingProfile": {
                  "type": "string",
                  "example": "shareholding Profile",
                  "description": "`status: Provisionally Registered`\nbian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).ShareholderRegister\n general-info: Shareholding Profile (lists major shareholders and shareholdings of significance)\n"
                }
              },
              "example": {
                "legalEntityAssociationType": "L2",
                "associationDirectoryEntryReference": "47654676",
                "subsidiaryLegalEntityReference": "47654676",
                "partyDirectoryEntryReference": "47654676",
                "legalEntityAssociationObligation": "Association Obligation",
                "shareholdingProfile": "shareholding Profile",
                "legalEntityAssociationReference": "47654676",
                "parentLegalEntityReference": "47654676"
              }
            }
          }
        }
      }
    },
    "/party-data-management/party-directory-entry/{cr-reference-id}/references/registration": {
      "post": {
        "tags": [
          "register"
        ],
        "summary": "Register a new party directory entry",
        "operationId": "registerPartyDirectoryEntryReference",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Party Directory Entry Reference",
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
                "legalEntityReference": {
                  "type": "string",
                  "example": "47654676",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_yagFILl5EeOpCN0IL2Swqw)\ngeneral-info: Legal Entity\n"
                },
                "legalEntityOfficialName": {
                  "type": "string",
                  "example": "Entity Official Name",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_E7L5qcTGEeChad0JzLk7QA_-1556021177/elements/_E7VDkMTGEeChad0JzLk7QA_151261734)\ngeneral-info: Legal Entity Official Name\n"
                },
                "legalEntityType": {
                  "type": "string",
                  "example": "T2",
                  "description": "`status: Registered`\n iso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_zJK20OVaEeG_peKHD7roXg_-1787384341)\n general-info: Legal Entity Type\n"
                },
                "sectorsofOperation": {
                  "type": "string",
                  "example": "Sectors of Operation",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_FNqJssTGEeChad0JzLk7QA_-694813541)\ngeneral-info: Sectors of Operation\n"
                },
                "registeredAddress": {
                  "type": "string",
                  "example": "Address",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_w8TGEeChad0JzLk7QA_1650940768/elements/_FNg_xcTGEeChad0JzLk7QA_1331688362)\ngeneral-info: Registered Address\n"
                },
                "headquartersLocation": {
                  "type": "string",
                  "example": "Headquarters Location",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_z2I6YGx5EeKmZJ0Ago--9g_239738909)\ngeneral-info: Headquarters Location\n"
                },
                "dateofIncorporation": {
                  "type": "string",
                  "example": "08/08/2018",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_FNqJsMTGEeChad0JzLk7QA_-992959099)\ngeneral-info: Date Of InCorporation\n"
                },
                "jurisdictionofIncorporation": {
                  "type": "string",
                  "example": "Jurisdiction of Incorporation",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_w8TGEeChad0JzLk7QA_1650940768/elements/__-cVZ2IiEeGD28DQaMef-g)\ngeneral-info: Jurisdiction of Incorporation\n"
                },
                "registrationAuthority": {
                  "type": "string",
                  "example": "Registration Authority",
                  "description": "`status: Provisionally Registered`\nbian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).RegistraftionAuthority\ngeneral-info: Registration Authority\n"
                },
                "primaryRegulator": {
                  "type": "string",
                  "example": "Primary Regulator",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FI4-csTGEeChad0JzLk7QA_-1972046907/elements/_I8jqIHQzEeKIFpWttHerUA_2136525583)\ngeneral-info: Primary Regulator\n"
                },
                "taxIdentifier": {
                  "type": "string",
                  "example": "Tax Identifier",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_FEHzNcTGEeChad0JzLk7QA_-1792766550)\ngeneral-info: Tax Identifier\n"
                },
                "contactRole": {
                  "type": "string",
                  "example": "contact Role",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_YaxeYNTxEeO8xr27LwkIFw)\ngeneral-info: Contact Role\n"
                },
                "contactAddressDetails": {
                  "type": "string",
                  "example": "Contact Address Details",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\ngeneral-info: Contact Address Details\n"
                }
              },
              "example": {
                "dateofIncorporation": "08/08/2018",
                "legalEntityReference": "47654676",
                "headquartersLocation": "Headquarters Location",
                "taxIdentifier": "Tax Identifier",
                "jurisdictionofIncorporation": "Jurisdiction of Incorporation",
                "contactAddressDetails": "Contact Address Details",
                "sectorsofOperation": "Sectors of Operation",
                "primaryRegulator": "Primary Regulator",
                "registeredAddress": "Address",
                "registrationAuthority": "Registration Authority",
                "legalEntityOfficialName": "Entity Official Name",
                "legalEntityType": "T2",
                "contactRole": "contact Role"
              }
            }
          }
        ],
        "responses": {
          "201": {
            "description": "A new party reference is created successfully",
            "schema": {
              "type": "object",
              "properties": {
                "partyDirectoryEntryReference": {
                  "type": "string",
                  "example": "47654676",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "referenceDirectoryEntryReference": {
                  "type": "string",
                  "example": "47654676",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "legalEntityReference": {
                  "type": "string",
                  "example": "47654676",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_yagFILl5EeOpCN0IL2Swqw)\ngeneral-info: Legal Entity\n"
                },
                "legalEntityOfficialName": {
                  "type": "string",
                  "example": "Entity Official Name",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_E7L5qcTGEeChad0JzLk7QA_-1556021177/elements/_E7VDkMTGEeChad0JzLk7QA_151261734)\ngeneral-info: Entity Official Name\n"
                },
                "legalEntityType": {
                  "type": "string",
                  "example": "T2",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_zJK20OVaEeG_peKHD7roXg_-1787384341)\ngeneral-info: Legal Entity Type\n"
                },
                "sectorsofOperation": {
                  "type": "string",
                  "example": "Sectors of Operation",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_FNqJssTGEeChad0JzLk7QA_-694813541)\ngeneral-info: Sectors of Operation\n"
                },
                "registeredAddress": {
                  "type": "string",
                  "example": "Address",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_w8TGEeChad0JzLk7QA_1650940768/elements/_FNg_xcTGEeChad0JzLk7QA_1331688362)\ngeneral-info: Registered Address\n"
                },
                "headquartersLocation": {
                  "type": "string",
                  "example": "Headquarters Location",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_z2I6YGx5EeKmZJ0Ago--9g_239738909)\ngeneral-info: Headquarters Location\n"
                },
                "dateofIncorporation": {
                  "type": "string",
                  "example": "08/08/2018",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_FNqJsMTGEeChad0JzLk7QA_-992959099)\ngeneral-info: Date Of InCorporation\n"
                },
                "jurisdictionofIncorporation": {
                  "type": "string",
                  "example": "Jurisdiction of Incorporation",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_w8TGEeChad0JzLk7QA_1650940768/elements/__-cVZ2IiEeGD28DQaMef-g)\ngeneral-info: Jurisdiction of Incorporation\n"
                },
                "registrationAuthority": {
                  "type": "string",
                  "example": "Registration Authority",
                  "description": "`status: Provisionally Registered`\n bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).RegistraftionAuthority\ngeneral-info: Registration Authority\n"
                },
                "primaryRegulator": {
                  "type": "string",
                  "example": "Primary Regulator",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FI4-csTGEeChad0JzLk7QA_-1972046907/elements/_I8jqIHQzEeKIFpWttHerUA_2136525583)\ngeneral-info: Primary Regulator\n"
                },
                "taxIdentifier": {
                  "type": "string",
                  "example": "Tax Identifier",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_FEHzNcTGEeChad0JzLk7QA_-1792766550)\ngeneral-info: Tax Identifier\n"
                },
                "contactRole": {
                  "type": "string",
                  "example": "contact Role",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_YaxeYNTxEeO8xr27LwkIFw)\ngeneral-info: Contact Role\n"
                },
                "contactAddressDetails": {
                  "type": "string",
                  "example": "Contact Address Details",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\ngeneral-info: Contact Address Details\n"
                }
              },
              "example": {
                "dateofIncorporation": "08/08/2018",
                "referenceDirectoryEntryReference": "47654676",
                "legalEntityReference": "47654676",
                "headquartersLocation": "Headquarters Location",
                "taxIdentifier": "Tax Identifier",
                "jurisdictionofIncorporation": "Jurisdiction of Incorporation",
                "partyDirectoryEntryReference": "47654676",
                "contactAddressDetails": "Contact Address Details",
                "sectorsofOperation": "Sectors of Operation",
                "primaryRegulator": "Primary Regulator",
                "registeredAddress": "Address",
                "registrationAuthority": "Registration Authority",
                "legalEntityOfficialName": "Entity Official Name",
                "legalEntityType": "T2",
                "contactRole": "contact Role"
              }
            }
          }
        }
      }
    },
    "/party-data-management/party-directory-entry/{cr-reference-id}/profiles/registration": {
      "post": {
        "tags": [
          "register"
        ],
        "summary": "Register key high level financiall profile details",
        "operationId": "registerPartyDirectoryEntryProfile",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Party Directory Entry Reference",
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
                "organizationCapitalization": {
                  "type": "string",
                  "example": "Organization Capitalization",
                  "description": "`status: Provisionally Registered`\n bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.Capitalisation\n   general-info: Organization Capitalization\n \n"
                },
                "organizationDebtLevel": {
                  "type": "string",
                  "example": "Organization Debt Level",
                  "description": "`status: Provisionally Registered`\n  bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.DebtLevel\n   general-info: Organization Debt Level\n"
                },
                "organizationEconomicIntent": {
                  "type": "string",
                  "example": "Organization Economic Intent",
                  "description": "`status: Provisionally Registered`\n  bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.EconomicIntent\n    general-info: Organization Economic Intent\n"
                },
                "organizationGrowthRate": {
                  "type": "string",
                  "example": "Organization Growth Rate",
                  "description": "`status: Provisionally Registered`\n  bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.GrowthRate\n  general-info: Organization Growth Rate\n"
                },
                "organizationProfitabilityStocks": {
                  "type": "string",
                  "example": "Organization Profitability Stocks",
                  "description": "`status: Provisionally Registered`\n bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.GrowthRate\n  general-info: Organization Profitability/Stocks\n"
                },
                "organizationRevenueTurnover": {
                  "type": "string",
                  "example": "Organization Revenue  Turnover",
                  "description": "`status: Provisionally Registered`\n bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.Revenue\n  general-info: Organization Revenue/Turnover\n"
                }
              },
              "example": {
                "organizationDebtLevel": "Organization Debt Level",
                "organizationCapitalization": "Organization Capitalization",
                "organizationEconomicIntent": "Organization Economic Intent",
                "organizationGrowthRate": "Organization Growth Rate",
                "organizationRevenueTurnover": "Organization Revenue  Turnover",
                "organizationProfitabilityStocks": "Organization Profitability Stocks"
              }
            }
          }
        ],
        "responses": {
          "201": {
            "description": "A new party profile is created successfully",
            "schema": {
              "type": "object",
              "properties": {
                "partyDirectoryEntryReference": {
                  "type": "string",
                  "example": "Organization Capitalization",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "profileDirectoryEntryReference": {
                  "type": "string",
                  "example": "Organization Capitalization",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "organizationCapitalization": {
                  "type": "string",
                  "example": "Organization Capitalization",
                  "description": "`status: Provisionally Registered`\nbian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.Capitalisation\n  general-info: Organization Capitalization\n  \n"
                },
                "organizationDebtLevel": {
                  "type": "string",
                  "example": "Organization Debt Level",
                  "description": "`status: Provisonally Registered`\n  bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.DebtLevel\n   general-info: Organization Debt Level\n  \n"
                },
                "organizationEconomicIntent": {
                  "type": "string",
                  "example": "Organization Economic Intent",
                  "description": "`status: Provisionally Registered`\nbian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.EconomicIntent\n  general-info: Organization Economic Intent\n  \n"
                },
                "organizationGrowthRate": {
                  "type": "string",
                  "example": "Organization Growth Rate",
                  "description": "`status: Provisionally Registered`\n bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.GrowthRate\n   general-info: Organization Growth Rate\n   \n \n"
                },
                "organizationProfitabilityStocks": {
                  "type": "string",
                  "example": "Organization Profitability Stocks",
                  "description": "`status: Provisionally Registered`\n bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.GrowthRate\n general-info: Organization Profitability/Stocks\n \n"
                },
                "organizationRevenueTurnover": {
                  "type": "string",
                  "example": "Organization Revenue  Turnover",
                  "description": "`status: Provisionally Regsitered`\n  bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.Revenue\n    general-info: Organization Revenue/Turnover\n"
                }
              },
              "example": {
                "organizationDebtLevel": "Organization Debt Level",
                "organizationCapitalization": "Organization Capitalization",
                "profileDirectoryEntryReference": "Organization Capitalization",
                "organizationEconomicIntent": "Organization Economic Intent",
                "organizationGrowthRate": "Organization Growth Rate",
                "organizationRevenueTurnover": "Organization Revenue  Turnover",
                "partyDirectoryEntryReference": "Organization Capitalization",
                "organizationProfitabilityStocks": "Organization Profitability Stocks"
              }
            }
          }
        }
      }
    },
    "/party-data-management/party-directory-entry/{cr-reference-id}/associations/registration": {
      "post": {
        "tags": [
          "register"
        ],
        "summary": "Register a new party association within the directory",
        "operationId": "registerPartyDirectoryEntryAssociation",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Party Directory Entry Reference",
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
                "legalEntityAssociationReference": {
                  "type": "string",
                  "example": "47654676",
                  "description": "`status: Provisionally Registered`\nbian-reference: PartyRegistryEntry.RegisteredParty(as RolePlayer).Role.PartyRelationship\n general-info: Legal Entity Association Reference (company or individual)\n"
                },
                "legalEntityAssociationType": {
                  "type": "string",
                  "example": "L2",
                  "description": "`status: Provisionally Registered`\n general-info: Legal Entity Association Reference (company or individual)\n   general-info: Legal Entity Association Type (corporate or familial)\n"
                },
                "legalEntityAssociationObligation": {
                  "type": "string",
                  "example": "Association Obligation",
                  "description": "`status: Provisionally Registered`\nbian-reference: PartyRegistryEntry.RegisteredParty(as RolePlayer).Role.PartyRelationship.RelationshipAgreement.Obligation\ngeneral-info: Legal Entity Association Obligation (e.g. shareholder, director, guardian, guarantor)\n"
                },
                "parentLegalEntityReference": {
                  "type": "string",
                  "example": "47654676",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_yagFILl5EeOpCN0IL2Swqw)\ngeneral-info: Parent Legal Entity\n"
                },
                "subsidiaryLegalEntityReference": {
                  "type": "string",
                  "example": "47654676",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_yagFILl5EeOpCN0IL2Swqw)\ngeneral-info: Subsidiary Legal Entity Reference\n"
                },
                "shareholdingProfile": {
                  "type": "string",
                  "example": "shareholding Profile",
                  "description": "`status: Provisionally Registered`\nbian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).ShareholderRegister\ngeneral-info: Shareholding Profile (lists major shareholders and shareholdings of significance) \n"
                }
              },
              "example": {
                "legalEntityAssociationType": "L2",
                "subsidiaryLegalEntityReference": "47654676",
                "legalEntityAssociationObligation": "Association Obligation",
                "shareholdingProfile": "shareholding Profile",
                "legalEntityAssociationReference": "47654676",
                "parentLegalEntityReference": "47654676"
              }
            }
          }
        ],
        "responses": {
          "201": {
            "description": "A new party assiciation is created successfully",
            "schema": {
              "type": "object",
              "properties": {
                "partyDirectoryEntryReference": {
                  "type": "string",
                  "example": "47654676",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "associationDirectoryEntryReference": {
                  "type": "string",
                  "example": "47654676",
                  "description": "`status: Not Mapped\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "legalEntityAssociationReference": {
                  "type": "string",
                  "example": "47654676",
                  "description": "`status: Provisionally Registered`\nbian-reference: PartyRegistryEntry.RegisteredParty(as RolePlayer).Role.PartyRelationship\ngeneral-info: Legal Entity Association Reference (company or individual)\n"
                },
                "legalEntityAssociationType": {
                  "type": "string",
                  "example": "L2",
                  "description": "`status: Provisionally Registered`\n  bian-reference: PartyRegistryEntry.RegisteredParty(as RolePlayer).Role.PartyRelationship.PartyRelationshipType\n  general-info: Legal Entity Association Type (corporate or familial)\n"
                },
                "legalEntityAssociationObligation": {
                  "type": "string",
                  "example": "Association Obligation",
                  "description": "`status: Provisionally Registered`\nbian-reference: PartyRegistryEntry.RegisteredParty(as RolePlayer).Role.PartyRelationship.RelationshipAgreement.Obligation\n general-info: Legal Entity Association Obligation (e.g. shareholder, director, guardian, guarantor)\n"
                },
                "parentLegalEntityReference": {
                  "type": "string",
                  "example": "47654676",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_yagFILl5EeOpCN0IL2Swqw)\ngeneral-info: Parent Legal Entity\n"
                },
                "subsidiaryLegalEntityReference": {
                  "type": "string",
                  "example": "47654676",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_yagFILl5EeOpCN0IL2Swqw)\ngeneral-info: Subsidiary Legal Entity Reference\n"
                },
                "shareholdingProfile": {
                  "type": "string",
                  "example": "shareholding Profile",
                  "description": "`status: Provisionally Registered`\nbian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).ShareholderRegister\n general-info: Shareholding Profile (lists major shareholders and shareholdings of significance)\n"
                }
              },
              "example": {
                "legalEntityAssociationType": "L2",
                "associationDirectoryEntryReference": "47654676",
                "subsidiaryLegalEntityReference": "47654676",
                "partyDirectoryEntryReference": "47654676",
                "legalEntityAssociationObligation": "Association Obligation",
                "shareholdingProfile": "shareholding Profile",
                "legalEntityAssociationReference": "47654676",
                "parentLegalEntityReference": "47654676"
              }
            }
          }
        }
      }
    },
    "/party-data-management/party-directory-entry/{cr-reference-id}/requisition": {
      "put": {
        "tags": [
          "request"
        ],
        "summary": "Request to refresh an existing party directory entry",
        "description": "Update existing party directory",
        "operationId": "requestPartyDirectoryEntryUpdate",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Party Directory Entry Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "Successfully refreshed",
            "schema": {
              "type": "object",
              "properties": {
                "refreshStatus": {
                  "type": "string",
                  "example": "Refreshed",
                  "description": "`status: Not Mapped`\nBIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                }
              },
              "example": {
                "refreshStatus": "Refreshed"
              }
            }
          }
        }
      }
    },
    "/party-data-management/party-directory-entry/{cr-reference-id}/recording": {
      "post": {
        "tags": [
          "record"
        ],
        "summary": "Record usage or feedback against a directory entry",
        "operationId": "recordPartyDirectoryEntry",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Party Directory Entry Reference",
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
                "recordingRecordType": {
                  "type": "string",
                  "example": "The layout/type of the feedback",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "recordingRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
                  "properties": {}
                },
                "recordingRecordDateTime": {
                  "type": "string",
                  "pattern": "^(?:[1-9]\\d{3}-(?:(?:0[1-9]|1[0-2])-(?:0[1-9]|1\\d|2[0-8])|(?:0[13-9]|1[0-2])-(?:29|30)|(?:0[13578]|1[02])-31)|(?:[1-9]\\d(?:0[48]|[2468][048]|[13579][26])|(?:[2468][048]|[13579][26])00)-02-29)T(?:[01]\\d|2[0-3]):[0-5]\\d:[0-5]\\d(?:\\.[0-9]+)?(?:Z|[+-][01]\\d:[0-5]\\d)?$",
                  "description": "`status: Registered`,\niso-link: [click_here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/datatypes/_YW1tKtp-Ed-ak6NoX_4Aeg_-1624336183)\ngeneral-info: A particular point in the progression of time defined by a mandatory date and a mandatory time component, expressed in either UTC time format (YYYY-MM-DDThh:mm:ss.sssZ), local time with UTC offset format (YYYY-MM-DDThh:mm:ss.sss+/-hh:mm), or local time format (YYYY-MM-DDThh:mm:ss.sss). These representations are defined in \"XML Schema Part 2: Datatypes Second Edition - W3C Recommendation 28 October 2004\" which is aligned with ISO 8601.\nNote on the time format:\n1) beginning / end of calendar day\n00:00:00 = the beginning of a calendar day\n24:00:00 = the end of a calendar day\n2) fractions of second in time format\nDecimal fractions of seconds may be included. In this case, the involved parties shall agree on the maximum number of digits that are allowed.\n",
                  "example": "2018-09-26T05:56:05.007"
                },
                "employeeBusinessUnitReference": {
                  "type": "string",
                  "example": "47654676",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                }
              },
              "example": {
                "recordingRecordType": "The layout/type of the feedback",
                "employeeBusinessUnitReference": "47654676",
                "recordingRecordDateTime": "2018-09-26T05:56:05.007",
                "recordingRecord": "{}"
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
                  "example": "47654676",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "recordingRecordStatus": {
                  "type": "string",
                  "example": "Applied",
                  "description": "`status: Not Mapped`\nBIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                }
              },
              "example": {
                "recordingRecordReference": "47654676",
                "recordingRecordStatus": "Applied"
              }
            }
          }
        }
      }
    },
    "/party-data-management/party-directory-entry": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve Directory entry reference ids according to a filtering criteria",
        "operationId": "retrieveLocationDirectoryEntryReferenceIds",
        "parameters": [
          {
            "name": "collection-filter",
            "in": "query",
            "description": "Filter to refine the result set",
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
                "PDER4388",
                "PDER3246243"
              ]
            }
          }
        }
      }
    },
    "/party-data-management/party-directory-entry/behavior-qualifiers": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve all behavior qualifiers of the control record",
        "operationId": "retrieveLocationDirectoryEntryBehaviorQualifiers",
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
                "reference",
                "profile",
                "association"
              ]
            }
          }
        }
      }
    },
    "/party-data-management/party-directory-entry/{cr-reference-id}/{behavior-qualifier}": {
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
            "description": "Party Directory Entry Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "behavior-qualifier",
            "in": "path",
            "description": "Behavior Qualifier Name. ex- Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "collection-filter",
            "in": "query",
            "description": "Filter to refine the result set. ex- 'legal-entity-reference = LER123'",
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
                "RDER3465346",
                "RDER4563",
                "RDER45687"
              ]
            }
          }
        }
      }
    },
    "/party-data-management/party-directory-entry/{cr-reference-id}/references/{bq-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve party directory entry references",
        "operationId": "retrieveReference",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Party Directory Entry Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Reference Directory Entry Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "successful",
            "schema": {
              "type": "object",
              "properties": {
                "partyDirectoryEntryReference": {
                  "type": "string",
                  "example": "47654676",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "referenceDirectoryEntryReference": {
                  "type": "string",
                  "example": "47654676",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "legalEntityReference": {
                  "type": "string",
                  "example": "47654676",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_yagFILl5EeOpCN0IL2Swqw)\ngeneral-info: Legal Entity\n"
                },
                "legalEntityOfficialName": {
                  "type": "string",
                  "example": "Entity Official Name",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_E7L5qcTGEeChad0JzLk7QA_-1556021177/elements/_E7VDkMTGEeChad0JzLk7QA_151261734)\ngeneral-info: Entity Official Name\n"
                },
                "legalEntityType": {
                  "type": "string",
                  "example": "T2",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_zJK20OVaEeG_peKHD7roXg_-1787384341)\ngeneral-info: Legal Entity Type\n"
                },
                "sectorsofOperation": {
                  "type": "string",
                  "example": "Sectors of Operation",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_FNqJssTGEeChad0JzLk7QA_-694813541)\ngeneral-info: Sectors of Operation\n"
                },
                "registeredAddress": {
                  "type": "string",
                  "example": "Address",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_w8TGEeChad0JzLk7QA_1650940768/elements/_FNg_xcTGEeChad0JzLk7QA_1331688362)\ngeneral-info: Registered Address\n"
                },
                "headquartersLocation": {
                  "type": "string",
                  "example": "Headquarters Location",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_z2I6YGx5EeKmZJ0Ago--9g_239738909)\ngeneral-info: Headquarters Location\n"
                },
                "dateofIncorporation": {
                  "type": "string",
                  "example": "08/08/2018",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_FNqJsMTGEeChad0JzLk7QA_-992959099)\ngeneral-info: Date Of InCorporation\n"
                },
                "jurisdictionofIncorporation": {
                  "type": "string",
                  "example": "Jurisdiction of Incorporation",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_w8TGEeChad0JzLk7QA_1650940768/elements/__-cVZ2IiEeGD28DQaMef-g)\ngeneral-info: Jurisdiction of Incorporation\n"
                },
                "registrationAuthority": {
                  "type": "string",
                  "example": "Registration Authority",
                  "description": "`status: Provisionally Registered`\n bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).RegistraftionAuthority\ngeneral-info: Registration Authority\n"
                },
                "primaryRegulator": {
                  "type": "string",
                  "example": "Primary Regulator",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FI4-csTGEeChad0JzLk7QA_-1972046907/elements/_I8jqIHQzEeKIFpWttHerUA_2136525583)\ngeneral-info: Primary Regulator\n"
                },
                "taxIdentifier": {
                  "type": "string",
                  "example": "Tax Identifier",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_FEHzNcTGEeChad0JzLk7QA_-1792766550)\ngeneral-info: Tax Identifier\n"
                },
                "contactRole": {
                  "type": "string",
                  "example": "contact Role",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_YaxeYNTxEeO8xr27LwkIFw)\ngeneral-info: Contact Role\n"
                },
                "contactAddressDetails": {
                  "type": "string",
                  "example": "Contact Address Details",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\ngeneral-info: Contact Address Details\n"
                }
              },
              "example": {
                "dateofIncorporation": "08/08/2018",
                "referenceDirectoryEntryReference": "47654676",
                "legalEntityReference": "47654676",
                "headquartersLocation": "Headquarters Location",
                "taxIdentifier": "Tax Identifier",
                "jurisdictionofIncorporation": "Jurisdiction of Incorporation",
                "partyDirectoryEntryReference": "47654676",
                "contactAddressDetails": "Contact Address Details",
                "sectorsofOperation": "Sectors of Operation",
                "primaryRegulator": "Primary Regulator",
                "registeredAddress": "Address",
                "registrationAuthority": "Registration Authority",
                "legalEntityOfficialName": "Entity Official Name",
                "legalEntityType": "T2",
                "contactRole": "contact Role"
              }
            }
          }
        }
      }
    },
    "/party-data-management/party-directory-entry/{cr-reference-id}/profiles/{bq-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve party directory entry profiles",
        "operationId": "retrieveProfile",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Party Directory Entry Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Profile Directory Entry Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "successful",
            "schema": {
              "type": "object",
              "properties": {
                "partyDirectoryEntryReference": {
                  "type": "string",
                  "example": "Organization Capitalization",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "profileDirectoryEntryReference": {
                  "type": "string",
                  "example": "Organization Capitalization",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "organizationCapitalization": {
                  "type": "string",
                  "example": "Organization Capitalization",
                  "description": "`status: Provisionally Registered`\nbian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.Capitalisation\n  general-info: Organization Capitalization\n  \n"
                },
                "organizationDebtLevel": {
                  "type": "string",
                  "example": "Organization Debt Level",
                  "description": "`status: Provisonally Registered`\n  bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.DebtLevel\n   general-info: Organization Debt Level\n  \n"
                },
                "organizationEconomicIntent": {
                  "type": "string",
                  "example": "Organization Economic Intent",
                  "description": "`status: Provisionally Registered`\nbian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.EconomicIntent\n  general-info: Organization Economic Intent\n  \n"
                },
                "organizationGrowthRate": {
                  "type": "string",
                  "example": "Organization Growth Rate",
                  "description": "`status: Provisionally Registered`\n bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.GrowthRate\n   general-info: Organization Growth Rate\n   \n \n"
                },
                "organizationProfitabilityStocks": {
                  "type": "string",
                  "example": "Organization Profitability Stocks",
                  "description": "`status: Provisionally Registered`\n bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.GrowthRate\n general-info: Organization Profitability/Stocks\n \n"
                },
                "organizationRevenueTurnover": {
                  "type": "string",
                  "example": "Organization Revenue  Turnover",
                  "description": "`status: Provisionally Regsitered`\n  bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.Revenue\n    general-info: Organization Revenue/Turnover\n"
                }
              },
              "example": {
                "organizationDebtLevel": "Organization Debt Level",
                "organizationCapitalization": "Organization Capitalization",
                "profileDirectoryEntryReference": "Organization Capitalization",
                "organizationEconomicIntent": "Organization Economic Intent",
                "organizationGrowthRate": "Organization Growth Rate",
                "organizationRevenueTurnover": "Organization Revenue  Turnover",
                "partyDirectoryEntryReference": "Organization Capitalization",
                "organizationProfitabilityStocks": "Organization Profitability Stocks"
              }
            }
          }
        }
      }
    },
    "/party-data-management/party-directory-entry/{cr-reference-id}/associations/{bq-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve party directory entry associations",
        "operationId": "retrieveAssociation",
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Party Directory Entry Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Association Directory Entry Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "successful",
            "schema": {
              "type": "object",
              "properties": {
                "partyDirectoryEntryReference": {
                  "type": "string",
                  "example": "47654676",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "associationDirectoryEntryReference": {
                  "type": "string",
                  "example": "47654676",
                  "description": "`status: Not Mapped\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "legalEntityAssociationReference": {
                  "type": "string",
                  "example": "47654676",
                  "description": "`status: Provisionally Registered`\nbian-reference: PartyRegistryEntry.RegisteredParty(as RolePlayer).Role.PartyRelationship\ngeneral-info: Legal Entity Association Reference (company or individual)\n"
                },
                "legalEntityAssociationType": {
                  "type": "string",
                  "example": "L2",
                  "description": "`status: Provisionally Registered`\n  bian-reference: PartyRegistryEntry.RegisteredParty(as RolePlayer).Role.PartyRelationship.PartyRelationshipType\n  general-info: Legal Entity Association Type (corporate or familial)\n"
                },
                "legalEntityAssociationObligation": {
                  "type": "string",
                  "example": "Association Obligation",
                  "description": "`status: Provisionally Registered`\nbian-reference: PartyRegistryEntry.RegisteredParty(as RolePlayer).Role.PartyRelationship.RelationshipAgreement.Obligation\n general-info: Legal Entity Association Obligation (e.g. shareholder, director, guardian, guarantor)\n"
                },
                "parentLegalEntityReference": {
                  "type": "string",
                  "example": "47654676",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_yagFILl5EeOpCN0IL2Swqw)\ngeneral-info: Parent Legal Entity\n"
                },
                "subsidiaryLegalEntityReference": {
                  "type": "string",
                  "example": "47654676",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_yagFILl5EeOpCN0IL2Swqw)\ngeneral-info: Subsidiary Legal Entity Reference\n"
                },
                "shareholdingProfile": {
                  "type": "string",
                  "example": "shareholding Profile",
                  "description": "`status: Provisionally Registered`\nbian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).ShareholderRegister\n general-info: Shareholding Profile (lists major shareholders and shareholdings of significance)\n"
                }
              },
              "example": {
                "legalEntityAssociationType": "L2",
                "associationDirectoryEntryReference": "47654676",
                "subsidiaryLegalEntityReference": "47654676",
                "partyDirectoryEntryReference": "47654676",
                "legalEntityAssociationObligation": "Association Obligation",
                "shareholdingProfile": "shareholding Profile",
                "legalEntityAssociationReference": "47654676",
                "parentLegalEntityReference": "47654676"
              }
            }
          }
        }
      }
    }
  },
  "definitions": {
    "ReferenceBase": {
      "type": "object",
      "properties": {
        "legalEntityReference": {
          "type": "string",
          "example": "47654676",
          "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_yagFILl5EeOpCN0IL2Swqw)\ngeneral-info: Legal Entity\n"
        },
        "legalEntityOfficialName": {
          "type": "string",
          "example": "Entity Official Name",
          "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_E7L5qcTGEeChad0JzLk7QA_-1556021177/elements/_E7VDkMTGEeChad0JzLk7QA_151261734)\ngeneral-info: Legal Entity Official Name\n"
        },
        "legalEntityType": {
          "type": "string",
          "example": "T2",
          "description": "`status: Registered`\n iso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_zJK20OVaEeG_peKHD7roXg_-1787384341)\n general-info: Legal Entity Type\n"
        },
        "sectorsofOperation": {
          "type": "string",
          "example": "Sectors of Operation",
          "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_FNqJssTGEeChad0JzLk7QA_-694813541)\ngeneral-info: Sectors of Operation\n"
        },
        "registeredAddress": {
          "type": "string",
          "example": "Address",
          "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_w8TGEeChad0JzLk7QA_1650940768/elements/_FNg_xcTGEeChad0JzLk7QA_1331688362)\ngeneral-info: Registered Address\n"
        },
        "headquartersLocation": {
          "type": "string",
          "example": "Headquarters Location",
          "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_z2I6YGx5EeKmZJ0Ago--9g_239738909)\ngeneral-info: Headquarters Location\n"
        },
        "dateofIncorporation": {
          "type": "string",
          "example": "08/08/2018",
          "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_FNqJsMTGEeChad0JzLk7QA_-992959099)\ngeneral-info: Date Of InCorporation\n"
        },
        "jurisdictionofIncorporation": {
          "type": "string",
          "example": "Jurisdiction of Incorporation",
          "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_w8TGEeChad0JzLk7QA_1650940768/elements/__-cVZ2IiEeGD28DQaMef-g)\ngeneral-info: Jurisdiction of Incorporation\n"
        },
        "registrationAuthority": {
          "type": "string",
          "example": "Registration Authority",
          "description": "`status: Provisionally Registered`\nbian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).RegistraftionAuthority\ngeneral-info: Registration Authority\n"
        },
        "primaryRegulator": {
          "type": "string",
          "example": "Primary Regulator",
          "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FI4-csTGEeChad0JzLk7QA_-1972046907/elements/_I8jqIHQzEeKIFpWttHerUA_2136525583)\ngeneral-info: Primary Regulator\n"
        },
        "taxIdentifier": {
          "type": "string",
          "example": "Tax Identifier",
          "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_FEHzNcTGEeChad0JzLk7QA_-1792766550)\ngeneral-info: Tax Identifier\n"
        },
        "contactRole": {
          "type": "string",
          "example": "contact Role",
          "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_YaxeYNTxEeO8xr27LwkIFw)\ngeneral-info: Contact Role\n"
        },
        "contactAddressDetails": {
          "type": "string",
          "example": "Contact Address Details",
          "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\ngeneral-info: Contact Address Details\n"
        }
      },
      "example": {
        "dateofIncorporation": "08/08/2018",
        "legalEntityReference": "47654676",
        "headquartersLocation": "Headquarters Location",
        "taxIdentifier": "Tax Identifier",
        "jurisdictionofIncorporation": "Jurisdiction of Incorporation",
        "contactAddressDetails": "Contact Address Details",
        "sectorsofOperation": "Sectors of Operation",
        "primaryRegulator": "Primary Regulator",
        "registeredAddress": "Address",
        "registrationAuthority": "Registration Authority",
        "legalEntityOfficialName": "Entity Official Name",
        "legalEntityType": "T2",
        "contactRole": "contact Role"
      }
    },
    "ReferenceBaseWithId": {
      "type": "object",
      "properties": {
        "partyDirectoryEntryReference": {
          "type": "string",
          "example": "47654676",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "referenceDirectoryEntryReference": {
          "type": "string",
          "example": "47654676",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "legalEntityReference": {
          "type": "string",
          "example": "47654676",
          "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_yagFILl5EeOpCN0IL2Swqw)\ngeneral-info: Legal Entity\n"
        },
        "legalEntityOfficialName": {
          "type": "string",
          "example": "Entity Official Name",
          "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_E7L5qcTGEeChad0JzLk7QA_-1556021177/elements/_E7VDkMTGEeChad0JzLk7QA_151261734)\ngeneral-info: Entity Official Name\n"
        },
        "legalEntityType": {
          "type": "string",
          "example": "T2",
          "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_zJK20OVaEeG_peKHD7roXg_-1787384341)\ngeneral-info: Legal Entity Type\n"
        },
        "sectorsofOperation": {
          "type": "string",
          "example": "Sectors of Operation",
          "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_FNqJssTGEeChad0JzLk7QA_-694813541)\ngeneral-info: Sectors of Operation\n"
        },
        "registeredAddress": {
          "type": "string",
          "example": "Address",
          "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_w8TGEeChad0JzLk7QA_1650940768/elements/_FNg_xcTGEeChad0JzLk7QA_1331688362)\ngeneral-info: Registered Address\n"
        },
        "headquartersLocation": {
          "type": "string",
          "example": "Headquarters Location",
          "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_z2I6YGx5EeKmZJ0Ago--9g_239738909)\ngeneral-info: Headquarters Location\n"
        },
        "dateofIncorporation": {
          "type": "string",
          "example": "08/08/2018",
          "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_FNqJsMTGEeChad0JzLk7QA_-992959099)\ngeneral-info: Date Of InCorporation\n"
        },
        "jurisdictionofIncorporation": {
          "type": "string",
          "example": "Jurisdiction of Incorporation",
          "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_w8TGEeChad0JzLk7QA_1650940768/elements/__-cVZ2IiEeGD28DQaMef-g)\ngeneral-info: Jurisdiction of Incorporation\n"
        },
        "registrationAuthority": {
          "type": "string",
          "example": "Registration Authority",
          "description": "`status: Provisionally Registered`\n bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).RegistraftionAuthority\ngeneral-info: Registration Authority\n"
        },
        "primaryRegulator": {
          "type": "string",
          "example": "Primary Regulator",
          "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FI4-csTGEeChad0JzLk7QA_-1972046907/elements/_I8jqIHQzEeKIFpWttHerUA_2136525583)\ngeneral-info: Primary Regulator\n"
        },
        "taxIdentifier": {
          "type": "string",
          "example": "Tax Identifier",
          "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_FEHzNcTGEeChad0JzLk7QA_-1792766550)\ngeneral-info: Tax Identifier\n"
        },
        "contactRole": {
          "type": "string",
          "example": "contact Role",
          "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_YaxeYNTxEeO8xr27LwkIFw)\ngeneral-info: Contact Role\n"
        },
        "contactAddressDetails": {
          "type": "string",
          "example": "Contact Address Details",
          "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\ngeneral-info: Contact Address Details\n"
        }
      },
      "example": {
        "dateofIncorporation": "08/08/2018",
        "referenceDirectoryEntryReference": "47654676",
        "legalEntityReference": "47654676",
        "headquartersLocation": "Headquarters Location",
        "taxIdentifier": "Tax Identifier",
        "jurisdictionofIncorporation": "Jurisdiction of Incorporation",
        "partyDirectoryEntryReference": "47654676",
        "contactAddressDetails": "Contact Address Details",
        "sectorsofOperation": "Sectors of Operation",
        "primaryRegulator": "Primary Regulator",
        "registeredAddress": "Address",
        "registrationAuthority": "Registration Authority",
        "legalEntityOfficialName": "Entity Official Name",
        "legalEntityType": "T2",
        "contactRole": "contact Role"
      }
    },
    "PartyDataManagementRecordRequest": {
      "type": "object",
      "properties": {
        "recordingRecordType": {
          "type": "string",
          "example": "The layout/type of the feedback",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "recordingRecord": {
          "type": "object",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
          "properties": {}
        },
        "recordingRecordDateTime": {
          "type": "string",
          "pattern": "^(?:[1-9]\\d{3}-(?:(?:0[1-9]|1[0-2])-(?:0[1-9]|1\\d|2[0-8])|(?:0[13-9]|1[0-2])-(?:29|30)|(?:0[13578]|1[02])-31)|(?:[1-9]\\d(?:0[48]|[2468][048]|[13579][26])|(?:[2468][048]|[13579][26])00)-02-29)T(?:[01]\\d|2[0-3]):[0-5]\\d:[0-5]\\d(?:\\.[0-9]+)?(?:Z|[+-][01]\\d:[0-5]\\d)?$",
          "description": "`status: Registered`,\niso-link: [click_here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/datatypes/_YW1tKtp-Ed-ak6NoX_4Aeg_-1624336183)\ngeneral-info: A particular point in the progression of time defined by a mandatory date and a mandatory time component, expressed in either UTC time format (YYYY-MM-DDThh:mm:ss.sssZ), local time with UTC offset format (YYYY-MM-DDThh:mm:ss.sss+/-hh:mm), or local time format (YYYY-MM-DDThh:mm:ss.sss). These representations are defined in \"XML Schema Part 2: Datatypes Second Edition - W3C Recommendation 28 October 2004\" which is aligned with ISO 8601.\nNote on the time format:\n1) beginning / end of calendar day\n00:00:00 = the beginning of a calendar day\n24:00:00 = the end of a calendar day\n2) fractions of second in time format\nDecimal fractions of seconds may be included. In this case, the involved parties shall agree on the maximum number of digits that are allowed.\n",
          "example": "2018-09-26T05:56:05.007"
        },
        "employeeBusinessUnitReference": {
          "type": "string",
          "example": "47654676",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        }
      },
      "example": {
        "recordingRecordType": "The layout/type of the feedback",
        "employeeBusinessUnitReference": "47654676",
        "recordingRecordDateTime": "2018-09-26T05:56:05.007",
        "recordingRecord": "{}"
      }
    },
    "PartyDataManagementRecordResponse": {
      "type": "object",
      "properties": {
        "recordingRecordReference": {
          "type": "string",
          "example": "47654676",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "recordingRecordStatus": {
          "type": "string",
          "example": "Applied",
          "description": "`status: Not Mapped`\nBIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        }
      },
      "example": {
        "recordingRecordReference": "47654676",
        "recordingRecordStatus": "Applied"
      }
    },
    "ProfileBase": {
      "type": "object",
      "properties": {
        "organizationCapitalization": {
          "type": "string",
          "example": "Organization Capitalization",
          "description": "`status: Provisionally Registered`\n bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.Capitalisation\n   general-info: Organization Capitalization\n \n"
        },
        "organizationDebtLevel": {
          "type": "string",
          "example": "Organization Debt Level",
          "description": "`status: Provisionally Registered`\n  bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.DebtLevel\n   general-info: Organization Debt Level\n"
        },
        "organizationEconomicIntent": {
          "type": "string",
          "example": "Organization Economic Intent",
          "description": "`status: Provisionally Registered`\n  bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.EconomicIntent\n    general-info: Organization Economic Intent\n"
        },
        "organizationGrowthRate": {
          "type": "string",
          "example": "Organization Growth Rate",
          "description": "`status: Provisionally Registered`\n  bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.GrowthRate\n  general-info: Organization Growth Rate\n"
        },
        "organizationProfitabilityStocks": {
          "type": "string",
          "example": "Organization Profitability Stocks",
          "description": "`status: Provisionally Registered`\n bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.GrowthRate\n  general-info: Organization Profitability/Stocks\n"
        },
        "organizationRevenueTurnover": {
          "type": "string",
          "example": "Organization Revenue  Turnover",
          "description": "`status: Provisionally Registered`\n bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.Revenue\n  general-info: Organization Revenue/Turnover\n"
        }
      },
      "example": {
        "organizationDebtLevel": "Organization Debt Level",
        "organizationCapitalization": "Organization Capitalization",
        "organizationEconomicIntent": "Organization Economic Intent",
        "organizationGrowthRate": "Organization Growth Rate",
        "organizationRevenueTurnover": "Organization Revenue  Turnover",
        "organizationProfitabilityStocks": "Organization Profitability Stocks"
      }
    },
    "ProfileBaseWithId": {
      "type": "object",
      "properties": {
        "partyDirectoryEntryReference": {
          "type": "string",
          "example": "Organization Capitalization",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "profileDirectoryEntryReference": {
          "type": "string",
          "example": "Organization Capitalization",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "organizationCapitalization": {
          "type": "string",
          "example": "Organization Capitalization",
          "description": "`status: Provisionally Registered`\nbian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.Capitalisation\n  general-info: Organization Capitalization\n  \n"
        },
        "organizationDebtLevel": {
          "type": "string",
          "example": "Organization Debt Level",
          "description": "`status: Provisonally Registered`\n  bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.DebtLevel\n   general-info: Organization Debt Level\n  \n"
        },
        "organizationEconomicIntent": {
          "type": "string",
          "example": "Organization Economic Intent",
          "description": "`status: Provisionally Registered`\nbian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.EconomicIntent\n  general-info: Organization Economic Intent\n  \n"
        },
        "organizationGrowthRate": {
          "type": "string",
          "example": "Organization Growth Rate",
          "description": "`status: Provisionally Registered`\n bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.GrowthRate\n   general-info: Organization Growth Rate\n   \n \n"
        },
        "organizationProfitabilityStocks": {
          "type": "string",
          "example": "Organization Profitability Stocks",
          "description": "`status: Provisionally Registered`\n bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.GrowthRate\n general-info: Organization Profitability/Stocks\n \n"
        },
        "organizationRevenueTurnover": {
          "type": "string",
          "example": "Organization Revenue  Turnover",
          "description": "`status: Provisionally Regsitered`\n  bian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).OrganisationProfile.Revenue\n    general-info: Organization Revenue/Turnover\n"
        }
      },
      "example": {
        "organizationDebtLevel": "Organization Debt Level",
        "organizationCapitalization": "Organization Capitalization",
        "profileDirectoryEntryReference": "Organization Capitalization",
        "organizationEconomicIntent": "Organization Economic Intent",
        "organizationGrowthRate": "Organization Growth Rate",
        "organizationRevenueTurnover": "Organization Revenue  Turnover",
        "partyDirectoryEntryReference": "Organization Capitalization",
        "organizationProfitabilityStocks": "Organization Profitability Stocks"
      }
    },
    "AssociationBase": {
      "type": "object",
      "properties": {
        "legalEntityAssociationReference": {
          "type": "string",
          "example": "47654676",
          "description": "`status: Provisionally Registered`\nbian-reference: PartyRegistryEntry.RegisteredParty(as RolePlayer).Role.PartyRelationship\n general-info: Legal Entity Association Reference (company or individual)\n"
        },
        "legalEntityAssociationType": {
          "type": "string",
          "example": "L2",
          "description": "`status: Provisionally Registered`\n general-info: Legal Entity Association Reference (company or individual)\n   general-info: Legal Entity Association Type (corporate or familial)\n"
        },
        "legalEntityAssociationObligation": {
          "type": "string",
          "example": "Association Obligation",
          "description": "`status: Provisionally Registered`\nbian-reference: PartyRegistryEntry.RegisteredParty(as RolePlayer).Role.PartyRelationship.RelationshipAgreement.Obligation\ngeneral-info: Legal Entity Association Obligation (e.g. shareholder, director, guardian, guarantor)\n"
        },
        "parentLegalEntityReference": {
          "type": "string",
          "example": "47654676",
          "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_yagFILl5EeOpCN0IL2Swqw)\ngeneral-info: Parent Legal Entity\n"
        },
        "subsidiaryLegalEntityReference": {
          "type": "string",
          "example": "47654676",
          "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_yagFILl5EeOpCN0IL2Swqw)\ngeneral-info: Subsidiary Legal Entity Reference\n"
        },
        "shareholdingProfile": {
          "type": "string",
          "example": "shareholding Profile",
          "description": "`status: Provisionally Registered`\nbian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).ShareholderRegister\ngeneral-info: Shareholding Profile (lists major shareholders and shareholdings of significance) \n"
        }
      },
      "example": {
        "legalEntityAssociationType": "L2",
        "subsidiaryLegalEntityReference": "47654676",
        "legalEntityAssociationObligation": "Association Obligation",
        "shareholdingProfile": "shareholding Profile",
        "legalEntityAssociationReference": "47654676",
        "parentLegalEntityReference": "47654676"
      }
    },
    "AssociationBaseWithId": {
      "type": "object",
      "properties": {
        "partyDirectoryEntryReference": {
          "type": "string",
          "example": "47654676",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "associationDirectoryEntryReference": {
          "type": "string",
          "example": "47654676",
          "description": "`status: Not Mapped\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "legalEntityAssociationReference": {
          "type": "string",
          "example": "47654676",
          "description": "`status: Provisionally Registered`\nbian-reference: PartyRegistryEntry.RegisteredParty(as RolePlayer).Role.PartyRelationship\ngeneral-info: Legal Entity Association Reference (company or individual)\n"
        },
        "legalEntityAssociationType": {
          "type": "string",
          "example": "L2",
          "description": "`status: Provisionally Registered`\n  bian-reference: PartyRegistryEntry.RegisteredParty(as RolePlayer).Role.PartyRelationship.PartyRelationshipType\n  general-info: Legal Entity Association Type (corporate or familial)\n"
        },
        "legalEntityAssociationObligation": {
          "type": "string",
          "example": "Association Obligation",
          "description": "`status: Provisionally Registered`\nbian-reference: PartyRegistryEntry.RegisteredParty(as RolePlayer).Role.PartyRelationship.RelationshipAgreement.Obligation\n general-info: Legal Entity Association Obligation (e.g. shareholder, director, guardian, guarantor)\n"
        },
        "parentLegalEntityReference": {
          "type": "string",
          "example": "47654676",
          "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_yagFILl5EeOpCN0IL2Swqw)\ngeneral-info: Parent Legal Entity\n"
        },
        "subsidiaryLegalEntityReference": {
          "type": "string",
          "example": "47654676",
          "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_yagFILl5EeOpCN0IL2Swqw)\ngeneral-info: Subsidiary Legal Entity Reference\n"
        },
        "shareholdingProfile": {
          "type": "string",
          "example": "shareholding Profile",
          "description": "`status: Provisionally Registered`\nbian-reference: PartyRegistryEntry.RegisteredParty(as Organisation).ShareholderRegister\n general-info: Shareholding Profile (lists major shareholders and shareholdings of significance)\n"
        }
      },
      "example": {
        "legalEntityAssociationType": "L2",
        "associationDirectoryEntryReference": "47654676",
        "subsidiaryLegalEntityReference": "47654676",
        "partyDirectoryEntryReference": "47654676",
        "legalEntityAssociationObligation": "Association Obligation",
        "shareholdingProfile": "shareholding Profile",
        "legalEntityAssociationReference": "47654676",
        "parentLegalEntityReference": "47654676"
      }
    },
    "DirectoryEntryRefreshResponse": {
      "type": "object",
      "properties": {
        "refreshStatus": {
          "type": "string",
          "example": "Refreshed",
          "description": "`status: Not Mapped`\nBIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        }
      },
      "example": {
        "refreshStatus": "Refreshed"
      }
    },
    "ISODateTime": {
      "type": "string",
      "pattern": "^(?:[1-9]\\d{3}-(?:(?:0[1-9]|1[0-2])-(?:0[1-9]|1\\d|2[0-8])|(?:0[13-9]|1[0-2])-(?:29|30)|(?:0[13578]|1[02])-31)|(?:[1-9]\\d(?:0[48]|[2468][048]|[13579][26])|(?:[2468][048]|[13579][26])00)-02-29)T(?:[01]\\d|2[0-3]):[0-5]\\d:[0-5]\\d(?:\\.[0-9]+)?(?:Z|[+-][01]\\d:[0-5]\\d)?$",
      "description": "`status: Registered`,\niso-link: [click_here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/datatypes/_YW1tKtp-Ed-ak6NoX_4Aeg_-1624336183)\ngeneral-info: A particular point in the progression of time defined by a mandatory date and a mandatory time component, expressed in either UTC time format (YYYY-MM-DDThh:mm:ss.sssZ), local time with UTC offset format (YYYY-MM-DDThh:mm:ss.sss+/-hh:mm), or local time format (YYYY-MM-DDThh:mm:ss.sss). These representations are defined in \"XML Schema Part 2: Datatypes Second Edition - W3C Recommendation 28 October 2004\" which is aligned with ISO 8601.\nNote on the time format:\n1) beginning / end of calendar day\n00:00:00 = the beginning of a calendar day\n24:00:00 = the end of a calendar day\n2) fractions of second in time format\nDecimal fractions of seconds may be included. In this case, the involved parties shall agree on the maximum number of digits that are allowed.\n",
      "example": "2018-09-26T05:56:05.007"
    }
  }
}
</script>