---
title: "Ein benutzerdefiniertes Kriterium in einem Excel-Arbeitsblatt hinzufügen"
second_title: "Dokument"
linktitle: "Benutzerdefinierten Filter hinzufügen"
type: docs
url: /autofilter/add-custom-filter/
aliases: [/filter-a-list-with-a-custom-criteria/,/autofilter/add-a-custom-filter/]
keywords: "Excel, benutzerdefinierter Filter, Aspose.Cells Cloud, REST-API, AutoFilter, Arbeitsblatt, benutzerdefiniertes Kriterium"
description: "Erfahren Sie, wie Sie mit der Aspose.Cells Cloud REST-API einen benutzerdefinierten Filter in einem Excel-Arbeitsblatt anwenden. Enthält Anforderungsdetails, ein cURL-Beispiel und SDK-Codebeispiele für mehrere Programmiersprachen."
weight: 65
ArticleTitle: "Ein benutzerdefiniertes Kriterium in einem Excel-Arbeitsblatt hinzufügen – Aspose.Cells Cloud API"
---

Diese REST-API filtert eine Liste mithilfe eines **benutzerdefinierten Kriteriums**.

## PutWorksheetCustomFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/custom
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter:

| Parametername     | Typ     | Standort              | Beschreibung                                                                 |
|-------------------|---------|-----------------------|------------------------------------------------------------------------------|
| name              | string  | path                  | Name der Excel-Datei.                                                        |
| sheetName         | string  | path                  | Name des Arbeitsblatts, das die zu filternden Daten enthält.                |
| range             | string  | query                 | Zellbereich, auf den der Filter angewendet wird (z. B. `A1:B1`).           |
| fieldIndex        | integer | query                 | Nullbasierter Index der Spalte, auf die der Filter angewendet wird.        |
| operatorType1     | string  | query                 | Erster Vergleichsoperator (z. B. `LessOrEqual`, `Equal`).                   |
| criteria1         | string  | query                 | Erster Filterwert oder Ausdruck.                                             |
| isAnd             | boolean | query                 | Wenn `true`, werden die beiden Kriterien mit **UND** verknüpft, andernfalls mit **ODER**. |
| operatorType2     | string  | query                 | Zweiter Vergleichsoperator (optional).                                      |
| criteria2         | string  | query                 | Zweiter Filterwert oder Ausdruck (optional).                                |
| matchBlanks       | boolean | query                 | Wenn `true`, werden leere Zellen in die Filterergebnisse einbezogen.       |
| refresh           | boolean | query                 | Wenn `true`, wird das Arbeitsblatt nach dem Anwenden des Filters aktualisiert. |
| folder            | string  | query                 | Ordnerpfad im Speicher, in dem sich die Datei befindet.                     |
| storageName       | string  | query                 | Name des Speicherdiensts.                                                    |

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
| 200  | OK                          | Filter wurde erfolgreich angewendet; die Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).     |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                        |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet die Größenbeschränkung.               |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                                   |

## Verwendung der PutWorksheetCustomFilter API mit SDKs

### PutWorksheetCustomFilter API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetCustomFilter) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das **cURL**-Befehlszeilentool verwenden, um Aspose.Cells-Webservices einfach aufzurufen. Das folgende Beispiel zeigt, wie ein Aufruf der Cloud-API mit cURL durchgeführt wird.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/custom?range=A1:B1&fieldIndex=0&operatorType1=LessOrEqual&criteria1=1" \
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

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung. Ein SDK übernimmt Details auf niedriger Ebene, sodass Sie sich auf Ihre Projeklogik konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetCustomFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetCustomFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetCustomFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetCustomFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetCustomFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetCustomFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetCustomFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetCustomFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

Weitere AutoFilter-Vorgänge, wie das Hinzufügen eines Standardfilters oder eines Datumsfilters, finden Sie in den zugehörigen Dokumentationsseiten im Abschnitt AutoFilter.