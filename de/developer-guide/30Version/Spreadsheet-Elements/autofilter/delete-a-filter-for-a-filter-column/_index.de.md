---
title: "Ein Filter aus einem Excel-Arbeitsblatt löschen – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Filter löschen"
type: docs
url: /de/delete-filter/
aliases: [/de/delete-a-filter-for-a-filter-column/, /de/delete-auto-filter/]
keywords: "Aspose.Cells Cloud Filter löschen, Excel, REST API, SDK"
description: "Erfahren Sie, wie Sie einen AutoFilter aus einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API, cURL und SDKs (C#, Java, Python usw.) löschen. Enthält Endpunkt, Parameter, Authentifizierung und Beispielcode."
weight: 100
---

## REST API

Diese REST API löscht einen **AutoFilter** in einem Excel-Arbeitsblatt.

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/filter
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername            | Typ     | Ort      | Erforderlich? | Beschreibung                                                                                      |
| ------------------------ | ------- | -------- | ------------- | ------------------------------------------------------------------------------------------------- |
| **name**                 | string  | Path     | Ja            | Der Name der Arbeitsmappe.                                                                        |
| **sheetName**            | string  | Path     | Ja            | Der Name des Arbeitsblatts.                                                                       |
| **range**                | string  | Query    | Nein          | Der Zellbereich, auf den der Filter angewendet wird (z. B. `A1:C10`).                             |
| **fieldIndex**           | integer | Query    | Ja            | Nullbasierter Index der Spalte, auf die der Filter angewendet wird.                               |
| **dateTimeGroupingType** | string  | Query    | Nein          | Art der Gruppierung von Datums-/Uhrzeitenwerten: `Day`, `Hour`, `Minute`, `Month`, `Second` oder `Year`. |
| **year**                 | integer | Query    | Nein          | Jahreskomponente für Datumsgruppierung.                                                           |
| **month**                | integer | Query    | Nein          | Monatskomponente für Datumsgruppierung.                                                           |
| **day**                  | integer | Query    | Nein          | Tageskomponente für Datumsgruppierung.                                                            |
| **hour**                 | integer | Query    | Nein          | Stundenkomponente für Datumsgruppierung.                                                          |
| **minute**               | integer | Query    | Nein          | Minutenkomponente für Datumsgruppierung.                                                          |
| **second**               | integer | Query    | Nein          | Sekundenkomponente für Datumsgruppierung.                                                         |
| **matchBlanks**          | boolean | Query    | Nein          | `true` / `false` – ob leere Zellen in den Filter einbezogen werden.                               |
| **refresh**              | boolean | Query    | Nein          | `true` / `false` – ob das Arbeitsblatt nach dem Löschen aktualisiert werden soll.                 |
| **folder**               | string  | Query    | Nein          | Ursprünglicher Ordner der Arbeitsmappe.                                                            |
| **storageName**          | string  | Query    | Nein          | Name des Speichers.                                                                                |

### **Antwort**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                                 |
|------|-----------------------------|------------------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang.         |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).     |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                        |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.                       |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                                   |

## Verwendung der DeleteWorksheetFilter API mit SDKs

### Spezifikation der DeleteWorksheetFilter API

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/AutoFilter/DeleteWorksheetFilter) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie die Cloud API mit cURL aufgerufen wird.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/filter?fieldIndex=0&dateTimeGroupingType=Year" \
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

{{< /tab >}}

{{< /tabs >}}

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist die effizienteste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK übernimmt Details auf niedriger Ebene, sodass Sie sich auf die Aufgaben Ihres Projekts konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}