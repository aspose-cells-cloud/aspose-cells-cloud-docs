---
title: "Datumsfilter zu einem Excel-Arbeitsblatt hinzufügen"
second_title: "Dokument"
linktitle: "Datumsfilter hinzufügen"
type: docs
url: /de/autofilter/add-date-filter/
aliases:
  - /add-date-filter-in-a-worksheet/
  - /autofilter/add-a-date-filter/
description: "Erfahren Sie, wie Sie mithilfe der Aspose.Cells Cloud REST API (v3.0) einen Datumsfilter zu einem Excel-Arbeitsblatt hinzufügen. Enthält cURL-Beispiel, SDK-Snippets (C#, Java, Python usw.), Parameter und Fehlerbehandlung."
weight: 65
ArticleTitle: "Datumsfilter zu einem Excel-Arbeitsblatt hinzufügen | Aspose.Cells Cloud API"
keywords: "Aspose.Cells, Excel-Datumsfilter, AutoFilter-API, REST-API, Cloud-SDK, cURL, Tabellenkalkulationsautomatisierung"
---

Diese REST-API fügt einem Excel-Arbeitsblatt einen **Datumsfilter** hinzu.

**Voraussetzungen:** Sie müssen über ein gültiges JWT-Token verfügen, und die Zielarbeitsmappe muss bereits am angegebenen Speicherort vorhanden sein. Die Anfrage erfordert keinen JSON-Body.

## PutWorksheetDateFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dateFilter
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anfrageparameter


| Parametername            | Typ     | Ort     | Beschreibung                                                                                                                                                      |
| ------------------------ | ------- | ------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**                 | string  | Path    | Name der Arbeitsmappe.                                                                                                                                            |
| **sheetName**            | string  | Path    | Name des Arbeitsblatts.                                                                                                                                           |
| **range**                | string  | Query   | Excel-Bereich, auf den der Filter angewendet wird (z. B. `A1:B1`).                                                                                               |
| **fieldIndex**           | integer | Query   | Nullbasierter Index der zu filternden Spalte.                                                                                                                     |
| **dateTimeGroupingType** | string  | Query   | Gruppierungstyp für den Datums-/Uhrzeitfilter. Zulässige Werte sind `Day`, `Hour`, `Minute`, `Month`, `Second`, `Year`. Werte sind groß-/kleinschreibungsabhängig; der Standardwert ist `Day`. |
| **year**                 | integer | Query   | Jahreskomponente des Filterwerts.                                                                                                                                 |
| **month**                | integer | Query   | Monatskomponente des Filterwerts.                                                                                                                                 |
| **day**                  | integer | Query   | Tageskomponente des Filterwerts.                                                                                                                                  |
| **hour**                 | integer | Query   | Stundenkomponente des Filterwerts.                                                                                                                                |
| **minute**               | integer | Query   | Minutenkomponente des Filterwerts.                                                                                                                                |
| **second**               | integer | Query   | Sekundenkomponente des Filterwerts.                                                                                                                               |
| **matchBlanks**          | boolean | Query   | Leere Zellen einschließen (`true` oder `false`).                                                                                                                 |
| **refresh**              | boolean | Query   | Filter nach Anwendung aktualisieren (`true` oder `false`).                                                                                                       |
| **folder**               | string  | Query   | Ordnerpfad der ursprünglichen Arbeitsmappe.                                                                                                                       |
| **storageName**          | string  | Query   | Name des Speicherdienstes.                                                                                                                                        |

*Die PUT-Anfrage erfordert keinen Anfragebody; alle Parameter werden über die Abfragezeichenfolge übergeben.*

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
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).      |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                         |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.                        |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                                   |

## Verwendung der PutWorksheetDateFilter API mit SDKs

### PutWorksheetDateFilter API-Spezifikation


Die <a href="https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetDateFilter" rel="noopener noreferrer">OpenAPI-Spezifikation</a> definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt über einen Webbrowser.

Sie können das Kommandozeilentool **cURL** verwenden, um problemlos auf die Aspose.Cells-Webservices zuzugreifen. Das folgende Beispiel zeigt, wie ein Aufruf der Cloud-API mit cURL erfolgt.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dateFilter?range=A1:B1&fieldIndex=0&dateTimeGroupingType=Year&year=1920&refresh=true" \
-X PUT \
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

Die Verwendung eines SDKs ist die schnellste Möglichkeit zur Entwicklung. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihre Projektinhalte konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a>.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetDateFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetDateFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetDateFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetDateFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_PutWorksheetDateFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetDateFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetDateFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetDateFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}
---