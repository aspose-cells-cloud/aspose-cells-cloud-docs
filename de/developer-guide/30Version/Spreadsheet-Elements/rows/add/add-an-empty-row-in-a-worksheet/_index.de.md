---
title: "Fügen Sie eine leere Zeile in ein Excel-Arbeitsblatt ein"
ArticleTitle: "Fügen Sie eine leere Zeile in ein Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud API ein"
second_title: "Dokument"
linktype: "Row"
type: docs
url: /de/rows/add/row/
aliases: [  /de/add-an-empty-row-in-a-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel, leere Zeile hinzufügen, Arbeitsblatt, REST-API, Zeile einfügen, Cloud-Tabellenkalkulation"
description: "Verwenden Sie die Aspose.Cells Cloud REST API, um eine leere Zeile in ein Excel-Arbeitsblatt einzufügen. Unterstützt mehrere SDKs (C#, Java, Python, Go, PHP, Ruby, Node.js, Perl, Android, Swift) für schnelle Entwicklung."
weight: 20
---

Diese REST API fügt eine neue Zeile in ein Excel-Arbeitsblatt ein. Sie fügt eine leere Zeile am angegebenen nullbasierten Index ein.

**Voraussetzungen:**  
- Ein gültiger Aspose Cloud-Zugriffstoken (Bearer JWT) muss im `Authorization`-Header enthalten sein.  
- Die Ziel-Arbeitsmappe muss in Ihren Aspose Cloud-Speicher hochgeladen sein, und die Parameter `folder` und `storageName` müssen auf ihren Speicherort zeigen.

**Hinweise:**  
- Der `rowIndex` ist nullbasiert; das Einfügen bei Index 0 fügt eine Zeile oben im Arbeitsblatt ein.  
- Excel-Arbeitsblätter haben maximal 1.048.576 Zeilen; der Versuch, darüber hinaus einzufügen, führt zu einem Fehler.

## PutInsertWorksheetRow API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter**

| Parametername   | Typ     | Position | Beschreibung                                            |
| --------------- | ------- | -------- | ------------------------------------------------------- |
| name            | string  | path     | Der Name der Arbeitsmappen-Datei.                       |
| sheetName       | string  | path     | Der Name des Arbeitsblatts.                             |
| rowIndex        | integer | path     | Der nullbasierte Index, an dem die neue Zeile eingefügt wird. |
| folder          | string  | query    | Der Ordnerpfad im Speicher, in dem sich die Arbeitsmappe befindet. |
| storageName     | string  | query    | Der Name des zu verwendenden Aspose Cloud-Speichers.    |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetRow) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webservices einfach aufzurufen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/10" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **Hinweis:** Alle Aspose.Cells Cloud-Endpunkte erfordern HTTPS. Verwenden Sie für Produktionsaufrufe das sichere Schema `https://`.

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

| Code | Bedeutung                   | Beschreibung                                            |
|------|-----------------------------|---------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Operationsdetails. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiger oder fehlender JWT-Token.                    |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.   |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                              |

*Beispiel einer Fehlerantwort (z. B. wenn der Zeilenindex das Arbeitsblatt-Limit überschreitet):*

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "Zeilenindex außerhalb des gültigen Bereichs. Maximal zulässige Zeilen: 1048576."
}
```

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK abstrahiert Low-Level-Details und ermöglicht es Ihnen, sich auf Ihre Projektziele zu konzentrieren. Besuchen Sie das <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a>, um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetRow.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetRow.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetRow.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetRow.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetRow.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetRow.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetRow.go" >}}

{{< /tab >}}

{{< /tabs >}}