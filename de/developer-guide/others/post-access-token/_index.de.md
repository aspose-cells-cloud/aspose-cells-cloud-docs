---
title: Aspose.Cells Cloud Web API - Post Access Token
second_title: Documen
ArticleTitle: Get Access Token with Client ID and Secre
linktitle: Post-Access-Token
type: docs
url: /de/post-access-token/
keywords: Access Token, Aspose Cloud, API Authentication, OAuth, REST API, Excel, Office Cloud, Token Managemen
description: Rufen Sie ein Zugriffstoken mit dem Cells Cloud Get Token API ab, das als Proxy-Dienst fungiert, der Benutzeranfragen an den Aspose Cloud-Authentifizierungsserver weiterleitet und das resultierende Zugriffstoken sicher an den Client zurückgibt
weight: 100
kwords: Excel, Office Cloud, REST API, Authentifizierung, Token-Management, Middleware-Integration, Sicher API, Aspose Clou
---
Rufen Sie ein Zugriffstoken mit dem Cells Cloud Get Token API mit Client-ID und Geheimnis ab.

## **Post-Zugriffstoken API**

```
POST http://api.aspose.cloud/v4.0/cells/connect/token
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:- |:- |:- |:- |
| Client-ID| Schnur| Abfrage| Client-ID|
| Client-Geheimnis| Schnur| Abfrage| Client-Geheimnis|

### **Antwort**

```json
 [
        {
          "Name": "String",
          "DataType": {
            "Identifier": "String",
            "Name": "string"
          }
        }
  ]
```

## So verwenden Sie den öffentlichen Schlüssel API mit SDKs

### OpenAPI-Spezifikation

 Der[OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/CellsAuthorityController/PostAccessToken) definiert eine öffentlich zugängliche Programmierschnittstelle, die es Ihnen ermöglicht, REST-Interaktionen direkt von einem Webbrowser aus durchzuführen.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK beschleunigt die Entwicklung am besten. Das SDK übernimmt die zugrunde liegenden Details und ermöglicht Ihnen die Implementierung von Zugriffstoken für Zellen mit minimalem Code.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) Eine vollständige Liste der Aspose.Cells Cloud SDKs.nt finden Sie hier. Ein SDK kümmert sich um die Details auf niedriger Ebene und ermöglicht Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:
