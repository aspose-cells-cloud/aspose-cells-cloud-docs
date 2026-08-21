---
title: "Hinzufügen eines Farbfilters in einer Excel-Arbeitsmappe"
second_title: "Dokument"
linktitle: "Farbfilter hinzufügen"
type: docs
url: /de/autofilter/add-color-filter/
aliases: [  /de/filter-a-list-using-a-color-filter/ , /de/autofilter/add-a-color-filter/ ]
keywords: "Excel, Farbfilter, Aspose.Cells Cloud, REST-API, AutoFilter, JWT-Authentifizierung"
description: "Erfahren Sie, wie Sie mithilfe der Aspose.Cells Cloud-API einen Farbfilter in einer Excel-Arbeitsmappe anwenden. Enthält Endpunkt, Parameter, cURL-Beispiel, Fehlerbehandlung und SDK-Beispiele."
weight: 65
ArticleTitle: "Hinzufügen eines Farbfilters in einer Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud-API"
---

Erfahren Sie, wie Sie mithilfe der Aspose.Cells Cloud-API einen Farbfilter in einer Excel-Arbeitsmappe hinzufügen. Diese Anleitung behandelt den erforderlichen Endpunkt, Parameter, Authentifizierungsvoraussetzungen, ein cURL-Beispielanforderung, SDK-Beispiele und die Antwortverarbeitung.

Diese REST-API fügt einen **Farbfilter** zu einer Excel-Arbeitsmappe hinzu.

## PutWorksheetColorFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/colorFilter
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter:

| Parametername   | Typ     | Speicherort | Beschreibung                                                                 |
|-----------------|---------|-------------|------------------------------------------------------------------------------|
| name            | string  | path        | Der Name der Excel-Datei.                                                    |
| sheetName       | string  | path        | Der Name des Arbeitsblatts, das die zu filternden Daten enthält.             |
| range           | string  | query       | Der Zellbereich, auf den der Filter angewendet wird (z. B. `A1:B10`).        |
| fieldIndex      | integer | query       | Nullbasierter Index der Spalte, für die der Farbfilter angewendet wird.      |
| colorFilter     | object  | body        | JSON-Objekt, das die zu filternden Vorder- und Hintergrundfarben definiert. |
| matchBlanks     | boolean | query       | Gibt an, ob Zeilen mit leeren Zellen in die Filterergebnisse einbezogen werden sollen. |
| refresh         | boolean | query       | Wenn `true`, wird das Arbeitsblatt nach dem Anwenden des Filters neu geladen. |
| folder          | string  | query       | Der Ordner im Speicher, in dem sich die Excel-Datei befindet.                |
| storageName     | string  | query       | Der Name des Speicherdienstes (z. B. Aspose Cloud Storage).                  |

**JSON-Schema für `colorFilter`**

| Eigenschaft         | Typ    | Beschreibung                                                                    | Erforderlich |
|---------------------|--------|----------------------------------------------------------------------------------|--------------|
| Pattern             | string | Filtermuster (z. B. `"Solid"`).                                                 | Ja           |
| ForegroundColor     | object | Definiert die Vordergrundfarbe. Enthält Untereigenschaften wie `Color`, `ColorIndex`, `IsShapeColor`, `ThemeColor` und `Type`. | Nein |
| BackgroundColor     | object | Definiert die Hintergrundfarbe. Gleiches Untereigenschaften-Set wie `ForegroundColor`. | Nein |

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
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails.             |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).     |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                        |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.                       |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                                  |

## Verwenden der PutWorksheetColorFilter API mit SDKs

### PutWorksheetColorFilter API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetColorFilter) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste problemlos aufzurufen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud-API durchführen.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/colorFilter?range=A1%3AB1&fieldIndex=0" \
-X PUT \
-d "{ \"Pattern\": \"Solid\", \"ForegroundColor\": { \"Color\": { \"A\": 255, \"R\": 0, \"G\": 255, \"B\": 255 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"Text2\", \"Tint\": 1 }, \"Type\": \"Automatic\" }, \"BackgroundColor\": { \"Color\": { \"A\": 255, \"R\": 0, \"G\": 255, \"B\": 255 }, \"ColorIndex\": 0, \"IsShapeColor\": true, \"ThemeColor\": { \"ColorType\": \"Text2\", \"Tint\": 0 }, \"Type\": \"Automatic\" }}" \
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

### Verwenden von Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, die Entwicklungsgeschwindigkeit zu erhöhen. Ein SDK abstrahiert die Low-Level-Details, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetColorFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetColorFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetColorFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetColorFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetColorFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetColorFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetColorFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetColorFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Siehe auch:** [Hinzufügen eines benutzerdefinierten Filters](https://docs.aspose.cloud/cells/autofilter/add-custom-filter/), [Hinzufügen eines Datumsfilters](https://docs.aspose.cloud/cells/autofilter/add-date-filter/), [Entfernen eines AutoFilters](https://docs.aspose.cloud/cells/autofilter/remove-auto-filter/).
---