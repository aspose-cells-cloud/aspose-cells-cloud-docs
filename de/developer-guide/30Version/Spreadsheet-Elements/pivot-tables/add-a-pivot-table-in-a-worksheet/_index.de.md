---
title: "Hinzufügen einer Pivot-Tabelle in einem Excel-Arbeitsblatt"
second_title: "Dokument"
linktitle: Hinzufügen
type: docs
url: /pivot-tables/add/
aliases: [/add-a-pivot-table-in-a-worksheet/]
keywords: "Pivot-Tabelle hinzufügen, Excel-Arbeitsblatt, Aspose.Cells Cloud, REST-API, SDK, Excel-Pivot-Tabelle"
description: "Verwenden Sie die Aspose.Cells Cloud REST-API, um eine Pivot-Tabelle in ein Excel-Arbeitsblatt einzufügen. Verfügbar über SDKs für C#, Java, PHP, Python, Node.js, Android, Swift, Perl, Go."
weight: 30
ArticleTitle: "So fügen Sie eine Pivot-Tabelle in ein Excel-Arbeitsblatt mithilfe von Aspose.Cells Cloud hinzu"
---

Diese REST-API fügt eine Pivot-Tabelle in ein Arbeitsblatt ein.

**Voraussetzungen:**  
- Ein Aspose.Cells Cloud-Konto mit einem gültigen JWT-Zugriffstoken.  
- Die Zielarbeitsmappe muss in einem unterstützten Speicherort gespeichert sein (Standardspeicher oder benutzerdefinierter Speicher).  
- Das Arbeitsblatt, das durch `sheetName` angegeben wird, muss in der Arbeitsmappe vorhanden sein.  

## PutWorksheetPivotTable API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter**

| Parametername   | Typ     | Position | Beschreibung                                                                                                                         |
| --------------- | ------- | -------- | ------------------------------------------------------------------------------------------------------------------------------------ |
| name            | string  | path     | Der Name der Excel-Datei.                                                                                                            |
| sheetName       | string  | path     | Der Name des Arbeitsblatts, in dem die Pivot-Tabelle erstellt werden soll.                                                           |
| request         | object  | body     | `CreatePivotTableRequest`-DTO, das die Pivot-Tabellendefinition enthält.                                                             |
| folder          | string  | query    | Der Ordner, der das Dokument enthält.                                                                                                |
| storageName     | string  | query    | Der Name des Speichers, in dem sich das Dokument befindet.                                                                           |
| sourceData      | string  | query    | Der Bereich, der die Quelldaten für den neuen Pivot-Tabellencache bereitstellt (z. B. `A5:E10`).                                    |
| destCellName    | string  | query    | Die Adresse der oberen linken Zelle des Zielbereichs für den Pivot-Tabellenbericht.                                                 |
| tableName       | string  | query    | Der Name, der der neuen Pivot-Tabelle zugewiesen wird.                                                                               |
| useSameSource   | boolean | query    | Wenn `true`, verwendet die neue Pivot-Tabelle eine bereits vorhandene Quelldatenquelle und spart Speicherplatz, sofern diese bereits verwendet wurde. |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/PivotTables/PutWorksheetPivotTable) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt über einen Webbrowser.

Sie können das Kommandozeilentool **cURL** verwenden, um problemlos auf Aspose.Cells-Webservices zuzugreifen. Das folgende Beispiel zeigt, wie die Cloud-API mit cURL aufgerufen wird.

**Sicherheitshinweis:** Verwenden Sie stets `https://` beim Aufruf der API, und bewahren Sie Ihr JWT-Token vertraulich auf; die Übertragung über HTTP ohne Verschlüsselung birgt das Risiko, dass das Token abgefangen wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/pivottables" \
-X PUT \
-d '{"Name":"MyPivot","SourceData":"A5:E10","DestCellName":"H20","UseSameSource":true,"PivotFieldRows":[1],"PivotFieldColumns":[1],"PivotFieldData":[1]}' \
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

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                                 |
|------|-----------------------------|------------------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang.         |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).     |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                        |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.                       |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                                   |

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details und ermöglicht es Ihnen, sich auf Ihre Projektziele zu konzentrieren. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-AddPivottableWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-AddPivottableWorksheet-add-pivot-table-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddPivotTableInw" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-AddPivottableWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-AddPivottableWorksheet-add-pivot-table-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-AddPivottableWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "980246b631d7816f257f2ad4664788ea" >}}

{{< /tab >}}

{{< /tabs >}}

Weitere Vorgänge finden Sie auf den zugehörigen API-Seiten: **[Abrufen einer Pivot-Tabelle](https://docs.aspose.cloud/cells/pivot-tables/get/)**, **[Löschen einer Pivot-Tabelle](https://docs.aspose.cloud/cells/pivot-tables/delete/)** und **[Aktualisieren einer Pivot-Tabelle](https://docs.aspose.cloud/cells/pivot-tables/update/)**.