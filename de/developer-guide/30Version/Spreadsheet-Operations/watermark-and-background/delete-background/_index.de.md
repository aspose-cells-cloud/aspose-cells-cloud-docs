---
title: "Hintergrund in einer Excel-Arbeitsmappe entfernen"
second_title: "Dokument"
linktitle: "Entfernen"
type: docs
url: /delete-background-in-excel-file/
aliases:
  - /delete-background-in-workbook/
  - /workbook/delete-background/
  - /workbook/background/delete/
keywords: "Aspose Cells Hintergrund entfernen, Excel API Hintergrund entfernen, Aspose.Cells Cloud, DELETE /cells background"
description: "Entfernen Sie ein Hintergrundbild aus einer Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud API. Erfahren Sie mehr über den DELETE-Endpunkt, die erforderlichen Parameter, ein cURL-Beispiel und SDK-Code in C#, Java, Python und weiteren Sprachen."
weight: 170
ArticleTitle: "Hintergrundbild aus Excel-Arbeitsmappe mit Aspose.Cells Cloud API entfernen"
---

Diese REST-API entfernt das Hintergrundbild einer Excel-Arbeitsmappe.

## DeleteWorkbookBackground API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/background
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Abfrageparameter**

| Parametername | Typ   | Beschreibung                                           | Erforderlich |
| -------------- | ------ | ------------------------------------------------------ | ------------ |
| folder         | string | Ordner, der die ursprüngliche Arbeitsmappe enthält.    | Nein         |
| storageName    | string | Name des zu verwendenden Speicherdienstes.            | Nein         |

### **Antwort**

```json
{
    "Status" : "OK",
    "Code" : 200
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                    |
|------|-----------------------------|-----------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                           |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet die Größenbeschränkung.   |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                     |

## Verwendung der DeleteWorkbookBackground API mit SDKs

### DeleteWorkbookBackground API-Spezifikation

Die <a href="https://apireference.aspose.cloud/cells/#/Workbook/DeleteWorkbookBackground" target="_blank" rel="noopener noreferrer">OpenAPI-Spezifikation</a> definiert eine öffentlich zugängliche Programmierschnittstelle, über die Sie REST-Interaktionen direkt aus einem Webbrowser heraus durchführen können.

Sie können das Kommandozeilentool **cURL** verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt eine vollständige DELETE-Anfrage mit dem erforderlichen Authentifizierungsheader; es ist kein Anforderungstext erforderlich.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/{name}/background?folder=DotnetFiles" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -H "x-aspose-client: Containerize.Swagger"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist die beste Möglichkeit, die Entwicklungszeit zu verkürzen. Ein SDK übernimmt die Details auf niedriger Ebene, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Weitere Informationen finden Sie im <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4"
   tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby"
   tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}
---