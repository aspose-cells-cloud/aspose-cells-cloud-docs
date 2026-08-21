---
title: "Diagrammwertachse abrufen"
type: docs
url: /charts/value-axis/get/
weight: 60
keywords: Aspose.Cells, Diagrammwertachse, REST API, Excel, Cloud SDK, Diagrammwertachse abrufen
description: "Aspose.Cells Cloud REST API – Abrufen der Wertachse eines Diagramms in einem Excel-Arbeitsblatt."
ArticleTitle: "Diagrammwertachse abrufen – Aspose.Cells Cloud REST API"
---

Diese REST API ruft die Wertachse eines Diagramms ab. Sie ist Teil der **Aspose.Cells Cloud REST API** und arbeitet mit Excel-Arbeitsblättern, die in der Cloud gespeichert sind.

Weitere verwandte Vorgänge finden Sie im Endpunkt **[Get Chart Category Axis](/charts/category-axis/get/)**.

## GetChartValueAxis API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername   | Typ    | Ort   | Beschreibung                                                |
|-----------------|--------|-------|-------------------------------------------------------------|
| name            | string | path  | Der Name der Excel-Datei (einschließlich Erweiterung).     |
| sheetName       | string | path  | Der Name des Arbeitsblatts, das das Diagramm enthält.      |
| chartIndex      | integer| path  | Der nullbasierte Index des Diagramms innerhalb des Arbeitsblatts. |
| folder          | string | query | Der Ordner im Cloud-Speicher, in dem sich die Datei befindet. |
| storageName     | string | query | Der Name des Speicherdiensts (z. B. Aspose Cloud).         |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Charts/GetChartValueAxis) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser heraus durchzuführen.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste problemlos aufzurufen. Das folgende Beispiel zeigt, wie ein Aufruf an die Cloud-API mit cURL durchgeführt wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}/valueaxis" \
 -X GET \
 -H "Content-Type: application/json" \
 -H "Accept: application/json" \
 -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "ValueAxis": {
    "Minimum": 0,
    "Maximum": 100,
    "MajorUnit": 10,
    "MinorUnit": 5,
    "Title": "Werte",
    "Format": {
      "NumberFormat": "Allgemein",
      "Font": {
        "Name": "Arial",
        "Size": 10,
        "Bold": false,
        "Italic": false
      }
    }
  }
}
```

**Mögliche HTTP-Statuscodes**

| Code | Beschreibung                                                 |
|------|--------------------------------------------------------------|
| 200  | Erfolg – die Wertachseninformationen werden zurückgegeben.  |
| 400  | Ungültige Anforderung – erforderliche Parameter fehlen oder sind ungültig. |
| 401  | Nicht autorisiert – Authentifizierungstoken fehlt oder ist ungültig. |
| 404  | Nicht gefunden – die angegebene Arbeitsmappe, das Arbeitsblatt oder das Diagramm existiert nicht. |
| 500  | Interner Serverfehler – auf dem Server ist ein unerwarteter Fehler aufgetreten. |

Die Antwort enthält ein detailliertes `ValueAxis`-Objekt mit Eigenschaften wie `Minimum`, `Maximum`, `MajorUnit`, `MinorUnit`, `Title` und `Format`. In einer vollständigen Implementierung können zusätzliche Formatierungsdetails bereitgestellt werden.

{{< /tab >}}

{{< /tabs >}}

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Details der unteren Schichten, sodass Sie sich auf die Aufgaben Ihres Projekts konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste unter Verwendung verschiedener SDKs durchgeführt werden:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

<!-- C# example placeholder -->

{{< /tab >}}

{{< tab tabNum="2" >}}

<!-- Java example placeholder -->

{{< /tab >}}

{{< tab tabNum="3" >}}

<!-- PHP example placeholder -->

{{< /tab >}}

{{< tab tabNum="4" >}}

<!-- Ruby example placeholder -->

{{< /tab >}}

{{< tab tabNum="5" >}}

<!-- Python example placeholder -->

{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example-Get-ChartValueAxis.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

<!-- Android example placeholder -->

{{< /tab >}}

{{< tab tabNum="8" >}}

<!-- Swift example placeholder -->

{{< /tab >}}

{{< tab tabNum="9" >}}

<!-- Perl example placeholder -->

{{< /tab >}}

{{< tab tabNum="10" >}}

<!-- Go example placeholder -->

{{< /tab >}}

{{< /tabs >}}
---