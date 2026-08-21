---
title: "Ermitteln der Seitenanzahl für ein Excel-Arbeitsblatt"
second_title: "Dokument"
linktitle: "Seitenanzahl"
type: docs
url: /worksheets/page-count/
keywords: "Aspose.Cells, Excel-API, Seitenanzahl des Arbeitsblatts, REST, Cloud-SDK, Excel-Seitenumbrüche"
description: "Abrufen der Anzahl der druckbaren Seiten in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API (v3.0). Enthält HTTPS-Anforderungsformat, Authentifizierungsschritte, Beispiel-cURL, vollständige JSON-Antwort, HTTP-Statuscodes und SDK-Codebeispiele."
weight: 10
ArticleTitle: "Ermitteln der Seitenanzahl für ein Excel-Arbeitsblatt – Aspose.Cells Cloud API"
---

Diese REST API gibt die **Seitenanzahl** für ein Arbeitsblatt zurück.

**Authentifizierung:** Alle Aspose.Cells Cloud-Endpunkte erfordern ein Bearer-Token, das über den OAuth2-Fluss abgerufen wird. Geben Sie das Token im `Authorization`-Header an, wie im folgenden cURL-Beispiel gezeigt.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pagecount
```

### Anforderungsparameter

| Parameter   | Typ    | Ort      | Beschreibung                            |
| ----------- | ------ | -------- | --------------------------------------- |
| name        | string | path     | Name des Dokuments.                     |
| sheetName   | string | path     | Name des Arbeitsblatts.                 |
| folder      | string | query    | Ordner, der das Dokument enthält.       |
| storageName | string | query    | Name des Speichers.                     |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Worksheets/GetPageCount) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das Kommandozeilentool **cURL** verwenden, um problemlos auf Aspose.Cells-Webservices zuzugreifen. Das folgende Beispiel zeigt, wie die API mit cURL aufgerufen wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/worksheets/Sheet1/pagecount" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <access_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "PageCount": 3
}
```

{{< /tab >}}

{{< /tabs >}}

### Antwortdetails

| HTTP-Status | Bedeutung                                           |
| ----------- | --------------------------------------------------- |
| **200**     | Erfolg – gibt die oben gezeigte JSON-Nutzdatenstruktur zurück. |
| **401**     | Nicht autorisiert – fehlendes oder ungültiges Token. |
| **404**     | Nicht gefunden – die Datei oder das Arbeitsblatt ist nicht vorhanden. |
| **500**     | Interner Serverfehler – unerwarteter Serverzustand. |

### Versionshistorie

_API-Version **v3.0** (veröffentlicht 2025). Falls Sie eine neuere Version verwenden, beachten Sie die aktualisierte Endpunkt-Dokumentation._

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung. Ein SDK abstractisiert Low-Level-Details, sodass Sie sich auf Ihre Geschäftslogik konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetPageCount.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetPageCount.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetPageCount.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetPageCount.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetPageCount.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetPageCount.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetPageCount.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetPageCount.go" >}}

{{< /tab >}}

{{< /tabs >}}

### Hinweise

- Die Seitenanzahl spiegelt das druckbare Layout wider und berücksichtigt Seitenumbrüche, Ränder sowie Skalierung. Ausgeblendete Zeilen oder Spalten können das Ergebnis beeinflussen.
- Stellen Sie sicher, dass das Zielarbeitsblatt vorhanden ist und die Datei im angegebenen `folder` und `storageName` gespeichert ist, bevor Sie die Anforderung senden.