---
title: Aspose.Cells Cloud Web API - Hämta offentlig nyckel
second_title: Documen
ArticleTitle: Get Public Ke
linktitle: Hämta offentlig nyckel
type: docs
url: /sv/get-public-key/
keywords: asymmetric encryption, public key retrieval, REST API, Excel API, security, data encryption, API integratio
description: Hämta en asymmetrisk offentlig nyckel för säker datakryptering
weight: 100
kwords: asymmetrisk kryptering, publik nyckel, REST API, Excel API, säkerhet, datakryptering, API integration, JSON, API dokumentation
---
Hämtar den publika nyckeln från en asymmetrisk krypteringsalgoritm.

## **Hämta offentlig nyckel API**

```
GET http://api.aspose.cloud/v4.0/cells/publickey
```

### **Begäranparametrar:**

| Parameternamn| Typ| Sökväg/Frågesträng/HTTP-text| Beskrivning|
|:- |:- |:- |:- |
|||||

### **Svar**

```json
{
  "Name": "CellsCloudPublicKeyResponse",
  "Type": "Class",
  "ParentName": "CellsCloudResponse",
  "IsAbstract": false,
  "Properties": [
    {
      "Name": "CellsCloudPublicKey",
      "DataType": {
        "Identifier": "Class",
        "Reference": "CellsCloudPublicKey",
      }
    },
    {
      "Name": "Code",
      "DataType": {
        "Identifier": "Integer",
      }
    },
    {
      "Name": "Status",
      "DataType": {
        "Identifier": "String",
      }
    }
  ]
}
```

## Så här använder du Get public key API med SDK:er

### OpenAPI-specifikation

 De[OpenAPI-specifikation](https://reference.aspose.cloud/cells/#/KeyController/GetPublicKey) definierar ett offentligt tillgängligt programmeringsgränssnitt som gör att du kan utföra REST-interaktioner direkt från din webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda SDK:et är det bästa sättet att påskynda utvecklingen. SDK:et hanterar de underliggande detaljerna, vilket gör att du enkelt kan implementera "get public key for cells" med minimal kod.
 Vänligen kolla in[GitHub-arkiv](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel illustrerar hur man interagerar med Aspose.Cells-webbtjänster med hjälp av olika SDK:er:
