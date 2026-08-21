---
title: "Alle Dokumenteigenschaften abrufen"
second_title: "Dokument"
linktitle: "Alle abrufen"
type: docs
url: /de/document-properties/get-all/
aliases: [  /de/get-all-document-properties/ ]
keywords: "Alle Dokumenteigenschaften abrufen, Aspose.Cells Cloud, Excel-Dokumenteigenschaften, REST API, SDK, Excel-Metadaten"
description: "Rufen Sie alle Dokumenteigenschaften aus einer Excel-Datei mithilfe der Aspose.Cells Cloud REST API ab. Der Endpunkt funktioniert mit allen unterstützten SDKs und Programmiersprachen."
ArticleTitle: "Alle Dokumenteigenschaften abrufen – Aspose.Cells Cloud API"
weight: 25
---

Diese REST API liest Dokumenteigenschaften.

## GetDocumentProperties API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/documentproperties
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername   | Typ    | Speicherort | Beschreibung                    |
| --------------- | ------ | ----------- | ------------------------------- |
| name            | string | path        | Name der Excel-Datei.           |
| folder          | string | query       | Ordner, der die Datei enthält.  |
| storageName     | string | query       | Name des Speicherdienstes.      |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Properties/GetDocumentProperties) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser heraus durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie die Cloud-API mit cURL aufgerufen wird.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/documentproperties" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "DocumentProperties": {
    "DocumentPropertyList": [
      {
        "Name": "Title",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Title",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Subject",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Subject",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Author",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Author",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Keywords",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Keywords",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Comments",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Comments",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "LastSavedBy",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/LastSavedBy",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "CreateTime",
        "Value": "6/5/2015 6:17:20 PM",
        "BuiltIn": "True",
        "link": {
          "Href": "/CreateTime",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "LastSavedTime",
        "Value": "9/27/2019 9:09:43 PM",
        "BuiltIn": "True",
        "link": {
          "Href": "/LastSavedTime",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Category",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Category",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "NameOfApplication",
        "Value": "Microsoft Excel",
        "BuiltIn": "True",
        "link": {
          "Href": "/NameOfApplication",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Version",
        "Value": "16.0300",
        "BuiltIn": "True",
        "link": {
          "Href": "/Version",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Security",
        "Value": "0",
        "BuiltIn": "True",
        "link": {
          "Href": "/Security",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "ScaleCrop",
        "Value": "False",
        "BuiltIn": "True",
        "link": {
          "Href": "/ScaleCrop",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Template",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Template",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Manager",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Manager",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "Company",
        "Value": "",
        "BuiltIn": "True",
        "link": {
          "Href": "/Company",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      {
        "Name": "LinksUpToDate",
        "Value": "False",
        "BuiltIn": "True",
        "link": {
          "Href": "/LinksUpToDate",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      }
    ],
    "link": {
      "Href": "/test.xlsx/documentproperties",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                       |
|------|-----------------------------|--------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                              |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.             |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                        |

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Details auf unterster Ebene und lässt Sie sich auf Ihre ProjektAufgaben konzentrieren. Bitte prüfen Sie den [GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetDocumentProperties.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetDocumentProperties.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetDocumentProperties.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetDocumentProperties.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetDocumentProperties.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetDocumentProperties.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetDocumentProperties.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetDocumentProperties.go" >}}

{{< /tab >}}

{{< /tabs >}}