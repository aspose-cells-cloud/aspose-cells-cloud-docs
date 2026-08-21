---
title: "Datumsfilter löschen – Aspose.Cells Cloud"
second_title: "Dokument"
linktitle: "Datumsfilter löschen"
type: docs
url: /autofilter/delete-date-filter/
aliases:
  - /remove-a-date-filter/
  - /autofilter/delete-a-date-filter/
weight: 100
keywords: "Aspose.Cells, Datumsfilter löschen, Excel-Autofilter, REST-API, SDK"
description: "Erfahren Sie, wie Sie einen Datumsfilter in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST-API löschen. Enthält Endpunkt, Parameter, HTTPS-cURL-Beispiel, Antwortpayload und SDK-Codebeispiele."
ArticleTitle: "Datumsfilter löschen – Aspose.Cells Cloud API-Dokumentation"
---

Diese REST-API löscht einen Datumsfilter in einem Excel-Arbeitsblatt.

**Voraussetzungen:** Stellen Sie sicher, dass Sie ein gültiges JWT-Token besitzen, die Arbeitsmappe im Aspose Cloud-Speicher gespeichert ist und Sie über die erforderlichen Berechtigungen zum Ändern des Arbeitsblatts verfügen.

## DeleteWorksheetDateFilter API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/dateFilter
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername          | Typ     | Ort    | Beschreibung                                                                              |
|------------------------|---------|--------|-------------------------------------------------------------------------------------------|
| name                   | string  | path   | Name der Excel-Datei.                                                                     |
| sheetName              | string  | path   | Name des Arbeitsblatts.                                                                   |
| fieldIndex             | integer | query  | Nullbasierter Index der Spalte, auf die der Filter angewendet wird.                      |
| dateTimeGroupingType   | string  | query  | Gruppierungstyp für den Datumsfilter (z. B. Year, Month, Day).                           |
| year                   | integer | query  | Jahrkomponente des Filters (Standardwert 0).                                              |
| month                  | integer | query  | Monatskomponente des Filters (Standardwert 0).                                            |
| day                    | integer | query  | Tageskomponente des Filters (Standardwert 0).                                             |
| hour                   | integer | query  | Stundenkomponente des Filters (Standardwert 0).                                           |
| minute                 | integer | query  | Minutenkomponente des Filters (Standardwert 0).                                           |
| second                 | integer | query  | Sekundenkomponente des Filters (Standardwert 0).                                          |
| folder                 | string  | query  | Ordnerpfad im Speicher, in dem sich die Datei befindet.                                   |
| storageName            | string  | query  | Name des Aspose Cloud-Speichers.                                                          |

### **Antwort**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                                      |
|------|-----------------------------|-----------------------------------------------------------------------------------|
| 200  | OK                          | Filter wurde erfolgreich angewendet; die Antwort enthält Details zum Vorgang.   |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).          |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                             |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.                            |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                                        |

Die API gibt Standard-HTTP-Statuscodes zurück, die das Ergebnis des Löschvorgangs angeben.

| Code | Bedeutung             | Beschreibung                                                                      |
|------|-----------------------|-----------------------------------------------------------------------------------|
| 200  | OK                    | Der Datumsfilter wurde erfolgreich gelöscht; die Antwort enthält den Status.    |
| 400  | Bad Request           | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).           |
| 401  | Unauthorized          | Ungültiges oder fehlendes JWT-Token.                                             |
| 413  | Payload Too Large     | Die hochgeladene Datei überschreitet das Größenlimit.                            |
| 500  | Internal Server Error | Unerwarteter Serverfehler.                                                        |

## Verwendung der DeleteWorksheetDateFilter API mit SDKs

### DeleteWorksheetDateFilter API-Spezifikation

Die <a href="https://apireference.aspose.cloud/cells/#/AutoFilter/DeleteWorksheetDateFilter" rel="noopener noreferrer">OpenAPI-Spezifikation</a> definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool nutzen, um Aspose.Cells-Webdienste einfach aufzurufen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/dateFilter?fieldIndex=0&dateTimeGroupingType=Year&year=1920" \
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

### Verwendung von Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist die beste Möglichkeit, die Entwicklungsgeschwindigkeit zu erhöhen. Ein SDK übernimmt die Details auf niedriger Ebene, sodass Sie sich auf Ihre Projektanforderungen konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a>.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mithilfe verschiedener SDKs durchgeführt werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetDateFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetDateFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetDateFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetDateFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetDateFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetDateFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetDateFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetDateFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}