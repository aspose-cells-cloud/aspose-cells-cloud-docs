---
title: "Gruppieren von Zeilen in einem Excel-Arbeitsblatt"
second_title: "Dokument"
linktitle: "Gruppieren"
type: docs
url: /de/rows/group/
aliases: [  /de/group-rows-in-excel-worksheet/ ]
keywords: "Zeilen gruppieren, Excel, Aspose.Cells Cloud, REST API, SDK, Arbeitsblatt, Excel-API"
description: "Gruppieren Sie Zeilen in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API. Unterstützt mehrere SDKs (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go) für einfache Integration."
weight: 60
ArticleTitle: "Gruppieren von Zeilen in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud API"
---

Diese REST API gruppiert Zeilen in einem Excel-Arbeitsblatt.

**Voraussetzungen:**  
- Ein gültiges OAuth 2.0-Zugriffstoken (Bearer JWT) muss im `Authorization`-Header übermittelt werden.  
- Die Arbeitsmappe muss bereits im angegebenen `folder` des gewählten `storageName` (oder im Standard-Speicher) vorhanden sein, bevor die Anforderung gestellt wird.

## PostGroupWorksheetRows API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/group
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter**

| Parametername   | Typ     | Ort     | Beschreibung                                                             |
| ---------------- | ------- | ------- | ------------------------------------------------------------------------ |
| name             | string  | path    | Der Name der Arbeitsmappendatei.                                         |
| sheetName        | string  | path    | Der Name des Arbeitsblatts.                                              |
| firstIndex       | integer | query   | Nullbasierter Index der ersten zu gruppierenden Zeile.                  |
| lastIndex        | integer | query   | Nullbasierter Index der letzten zu gruppierenden Zeile.                 |
| hide             | boolean | query   | Gibt an, ob die gruppierten Zeilen ausgeblendet werden sollen (`true` oder `false`). |
| folder           | string  | query   | Pfad zum Ordner, der die Arbeitsmappe enthält.                           |
| storageName      | string  | query   | Name des Speichers, in dem sich die Arbeitsmappe befindet.              |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Cells/PostGroupWorksheetRows) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf Aspose.Cells-Webservices zuzugreifen. Das folgende Beispiel zeigt, wie Aufrufe an die Cloud-API mit cURL durchgeführt werden.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/group?firstIndex=1&lastIndex=2&hide=true" \
-X POST \
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

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                                 |
|------|-----------------------------|------------------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang.         |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).     |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                        |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.                       |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                                  |

Typische Fehlerantworten:

- **400 Bad Request** – Stellen Sie sicher, dass `firstIndex` und `lastIndex` gültige Ganzzahlen sind und dass `firstIndex` ≤ `lastIndex` gilt.  
- **401 Unauthorized** – Prüfen Sie, ob der `Authorization`-Header ein aktuelles JWT-Token enthält.  
- **404 Not Found** – Stellen Sie sicher, dass die Arbeitsmappe (`name`) und das Arbeitsblatt (`sheetName`) im angegebenen `folder`/`storageName` vorhanden sind.

{{< /tab >}}

{{< /tabs >}}

**Siehe auch:** [Zeilen in einem Excel-Arbeitsblatt aufheben](../rows/ungroup/ "Zeilen in einem Excel-Arbeitsblatt aufheben"), [Zeilen in einem Excel-Arbeitsblatt ausblenden](../rows/hide/ "Zeilen in einem Excel-Arbeitsblatt ausblenden"), [Zeilen in einem Excel-Arbeitsblatt einblenden](../rows/unhide/ "Zeilen in einem Excel-Arbeitsblatt einblenden").

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die beste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK übernimmt Low-Level-Details, sodass Sie sich auf Ihre Projekt Aufgaben konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostGroupWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostGroupWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostGroupWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostGroupWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostGroupWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostGroupWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostGroupWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostGroupWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}