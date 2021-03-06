---
layout: api-single
title: Customer Reference Data Management
parent-title: BIAN APIs
description: Banking API Standards - APIs - Customer Reference Data Management
keywords: 
duration: 
type: api
standard: bian
order: 4
parent: /categories/banking/bian
api-logo: /dist/images/logos/bian_logo.svg
api-summary: This service domain maintains a range customer relationship reference information covering aspects including general reference details, contacts and associations and demographic information.
api-example-use: Customer reference details are accessed to pre-populate an application form for a new product opportunity with the customer.
api-published-by: Bianuser06 Team
---
<script id="api-spec" type="application/json">
{
  "swagger": "2.0",
  "info": {
    "version": "1.0.0",
    "title": "Customer Reference Data Management",
    "description": "It maintains a range customer relationship reference information covering aspects."
  },
  "host": "bianorg.azure-api.net",
  "basePath": "/sd-cust-ref-data-mgt/v1",
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
    "/customer-reference-data-management/customer-reference-data-directory/{cr-reference-id}/references/registration": {
      "post": {
        "tags": [
          "register"
        ],
        "summary": "Register bank relationship",
        "operationId": "registerCustomerReferenceDataDirectoryEntryReference",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Reference Data Directory Entry Reference",
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
                  "example": "CR1234",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty)\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwTfUMTGEeChad0JzLk7QA_-1978180945/elements/_EwTfUcTGEeChad0JzLk7QA_434950303)\ngeneral-info: consumer\n"
                },
                "customerLegalEntityReference": {
                  "type": "string",
                  "example": "CS75433",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).Identification\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FNqJucTGEeChad0JzLk7QA_1357540588)\n"
                },
                "customerNameSalutation": {
                  "type": "string",
                  "example": "Mr.John",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).Identification.PartyName\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_FEHzN8TGEeChad0JzLk7QA_1608854558)\n"
                },
                "governmentIssuedIdentityReference": {
                  "type": "string",
                  "example": "SocialSecurityNumber",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_wetlYA93EeGeV5vP7Mvdig_1485186470)\ngeneral-info: social security number\n"
                },
                "governmentIssuedDocumentDetails": {
                  "type": "string",
                  "example": "Passport",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).PersonIdentification\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_E7VDkcTGEeChad0JzLk7QA_-2076942625/elements/_E7VDksTGEeChad0JzLk7QA_-855295891)\ngeneral-info: driving license/passport details\n"
                },
                "residencyStatus": {
                  "type": "string",
                  "example": "Own",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).ResidentialStatus\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOxsTGEeChad0JzLk7QA_-1496564084)\n"
                },
                "dateOfBirth": {
                  "type": "string",
                  "example": "1970-08-01",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).BirthDate\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOwcTGEeChad0JzLk7QA_-1677946145)\n"
                },
                "nationality": {
                  "type": "string",
                  "example": "US",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty)(asPerson).Nationality\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOxMTGEeChad0JzLk7QA_-1677946132)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).PlaceOfBirth\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOyMTGEeChad0JzLk7QA_-1037578805)\n"
                },
                "residentialAddress": {
                  "type": "string",
                  "example": "23 Dallas Texas",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).Residence\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FNz6sMTGEeChad0JzLk7QA_1111100108)\n"
                },
                "emailAddress": {
                  "type": "string",
                  "example": "john@email.co",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FQ8HM8TGEeChad0JzLk7QA_1582936206)\n"
                },
                "cellPhoneNumber": {
                  "type": "string",
                  "example": "+1-4123464748",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asPhoneAddress)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asPhoneAddress)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNz6usTGEeChad0JzLk7QA_352593535)\n"
                },
                "socialNetworkContacts": {
                  "type": "string",
                  "example": "john@twiiter",
                  "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress).SocialNetworkAddress\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress).SocialNetworkAddress\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\n"
                },
                "politicalExposureType": {
                  "type": "string",
                  "example": "Senior",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "politicalExposureRecord": {
                  "type": "object",
                  "example": "PoliticalRecord",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Binary\n",
                  "properties": {}
                },
                "corporateCustomerReference": {
                  "type": "string",
                  "example": "CCRE6010",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwTfUMTGEeChad0JzLk7QA_-1978180945/elements/_EwTfUcTGEeChad0JzLk7QA_434950303)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601)\ngeneral-info: Company\n"
                },
                "corporateCustomerLegalEntityReference": {
                  "type": "string",
                  "example": "CCLE2010",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation).OrganisationIdentification(asPartyIdentificationInformation).LEI\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_yagFILl5EeOpCN0IL2Swqw)\n"
                },
                "corporateAddress": {
                  "type": "string",
                  "example": "78B Chruch Street  Dallas Texas United States",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation).PlaceOfOperation\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_FNqJtcTGEeChad0JzLk7QA_-1846259904)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation).PlaceOfRegistration\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_FNqJtMTGEeChad0JzLk7QA_-847083437)\n"
                },
                "companyOfficerRole": {
                  "type": "string",
                  "example": "Accountant",
                  "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwKVZ8TGEeChad0JzLk7QA_-1034255710)\n"
                },
                "companyOfficerReference": {
                  "type": "string",
                  "example": "CORE1962",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager(asRole).Player(asPerson)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwTfUMTGEeChad0JzLk7QA_-1978180945/elements/_EwTfUcTGEeChad0JzLk7QA_434950303)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager(asRole).Player(asPerson)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147)\n"
                },
                "customerSinceDate": {
                  "type": "string",
                  "example": "2010-08-01",
                  "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).ApplicablePeriod.FromDateTime\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).ApplicablePeriod.FromDateTime\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FJ8HVcTGEeChad0JzLk7QA_726404707)\n"
                },
                "customerReferenceRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Binary\n",
                  "properties": {}
                }
              },
              "example": {
                "socialNetworkContacts": "john@twiiter",
                "corporateCustomerLegalEntityReference": "CCLE2010",
                "corporateCustomerReference": "CCRE6010",
                "customerNameSalutation": "Mr.John",
                "companyOfficerReference": "CORE1962",
                "dateOfBirth": "1970-08-01",
                "customerReferenceRecord": "{}",
                "customerSinceDate": "2010-08-01",
                "companyOfficerRole": "Accountant",
                "governmentIssuedIdentityReference": "SocialSecurityNumber",
                "residencyStatus": "Own",
                "emailAddress": "john@email.co",
                "politicalExposureRecord": "PoliticalRecord",
                "corporateAddress": "78B Chruch Street  Dallas Texas United States",
                "customerLegalEntityReference": "CS75433",
                "nationality": "US",
                "cellPhoneNumber": "+1-4123464748",
                "politicalExposureType": "Senior",
                "customerReference": "CR1234",
                "residentialAddress": "23 Dallas Texas",
                "governmentIssuedDocumentDetails": "Passport"
              }
            }
          }
        ],
        "responses": {
          "201": {
            "description": "Successfully registerd reference",
            "schema": {
              "type": "object",
              "properties": {
                "customerReferenceDataDirectoryEntryReference": {
                  "type": "string",
                  "example": "CRDDER679",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "referenceDirectoryEntryReference": {
                  "type": "string",
                  "example": "EX7777",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerReference": {
                  "type": "string",
                  "example": "CR1234",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty)\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwTfUMTGEeChad0JzLk7QA_-1978180945/elements/_EwTfUcTGEeChad0JzLk7QA_434950303)\ngeneral-info: consumer\n"
                },
                "customerLegalEntityReference": {
                  "type": "string",
                  "example": "CS75433",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).Identification\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FNqJucTGEeChad0JzLk7QA_1357540588)\n"
                },
                "customerNameSalutation": {
                  "type": "string",
                  "example": "Mr.John",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).Identification.PartyName\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_FEHzN8TGEeChad0JzLk7QA_1608854558)\n"
                },
                "governmentIssuedIdentityReference": {
                  "type": "string",
                  "example": "SocialSecurityNumber",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_wetlYA93EeGeV5vP7Mvdig_1485186470)\ngeneral-info: social security number\n"
                },
                "governmentIssuedDocumentDetails": {
                  "type": "string",
                  "example": "Passport",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).PersonIdentification\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_E7VDkcTGEeChad0JzLk7QA_-2076942625/elements/_E7VDksTGEeChad0JzLk7QA_-855295891)\ngeneral-info: driving license/passport details\n"
                },
                "residencyStatus": {
                  "type": "string",
                  "example": "Own",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).ResidentialStatus\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOxsTGEeChad0JzLk7QA_-1496564084)\n"
                },
                "dateOfBirth": {
                  "type": "string",
                  "example": "1970-08-01",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).BirthDate\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOwcTGEeChad0JzLk7QA_-1677946145)\n"
                },
                "nationality": {
                  "type": "string",
                  "example": "US",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty)(asPerson).Nationality\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOxMTGEeChad0JzLk7QA_-1677946132)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).PlaceOfBirth\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOyMTGEeChad0JzLk7QA_-1037578805)\n"
                },
                "residentialAddress": {
                  "type": "string",
                  "example": "23 Dallas Texas",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).Residence\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FNz6sMTGEeChad0JzLk7QA_1111100108)\n"
                },
                "emailAddress": {
                  "type": "string",
                  "example": "john@email.co",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FQ8HM8TGEeChad0JzLk7QA_1582936206)\n"
                },
                "cellPhoneNumber": {
                  "type": "string",
                  "example": "+1-4123464748",
                  "description": "`status: Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asPhoneAddress)\n iso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\n `status: Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asPhoneAddress)\n iso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNz6usTGEeChad0JzLk7QA_352593535)\n"
                },
                "socialNetworkContacts": {
                  "type": "string",
                  "example": "john@twiiter",
                  "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress).SocialNetworkAddress\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress).SocialNetworkAddress\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\n"
                },
                "politicalExposureType": {
                  "type": "string",
                  "example": "Senior",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "politicalExposureRecord": {
                  "type": "object",
                  "example": "PoliticalRecord",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Binary\n",
                  "properties": {}
                },
                "corporateCustomerReference": {
                  "type": "string",
                  "example": "CCRE6010",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation)\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwTfUMTGEeChad0JzLk7QA_-1978180945/elements/_EwTfUcTGEeChad0JzLk7QA_434950303)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601)\ngeneral-info: Company\n"
                },
                "corporateCustomerLegalEntityReference": {
                  "type": "string",
                  "example": "CCLE2010",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation).OrganisationIdentification(asPartyIdentificationInformation).LEI\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_yagFILl5EeOpCN0IL2Swqw)\n"
                },
                "corporateAddress": {
                  "type": "string",
                  "example": "78B Chruch Street  Dallas Texas United States",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation).PlaceOfOperation\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_FNqJtcTGEeChad0JzLk7QA_-1846259904)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation).PlaceOfRegistration\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_FNqJtMTGEeChad0JzLk7QA_-847083437)\n"
                },
                "companyOfficerRole": {
                  "type": "string",
                  "example": "Accountant",
                  "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwKVZ8TGEeChad0JzLk7QA_-1034255710)\n"
                },
                "companyOfficerReference": {
                  "type": "string",
                  "example": "CORE1962",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager(asRole).Player(asPerson)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwTfUMTGEeChad0JzLk7QA_-1978180945/elements/_EwTfUcTGEeChad0JzLk7QA_434950303)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager(asRole).Player(asPerson)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147)\n"
                },
                "customerSinceDate": {
                  "type": "string",
                  "example": "2010-08-01",
                  "description": "`status: Provisionally Registered`\n  bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).ApplicablePeriod.FromDateTime\n  `status: Registered`\n  bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).ApplicablePeriod.FromDateTime\n  iso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FJ8HVcTGEeChad0JzLk7QA_726404707)\n"
                },
                "customerReferenceRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Binary\n",
                  "properties": {}
                }
              },
              "example": {
                "socialNetworkContacts": "john@twiiter",
                "corporateCustomerLegalEntityReference": "CCLE2010",
                "referenceDirectoryEntryReference": "EX7777",
                "corporateCustomerReference": "CCRE6010",
                "customerNameSalutation": "Mr.John",
                "companyOfficerReference": "CORE1962",
                "dateOfBirth": "1970-08-01",
                "customerReferenceRecord": "{}",
                "customerSinceDate": "2010-08-01",
                "companyOfficerRole": "Accountant",
                "governmentIssuedIdentityReference": "SocialSecurityNumber",
                "residencyStatus": "Own",
                "emailAddress": "john@email.co",
                "politicalExposureRecord": "PoliticalRecord",
                "corporateAddress": "78B Chruch Street  Dallas Texas United States",
                "customerLegalEntityReference": "CS75433",
                "nationality": "US",
                "cellPhoneNumber": "+1-4123464748",
                "customerReferenceDataDirectoryEntryReference": "CRDDER679",
                "politicalExposureType": "Senior",
                "customerReference": "CR1234",
                "residentialAddress": "23 Dallas Texas",
                "governmentIssuedDocumentDetails": "Passport"
              }
            }
          }
        }
      }
    },
    "/customer-reference-data-management/customer-reference-data-directory/{cr-reference-id}/associations/registration": {
      "post": {
        "tags": [
          "register"
        ],
        "summary": "Register a customer relationship",
        "description": "Register: Customer relationships/association detail",
        "operationId": "registerCustomerReferenceDataDirectoryRelationship",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Reference Data Directory Entry Reference",
            "required": true,
            "type": "string"
          },
          {
            "in": "body",
            "name": "body",
            "required": false,
            "schema": {
              "type": "object",
              "properties": {
                "customerReference": {
                  "type": "string",
                  "example": "CR3816",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "employeeReference": {
                  "type": "string",
                  "example": "EMPR3816",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager(asRole).Player(asPerson).EmployerIdentificationNumber\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_E7VDkcTGEeChad0JzLk7QA_-2076942625/elements/_E7VDlcTGEeChad0JzLk7QA_-912215424)\n"
                },
                "associateType": {
                  "type": "string",
                  "example": "Familial",
                  "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).PartyRelationship.PartyRelationshipType\ngeneral-info: familial or corporate\n"
                },
                "associateReference": {
                  "type": "string",
                  "example": "ASRE4820",
                  "description": "`status: Provisionally Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).PartyRelationship\n"
                },
                "associateObligationDependencyDescription": {
                  "type": "string",
                  "example": "Legal Assistant Obligation",
                  "description": "`status: Provisionally Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).PartyRelationship.Agreement\n"
                },
                "associationValidFromTo": {
                  "type": "string",
                  "example": "2017-07-01 To 2018-07-31",
                  "description": "`status: Provisionally Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).PartyRelationship.ValidityPeriod\n"
                },
                "productInstanceReference": {
                  "type": "string",
                  "example": "PRIR5859",
                  "description": "`status: Provisionally Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).PartyRelationship.RelationshipAgreement.Product\ngeneral-info: association tied to bank product/service\n"
                },
                "preferredBeneficiary": {
                  "type": "string",
                  "example": "Father",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player.Role(asAccountPartyRole).Account.A\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EuN0p8TGEeChad0JzLk7QA_-1821987913)\ngeneral-info: list\n"
                },
                "proxyRepresentativePowerOfAttorneyReference": {
                  "type": "string",
                  "example": "PRPA7398",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).PowerOfAttorney\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/___CLVmIiEeGD28DQaMef-g)\n"
                }
              },
              "example": {
                "associateObligationDependencyDescription": "Legal Assistant Obligation",
                "productInstanceReference": "PRIR5859",
                "associateReference": "ASRE4820",
                "preferredBeneficiary": "Father",
                "employeeReference": "EMPR3816",
                "customerReference": "CR3816",
                "associateType": "Familial",
                "associationValidFromTo": "2017-07-01 To 2018-07-31",
                "proxyRepresentativePowerOfAttorneyReference": "PRPA7398"
              }
            }
          }
        ],
        "responses": {
          "201": {
            "description": "Successfully registered an association",
            "schema": {
              "type": "object",
              "properties": {
                "customerReferenceDataDirectoryEntryReference": {
                  "type": "string",
                  "example": "CRDDER679",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "associationsDirectoryEntryReference": {
                  "type": "string",
                  "example": "ADER123",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerReference": {
                  "type": "string",
                  "example": "CR3816",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "employeeReference": {
                  "type": "string",
                  "example": "EMPR3816",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager(asRole).Player(asPerson).EmployerIdentificationNumber\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_E7VDkcTGEeChad0JzLk7QA_-2076942625/elements/_E7VDlcTGEeChad0JzLk7QA_-912215424)\n"
                },
                "associateType": {
                  "type": "string",
                  "example": "Familial",
                  "description": "`status: Provisionally Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).PartyRelationship.PartyRelationshipType\n general-info: familial or corporate\n"
                },
                "associateReference": {
                  "type": "string",
                  "example": "ASRE4820",
                  "description": "`status: Provisionally Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).PartyRelationship\n"
                },
                "associateObligationDependencyDescription": {
                  "type": "string",
                  "example": "Legal Assistant Obligation",
                  "description": "`status: Provisionally Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).PartyRelationship.Agreement\n"
                },
                "associationValidFromTo": {
                  "type": "string",
                  "example": "2017-07-01 To 2018-07-31",
                  "description": "`status: Provisionally Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).PartyRelationship.ValidityPeriod\n"
                },
                "productInstanceReference": {
                  "type": "string",
                  "example": "PRIR5859",
                  "description": "`status: Provisionally Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).PartyRelationship.RelationshipAgreement.Product\n general-info: association tied to bank product/service\n"
                },
                "preferredBeneficiary": {
                  "type": "string",
                  "example": "Father",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player.Role(asAccountPartyRole).Account.A\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EuN0p8TGEeChad0JzLk7QA_-1821987913)\ngeneral-info: list\n"
                },
                "proxyRepresentativePowerOfAttorneyReference": {
                  "type": "string",
                  "example": "PRPA7398",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).PowerOfAttorney\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/___CLVmIiEeGD28DQaMef-g)\n"
                }
              },
              "example": {
                "associateObligationDependencyDescription": "Legal Assistant Obligation",
                "productInstanceReference": "PRIR5859",
                "associateReference": "ASRE4820",
                "preferredBeneficiary": "Father",
                "employeeReference": "EMPR3816",
                "customerReferenceDataDirectoryEntryReference": "CRDDER679",
                "customerReference": "CR3816",
                "associateType": "Familial",
                "associationValidFromTo": "2017-07-01 To 2018-07-31",
                "proxyRepresentativePowerOfAttorneyReference": "PRPA7398",
                "associationsDirectoryEntryReference": "ADER123"
              }
            }
          }
        }
      }
    },
    "/customer-reference-data-management/customer-reference-data-directory/{cr-reference-id}/demographics/registration": {
      "post": {
        "tags": [
          "register"
        ],
        "summary": "Register demographic details",
        "operationId": "registerCustomerReferenceDataDirectoryDemographic",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Reference Data Directory Entry Reference",
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
                  "example": "CSRE3456",
                  "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer\n"
                },
                "socioEconomicClassification": {
                  "type": "string",
                  "example": "High",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).Household\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_0Lx2wLZeEeOpCN0IL2Swqw)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).PersonProfile\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_q6wNUB9uEeO3iLV2voicmw)\n"
                },
                "ethnicityReligion": {
                  "type": "string",
                  "example": "Christian",
                  "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).Ethnicity\n`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).Religion\n"
                },
                "employment": {
                  "type": "string",
                  "example": "Analyst",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty)(asPerson).PersonProfile.SalaryRange\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_ZUHGwB9uEeO3iLV2voicmw/elements/_FNg_wMTGEeChad0JzLk7QA_666058283)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty)(asPerson).Profession\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOx8TGEeChad0JzLk7QA_-382216715)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).EmployerIdentificationNumber\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_E7VDkcTGEeChad0JzLk7QA_-2076942625/elements/_E7VDlcTGEeChad0JzLk7QA_-912215424)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.(asRole).Player(asParty)(asPerson).PersonProfile.EmploymentTerminationIndicator\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_ZUHGwB9uEeO3iLV2voicmw/elements/_SfbZ0CHSEeO3iLV2voicmw)\ngeneral-info: employer and position\n"
                },
                "employmentHistory": {
                  "type": "string",
                  "example": "2 Years in Google",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\ngeneral-info: employer, job position, salary\n"
                },
                "educationHistory": {
                  "type": "string",
                  "example": "Post Graduate From MIT University",
                  "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.(asRole).Player(asPerson).EducationLevel\n general-info: academic institutions, duration, certifications\n"
                },
                "servicingConstraints": {
                  "type": "string",
                  "example": "Collective",
                  "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.CustomerMasterAgreement(asAgreement).TermsAndConditions\n`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.CustomerMasterAgreement.TermsAndConditions\n"
                }
              },
              "example": {
                "employmentHistory": "2 Years in Google",
                "ethnicityReligion": "Christian",
                "servicingConstraints": "Collective",
                "customerReference": "CSRE3456",
                "socioEconomicClassification": "High",
                "employment": "Analyst",
                "educationHistory": "Post Graduate From MIT University"
              }
            }
          }
        ],
        "responses": {
          "201": {
            "description": "Successfully registered a demographic.",
            "schema": {
              "type": "object",
              "properties": {
                "customerReferenceDataDirectoryEntryReference": {
                  "type": "string",
                  "example": "CRDDER679",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "demographicsDirectoryEntryReference": {
                  "type": "string",
                  "example": "CSRE3456",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerReference": {
                  "type": "string",
                  "example": "CSRE3456",
                  "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer\n"
                },
                "socioEconomicClassification": {
                  "type": "string",
                  "example": "High",
                  "description": "`status: Registered`\n  bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).Household\n  iso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_0Lx2wLZeEeOpCN0IL2Swqw)\n  `status: Registered`\n  bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).PersonProfile\n  iso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_q6wNUB9uEeO3iLV2voicmw)\n"
                },
                "ethnicityReligion": {
                  "type": "string",
                  "example": "Christian",
                  "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).Ethnicity\n`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).Religion\n"
                },
                "employment": {
                  "type": "string",
                  "example": "Analyst",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty)(asPerson).PersonProfile.SalaryRange\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_ZUHGwB9uEeO3iLV2voicmw/elements/_FNg_wMTGEeChad0JzLk7QA_666058283)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty)(asPerson).Profession\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOx8TGEeChad0JzLk7QA_-382216715)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).EmployerIdentificationNumber\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_E7VDkcTGEeChad0JzLk7QA_-2076942625/elements/_E7VDlcTGEeChad0JzLk7QA_-912215424)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.(asRole).Player(asParty)(asPerson).PersonProfile.EmploymentTerminationIndicator\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_ZUHGwB9uEeO3iLV2voicmw/elements/_SfbZ0CHSEeO3iLV2voicmw)\ngeneral-info: employer and position\n"
                },
                "employmentHistory": {
                  "type": "string",
                  "example": "2 Years in Google",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\ngeneral-info: employer, job position, salary\n"
                },
                "educationHistory": {
                  "type": "string",
                  "example": "Post Graduate From MIT University",
                  "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.(asRole).Player(asPerson).EducationLevel\n  general-info: academic institutions, duration, certifications\n"
                },
                "servicingConstraints": {
                  "type": "string",
                  "example": "Collective",
                  "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.CustomerMasterAgreement(asAgreement).TermsAndConditions\n`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.CustomerMasterAgreement.TermsAndConditions\n"
                }
              },
              "example": {
                "employmentHistory": "2 Years in Google",
                "ethnicityReligion": "Christian",
                "servicingConstraints": "Collective",
                "demographicsDirectoryEntryReference": "CSRE3456",
                "customerReferenceDataDirectoryEntryReference": "CRDDER679",
                "customerReference": "CSRE3456",
                "socioEconomicClassification": "High",
                "employment": "Analyst",
                "educationHistory": "Post Graduate From MIT University"
              }
            }
          }
        }
      }
    },
    "/customer-reference-data-management/customer-reference-data-directory/{cr-reference-id}/bankrelations/registration": {
      "post": {
        "tags": [
          "register"
        ],
        "summary": "Register bank relationship",
        "operationId": "registerCustomerReferenceDataDirectoryBankRelationship",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Reference Data Directory Entry Reference",
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
                  "example": "CSRE3456",
                  "description": "`status: Provisionally Registered`\n  bian-reference:  CustomerRegistryEntry.RegisteredCustomer\n"
                },
                "bankRelationType": {
                  "type": "string",
                  "example": "Agent",
                  "description": "`status: Provisionally Registered`\n  bian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager\n  general-info: relationship manager\n"
                },
                "businessUnitEmployeeReference": {
                  "type": "string",
                  "example": "BUER2920",
                  "description": "`status: Provisionally Registered`\n  bian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager.BusinessUnit\n"
                }
              },
              "example": {
                "customerReference": "CSRE3456",
                "businessUnitEmployeeReference": "BUER2920",
                "bankRelationType": "Agent"
              }
            }
          }
        ],
        "responses": {
          "201": {
            "description": "Successfully registerd a bank relation",
            "schema": {
              "type": "object",
              "properties": {
                "customerReferenceDataDirectoryEntryReference": {
                  "type": "string",
                  "example": "CRDDER679",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "bankRelationsDirectoryEntryReference": {
                  "type": "string",
                  "example": "BR73654",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerReference": {
                  "type": "string",
                  "example": "CSRE3456",
                  "description": "`status: Provisionally Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer\n"
                },
                "bankRelationType": {
                  "type": "string",
                  "example": "Agent",
                  "description": "`status: Provisionally Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager\n general-info: relationship manager\n"
                },
                "businessUnitEmployeeReference": {
                  "type": "string",
                  "example": "BUER2920",
                  "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager.BusinessUnit\n"
                }
              },
              "example": {
                "customerReferenceDataDirectoryEntryReference": "CRDDER679",
                "customerReference": "CSRE3456",
                "businessUnitEmployeeReference": "BUER2920",
                "bankRelationsDirectoryEntryReference": "BR73654",
                "bankRelationType": "Agent"
              }
            }
          }
        }
      }
    },
    "/customer-reference-data-management/customer-reference-data-directory/": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve Control Record Ids.",
        "operationId": "RetrieveCustomerReferenceManagementReferenceIds",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "collection-filter",
            "in": "query",
            "description": "Filter to refine the result set. ex- \"customer-reference== 'CR123'\"",
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
                "CREF123",
                "CREF345"
              ]
            }
          }
        }
      }
    },
    "/customer-reference-data-management/customer-reference-data-directory/behavior-qualifiers/": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve all Behaviour Qualifier",
        "operationId": "RetrieveCustomerReferenceDataManagementBehaviorQualifiers",
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
                "reference",
                "associations",
                "demographics",
                "bankrelations"
              ]
            }
          }
        }
      }
    },
    "/customer-reference-data-management/customer-reference-data-directory/{cr-reference-id}/{behavior-qualifier}/": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve Behaviour Qualifier Ids.",
        "operationId": "RetrieveBehaviorQualifierReferenceIds",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Reference Data Management Directory Entry Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "behavior-qualifier",
            "in": "path",
            "description": "Behavior Qualifier Name. ex- bankrelations",
            "required": true,
            "type": "string"
          },
          {
            "name": "collection-filter",
            "in": "query",
            "description": "Filter to refine the result set. ex- \"'bankRelationType == RM'\"",
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
                "ODER345",
                "ODER789",
                "ODER456"
              ]
            }
          }
        }
      }
    },
    "/customer-reference-data-management/customer-reference-data-directory/{cr-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve Customer reference data management master record",
        "operationId": "retrieveCustomerReferenceDataDirectory",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Reference Data Management Directory Entry Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "Successfully retrieved Customer Reference Data Directory.",
            "schema": {
              "type": "object",
              "properties": {
                "customerReferenceDataDirectoryEntryReference": {
                  "type": "string",
                  "example": "CRDDER679",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                }
              },
              "example": {
                "customerReferenceDataDirectoryEntryReference": "CRDDER679"
              }
            }
          }
        }
      }
    },
    "/customer-reference-data-management/customer-reference-data-directory/{cr-reference-id}/references/{bq-reference-id}/": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve a reference",
        "operationId": "retrieveCustomerReferenceDataDirectoryReferences",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Reference Data Directory Entry Reference",
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
            "description": "Successfully retrieved Customer Reference Data Directory References.",
            "schema": {
              "type": "object",
              "properties": {
                "customerReferenceDataDirectoryEntryReference": {
                  "type": "string",
                  "example": "CRDDER679",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "referenceDirectoryEntryReference": {
                  "type": "string",
                  "example": "EX7777",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerReference": {
                  "type": "string",
                  "example": "CR1234",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty)\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwTfUMTGEeChad0JzLk7QA_-1978180945/elements/_EwTfUcTGEeChad0JzLk7QA_434950303)\ngeneral-info: consumer\n"
                },
                "customerLegalEntityReference": {
                  "type": "string",
                  "example": "CS75433",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).Identification\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FNqJucTGEeChad0JzLk7QA_1357540588)\n"
                },
                "customerNameSalutation": {
                  "type": "string",
                  "example": "Mr.John",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).Identification.PartyName\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_FEHzN8TGEeChad0JzLk7QA_1608854558)\n"
                },
                "governmentIssuedIdentityReference": {
                  "type": "string",
                  "example": "SocialSecurityNumber",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_wetlYA93EeGeV5vP7Mvdig_1485186470)\ngeneral-info: social security number\n"
                },
                "governmentIssuedDocumentDetails": {
                  "type": "string",
                  "example": "Passport",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).PersonIdentification\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_E7VDkcTGEeChad0JzLk7QA_-2076942625/elements/_E7VDksTGEeChad0JzLk7QA_-855295891)\ngeneral-info: driving license/passport details\n"
                },
                "residencyStatus": {
                  "type": "string",
                  "example": "Own",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).ResidentialStatus\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOxsTGEeChad0JzLk7QA_-1496564084)\n"
                },
                "dateOfBirth": {
                  "type": "string",
                  "example": "1970-08-01",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).BirthDate\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOwcTGEeChad0JzLk7QA_-1677946145)\n"
                },
                "nationality": {
                  "type": "string",
                  "example": "US",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty)(asPerson).Nationality\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOxMTGEeChad0JzLk7QA_-1677946132)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).PlaceOfBirth\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOyMTGEeChad0JzLk7QA_-1037578805)\n"
                },
                "residentialAddress": {
                  "type": "string",
                  "example": "23 Dallas Texas",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).Residence\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FNz6sMTGEeChad0JzLk7QA_1111100108)\n"
                },
                "emailAddress": {
                  "type": "string",
                  "example": "john@email.co",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FQ8HM8TGEeChad0JzLk7QA_1582936206)\n"
                },
                "cellPhoneNumber": {
                  "type": "string",
                  "example": "+1-4123464748",
                  "description": "`status: Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asPhoneAddress)\n iso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\n `status: Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asPhoneAddress)\n iso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNz6usTGEeChad0JzLk7QA_352593535)\n"
                },
                "socialNetworkContacts": {
                  "type": "string",
                  "example": "john@twiiter",
                  "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress).SocialNetworkAddress\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress).SocialNetworkAddress\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\n"
                },
                "politicalExposureType": {
                  "type": "string",
                  "example": "Senior",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "politicalExposureRecord": {
                  "type": "object",
                  "example": "PoliticalRecord",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Binary\n",
                  "properties": {}
                },
                "corporateCustomerReference": {
                  "type": "string",
                  "example": "CCRE6010",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation)\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwTfUMTGEeChad0JzLk7QA_-1978180945/elements/_EwTfUcTGEeChad0JzLk7QA_434950303)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601)\ngeneral-info: Company\n"
                },
                "corporateCustomerLegalEntityReference": {
                  "type": "string",
                  "example": "CCLE2010",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation).OrganisationIdentification(asPartyIdentificationInformation).LEI\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_yagFILl5EeOpCN0IL2Swqw)\n"
                },
                "corporateAddress": {
                  "type": "string",
                  "example": "78B Chruch Street  Dallas Texas United States",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation).PlaceOfOperation\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_FNqJtcTGEeChad0JzLk7QA_-1846259904)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation).PlaceOfRegistration\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_FNqJtMTGEeChad0JzLk7QA_-847083437)\n"
                },
                "companyOfficerRole": {
                  "type": "string",
                  "example": "Accountant",
                  "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwKVZ8TGEeChad0JzLk7QA_-1034255710)\n"
                },
                "companyOfficerReference": {
                  "type": "string",
                  "example": "CORE1962",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager(asRole).Player(asPerson)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwTfUMTGEeChad0JzLk7QA_-1978180945/elements/_EwTfUcTGEeChad0JzLk7QA_434950303)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager(asRole).Player(asPerson)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147)\n"
                },
                "customerSinceDate": {
                  "type": "string",
                  "example": "2010-08-01",
                  "description": "`status: Provisionally Registered`\n  bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).ApplicablePeriod.FromDateTime\n  `status: Registered`\n  bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).ApplicablePeriod.FromDateTime\n  iso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FJ8HVcTGEeChad0JzLk7QA_726404707)\n"
                },
                "customerReferenceRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Binary\n",
                  "properties": {}
                }
              },
              "example": {
                "socialNetworkContacts": "john@twiiter",
                "corporateCustomerLegalEntityReference": "CCLE2010",
                "referenceDirectoryEntryReference": "EX7777",
                "corporateCustomerReference": "CCRE6010",
                "customerNameSalutation": "Mr.John",
                "companyOfficerReference": "CORE1962",
                "dateOfBirth": "1970-08-01",
                "customerReferenceRecord": "{}",
                "customerSinceDate": "2010-08-01",
                "companyOfficerRole": "Accountant",
                "governmentIssuedIdentityReference": "SocialSecurityNumber",
                "residencyStatus": "Own",
                "emailAddress": "john@email.co",
                "politicalExposureRecord": "PoliticalRecord",
                "corporateAddress": "78B Chruch Street  Dallas Texas United States",
                "customerLegalEntityReference": "CS75433",
                "nationality": "US",
                "cellPhoneNumber": "+1-4123464748",
                "customerReferenceDataDirectoryEntryReference": "CRDDER679",
                "politicalExposureType": "Senior",
                "customerReference": "CR1234",
                "residentialAddress": "23 Dallas Texas",
                "governmentIssuedDocumentDetails": "Passport"
              }
            }
          }
        }
      }
    },
    "/customer-reference-data-management/customer-reference-data-directory/{cr-reference-id}/associations/{bq-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve an Associate",
        "operationId": "retrieveCustomerReferenceDataDirectoryAssociates",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Reference Data Directory Entry Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Associations Directory Entry Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "Successfully retrieved customer reference data directory associates.",
            "schema": {
              "type": "object",
              "properties": {
                "customerReferenceDataDirectoryEntryReference": {
                  "type": "string",
                  "example": "CRDDER679",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "associationsDirectoryEntryReference": {
                  "type": "string",
                  "example": "ADER123",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerReference": {
                  "type": "string",
                  "example": "CR3816",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "employeeReference": {
                  "type": "string",
                  "example": "EMPR3816",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager(asRole).Player(asPerson).EmployerIdentificationNumber\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_E7VDkcTGEeChad0JzLk7QA_-2076942625/elements/_E7VDlcTGEeChad0JzLk7QA_-912215424)\n"
                },
                "associateType": {
                  "type": "string",
                  "example": "Familial",
                  "description": "`status: Provisionally Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).PartyRelationship.PartyRelationshipType\n general-info: familial or corporate\n"
                },
                "associateReference": {
                  "type": "string",
                  "example": "ASRE4820",
                  "description": "`status: Provisionally Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).PartyRelationship\n"
                },
                "associateObligationDependencyDescription": {
                  "type": "string",
                  "example": "Legal Assistant Obligation",
                  "description": "`status: Provisionally Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).PartyRelationship.Agreement\n"
                },
                "associationValidFromTo": {
                  "type": "string",
                  "example": "2017-07-01 To 2018-07-31",
                  "description": "`status: Provisionally Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).PartyRelationship.ValidityPeriod\n"
                },
                "productInstanceReference": {
                  "type": "string",
                  "example": "PRIR5859",
                  "description": "`status: Provisionally Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).PartyRelationship.RelationshipAgreement.Product\n general-info: association tied to bank product/service\n"
                },
                "preferredBeneficiary": {
                  "type": "string",
                  "example": "Father",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player.Role(asAccountPartyRole).Account.A\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EuN0p8TGEeChad0JzLk7QA_-1821987913)\ngeneral-info: list\n"
                },
                "proxyRepresentativePowerOfAttorneyReference": {
                  "type": "string",
                  "example": "PRPA7398",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).PowerOfAttorney\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/___CLVmIiEeGD28DQaMef-g)\n"
                }
              },
              "example": {
                "associateObligationDependencyDescription": "Legal Assistant Obligation",
                "productInstanceReference": "PRIR5859",
                "associateReference": "ASRE4820",
                "preferredBeneficiary": "Father",
                "employeeReference": "EMPR3816",
                "customerReferenceDataDirectoryEntryReference": "CRDDER679",
                "customerReference": "CR3816",
                "associateType": "Familial",
                "associationValidFromTo": "2017-07-01 To 2018-07-31",
                "proxyRepresentativePowerOfAttorneyReference": "PRPA7398",
                "associationsDirectoryEntryReference": "ADER123"
              }
            }
          }
        }
      }
    },
    "/customer-reference-data-management/customer-reference-data-directory/{cr-reference-id}/demographics/{bq-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve a Demographic",
        "operationId": "retrieveCustomerReferenceDataDirectoryDemographics",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Reference Data Directory Entry Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Demographics Directory Entry Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "Successfully retrieved customer reference data directory demographics.",
            "schema": {
              "type": "object",
              "properties": {
                "customerReferenceDataDirectoryEntryReference": {
                  "type": "string",
                  "example": "CRDDER679",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "demographicsDirectoryEntryReference": {
                  "type": "string",
                  "example": "CSRE3456",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerReference": {
                  "type": "string",
                  "example": "CSRE3456",
                  "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer\n"
                },
                "socioEconomicClassification": {
                  "type": "string",
                  "example": "High",
                  "description": "`status: Registered`\n  bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).Household\n  iso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_0Lx2wLZeEeOpCN0IL2Swqw)\n  `status: Registered`\n  bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).PersonProfile\n  iso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_q6wNUB9uEeO3iLV2voicmw)\n"
                },
                "ethnicityReligion": {
                  "type": "string",
                  "example": "Christian",
                  "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).Ethnicity\n`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).Religion\n"
                },
                "employment": {
                  "type": "string",
                  "example": "Analyst",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty)(asPerson).PersonProfile.SalaryRange\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_ZUHGwB9uEeO3iLV2voicmw/elements/_FNg_wMTGEeChad0JzLk7QA_666058283)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty)(asPerson).Profession\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOx8TGEeChad0JzLk7QA_-382216715)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).EmployerIdentificationNumber\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_E7VDkcTGEeChad0JzLk7QA_-2076942625/elements/_E7VDlcTGEeChad0JzLk7QA_-912215424)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.(asRole).Player(asParty)(asPerson).PersonProfile.EmploymentTerminationIndicator\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_ZUHGwB9uEeO3iLV2voicmw/elements/_SfbZ0CHSEeO3iLV2voicmw)\ngeneral-info: employer and position\n"
                },
                "employmentHistory": {
                  "type": "string",
                  "example": "2 Years in Google",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\ngeneral-info: employer, job position, salary\n"
                },
                "educationHistory": {
                  "type": "string",
                  "example": "Post Graduate From MIT University",
                  "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.(asRole).Player(asPerson).EducationLevel\n  general-info: academic institutions, duration, certifications\n"
                },
                "servicingConstraints": {
                  "type": "string",
                  "example": "Collective",
                  "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.CustomerMasterAgreement(asAgreement).TermsAndConditions\n`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.CustomerMasterAgreement.TermsAndConditions\n"
                }
              },
              "example": {
                "employmentHistory": "2 Years in Google",
                "ethnicityReligion": "Christian",
                "servicingConstraints": "Collective",
                "demographicsDirectoryEntryReference": "CSRE3456",
                "customerReferenceDataDirectoryEntryReference": "CRDDER679",
                "customerReference": "CSRE3456",
                "socioEconomicClassification": "High",
                "employment": "Analyst",
                "educationHistory": "Post Graduate From MIT University"
              }
            }
          }
        }
      }
    },
    "/customer-reference-data-management/customer-reference-data-directory/{cr-reference-id}/bankrelations/{bq-reference-id}": {
      "get": {
        "tags": [
          "retrieve"
        ],
        "summary": "Retrieve a Bank Relation",
        "operationId": "retrieveCustomerReferenceDataDirectoryBankRelations",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Reference Data Directory Entry Reference",
            "required": true,
            "type": "string"
          },
          {
            "name": "bq-reference-id",
            "in": "path",
            "description": "Bank Relations Directory Entry Reference",
            "required": true,
            "type": "string"
          }
        ],
        "responses": {
          "200": {
            "description": "Successfully retrieved customer reference data directory bank relations.",
            "schema": {
              "type": "object",
              "properties": {
                "customerReferenceDataDirectoryEntryReference": {
                  "type": "string",
                  "example": "CRDDER679",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "bankRelationsDirectoryEntryReference": {
                  "type": "string",
                  "example": "BR73654",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerReference": {
                  "type": "string",
                  "example": "CSRE3456",
                  "description": "`status: Provisionally Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer\n"
                },
                "bankRelationType": {
                  "type": "string",
                  "example": "Agent",
                  "description": "`status: Provisionally Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager\n general-info: relationship manager\n"
                },
                "businessUnitEmployeeReference": {
                  "type": "string",
                  "example": "BUER2920",
                  "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager.BusinessUnit\n"
                }
              },
              "example": {
                "customerReferenceDataDirectoryEntryReference": "CRDDER679",
                "customerReference": "CSRE3456",
                "businessUnitEmployeeReference": "BUER2920",
                "bankRelationsDirectoryEntryReference": "BR73654",
                "bankRelationType": "Agent"
              }
            }
          }
        }
      }
    },
    "/customer-reference-data-management/customer-reference-data-directory/{cr-reference-id}/recording": {
      "post": {
        "tags": [
          "record"
        ],
        "summary": "Record a feedback",
        "operationId": "RecordCustomerDataDirectory",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Reference Data Directory Entry Reference",
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
                  "example": "Behavior Model Performance Feedback",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "recordingRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
                  "properties": {}
                },
                "recordingRecordDateTime": {
                  "type": "string",
                  "example": "2018-08-28T09:00:00",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
                },
                "empolyeeBusinessUnitReference": {
                  "type": "string",
                  "example": "EBUR6798",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                }
              },
              "example": {
                "recordingRecordType": "Behavior Model Performance Feedback",
                "empolyeeBusinessUnitReference": "EBUR6798",
                "recordingRecordDateTime": "2018-08-28T09:00:00",
                "recordingRecord": "{}"
              }
            }
          }
        ],
        "responses": {
          "201": {
            "description": "Successfuly recorded usage against customer directory entry.",
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
    "/customer-reference-data-management/customer-reference-data-directory/{cr-reference-id}/requisition": {
      "put": {
        "tags": [
          "request"
        ],
        "summary": "Request a Directory Update",
        "operationId": "RequestCustomerReferenceDataDirectoryUpdate",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Reference Data Directory Entry Reference",
            "required": true,
            "type": "string"
          },
          {
            "in": "body",
            "name": "body",
            "description": "Request customer reference request payload",
            "required": true,
            "schema": {
              "type": "object",
              "properties": {
                "customerReference": {
                  "type": "string",
                  "example": "CR1234",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty)\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwTfUMTGEeChad0JzLk7QA_-1978180945/elements/_EwTfUcTGEeChad0JzLk7QA_434950303)\ngeneral-info: consumer\n"
                },
                "customerLegalEntityReference": {
                  "type": "string",
                  "example": "CS75433",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).Identification\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FNqJucTGEeChad0JzLk7QA_1357540588)\n"
                },
                "customerNameSalutation": {
                  "type": "string",
                  "example": "Mr.John",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).Identification.PartyName\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_FEHzN8TGEeChad0JzLk7QA_1608854558)\n"
                },
                "governmentIssuedIdentityReference": {
                  "type": "string",
                  "example": "SocialSecurityNumber",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_wetlYA93EeGeV5vP7Mvdig_1485186470)\ngeneral-info: social security number\n"
                },
                "governmentIssuedDocumentDetails": {
                  "type": "string",
                  "example": "Passport",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).PersonIdentification\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_E7VDkcTGEeChad0JzLk7QA_-2076942625/elements/_E7VDksTGEeChad0JzLk7QA_-855295891)\ngeneral-info: driving license/passport details\n"
                },
                "residencyStatus": {
                  "type": "string",
                  "example": "Own",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).ResidentialStatus\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOxsTGEeChad0JzLk7QA_-1496564084)\n"
                },
                "dateOfBirth": {
                  "type": "string",
                  "example": "1970-08-01",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).BirthDate\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOwcTGEeChad0JzLk7QA_-1677946145)\n"
                },
                "nationality": {
                  "type": "string",
                  "example": "US",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty)(asPerson).Nationality\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOxMTGEeChad0JzLk7QA_-1677946132)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).PlaceOfBirth\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOyMTGEeChad0JzLk7QA_-1037578805)\n"
                },
                "residentialAddress": {
                  "type": "string",
                  "example": "23 Dallas Texas",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).Residence\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FNz6sMTGEeChad0JzLk7QA_1111100108)\n"
                },
                "emailAddress": {
                  "type": "string",
                  "example": "john@email.co",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FQ8HM8TGEeChad0JzLk7QA_1582936206)\n"
                },
                "cellPhoneNumber": {
                  "type": "string",
                  "example": "+1-4123464748",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asPhoneAddress)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asPhoneAddress)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNz6usTGEeChad0JzLk7QA_352593535)\n"
                },
                "socialNetworkContacts": {
                  "type": "string",
                  "example": "john@twiiter",
                  "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress).SocialNetworkAddress\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress).SocialNetworkAddress\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\n"
                },
                "politicalExposureType": {
                  "type": "string",
                  "example": "Senior",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "politicalExposureRecord": {
                  "type": "object",
                  "example": "PoliticalRecord",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Binary\n",
                  "properties": {}
                },
                "corporateCustomerReference": {
                  "type": "string",
                  "example": "CCRE6010",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwTfUMTGEeChad0JzLk7QA_-1978180945/elements/_EwTfUcTGEeChad0JzLk7QA_434950303)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601)\ngeneral-info: Company\n"
                },
                "corporateCustomerLegalEntityReference": {
                  "type": "string",
                  "example": "CCLE2010",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation).OrganisationIdentification(asPartyIdentificationInformation).LEI\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_yagFILl5EeOpCN0IL2Swqw)\n"
                },
                "corporateAddress": {
                  "type": "string",
                  "example": "78B Chruch Street  Dallas Texas United States",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation).PlaceOfOperation\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_FNqJtcTGEeChad0JzLk7QA_-1846259904)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation).PlaceOfRegistration\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_FNqJtMTGEeChad0JzLk7QA_-847083437)\n"
                },
                "companyOfficerRole": {
                  "type": "string",
                  "example": "Accountant",
                  "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwKVZ8TGEeChad0JzLk7QA_-1034255710)\n"
                },
                "companyOfficerReference": {
                  "type": "string",
                  "example": "CORE1962",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager(asRole).Player(asPerson)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwTfUMTGEeChad0JzLk7QA_-1978180945/elements/_EwTfUcTGEeChad0JzLk7QA_434950303)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager(asRole).Player(asPerson)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147)\n"
                },
                "customerSinceDate": {
                  "type": "string",
                  "example": "2010-08-01",
                  "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).ApplicablePeriod.FromDateTime\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).ApplicablePeriod.FromDateTime\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FJ8HVcTGEeChad0JzLk7QA_726404707)\n"
                },
                "customerReferenceRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Binary\n",
                  "properties": {}
                }
              },
              "example": {
                "socialNetworkContacts": "john@twiiter",
                "corporateCustomerLegalEntityReference": "CCLE2010",
                "corporateCustomerReference": "CCRE6010",
                "customerNameSalutation": "Mr.John",
                "companyOfficerReference": "CORE1962",
                "dateOfBirth": "1970-08-01",
                "customerReferenceRecord": "{}",
                "customerSinceDate": "2010-08-01",
                "companyOfficerRole": "Accountant",
                "governmentIssuedIdentityReference": "SocialSecurityNumber",
                "residencyStatus": "Own",
                "emailAddress": "john@email.co",
                "politicalExposureRecord": "PoliticalRecord",
                "corporateAddress": "78B Chruch Street  Dallas Texas United States",
                "customerLegalEntityReference": "CS75433",
                "nationality": "US",
                "cellPhoneNumber": "+1-4123464748",
                "politicalExposureType": "Senior",
                "customerReference": "CR1234",
                "residentialAddress": "23 Dallas Texas",
                "governmentIssuedDocumentDetails": "Passport"
              }
            }
          }
        ],
        "responses": {
          "200": {
            "description": "Successfully requested a refresh of an existing customer directory entry.",
            "schema": {
              "type": "object",
              "properties": {
                "customerReferenceDataDirectoryEntryReference": {
                  "type": "string",
                  "example": "CRDDER679",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "referenceDirectoryEntryReference": {
                  "type": "string",
                  "example": "EX7777",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerReference": {
                  "type": "string",
                  "example": "CR1234",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty)\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwTfUMTGEeChad0JzLk7QA_-1978180945/elements/_EwTfUcTGEeChad0JzLk7QA_434950303)\ngeneral-info: consumer\n"
                },
                "customerLegalEntityReference": {
                  "type": "string",
                  "example": "CS75433",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).Identification\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FNqJucTGEeChad0JzLk7QA_1357540588)\n"
                },
                "customerNameSalutation": {
                  "type": "string",
                  "example": "Mr.John",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).Identification.PartyName\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_FEHzN8TGEeChad0JzLk7QA_1608854558)\n"
                },
                "governmentIssuedIdentityReference": {
                  "type": "string",
                  "example": "SocialSecurityNumber",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_wetlYA93EeGeV5vP7Mvdig_1485186470)\ngeneral-info: social security number\n"
                },
                "governmentIssuedDocumentDetails": {
                  "type": "string",
                  "example": "Passport",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).PersonIdentification\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_E7VDkcTGEeChad0JzLk7QA_-2076942625/elements/_E7VDksTGEeChad0JzLk7QA_-855295891)\ngeneral-info: driving license/passport details\n"
                },
                "residencyStatus": {
                  "type": "string",
                  "example": "Own",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).ResidentialStatus\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOxsTGEeChad0JzLk7QA_-1496564084)\n"
                },
                "dateOfBirth": {
                  "type": "string",
                  "example": "1970-08-01",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).BirthDate\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOwcTGEeChad0JzLk7QA_-1677946145)\n"
                },
                "nationality": {
                  "type": "string",
                  "example": "US",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty)(asPerson).Nationality\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOxMTGEeChad0JzLk7QA_-1677946132)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).PlaceOfBirth\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOyMTGEeChad0JzLk7QA_-1037578805)\n"
                },
                "residentialAddress": {
                  "type": "string",
                  "example": "23 Dallas Texas",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).Residence\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FNz6sMTGEeChad0JzLk7QA_1111100108)\n"
                },
                "emailAddress": {
                  "type": "string",
                  "example": "john@email.co",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FQ8HM8TGEeChad0JzLk7QA_1582936206)\n"
                },
                "cellPhoneNumber": {
                  "type": "string",
                  "example": "+1-4123464748",
                  "description": "`status: Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asPhoneAddress)\n iso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\n `status: Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asPhoneAddress)\n iso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNz6usTGEeChad0JzLk7QA_352593535)\n"
                },
                "socialNetworkContacts": {
                  "type": "string",
                  "example": "john@twiiter",
                  "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress).SocialNetworkAddress\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress).SocialNetworkAddress\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\n"
                },
                "politicalExposureType": {
                  "type": "string",
                  "example": "Senior",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "politicalExposureRecord": {
                  "type": "object",
                  "example": "PoliticalRecord",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Binary\n",
                  "properties": {}
                },
                "corporateCustomerReference": {
                  "type": "string",
                  "example": "CCRE6010",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation)\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwTfUMTGEeChad0JzLk7QA_-1978180945/elements/_EwTfUcTGEeChad0JzLk7QA_434950303)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601)\ngeneral-info: Company\n"
                },
                "corporateCustomerLegalEntityReference": {
                  "type": "string",
                  "example": "CCLE2010",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation).OrganisationIdentification(asPartyIdentificationInformation).LEI\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_yagFILl5EeOpCN0IL2Swqw)\n"
                },
                "corporateAddress": {
                  "type": "string",
                  "example": "78B Chruch Street  Dallas Texas United States",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation).PlaceOfOperation\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_FNqJtcTGEeChad0JzLk7QA_-1846259904)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation).PlaceOfRegistration\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_FNqJtMTGEeChad0JzLk7QA_-847083437)\n"
                },
                "companyOfficerRole": {
                  "type": "string",
                  "example": "Accountant",
                  "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwKVZ8TGEeChad0JzLk7QA_-1034255710)\n"
                },
                "companyOfficerReference": {
                  "type": "string",
                  "example": "CORE1962",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager(asRole).Player(asPerson)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwTfUMTGEeChad0JzLk7QA_-1978180945/elements/_EwTfUcTGEeChad0JzLk7QA_434950303)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager(asRole).Player(asPerson)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147)\n"
                },
                "customerSinceDate": {
                  "type": "string",
                  "example": "2010-08-01",
                  "description": "`status: Provisionally Registered`\n  bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).ApplicablePeriod.FromDateTime\n  `status: Registered`\n  bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).ApplicablePeriod.FromDateTime\n  iso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FJ8HVcTGEeChad0JzLk7QA_726404707)\n"
                },
                "customerReferenceRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Binary\n",
                  "properties": {}
                }
              },
              "example": {
                "socialNetworkContacts": "john@twiiter",
                "corporateCustomerLegalEntityReference": "CCLE2010",
                "referenceDirectoryEntryReference": "EX7777",
                "corporateCustomerReference": "CCRE6010",
                "customerNameSalutation": "Mr.John",
                "companyOfficerReference": "CORE1962",
                "dateOfBirth": "1970-08-01",
                "customerReferenceRecord": "{}",
                "customerSinceDate": "2010-08-01",
                "companyOfficerRole": "Accountant",
                "governmentIssuedIdentityReference": "SocialSecurityNumber",
                "residencyStatus": "Own",
                "emailAddress": "john@email.co",
                "politicalExposureRecord": "PoliticalRecord",
                "corporateAddress": "78B Chruch Street  Dallas Texas United States",
                "customerLegalEntityReference": "CS75433",
                "nationality": "US",
                "cellPhoneNumber": "+1-4123464748",
                "customerReferenceDataDirectoryEntryReference": "CRDDER679",
                "politicalExposureType": "Senior",
                "customerReference": "CR1234",
                "residentialAddress": "23 Dallas Texas",
                "governmentIssuedDocumentDetails": "Passport"
              }
            }
          }
        }
      }
    },
    "/customer-reference-data-management/customer-reference-data-directory/requisition": {
      "post": {
        "tags": [
          "request"
        ],
        "summary": "Requests a Directory Creation",
        "description": "Create a new Customer Reference Data Directory",
        "operationId": "RequestCustomerReferenceDataDirectoryCreate",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "in": "body",
            "name": "body",
            "description": "Request customer reference request payload",
            "required": true,
            "schema": {
              "type": "object",
              "properties": {
                "customerReference": {
                  "type": "string",
                  "example": "CR1234",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty)\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwTfUMTGEeChad0JzLk7QA_-1978180945/elements/_EwTfUcTGEeChad0JzLk7QA_434950303)\ngeneral-info: consumer\n"
                },
                "customerLegalEntityReference": {
                  "type": "string",
                  "example": "CS75433",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).Identification\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FNqJucTGEeChad0JzLk7QA_1357540588)\n"
                },
                "customerNameSalutation": {
                  "type": "string",
                  "example": "Mr.John",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).Identification.PartyName\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_FEHzN8TGEeChad0JzLk7QA_1608854558)\n"
                },
                "governmentIssuedIdentityReference": {
                  "type": "string",
                  "example": "SocialSecurityNumber",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_wetlYA93EeGeV5vP7Mvdig_1485186470)\ngeneral-info: social security number\n"
                },
                "governmentIssuedDocumentDetails": {
                  "type": "string",
                  "example": "Passport",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).PersonIdentification\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_E7VDkcTGEeChad0JzLk7QA_-2076942625/elements/_E7VDksTGEeChad0JzLk7QA_-855295891)\ngeneral-info: driving license/passport details\n"
                },
                "residencyStatus": {
                  "type": "string",
                  "example": "Own",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).ResidentialStatus\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOxsTGEeChad0JzLk7QA_-1496564084)\n"
                },
                "dateOfBirth": {
                  "type": "string",
                  "example": "1970-08-01",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).BirthDate\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOwcTGEeChad0JzLk7QA_-1677946145)\n"
                },
                "nationality": {
                  "type": "string",
                  "example": "US",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty)(asPerson).Nationality\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOxMTGEeChad0JzLk7QA_-1677946132)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).PlaceOfBirth\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOyMTGEeChad0JzLk7QA_-1037578805)\n"
                },
                "residentialAddress": {
                  "type": "string",
                  "example": "23 Dallas Texas",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).Residence\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FNz6sMTGEeChad0JzLk7QA_1111100108)\n"
                },
                "emailAddress": {
                  "type": "string",
                  "example": "john@email.co",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FQ8HM8TGEeChad0JzLk7QA_1582936206)\n"
                },
                "cellPhoneNumber": {
                  "type": "string",
                  "example": "+1-4123464748",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asPhoneAddress)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asPhoneAddress)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNz6usTGEeChad0JzLk7QA_352593535)\n"
                },
                "socialNetworkContacts": {
                  "type": "string",
                  "example": "john@twiiter",
                  "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress).SocialNetworkAddress\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress).SocialNetworkAddress\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\n"
                },
                "politicalExposureType": {
                  "type": "string",
                  "example": "Senior",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "politicalExposureRecord": {
                  "type": "object",
                  "example": "PoliticalRecord",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Binary\n",
                  "properties": {}
                },
                "corporateCustomerReference": {
                  "type": "string",
                  "example": "CCRE6010",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwTfUMTGEeChad0JzLk7QA_-1978180945/elements/_EwTfUcTGEeChad0JzLk7QA_434950303)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601)\ngeneral-info: Company\n"
                },
                "corporateCustomerLegalEntityReference": {
                  "type": "string",
                  "example": "CCLE2010",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation).OrganisationIdentification(asPartyIdentificationInformation).LEI\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_yagFILl5EeOpCN0IL2Swqw)\n"
                },
                "corporateAddress": {
                  "type": "string",
                  "example": "78B Chruch Street  Dallas Texas United States",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation).PlaceOfOperation\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_FNqJtcTGEeChad0JzLk7QA_-1846259904)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation).PlaceOfRegistration\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_FNqJtMTGEeChad0JzLk7QA_-847083437)\n"
                },
                "companyOfficerRole": {
                  "type": "string",
                  "example": "Accountant",
                  "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwKVZ8TGEeChad0JzLk7QA_-1034255710)\n"
                },
                "companyOfficerReference": {
                  "type": "string",
                  "example": "CORE1962",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager(asRole).Player(asPerson)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwTfUMTGEeChad0JzLk7QA_-1978180945/elements/_EwTfUcTGEeChad0JzLk7QA_434950303)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager(asRole).Player(asPerson)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147)\n"
                },
                "customerSinceDate": {
                  "type": "string",
                  "example": "2010-08-01",
                  "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).ApplicablePeriod.FromDateTime\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).ApplicablePeriod.FromDateTime\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FJ8HVcTGEeChad0JzLk7QA_726404707)\n"
                },
                "customerReferenceRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Binary\n",
                  "properties": {}
                }
              },
              "example": {
                "socialNetworkContacts": "john@twiiter",
                "corporateCustomerLegalEntityReference": "CCLE2010",
                "corporateCustomerReference": "CCRE6010",
                "customerNameSalutation": "Mr.John",
                "companyOfficerReference": "CORE1962",
                "dateOfBirth": "1970-08-01",
                "customerReferenceRecord": "{}",
                "customerSinceDate": "2010-08-01",
                "companyOfficerRole": "Accountant",
                "governmentIssuedIdentityReference": "SocialSecurityNumber",
                "residencyStatus": "Own",
                "emailAddress": "john@email.co",
                "politicalExposureRecord": "PoliticalRecord",
                "corporateAddress": "78B Chruch Street  Dallas Texas United States",
                "customerLegalEntityReference": "CS75433",
                "nationality": "US",
                "cellPhoneNumber": "+1-4123464748",
                "politicalExposureType": "Senior",
                "customerReference": "CR1234",
                "residentialAddress": "23 Dallas Texas",
                "governmentIssuedDocumentDetails": "Passport"
              }
            }
          }
        ],
        "responses": {
          "201": {
            "description": "Successfully created customer directory entry.",
            "schema": {
              "type": "object",
              "properties": {
                "customerReferenceDataDirectoryEntryReference": {
                  "type": "string",
                  "example": "CRDDER679",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "referenceDirectoryEntryReference": {
                  "type": "string",
                  "example": "EX7777",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerReference": {
                  "type": "string",
                  "example": "CR1234",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty)\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwTfUMTGEeChad0JzLk7QA_-1978180945/elements/_EwTfUcTGEeChad0JzLk7QA_434950303)\ngeneral-info: consumer\n"
                },
                "customerLegalEntityReference": {
                  "type": "string",
                  "example": "CS75433",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).Identification\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FNqJucTGEeChad0JzLk7QA_1357540588)\n"
                },
                "customerNameSalutation": {
                  "type": "string",
                  "example": "Mr.John",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).Identification.PartyName\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_FEHzN8TGEeChad0JzLk7QA_1608854558)\n"
                },
                "governmentIssuedIdentityReference": {
                  "type": "string",
                  "example": "SocialSecurityNumber",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_wetlYA93EeGeV5vP7Mvdig_1485186470)\ngeneral-info: social security number\n"
                },
                "governmentIssuedDocumentDetails": {
                  "type": "string",
                  "example": "Passport",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).PersonIdentification\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_E7VDkcTGEeChad0JzLk7QA_-2076942625/elements/_E7VDksTGEeChad0JzLk7QA_-855295891)\ngeneral-info: driving license/passport details\n"
                },
                "residencyStatus": {
                  "type": "string",
                  "example": "Own",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).ResidentialStatus\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOxsTGEeChad0JzLk7QA_-1496564084)\n"
                },
                "dateOfBirth": {
                  "type": "string",
                  "example": "1970-08-01",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).BirthDate\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOwcTGEeChad0JzLk7QA_-1677946145)\n"
                },
                "nationality": {
                  "type": "string",
                  "example": "US",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty)(asPerson).Nationality\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOxMTGEeChad0JzLk7QA_-1677946132)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).PlaceOfBirth\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOyMTGEeChad0JzLk7QA_-1037578805)\n"
                },
                "residentialAddress": {
                  "type": "string",
                  "example": "23 Dallas Texas",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).Residence\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FNz6sMTGEeChad0JzLk7QA_1111100108)\n"
                },
                "emailAddress": {
                  "type": "string",
                  "example": "john@email.co",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FQ8HM8TGEeChad0JzLk7QA_1582936206)\n"
                },
                "cellPhoneNumber": {
                  "type": "string",
                  "example": "+1-4123464748",
                  "description": "`status: Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asPhoneAddress)\n iso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\n `status: Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asPhoneAddress)\n iso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNz6usTGEeChad0JzLk7QA_352593535)\n"
                },
                "socialNetworkContacts": {
                  "type": "string",
                  "example": "john@twiiter",
                  "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress).SocialNetworkAddress\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress).SocialNetworkAddress\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\n"
                },
                "politicalExposureType": {
                  "type": "string",
                  "example": "Senior",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "politicalExposureRecord": {
                  "type": "object",
                  "example": "PoliticalRecord",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Binary\n",
                  "properties": {}
                },
                "corporateCustomerReference": {
                  "type": "string",
                  "example": "CCRE6010",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation)\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwTfUMTGEeChad0JzLk7QA_-1978180945/elements/_EwTfUcTGEeChad0JzLk7QA_434950303)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601)\ngeneral-info: Company\n"
                },
                "corporateCustomerLegalEntityReference": {
                  "type": "string",
                  "example": "CCLE2010",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation).OrganisationIdentification(asPartyIdentificationInformation).LEI\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_yagFILl5EeOpCN0IL2Swqw)\n"
                },
                "corporateAddress": {
                  "type": "string",
                  "example": "78B Chruch Street  Dallas Texas United States",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation).PlaceOfOperation\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_FNqJtcTGEeChad0JzLk7QA_-1846259904)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation).PlaceOfRegistration\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_FNqJtMTGEeChad0JzLk7QA_-847083437)\n"
                },
                "companyOfficerRole": {
                  "type": "string",
                  "example": "Accountant",
                  "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwKVZ8TGEeChad0JzLk7QA_-1034255710)\n"
                },
                "companyOfficerReference": {
                  "type": "string",
                  "example": "CORE1962",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager(asRole).Player(asPerson)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwTfUMTGEeChad0JzLk7QA_-1978180945/elements/_EwTfUcTGEeChad0JzLk7QA_434950303)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager(asRole).Player(asPerson)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147)\n"
                },
                "customerSinceDate": {
                  "type": "string",
                  "example": "2010-08-01",
                  "description": "`status: Provisionally Registered`\n  bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).ApplicablePeriod.FromDateTime\n  `status: Registered`\n  bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).ApplicablePeriod.FromDateTime\n  iso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FJ8HVcTGEeChad0JzLk7QA_726404707)\n"
                },
                "customerReferenceRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Binary\n",
                  "properties": {}
                }
              },
              "example": {
                "socialNetworkContacts": "john@twiiter",
                "corporateCustomerLegalEntityReference": "CCLE2010",
                "referenceDirectoryEntryReference": "EX7777",
                "corporateCustomerReference": "CCRE6010",
                "customerNameSalutation": "Mr.John",
                "companyOfficerReference": "CORE1962",
                "dateOfBirth": "1970-08-01",
                "customerReferenceRecord": "{}",
                "customerSinceDate": "2010-08-01",
                "companyOfficerRole": "Accountant",
                "governmentIssuedIdentityReference": "SocialSecurityNumber",
                "residencyStatus": "Own",
                "emailAddress": "john@email.co",
                "politicalExposureRecord": "PoliticalRecord",
                "corporateAddress": "78B Chruch Street  Dallas Texas United States",
                "customerLegalEntityReference": "CS75433",
                "nationality": "US",
                "cellPhoneNumber": "+1-4123464748",
                "customerReferenceDataDirectoryEntryReference": "CRDDER679",
                "politicalExposureType": "Senior",
                "customerReference": "CR1234",
                "residentialAddress": "23 Dallas Texas",
                "governmentIssuedDocumentDetails": "Passport"
              }
            }
          }
        }
      }
    },
    "/customer-reference-data-management/customer-reference-data-directory/{cr-reference-id}/updation": {
      "put": {
        "tags": [
          "update"
        ],
        "summary": "Update reference data",
        "operationId": "UpdateCustomerReferenceDataDirectory",
        "produces": [
          "application/json"
        ],
        "parameters": [
          {
            "name": "cr-reference-id",
            "in": "path",
            "description": "Customer Reference Data Directory Entry Reference",
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
                "customerNameSalutation": {
                  "type": "string",
                  "example": "Mr.John/Mr.Peter"
                },
                "governmentIssuedIdentityReference": {
                  "type": "string",
                  "example": "GIIR4001"
                },
                "governmentIssuedDocumentDetails": {
                  "type": "string",
                  "example": "SocialSecurityNumber/Passport/DrivingLicense"
                },
                "residencyStatus": {
                  "type": "string",
                  "example": "Own/Leased/Rented"
                },
                "dateOfBirth": {
                  "type": "string",
                  "example": "1970-08-01"
                },
                "nationality": {
                  "type": "string",
                  "example": "US/Canada/India"
                },
                "residentialAddress": {
                  "type": "string",
                  "example": "23 Dallas Texas"
                },
                "emailAddress": {
                  "type": "string",
                  "example": "john@email.co"
                },
                "cellPhoneNumber": {
                  "type": "string",
                  "example": "+1-4123464748"
                },
                "socialNetworkContacts": {
                  "type": "string",
                  "example": "john@twiiter/john@facebook"
                },
                "politicalExposureType": {
                  "type": "string",
                  "example": "Senior/PoliticalPosition/Exposure"
                },
                "politicalExposureRecord": {
                  "type": "object",
                  "properties": {}
                },
                "corporateCustomerReference": {
                  "type": "string",
                  "example": "CCRE6010"
                },
                "corporateAddress": {
                  "type": "string",
                  "example": "4 Dallas Texas"
                },
                "companyOfficerRole": {
                  "type": "string",
                  "example": "Accountant/Consultant/Manager"
                },
                "companyOfficerReference": {
                  "type": "string",
                  "example": "CORE1962"
                },
                "customerSinceDate": {
                  "type": "string",
                  "example": "2010-08-01"
                },
                "customerReferenceRecord": {
                  "type": "object",
                  "properties": {}
                }
              },
              "example": {
                "socialNetworkContacts": "john@twiiter/john@facebook",
                "corporateCustomerReference": "CCRE6010",
                "customerNameSalutation": "Mr.John/Mr.Peter",
                "companyOfficerReference": "CORE1962",
                "dateOfBirth": "1970-08-01",
                "customerReferenceRecord": "{}",
                "customerSinceDate": "2010-08-01",
                "companyOfficerRole": "Accountant/Consultant/Manager",
                "governmentIssuedIdentityReference": "GIIR4001",
                "residencyStatus": "Own/Leased/Rented",
                "emailAddress": "john@email.co",
                "politicalExposureRecord": "{}",
                "corporateAddress": "4 Dallas Texas",
                "nationality": "US/Canada/India",
                "cellPhoneNumber": "+1-4123464748",
                "politicalExposureType": "Senior/PoliticalPosition/Exposure",
                "residentialAddress": "23 Dallas Texas",
                "governmentIssuedDocumentDetails": "SocialSecurityNumber/Passport/DrivingLicense"
              }
            }
          }
        ],
        "responses": {
          "200": {
            "description": "Successfully",
            "schema": {
              "type": "object",
              "properties": {
                "customerReferenceDataDirectoryEntryReference": {
                  "type": "string",
                  "example": "CRDDER679",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "referenceDirectoryEntryReference": {
                  "type": "string",
                  "example": "EX7777",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
                },
                "customerReference": {
                  "type": "string",
                  "example": "CR1234",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty)\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwTfUMTGEeChad0JzLk7QA_-1978180945/elements/_EwTfUcTGEeChad0JzLk7QA_434950303)\ngeneral-info: consumer\n"
                },
                "customerLegalEntityReference": {
                  "type": "string",
                  "example": "CS75433",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).Identification\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FNqJucTGEeChad0JzLk7QA_1357540588)\n"
                },
                "customerNameSalutation": {
                  "type": "string",
                  "example": "Mr.John",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).Identification.PartyName\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_FEHzN8TGEeChad0JzLk7QA_1608854558)\n"
                },
                "governmentIssuedIdentityReference": {
                  "type": "string",
                  "example": "SocialSecurityNumber",
                  "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_wetlYA93EeGeV5vP7Mvdig_1485186470)\ngeneral-info: social security number\n"
                },
                "governmentIssuedDocumentDetails": {
                  "type": "string",
                  "example": "Passport",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).PersonIdentification\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_E7VDkcTGEeChad0JzLk7QA_-2076942625/elements/_E7VDksTGEeChad0JzLk7QA_-855295891)\ngeneral-info: driving license/passport details\n"
                },
                "residencyStatus": {
                  "type": "string",
                  "example": "Own",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).ResidentialStatus\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOxsTGEeChad0JzLk7QA_-1496564084)\n"
                },
                "dateOfBirth": {
                  "type": "string",
                  "example": "1970-08-01",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).BirthDate\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOwcTGEeChad0JzLk7QA_-1677946145)\n"
                },
                "nationality": {
                  "type": "string",
                  "example": "US",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty)(asPerson).Nationality\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOxMTGEeChad0JzLk7QA_-1677946132)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).PlaceOfBirth\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOyMTGEeChad0JzLk7QA_-1037578805)\n"
                },
                "residentialAddress": {
                  "type": "string",
                  "example": "23 Dallas Texas",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).Residence\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FNz6sMTGEeChad0JzLk7QA_1111100108)\n"
                },
                "emailAddress": {
                  "type": "string",
                  "example": "john@email.co",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FQ8HM8TGEeChad0JzLk7QA_1582936206)\n"
                },
                "cellPhoneNumber": {
                  "type": "string",
                  "example": "+1-4123464748",
                  "description": "`status: Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asPhoneAddress)\n iso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\n `status: Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asPhoneAddress)\n iso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNz6usTGEeChad0JzLk7QA_352593535)\n"
                },
                "socialNetworkContacts": {
                  "type": "string",
                  "example": "john@twiiter",
                  "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress).SocialNetworkAddress\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress).SocialNetworkAddress\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\n"
                },
                "politicalExposureType": {
                  "type": "string",
                  "example": "Senior",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
                },
                "politicalExposureRecord": {
                  "type": "object",
                  "example": "PoliticalRecord",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Binary\n",
                  "properties": {}
                },
                "corporateCustomerReference": {
                  "type": "string",
                  "example": "CCRE6010",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation)\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwTfUMTGEeChad0JzLk7QA_-1978180945/elements/_EwTfUcTGEeChad0JzLk7QA_434950303)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601)\ngeneral-info: Company\n"
                },
                "corporateCustomerLegalEntityReference": {
                  "type": "string",
                  "example": "CCLE2010",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation).OrganisationIdentification(asPartyIdentificationInformation).LEI\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_yagFILl5EeOpCN0IL2Swqw)\n"
                },
                "corporateAddress": {
                  "type": "string",
                  "example": "78B Chruch Street  Dallas Texas United States",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation).PlaceOfOperation\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_FNqJtcTGEeChad0JzLk7QA_-1846259904)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation).PlaceOfRegistration\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_FNqJtMTGEeChad0JzLk7QA_-847083437)\n"
                },
                "companyOfficerRole": {
                  "type": "string",
                  "example": "Accountant",
                  "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwKVZ8TGEeChad0JzLk7QA_-1034255710)\n"
                },
                "companyOfficerReference": {
                  "type": "string",
                  "example": "CORE1962",
                  "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager(asRole).Player(asPerson)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwTfUMTGEeChad0JzLk7QA_-1978180945/elements/_EwTfUcTGEeChad0JzLk7QA_434950303)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager(asRole).Player(asPerson)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147)\n"
                },
                "customerSinceDate": {
                  "type": "string",
                  "example": "2010-08-01",
                  "description": "`status: Provisionally Registered`\n  bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).ApplicablePeriod.FromDateTime\n  `status: Registered`\n  bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).ApplicablePeriod.FromDateTime\n  iso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FJ8HVcTGEeChad0JzLk7QA_726404707)\n"
                },
                "customerReferenceRecord": {
                  "type": "object",
                  "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Binary\n",
                  "properties": {}
                }
              },
              "example": {
                "socialNetworkContacts": "john@twiiter",
                "corporateCustomerLegalEntityReference": "CCLE2010",
                "referenceDirectoryEntryReference": "EX7777",
                "corporateCustomerReference": "CCRE6010",
                "customerNameSalutation": "Mr.John",
                "companyOfficerReference": "CORE1962",
                "dateOfBirth": "1970-08-01",
                "customerReferenceRecord": "{}",
                "customerSinceDate": "2010-08-01",
                "companyOfficerRole": "Accountant",
                "governmentIssuedIdentityReference": "SocialSecurityNumber",
                "residencyStatus": "Own",
                "emailAddress": "john@email.co",
                "politicalExposureRecord": "PoliticalRecord",
                "corporateAddress": "78B Chruch Street  Dallas Texas United States",
                "customerLegalEntityReference": "CS75433",
                "nationality": "US",
                "cellPhoneNumber": "+1-4123464748",
                "customerReferenceDataDirectoryEntryReference": "CRDDER679",
                "politicalExposureType": "Senior",
                "customerReference": "CR1234",
                "residentialAddress": "23 Dallas Texas",
                "governmentIssuedDocumentDetails": "Passport"
              }
            }
          }
        }
      }
    }
  },
  "definitions": {
    "CustomerReferenceDataRecordRequest": {
      "type": "object",
      "properties": {
        "recordingRecordType": {
          "type": "string",
          "example": "Behavior Model Performance Feedback",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "recordingRecord": {
          "type": "object",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Binary\n",
          "properties": {}
        },
        "recordingRecordDateTime": {
          "type": "string",
          "example": "2018-08-28T09:00:00",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::DateTime\n"
        },
        "empolyeeBusinessUnitReference": {
          "type": "string",
          "example": "EBUR6798",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        }
      },
      "example": {
        "recordingRecordType": "Behavior Model Performance Feedback",
        "empolyeeBusinessUnitReference": "EBUR6798",
        "recordingRecordDateTime": "2018-08-28T09:00:00",
        "recordingRecord": "{}"
      }
    },
    "CustomerReferenceDataRecordResponse": {
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
    "CustomerAssociationBase": {
      "type": "object",
      "properties": {
        "customerReference": {
          "type": "string",
          "example": "CR3816",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "employeeReference": {
          "type": "string",
          "example": "EMPR3816",
          "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager(asRole).Player(asPerson).EmployerIdentificationNumber\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_E7VDkcTGEeChad0JzLk7QA_-2076942625/elements/_E7VDlcTGEeChad0JzLk7QA_-912215424)\n"
        },
        "associateType": {
          "type": "string",
          "example": "Familial",
          "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).PartyRelationship.PartyRelationshipType\ngeneral-info: familial or corporate\n"
        },
        "associateReference": {
          "type": "string",
          "example": "ASRE4820",
          "description": "`status: Provisionally Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).PartyRelationship\n"
        },
        "associateObligationDependencyDescription": {
          "type": "string",
          "example": "Legal Assistant Obligation",
          "description": "`status: Provisionally Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).PartyRelationship.Agreement\n"
        },
        "associationValidFromTo": {
          "type": "string",
          "example": "2017-07-01 To 2018-07-31",
          "description": "`status: Provisionally Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).PartyRelationship.ValidityPeriod\n"
        },
        "productInstanceReference": {
          "type": "string",
          "example": "PRIR5859",
          "description": "`status: Provisionally Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).PartyRelationship.RelationshipAgreement.Product\ngeneral-info: association tied to bank product/service\n"
        },
        "preferredBeneficiary": {
          "type": "string",
          "example": "Father",
          "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player.Role(asAccountPartyRole).Account.A\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EuN0p8TGEeChad0JzLk7QA_-1821987913)\ngeneral-info: list\n"
        },
        "proxyRepresentativePowerOfAttorneyReference": {
          "type": "string",
          "example": "PRPA7398",
          "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).PowerOfAttorney\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/___CLVmIiEeGD28DQaMef-g)\n"
        }
      },
      "example": {
        "associateObligationDependencyDescription": "Legal Assistant Obligation",
        "productInstanceReference": "PRIR5859",
        "associateReference": "ASRE4820",
        "preferredBeneficiary": "Father",
        "employeeReference": "EMPR3816",
        "customerReference": "CR3816",
        "associateType": "Familial",
        "associationValidFromTo": "2017-07-01 To 2018-07-31",
        "proxyRepresentativePowerOfAttorneyReference": "PRPA7398"
      }
    },
    "CustomerAssociationBaseWithIdAndRoot": {
      "type": "object",
      "properties": {
        "customerReferenceDataDirectoryEntryReference": {
          "type": "string",
          "example": "CRDDER679",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "associationsDirectoryEntryReference": {
          "type": "string",
          "example": "ADER123",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerReference": {
          "type": "string",
          "example": "CR3816",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "employeeReference": {
          "type": "string",
          "example": "EMPR3816",
          "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager(asRole).Player(asPerson).EmployerIdentificationNumber\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_E7VDkcTGEeChad0JzLk7QA_-2076942625/elements/_E7VDlcTGEeChad0JzLk7QA_-912215424)\n"
        },
        "associateType": {
          "type": "string",
          "example": "Familial",
          "description": "`status: Provisionally Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).PartyRelationship.PartyRelationshipType\n general-info: familial or corporate\n"
        },
        "associateReference": {
          "type": "string",
          "example": "ASRE4820",
          "description": "`status: Provisionally Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).PartyRelationship\n"
        },
        "associateObligationDependencyDescription": {
          "type": "string",
          "example": "Legal Assistant Obligation",
          "description": "`status: Provisionally Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).PartyRelationship.Agreement\n"
        },
        "associationValidFromTo": {
          "type": "string",
          "example": "2017-07-01 To 2018-07-31",
          "description": "`status: Provisionally Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).PartyRelationship.ValidityPeriod\n"
        },
        "productInstanceReference": {
          "type": "string",
          "example": "PRIR5859",
          "description": "`status: Provisionally Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).PartyRelationship.RelationshipAgreement.Product\n general-info: association tied to bank product/service\n"
        },
        "preferredBeneficiary": {
          "type": "string",
          "example": "Father",
          "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player.Role(asAccountPartyRole).Account.A\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EuN0p8TGEeChad0JzLk7QA_-1821987913)\ngeneral-info: list\n"
        },
        "proxyRepresentativePowerOfAttorneyReference": {
          "type": "string",
          "example": "PRPA7398",
          "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).PowerOfAttorney\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/___CLVmIiEeGD28DQaMef-g)\n"
        }
      },
      "example": {
        "associateObligationDependencyDescription": "Legal Assistant Obligation",
        "productInstanceReference": "PRIR5859",
        "associateReference": "ASRE4820",
        "preferredBeneficiary": "Father",
        "employeeReference": "EMPR3816",
        "customerReferenceDataDirectoryEntryReference": "CRDDER679",
        "customerReference": "CR3816",
        "associateType": "Familial",
        "associationValidFromTo": "2017-07-01 To 2018-07-31",
        "proxyRepresentativePowerOfAttorneyReference": "PRPA7398",
        "associationsDirectoryEntryReference": "ADER123"
      }
    },
    "DemographicBase": {
      "type": "object",
      "properties": {
        "customerReference": {
          "type": "string",
          "example": "CSRE3456",
          "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer\n"
        },
        "socioEconomicClassification": {
          "type": "string",
          "example": "High",
          "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).Household\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_0Lx2wLZeEeOpCN0IL2Swqw)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).PersonProfile\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_q6wNUB9uEeO3iLV2voicmw)\n"
        },
        "ethnicityReligion": {
          "type": "string",
          "example": "Christian",
          "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).Ethnicity\n`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).Religion\n"
        },
        "employment": {
          "type": "string",
          "example": "Analyst",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty)(asPerson).PersonProfile.SalaryRange\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_ZUHGwB9uEeO3iLV2voicmw/elements/_FNg_wMTGEeChad0JzLk7QA_666058283)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty)(asPerson).Profession\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOx8TGEeChad0JzLk7QA_-382216715)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).EmployerIdentificationNumber\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_E7VDkcTGEeChad0JzLk7QA_-2076942625/elements/_E7VDlcTGEeChad0JzLk7QA_-912215424)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.(asRole).Player(asParty)(asPerson).PersonProfile.EmploymentTerminationIndicator\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_ZUHGwB9uEeO3iLV2voicmw/elements/_SfbZ0CHSEeO3iLV2voicmw)\ngeneral-info: employer and position\n"
        },
        "employmentHistory": {
          "type": "string",
          "example": "2 Years in Google",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\ngeneral-info: employer, job position, salary\n"
        },
        "educationHistory": {
          "type": "string",
          "example": "Post Graduate From MIT University",
          "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.(asRole).Player(asPerson).EducationLevel\n general-info: academic institutions, duration, certifications\n"
        },
        "servicingConstraints": {
          "type": "string",
          "example": "Collective",
          "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.CustomerMasterAgreement(asAgreement).TermsAndConditions\n`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.CustomerMasterAgreement.TermsAndConditions\n"
        }
      },
      "example": {
        "employmentHistory": "2 Years in Google",
        "ethnicityReligion": "Christian",
        "servicingConstraints": "Collective",
        "customerReference": "CSRE3456",
        "socioEconomicClassification": "High",
        "employment": "Analyst",
        "educationHistory": "Post Graduate From MIT University"
      }
    },
    "DemographicBaseWithIdAndRoot": {
      "type": "object",
      "properties": {
        "customerReferenceDataDirectoryEntryReference": {
          "type": "string",
          "example": "CRDDER679",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "demographicsDirectoryEntryReference": {
          "type": "string",
          "example": "CSRE3456",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerReference": {
          "type": "string",
          "example": "CSRE3456",
          "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer\n"
        },
        "socioEconomicClassification": {
          "type": "string",
          "example": "High",
          "description": "`status: Registered`\n  bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).Household\n  iso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_0Lx2wLZeEeOpCN0IL2Swqw)\n  `status: Registered`\n  bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).PersonProfile\n  iso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_q6wNUB9uEeO3iLV2voicmw)\n"
        },
        "ethnicityReligion": {
          "type": "string",
          "example": "Christian",
          "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).Ethnicity\n`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).Religion\n"
        },
        "employment": {
          "type": "string",
          "example": "Analyst",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty)(asPerson).PersonProfile.SalaryRange\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_ZUHGwB9uEeO3iLV2voicmw/elements/_FNg_wMTGEeChad0JzLk7QA_666058283)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty)(asPerson).Profession\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOx8TGEeChad0JzLk7QA_-382216715)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).EmployerIdentificationNumber\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_E7VDkcTGEeChad0JzLk7QA_-2076942625/elements/_E7VDlcTGEeChad0JzLk7QA_-912215424)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.(asRole).Player(asParty)(asPerson).PersonProfile.EmploymentTerminationIndicator\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_ZUHGwB9uEeO3iLV2voicmw/elements/_SfbZ0CHSEeO3iLV2voicmw)\ngeneral-info: employer and position\n"
        },
        "employmentHistory": {
          "type": "string",
          "example": "2 Years in Google",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\ngeneral-info: employer, job position, salary\n"
        },
        "educationHistory": {
          "type": "string",
          "example": "Post Graduate From MIT University",
          "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.(asRole).Player(asPerson).EducationLevel\n  general-info: academic institutions, duration, certifications\n"
        },
        "servicingConstraints": {
          "type": "string",
          "example": "Collective",
          "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.CustomerMasterAgreement(asAgreement).TermsAndConditions\n`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.CustomerMasterAgreement.TermsAndConditions\n"
        }
      },
      "example": {
        "employmentHistory": "2 Years in Google",
        "ethnicityReligion": "Christian",
        "servicingConstraints": "Collective",
        "demographicsDirectoryEntryReference": "CSRE3456",
        "customerReferenceDataDirectoryEntryReference": "CRDDER679",
        "customerReference": "CSRE3456",
        "socioEconomicClassification": "High",
        "employment": "Analyst",
        "educationHistory": "Post Graduate From MIT University"
      }
    },
    "ReferenceBase": {
      "type": "object",
      "properties": {
        "customerReference": {
          "type": "string",
          "example": "CR1234",
          "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty)\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwTfUMTGEeChad0JzLk7QA_-1978180945/elements/_EwTfUcTGEeChad0JzLk7QA_434950303)\ngeneral-info: consumer\n"
        },
        "customerLegalEntityReference": {
          "type": "string",
          "example": "CS75433",
          "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).Identification\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FNqJucTGEeChad0JzLk7QA_1357540588)\n"
        },
        "customerNameSalutation": {
          "type": "string",
          "example": "Mr.John",
          "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).Identification.PartyName\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_FEHzN8TGEeChad0JzLk7QA_1608854558)\n"
        },
        "governmentIssuedIdentityReference": {
          "type": "string",
          "example": "SocialSecurityNumber",
          "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_wetlYA93EeGeV5vP7Mvdig_1485186470)\ngeneral-info: social security number\n"
        },
        "governmentIssuedDocumentDetails": {
          "type": "string",
          "example": "Passport",
          "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).PersonIdentification\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_E7VDkcTGEeChad0JzLk7QA_-2076942625/elements/_E7VDksTGEeChad0JzLk7QA_-855295891)\ngeneral-info: driving license/passport details\n"
        },
        "residencyStatus": {
          "type": "string",
          "example": "Own",
          "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).ResidentialStatus\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOxsTGEeChad0JzLk7QA_-1496564084)\n"
        },
        "dateOfBirth": {
          "type": "string",
          "example": "1970-08-01",
          "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).BirthDate\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOwcTGEeChad0JzLk7QA_-1677946145)\n"
        },
        "nationality": {
          "type": "string",
          "example": "US",
          "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty)(asPerson).Nationality\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOxMTGEeChad0JzLk7QA_-1677946132)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).PlaceOfBirth\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOyMTGEeChad0JzLk7QA_-1037578805)\n"
        },
        "residentialAddress": {
          "type": "string",
          "example": "23 Dallas Texas",
          "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).Residence\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FNz6sMTGEeChad0JzLk7QA_1111100108)\n"
        },
        "emailAddress": {
          "type": "string",
          "example": "john@email.co",
          "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FQ8HM8TGEeChad0JzLk7QA_1582936206)\n"
        },
        "cellPhoneNumber": {
          "type": "string",
          "example": "+1-4123464748",
          "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asPhoneAddress)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asPhoneAddress)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNz6usTGEeChad0JzLk7QA_352593535)\n"
        },
        "socialNetworkContacts": {
          "type": "string",
          "example": "john@twiiter",
          "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress).SocialNetworkAddress\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress).SocialNetworkAddress\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\n"
        },
        "politicalExposureType": {
          "type": "string",
          "example": "Senior",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "politicalExposureRecord": {
          "type": "object",
          "example": "PoliticalRecord",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Binary\n",
          "properties": {}
        },
        "corporateCustomerReference": {
          "type": "string",
          "example": "CCRE6010",
          "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwTfUMTGEeChad0JzLk7QA_-1978180945/elements/_EwTfUcTGEeChad0JzLk7QA_434950303)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601)\ngeneral-info: Company\n"
        },
        "corporateCustomerLegalEntityReference": {
          "type": "string",
          "example": "CCLE2010",
          "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation).OrganisationIdentification(asPartyIdentificationInformation).LEI\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_yagFILl5EeOpCN0IL2Swqw)\n"
        },
        "corporateAddress": {
          "type": "string",
          "example": "78B Chruch Street  Dallas Texas United States",
          "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation).PlaceOfOperation\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_FNqJtcTGEeChad0JzLk7QA_-1846259904)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation).PlaceOfRegistration\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_FNqJtMTGEeChad0JzLk7QA_-847083437)\n"
        },
        "companyOfficerRole": {
          "type": "string",
          "example": "Accountant",
          "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwKVZ8TGEeChad0JzLk7QA_-1034255710)\n"
        },
        "companyOfficerReference": {
          "type": "string",
          "example": "CORE1962",
          "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager(asRole).Player(asPerson)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwTfUMTGEeChad0JzLk7QA_-1978180945/elements/_EwTfUcTGEeChad0JzLk7QA_434950303)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager(asRole).Player(asPerson)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147)\n"
        },
        "customerSinceDate": {
          "type": "string",
          "example": "2010-08-01",
          "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).ApplicablePeriod.FromDateTime\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).ApplicablePeriod.FromDateTime\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FJ8HVcTGEeChad0JzLk7QA_726404707)\n"
        },
        "customerReferenceRecord": {
          "type": "object",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Binary\n",
          "properties": {}
        }
      },
      "example": {
        "socialNetworkContacts": "john@twiiter",
        "corporateCustomerLegalEntityReference": "CCLE2010",
        "corporateCustomerReference": "CCRE6010",
        "customerNameSalutation": "Mr.John",
        "companyOfficerReference": "CORE1962",
        "dateOfBirth": "1970-08-01",
        "customerReferenceRecord": "{}",
        "customerSinceDate": "2010-08-01",
        "companyOfficerRole": "Accountant",
        "governmentIssuedIdentityReference": "SocialSecurityNumber",
        "residencyStatus": "Own",
        "emailAddress": "john@email.co",
        "politicalExposureRecord": "PoliticalRecord",
        "corporateAddress": "78B Chruch Street  Dallas Texas United States",
        "customerLegalEntityReference": "CS75433",
        "nationality": "US",
        "cellPhoneNumber": "+1-4123464748",
        "politicalExposureType": "Senior",
        "customerReference": "CR1234",
        "residentialAddress": "23 Dallas Texas",
        "governmentIssuedDocumentDetails": "Passport"
      }
    },
    "ReferenceBaseWithIdAndRoot": {
      "type": "object",
      "properties": {
        "customerReferenceDataDirectoryEntryReference": {
          "type": "string",
          "example": "CRDDER679",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "referenceDirectoryEntryReference": {
          "type": "string",
          "example": "EX7777",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerReference": {
          "type": "string",
          "example": "CR1234",
          "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty)\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwTfUMTGEeChad0JzLk7QA_-1978180945/elements/_EwTfUcTGEeChad0JzLk7QA_434950303)\ngeneral-info: consumer\n"
        },
        "customerLegalEntityReference": {
          "type": "string",
          "example": "CS75433",
          "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).Identification\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FNqJucTGEeChad0JzLk7QA_1357540588)\n"
        },
        "customerNameSalutation": {
          "type": "string",
          "example": "Mr.John",
          "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).Identification.PartyName\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_FEHzN8TGEeChad0JzLk7QA_1608854558)\n"
        },
        "governmentIssuedIdentityReference": {
          "type": "string",
          "example": "SocialSecurityNumber",
          "description": "`status: Registered`\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_wetlYA93EeGeV5vP7Mvdig_1485186470)\ngeneral-info: social security number\n"
        },
        "governmentIssuedDocumentDetails": {
          "type": "string",
          "example": "Passport",
          "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).PersonIdentification\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_E7VDkcTGEeChad0JzLk7QA_-2076942625/elements/_E7VDksTGEeChad0JzLk7QA_-855295891)\ngeneral-info: driving license/passport details\n"
        },
        "residencyStatus": {
          "type": "string",
          "example": "Own",
          "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).ResidentialStatus\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOxsTGEeChad0JzLk7QA_-1496564084)\n"
        },
        "dateOfBirth": {
          "type": "string",
          "example": "1970-08-01",
          "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).BirthDate\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOwcTGEeChad0JzLk7QA_-1677946145)\n"
        },
        "nationality": {
          "type": "string",
          "example": "US",
          "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty)(asPerson).Nationality\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOxMTGEeChad0JzLk7QA_-1677946132)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asPerson).PlaceOfBirth\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147/elements/_FNXOyMTGEeChad0JzLk7QA_-1037578805)\n"
        },
        "residentialAddress": {
          "type": "string",
          "example": "23 Dallas Texas",
          "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).Residence\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FNz6sMTGEeChad0JzLk7QA_1111100108)\n"
        },
        "emailAddress": {
          "type": "string",
          "example": "john@email.co",
          "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FQ8HM8TGEeChad0JzLk7QA_1582936206)\n"
        },
        "cellPhoneNumber": {
          "type": "string",
          "example": "+1-4123464748",
          "description": "`status: Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asPhoneAddress)\n iso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\n `status: Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asPhoneAddress)\n iso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNz6usTGEeChad0JzLk7QA_352593535)\n"
        },
        "socialNetworkContacts": {
          "type": "string",
          "example": "john@twiiter",
          "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress).SocialNetworkAddress\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asParty).ContactPoint(asElectronicAddress).SocialNetworkAddress\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNqJt8TGEeChad0JzLk7QA_-1317971633/elements/_FEHzOMTGEeChad0JzLk7QA_-1894201405)\n"
        },
        "politicalExposureType": {
          "type": "string",
          "example": "Senior",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::UNCEFACT::Text\n"
        },
        "politicalExposureRecord": {
          "type": "object",
          "example": "PoliticalRecord",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Binary\n",
          "properties": {}
        },
        "corporateCustomerReference": {
          "type": "string",
          "example": "CCRE6010",
          "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation)\niso-link: [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwTfUMTGEeChad0JzLk7QA_-1978180945/elements/_EwTfUcTGEeChad0JzLk7QA_434950303)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601)\ngeneral-info: Company\n"
        },
        "corporateCustomerLegalEntityReference": {
          "type": "string",
          "example": "CCLE2010",
          "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation).OrganisationIdentification(asPartyIdentificationInformation).LEI\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FEHzNMTGEeChad0JzLk7QA_-1382123937/elements/_yagFILl5EeOpCN0IL2Swqw)\n"
        },
        "corporateAddress": {
          "type": "string",
          "example": "78B Chruch Street  Dallas Texas United States",
          "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation).PlaceOfOperation\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_FNqJtcTGEeChad0JzLk7QA_-1846259904)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).Player(asOrganisation).PlaceOfRegistration\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNg_x8TGEeChad0JzLk7QA_908383601/elements/_FNqJtMTGEeChad0JzLk7QA_-847083437)\n"
        },
        "companyOfficerRole": {
          "type": "string",
          "example": "Accountant",
          "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwKVZ8TGEeChad0JzLk7QA_-1034255710)\n"
        },
        "companyOfficerReference": {
          "type": "string",
          "example": "CORE1962",
          "description": "`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager(asRole).Player(asPerson)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_EwTfUMTGEeChad0JzLk7QA_-1978180945/elements/_EwTfUcTGEeChad0JzLk7QA_434950303)\n`status: Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager(asRole).Player(asPerson)\niso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FNXOwMTGEeChad0JzLk7QA_-1677946147)\n"
        },
        "customerSinceDate": {
          "type": "string",
          "example": "2010-08-01",
          "description": "`status: Provisionally Registered`\n  bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).ApplicablePeriod.FromDateTime\n  `status: Registered`\n  bian-reference:  CustomerRegistryEntry.RegisteredCustomer(asRole).ApplicablePeriod.FromDateTime\n  iso-link:  [click-here](https://www.iso20022.org/standardsrepository/public/wqt/Description/mx/dico/bc/_FJ8HVcTGEeChad0JzLk7QA_726404707)\n"
        },
        "customerReferenceRecord": {
          "type": "object",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Binary\n",
          "properties": {}
        }
      },
      "example": {
        "socialNetworkContacts": "john@twiiter",
        "corporateCustomerLegalEntityReference": "CCLE2010",
        "referenceDirectoryEntryReference": "EX7777",
        "corporateCustomerReference": "CCRE6010",
        "customerNameSalutation": "Mr.John",
        "companyOfficerReference": "CORE1962",
        "dateOfBirth": "1970-08-01",
        "customerReferenceRecord": "{}",
        "customerSinceDate": "2010-08-01",
        "companyOfficerRole": "Accountant",
        "governmentIssuedIdentityReference": "SocialSecurityNumber",
        "residencyStatus": "Own",
        "emailAddress": "john@email.co",
        "politicalExposureRecord": "PoliticalRecord",
        "corporateAddress": "78B Chruch Street  Dallas Texas United States",
        "customerLegalEntityReference": "CS75433",
        "nationality": "US",
        "cellPhoneNumber": "+1-4123464748",
        "customerReferenceDataDirectoryEntryReference": "CRDDER679",
        "politicalExposureType": "Senior",
        "customerReference": "CR1234",
        "residentialAddress": "23 Dallas Texas",
        "governmentIssuedDocumentDetails": "Passport"
      }
    },
    "BankRelationsBase": {
      "type": "object",
      "properties": {
        "customerReference": {
          "type": "string",
          "example": "CSRE3456",
          "description": "`status: Provisionally Registered`\n  bian-reference:  CustomerRegistryEntry.RegisteredCustomer\n"
        },
        "bankRelationType": {
          "type": "string",
          "example": "Agent",
          "description": "`status: Provisionally Registered`\n  bian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager\n  general-info: relationship manager\n"
        },
        "businessUnitEmployeeReference": {
          "type": "string",
          "example": "BUER2920",
          "description": "`status: Provisionally Registered`\n  bian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager.BusinessUnit\n"
        }
      },
      "example": {
        "customerReference": "CSRE3456",
        "businessUnitEmployeeReference": "BUER2920",
        "bankRelationType": "Agent"
      }
    },
    "BankRelationsBaseWithIdAndRoot": {
      "type": "object",
      "properties": {
        "customerReferenceDataDirectoryEntryReference": {
          "type": "string",
          "example": "CRDDER679",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "bankRelationsDirectoryEntryReference": {
          "type": "string",
          "example": "BR73654",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        },
        "customerReference": {
          "type": "string",
          "example": "CSRE3456",
          "description": "`status: Provisionally Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer\n"
        },
        "bankRelationType": {
          "type": "string",
          "example": "Agent",
          "description": "`status: Provisionally Registered`\n bian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager\n general-info: relationship manager\n"
        },
        "businessUnitEmployeeReference": {
          "type": "string",
          "example": "BUER2920",
          "description": "`status: Provisionally Registered`\nbian-reference:  CustomerRegistryEntry.RegisteredCustomer.RelationshipManager.BusinessUnit\n"
        }
      },
      "example": {
        "customerReferenceDataDirectoryEntryReference": "CRDDER679",
        "customerReference": "CSRE3456",
        "businessUnitEmployeeReference": "BUER2920",
        "bankRelationsDirectoryEntryReference": "BR73654",
        "bankRelationType": "Agent"
      }
    },
    "RetrieveCustomerReferenceDataManagementRoot": {
      "type": "object",
      "properties": {
        "customerReferenceDataDirectoryEntryReference": {
          "type": "string",
          "example": "CRDDER679",
          "description": "`status: Not Mapped`\ncore-data-type-reference: BIAN::DataTypesLibrary::CoreDataTypes::ISO20022andUNCEFACT::Identifier\n"
        }
      },
      "example": {
        "customerReferenceDataDirectoryEntryReference": "CRDDER679"
      }
    },
    "ReferenceBaseUpdateRequest": {
      "type": "object",
      "properties": {
        "customerNameSalutation": {
          "type": "string",
          "example": "Mr.John/Mr.Peter"
        },
        "governmentIssuedIdentityReference": {
          "type": "string",
          "example": "GIIR4001"
        },
        "governmentIssuedDocumentDetails": {
          "type": "string",
          "example": "SocialSecurityNumber/Passport/DrivingLicense"
        },
        "residencyStatus": {
          "type": "string",
          "example": "Own/Leased/Rented"
        },
        "dateOfBirth": {
          "type": "string",
          "example": "1970-08-01"
        },
        "nationality": {
          "type": "string",
          "example": "US/Canada/India"
        },
        "residentialAddress": {
          "type": "string",
          "example": "23 Dallas Texas"
        },
        "emailAddress": {
          "type": "string",
          "example": "john@email.co"
        },
        "cellPhoneNumber": {
          "type": "string",
          "example": "+1-4123464748"
        },
        "socialNetworkContacts": {
          "type": "string",
          "example": "john@twiiter/john@facebook"
        },
        "politicalExposureType": {
          "type": "string",
          "example": "Senior/PoliticalPosition/Exposure"
        },
        "politicalExposureRecord": {
          "type": "object",
          "properties": {}
        },
        "corporateCustomerReference": {
          "type": "string",
          "example": "CCRE6010"
        },
        "corporateAddress": {
          "type": "string",
          "example": "4 Dallas Texas"
        },
        "companyOfficerRole": {
          "type": "string",
          "example": "Accountant/Consultant/Manager"
        },
        "companyOfficerReference": {
          "type": "string",
          "example": "CORE1962"
        },
        "customerSinceDate": {
          "type": "string",
          "example": "2010-08-01"
        },
        "customerReferenceRecord": {
          "type": "object",
          "properties": {}
        }
      },
      "example": {
        "socialNetworkContacts": "john@twiiter/john@facebook",
        "corporateCustomerReference": "CCRE6010",
        "customerNameSalutation": "Mr.John/Mr.Peter",
        "companyOfficerReference": "CORE1962",
        "dateOfBirth": "1970-08-01",
        "customerReferenceRecord": "{}",
        "customerSinceDate": "2010-08-01",
        "companyOfficerRole": "Accountant/Consultant/Manager",
        "governmentIssuedIdentityReference": "GIIR4001",
        "residencyStatus": "Own/Leased/Rented",
        "emailAddress": "john@email.co",
        "politicalExposureRecord": "{}",
        "corporateAddress": "4 Dallas Texas",
        "nationality": "US/Canada/India",
        "cellPhoneNumber": "+1-4123464748",
        "politicalExposureType": "Senior/PoliticalPosition/Exposure",
        "residentialAddress": "23 Dallas Texas",
        "governmentIssuedDocumentDetails": "SocialSecurityNumber/Passport/DrivingLicense"
      }
    }
  }
}
</script>