---
title: Aspose.Cells Cloud WEb API - Öffentlichen Schlüssel erhalten
second_title: Documen
ArticleTitle: Get Public Ke
linktitle: Holen Sie sich Public Ke
type: docs
url: /de/get-public-key/
keywords: asymmetric encryption, public key retrieval, REST API, Excel API, security, data encryption, API integratio
description: Abrufen eines asymmetrischen öffentlichen Schlüssels zur sicheren Datenverschlüsselung
weight: 100
kwords: asymmetrische Verschlüsselung, öffentlicher Schlüssel, REST API, Excel API, Sicherheit, Datenverschlüsselung, API Integration, JSON, API Dokumentation
---
Ruft den öffentlichen Schlüssel aus einem asymmetrischen Verschlüsselungsalgorithmus ab.

## **Öffentlichen Schlüssel API erhalten**

```
GET http://api.aspose.cloud/v4.0/cells/publickey
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTP-Text| Beschreibung|
|:- |:- |:- |:- |
|||||

### **Antwort**

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

## So verwenden Sie den öffentlichen Schlüssel API mit SDKs

### OpenAPI-Spezifikation

 Der[OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/KeyController/GetPublicKey) definiert eine öffentlich zugängliche Programmierschnittstelle, die es Ihnen ermöglicht, REST-Interaktionen direkt von Ihrem Webbrowser aus durchzuführen.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK beschleunigt die Entwicklung am besten. Das SDK übernimmt die zugrunde liegenden Details und ermöglicht Ihnen die Implementierung des öffentlichen Schlüssels für Zellen mit minimalem Code.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele veranschaulichen die Interaktion mit Aspose.Cells-Webdiensten mithilfe verschiedener SDKs:
