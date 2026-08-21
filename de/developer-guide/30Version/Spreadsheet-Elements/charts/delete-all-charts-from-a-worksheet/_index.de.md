---
title: "Alle Diagramme aus einem Arbeitsblatt löschen"
type: docs
url: /de/charts/clear/
aliases: [  /delete-all-charts-from-a-worksheet/ ]
weight: 30
keywords: "Aspose.Cells, Cloud, löschen, alle Diagramme, Arbeitsblatt, REST API, DELETE, SDK"
description: "Erfahren Sie, wie Sie alle Diagramme in einem Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API (v3.0) löschen. Enthält Endpunkt, Parameter, cURL-Beispiel, SDK-Code-Snippets, Authentifizierungsschritte und Fehlerbehandlung."
ArticleTitle: "Alle Diagramme aus einem Arbeitsblatt mit der Aspose.Cells Cloud API löschen"
---

Diese REST API löscht alle Diagramme aus dem angegebenen Arbeitsblatt.

**Hintergrund** – Das Entfernen aller Diagramme aus einem Arbeitsblatt ist nützlich, wenn Sie das visuelle Layout einer Tabelle zurücksetzen, veraltete Visualisierungen ersetzen oder eine Arbeitsmappe für die erneute Verwendung vorbereiten möchten, ohne vorherige Diagrammdaten beizubehalten.

Vor dem Aufrufen der API stellen Sie sicher, dass die folgenden Voraussetzungen erfüllt sind:

- Ein gültiges JWT-Token steht für die Authentifizierung zur Verfügung.  
- Die Arbeitsmappendatei existiert am angegebenen Speicherort und im angegebenen Ordner.  
- Sie verwenden API-Version **v3.0**.

## DeleteWorksheetClearCharts API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername   | Typ    | Ort   | Beschreibung                                |
| --------------- | ------ | ----- | ------------------------------------------- |
| name            | string | path  | Name der Arbeitsmappendatei.                |
| sheetName       | string | path  | Name des Arbeitsblatts.                     |
| folder          | string | query | Ordner, in dem die Arbeitsmappe gespeichert ist. |
| storageName     | string | query | Name des Speichers.                         |

**Anforderungsheader**

| Header        | Beschreibung                     |
|---------------|----------------------------------|
| Authorization | Bearer `<jwt token>`             |
| Accept        | `application/json`               |
| Content-Type  | `application/json` (kein Body)   |

**Anforderungstext**

Der DELETE-Vorgang erfordert **keinen** Anforderungstext.

**Antwort**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                               |
|------|-----------------------------|------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token. |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet die maximale Größe. |
| 500  | Internal Server Error       | Unerwarteter Serverfehler. |

*Beispiel für Fehlerantworten*

```json
// 400 Bad Request
{
    "Code": 400,
    "Message": "Ungültiger Parameter: 'sheetName' ist erforderlich."
}

// 401 Unauthorized
{
    "Code": 401,
    "Message": "Authentifizierung fehlgeschlagen. Ungültiges JWT-Token."
}

// 413 Payload Too Large
{
    "Code": 413,
    "Message": "Die Anforderungsnutzlast überschreitet die maximal zulässige Größe."
}

// 500 Internal Server Error
{
    "Code": 500,
    "Message": "Auf dem Server ist ein unerwarteter Fehler aufgetreten."
}
```

## Verwendung der DeleteWorksheetClearCharts API mit SDKs

### DeleteWorksheetClearCharts API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetClearCharts) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/charts" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```


{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Verwendung von Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, die Entwicklungszeit zu verkürzen, wenn Sie **alle Diagramme** aus einem Arbeitsblatt löschen müssen. Ein SDK übernimmt die Details auf niedriger Ebene und lässt Sie sich auf Ihre Projekt Aufgaben konzentrieren. Weitere Informationen finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-DeleteAllCharts-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-DeleteAllCharts-delete-all-charts.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetClearCharts-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-clear_the_charts-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteAllChartsFromAWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-DeleteAllCharts-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-DeleteAllCharts-delete-all-charts.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-DeleteAllCharts-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "1775c5a8985efa819486b7ede2c34bfc" >}}

{{< /tab >}}

{{< /tabs >}}
---