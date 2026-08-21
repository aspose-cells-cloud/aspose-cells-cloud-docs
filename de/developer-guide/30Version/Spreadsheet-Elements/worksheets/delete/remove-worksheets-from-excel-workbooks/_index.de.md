---
title: "Arbeitsblatt löschen"
second_title: "Dokument"
linktitle: "Ein Arbeitsblatt"
type: docs
url: /de/worksheets/delete-worksheet/
aliases: [  /de/remove-worksheets-from-excel-workbooks/ ]
keywords: "Aspose.Cells Cloud, Arbeitsblatt löschen, Excel, Tabellendokument, REST-API"
description: "Löschen Sie ein Arbeitsblatt aus einer Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud REST-API. Unterstützt SDKs für C#, Java, PHP, Ruby, Node.js, Python, Perl, Go und cURL."
weight: 20
ArticleTitle: "Arbeitsblatt löschen – Aspose.Cells Cloud API"
---

Diese REST-API löscht ein Arbeitsblatt.  
Voraussetzungen: Um diese API aufzurufen, müssen Sie ein gültiges JWT-Authentifizierungstoken im **Authorization**-Header bereitstellen und Zugriff auf den Speicherort haben, an dem sich die Arbeitsmappe befindet.

## REST-API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

*Hinweis: Die API verwendet Version **v3.0**, die gegenwärtig die stabile Version ist. Zukünftige Versionen werden in den Release Notes angekündigt.*

### **Anforderungsparameter**

| Parametername | Typ    | Ort     | Beschreibung           |
| ------------- | ------ | ------- | ---------------------- |
| name          | string | path    | Name des Dokuments.    |
| sheetName     | string | path    | Name des Arbeitsblatts.|
| folder        | string | query   | Ordner des Dokuments.  |
| storageName   | string | query   | Name des Speichers.    |

Mögliche HTTP-Antworten:

| Statuscode | Beschreibung                                      |
| ---------- | ------------------------------------------------- |
| 200 OK     | Arbeitsblatt erfolgreich gelöscht.                |
| 400 Bad Request | Ungültige Anforderungsparameter.              |
| 401 Unauthorized | Authentifizierung fehlgeschlagen oder Token fehlt. |
| 404 Not Found | Angegebene Arbeitsmappe oder Arbeitsblatt existiert nicht. |
| 500 Internal Server Error | Unerwarteter Serverfehler.                 |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Worksheets/DeleteWorksheet) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool nutzen, um problemlos auf Aspose.Cells-Webservices zuzugreifen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet3" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

*Alle Anforderungen müssen über HTTPS erfolgen; die API unterstützt keine Nicht-TLS-Verbindungen.*

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

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf die Aufgaben Ihres Projekts konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webservices mithilfe verschiedener SDKs durchgeführt werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheet.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheet.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheet.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheet.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheet.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheet.go" >}}

{{< /tab >}}

{{< /tabs >}}