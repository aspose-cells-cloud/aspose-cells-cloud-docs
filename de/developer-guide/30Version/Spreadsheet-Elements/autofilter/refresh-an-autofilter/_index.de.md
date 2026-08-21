---
title: "Ein automatischer Filter in einer Excel-Arbeitsmappe aktualisieren"
second_title: "Dokument"
linktitle: "Automatischen Filter aktualisieren"
type: docs
url: /autofilter/refresh/
aliases: [/refresh-an-autofilter/]
weight: 100
keywords: "Aspose.Cells, AutoFilter, aktualisieren, Excel, API, REST"
description: "Aktualisieren eines vorhandenen automatischen Filters in einer Excel-Arbeitsmappe mithilfe der Aspose.Cells Cloud REST API. Enthält cURL- und SDK-Beispiele für C#, Java, Python und weitere."
ArticleTitle: "Ein automatischer Filter in einer Excel-Arbeitsmappe aktualisieren"
---

### Was bewirkt **Aktualisieren**?

Das Aufrufen des Endpunkts wendet die aktuellen Filterkriterien erneut an, nachdem sich die Daten im Arbeitsblatt geändert haben (z. B. Zeilen wurden hinzugefügt oder entfernt). Der Vorgang ändert die Filterdefinition nicht; er aktualisiert lediglich die Anzeige und gibt eine Statusantwort zurück.

### REST-API

Diese REST-API aktualisiert einen automatischen Filter in einer Excel-Arbeitsmappe (API-Version **v3.0**).

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/refresh
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Antwort**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                     |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Ungültige Anforderung       | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Nicht autorisiert           | Ungültiges oder fehlendes JWT-Token. |
| 413  | Anforderung zu groß         | Die hochgeladene Datei überschreitet das maximale Größe limit. |
| 500  | Interner Serverfehler       | Unerwarteter Serverfehler. |

*Beispiele für Fehlerantworten*  

```json
// 400 Ungültige Anforderung
{
    "Code": 400,
    "Message": "Ungültiger Parameter: sheetName wurde nicht gefunden."
}

// 401 Nicht autorisiert
{
    "Code": 401,
    "Message": "Authentifizierung fehlgeschlagen. JWT-Token fehlt oder ist ungültig."
}

// 413 Anforderung zu groß
{
    "Code": 413,
    "Message": "Die hochgeladene Datei überschreitet die maximal zulässige Größe."
}

// 500 Interner Serverfehler
{
    "Code": 500,
    "Message": "Auf dem Server ist ein unerwarteter Fehler aufgetreten."
}
```

## Verwenden der PostWorksheetAutoFilterRefresh-API mit SDKs

### Spezifikation der PostWorksheetAutoFilterRefresh-API

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/AutoFilter/PostWorksheetAutoFilterRefresh) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um Aspose.Cells-Webdienste problemlos aufzurufen. Das folgende Beispiel zeigt, wie mit cURL Aufrufe an die Cloud-API durchgeführt werden.

{{< tabs tabTotal="2" tabID="11" tabName11="Anforderung" tabName12="Antwort" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/refresh" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your-jwt-token>"
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

### Verwenden der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist die beste Möglichkeit, die Entwicklungszeit zu verkürzen. Ein SDK übernimmt die Details auf unterster Ebene und ermöglicht es Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetAutoFilterRefresh.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetAutoFilterRefresh.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetAutoFilterRefresh.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetAutoFilterRefresh.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetAutoFilterRefresh.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetAutoFilterRefresh.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetAutoFilterRefresh.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetAutoFilterRefresh.go" >}}

{{< /tab >}}

{{< /tabs >}}