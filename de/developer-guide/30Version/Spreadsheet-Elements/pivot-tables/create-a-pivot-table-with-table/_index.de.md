---
title: "Tabelle in Pivot-Tabelle umwandeln"
second_title: "Dokument"
linktitle: Umwandeln
type: docs
url: /pivot-tables/convert-table-to-pivottable/
aliases:
  [
    /create-a-pivottable-with-table/,
    /create-new-pivot-table-with-list-object-as-source-data/,
  ]
keywords: "Pivot-Tabelle, Listenobjekt, Aspose.Cells Cloud, REST API, Tabelle in Pivot-Tabelle umwandeln"
description: "Erfahren Sie, wie Sie mit der Aspose.Cells Cloud REST API eine Pivot-Tabelle aus einem Listenobjekt erstellen. Enthält Anforderungsdetails, ein cURL-Beispiel und SDK-Referenzen."
weight: 60
ArticleTitle: "Tabelle in Pivot-Tabelle umwandeln – Aspose.Cells Cloud-Dokumentation"
---

Diese REST API erstellt eine **Pivot-Tabelle** aus einem Listenobjekt.

Eine Pivot-Tabelle fasst Daten aus einem Listenobjekt zusammen und ermöglicht es Ihnen, große Datensätze direkt in der Arbeitsmappe zu analysieren und zu berichten.

**Voraussetzungen:**  
- Ein gültiges JWT-Bearer-Token zur Authentifizierung.  
- Die Arbeitsmappe muss im angegebenen Speicherort vorhanden sein.  
- Das Ziel-Blatt muss das Listenobjekt enthalten, das Sie zusammenfassen möchten.

## PostWorksheetListObjectSummarizeWithPivotTable API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/SummarizeWithPivotTable
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter**

| Parametername     | Typ    | Ort    | Beschreibung                                    |
| ----------------- | ------ | ------ | ----------------------------------------------- |
| name              | string | path   | Dateiname der Arbeitsmappe.                     |
| sheetName         | string | path   | Blatt, das das Listenobjekt enthält.            |
| listObjectIndex   | integer| path   | Index des Listenobjekts im Blatt.               |
| destsheetName     | string | query  | Name des Zielblatts.                            |
| request           | object | body   | JSON-Payload, die die Pivot-Tabelle definiert.  |
| folder            | string | query  | Ordnerpfad, in dem sich die Arbeitsmappe befindet. |
| storageName       | string | query  | Name des Speichers.                             |

Der Anforderungstext muss dem unten definierten JSON-Schema entsprechen:

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "object",
  "properties": {
    "Name": { "type": "string", "description": "Name der neuen Pivot-Tabelle." },
    "DestCellName": { "type": "string", "description": "Obere linke Zelle der Pivot-Tabelle (z. B. \"C1\")." },
    "PivotFieldRows": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "Nullbasierte Indizes der Felder, die in den Zeilen platziert werden sollen."
    },
    "PivotFieldColumns": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "Nullbasierte Indizes der Felder, die in den Spalten platziert werden sollen."
    },
    "PivotFieldData": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "Nullbasierte Indizes der Felder, die als Datenfelder verwendet werden sollen."
    }
  },
  "required": ["Name", "DestCellName", "PivotFieldRows", "PivotFieldColumns", "PivotFieldData"]
}
```

Die <a href="https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObjectSummarizeWithPivotTable" rel="noopener noreferrer">OpenAPI-Spezifikation</a> definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

Sie können das Kommandozeilentool **cURL** verwenden, um einfach auf die Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/TestCase.xlsx/worksheets/Sheet2/listobjects/0/SummarizeWithPivotTable?folder=CellsTests&destsheetName=Sheet4" \
-X POST \
-d '{"Name":"TestPivot","DestCellName":"C1","PivotFieldRows":[0,1],"PivotFieldColumns":[2],"PivotFieldData":[3,4]}' \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

*Hinweis: Verwenden Sie für Produktionsumgebungen den Produktionsendpunkt (`api.aspose.cloud`). Der QA-Endpunkt (`api-qa.aspose.cloud`) ist ausschließlich für Testzwecke vorgesehen. HTTPS ist für alle Produktionsaufrufe erforderlich.*

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

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                      |
|------|-----------------------------|-------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details des Vorgangs. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                            |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.           |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                       |

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die beste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK übernimmt Details auf niedriger Ebene und ermöglicht es Ihnen, sich auf Ihre Projektaktivitäten zu konzentrieren. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an die Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:
---