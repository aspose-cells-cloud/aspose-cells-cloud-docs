---
title: "Ein Pivot-Feld zu einer Pivot-Tabelle hinzufügen"
second_title: "Dokument"
linktitle: "Pivot-Feld hinzufügen"
type: docs
url: /de/pivot-tables/add-pivot-field/
aliases: [  /de/add-a-pivot-table-in-a-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel, Pivot-Tabelle, Pivot-Feld hinzufügen, REST API, SDK"
description: "Fügen Sie ein Pivot-Feld mit der Aspose.Cells Cloud REST API zu einer vorhandenen Pivot-Tabelle hinzu. Enthält Anforderungsdetails, cURL-Beispiel und SDK-Snippets."
weight: 40
ArticleTitle: "Ein Pivot-Feld zu einer Pivot-Tabelle hinzufügen – Aspose.Cells Cloud-Dokumentation"
---

Diese REST API **fügt** ein Pivot-Feld zu einer vorhandenen Pivot-Tabelle hinzu.

> **Voraussetzung:** Um diesen Endpunkt aufzurufen, müssen Sie ein gültiges JWT-Authentifizierungstoken im `Authorization`-Header angeben und sicherstellen, dass die Arbeitsmappe im angegebenen Ordner oder im Standard-Speicher gespeichert ist.

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField
```

### Anforderungsparameter

| Parametername       | Typ     | Position | Beschreibung                                                                 |
| ------------------- | ------- | -------- | ---------------------------------------------------------------------------- |
| name                | string  | path     | Name des Dokuments.                                                          |
| sheetName           | string  | path     | Name des Arbeitsblatts.                                                      |
| pivotTableIndex     | integer | path     | Index der Pivot-Tabelle.                                                     |
| pivotFieldType      | string  | query    | Typ des Feldbereichs (z. B. Row, Column).                                   |
| request             | object  | body     | DTO, das die zu hinzufügenden Feldindizes enthält.                           |
| needReCalculate     | boolean | query    | Auf **true** setzen, um die Pivot-Tabelle nach der Operation neu zu berechnen. |
| folder              | string  | query    | Ordner, in dem das Dokument gespeichert ist.                                |
| storageName         | string  | query    | Name des Speichers.                                                          |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/PivotTables/PutPivotTableField) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser heraus durchzuführen.

Sie können das Kommandozeilentool **cURL** verwenden, um Aspose.Cells-Webdienste aufzurufen. Das folgende Beispiel zeigt, wie ein Pivot-Feld mithilfe von cURL hinzugefügt wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/PivotField?pivotFieldType=Row" \
  -X PUT \
  -d '{"Data":[1,2]}' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
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

Die erfolgreiche Antwort gibt ein JSON-Objekt mit den Feldern `Code` und `Status` zurück. Beispiel-Schema:

```json
{
  "Code": 0,        // Ganzzahl, die den HTTP-Statuscode angibt
  "Status": "OK"    // Zeichenfolge mit einer Nachricht
}
```

Mögliche Fehlerantworten umfassen **400 Bad Request** bei fehlenden Parametern, **401 Unauthorized**, wenn das Token ungültig ist, und **500 Internal Server Error** bei Serverproblemen.

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die schnellste Möglichkeit, diese Funktion zu integrieren. SDKs übernehmen die Details der unteren Schichten, sodass Sie sich auf Ihre Geschäftslogik konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="Ruby" tabName4="Python" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-AddPivotFieldInPivottable-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-AddPivotFieldInPivottable-add-pivot-field.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddPivotFieldInPivotTable.py" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-AddPivotFieldInPivottable-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-AddPivotFieldInPivottable-add-pivot-field.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-AddPivotFieldInPivottable-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "8f9b66d50f7cfa2b14c24fa7ddb396e7" >}}

{{< /tab >}}

{{< /tabs >}}

**Siehe auch:**  
- [Eine Pivot-Tabelle hinzufügen](https://docs.aspose.cloud/cells/pivot-tables/add-pivot-table/)  
- [Pivot-Feld löschen](https://docs.aspose.cloud/cells/pivot-tables/delete-pivot-field/)