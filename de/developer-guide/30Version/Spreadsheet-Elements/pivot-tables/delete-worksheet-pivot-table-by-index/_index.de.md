---
title: "Löschen einer Pivot-Tabelle in einem Excel-Arbeitsblatt"
second_title: "Document"
linktype: Delete
type: docs
url: /pivot-tables/delete/
aliases: [/delete-worksheet-pivot-table-by-index/]
keywords: "Aspose.Cells, Pivot-Tabelle, löschen, Excel, REST API"
description: "Löschen einer Pivot-Tabelle aus einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API (v3.0). Enthält Anforderungsformat, cURL-Beispiel, Fehlercodes und SDK-Snippets für C#, Java, Python und Node.js."
weight: 70
ArticleTitle: "So löschen Sie eine Pivot-Tabelle in einem Excel-Arbeitsblatt mit Aspose.Cells Cloud"
---

Diese REST API löscht eine Pivot-Tabelle aus einem Arbeitsblatt anhand ihres Index.

**Voraussetzungen** – Sie benötigen ein gültiges JWT-Access-Token für Aspose.Cells Cloud sowie die Ziel-Excel-Datei in einem unterstützten Speicherort. Stellen Sie sicher, dass Dateiname, Arbeitsblattname und Speicherdetails korrekt angegeben sind, bevor Sie die API aufrufen.

Pivot-Tabellen sind eine leistungsfähige Möglichkeit, Daten in einem **Excel-Arbeitsblatt** zusammenzufassen. Mithilfe von Aspose.Cells Cloud können Sie eine unerwünschte Pivot-Tabelle programmgesteuert mit einem einzigen HTTP-DELETE-Aufruf entfernen. Dieser Vorgang eignet sich ideal, um Arbeitsblätter zu bereinigen, Berichtsgenerierungen zu automatisieren oder Excel-Manipulationen in Ihre Anwendungen zu integrieren.

## DeleteWorksheetPivotTable API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter**

| Parametername     | Typ     | Speicherort | Beschreibung                                              |
| ----------------- | ------- | ----------- | --------------------------------------------------------- |
| name              | string  | path        | Name der Excel-Datei.                                     |
| sheetName         | string  | path        | Name des Arbeitsblatts, das die Pivot-Tabelle enthält.   |
| pivotTableIndex   | integer | path        | Nullbasierter Index der zu löschenden Pivot-Tabelle.     |
| folder            | string  | query       | Pfad zum Ordner, in dem das Dokument gespeichert ist.    |
| storageName       | string  | query       | Name des Speicherdienstes.                                |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/PivotTables/DeleteWorksheetPivotTable) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

Sie können das **cURL-Befehlszeilentool** verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie mithilfe von cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**Beispiel für Antwort**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Die Antwort folgt einem einfachen JSON-Schema:

```json
{
  "Code": integer,   // HTTP-ähnlicher Statuscode des Vorgangs
  "Status": string   // Textuelle Beschreibung, z. B. "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Fehlerbehandlung

Die häufigsten Antwort-Statuscodes sind nachfolgend aufgeführt:

| HTTP-Status | Beschreibung                                                    |
| ----------- | --------------------------------------------------------------- |
| 400         | Ungültige Anforderung – fehlende oder ungültige Parameter.     |
| 401         | Nicht autorisiert – ungültiges oder fehlendes JWT-Token.       |
| 404         | Nicht gefunden – die Datei, das Arbeitsblatt oder die Pivot-Tabelle ist nicht vorhanden. |
| 500         | Interner Serverfehler – ein unerwarteter Zustand trat auf dem Server auf. |

## Cloud SDK Family

Die Verwendung eines SDKs ist die beste Möglichkeit, die Entwicklungsgeschwindigkeit zu erhöhen. Ein SDK übernimmt die Details der unteren Schicht und lässt Sie sich auf Ihre Projekt Aufgaben konzentrieren. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-DeleteWorksheetPivotTableIndex-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-DeleteWorksheetPivotTableIndex-delete-worksheet-pivot-table-index.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteWorksheetPivotTablesByIndex.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-DeleteWorksheetPivotTableIndex-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-DeleteWorksheetPivotTableIndex-delete-worksheet-pivot-table-index.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-DeleteWorksheetPivotTableIndex-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "8798eca5f30bf41a4675b83583a72ec3" >}}

{{< /tab >}}

{{< /tabs >}}
---