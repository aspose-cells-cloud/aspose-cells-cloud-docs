---
title: "Seitenanzahl aus einer Excel-Datei abrufen"
second_title: "Dokument"
linktitle: "Seiten"
type: docs
url: /de/get-page-count-from-an-excel-file/
aliases: [  /de/workbook/page-count/ , /de/workbook/get/page-count/ ]
keywords: "Aspose.Cells, Cloud API, Excel-Seitenanzahl, Workbook-Pagination"
description: "Abrufen der Gesamtanzahl der druckbaren Seiten in einer Excel-Arbeitsmappe über die Aspose.Cells Cloud REST API (v3.0). Enthält Anforderungsformat, erforderliche Parameter, cURL-Beispiel, Antwortschema, Fehlerbehandlung und SDK-Snippets für mehrere Sprachen."
weight: 10
version: "v3.0"
ArticleTitle: "Seitenanzahl aus einer Excel-Datei mit der Aspose.Cells Cloud API abrufen"
---

Diese REST API gibt die **Seitenanzahl** einer Arbeitsmappe zurück.

## Sicherheit und Authentifizierung
Die Aspose.Cells Cloud APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/pagecount
```

### Die Anforderungsparameter

| Parametername   | Typ    | Ort    | Erforderlich | Beschreibung                                |
| --------------- | ------ | ------ | ------------ | ------------------------------------------- |
| name            | string | path   | Ja           | Der Name der Excel-Datei.                   |
| folder          | string | query  | Nein         | Der Ordner, der das Dokument enthält.       |
| storageName     | string | query  | Nein         | Der Name des zu verwendenden Speichers.     |

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Workbook/GetPageCount) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf die Aspose.Cells REST API zuzugreifen. Das folgende Beispiel zeigt, wie der Endpunkt mit cURL aufgerufen wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/IhreDatei.xlsx/pagecount" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

*Ersetzen Sie `IhreDatei.xlsx` durch den tatsächlichen Namen der Arbeitsmappe, die Sie abfragen möchten.*

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
13
```

{{< /tab >}}

{{< /tabs >}}

### Antwortschema

| HTTP-Status | Datentyp | Beschreibung                                                |
| ----------- | -------- | ----------------------------------------------------------- |
| 200         | integer  | Die Gesamtanzahl der druckbaren Seiten in der Arbeitsmappe (z. B. `13`). |
| 4xx‑5xx     | JSON     | Fehlerobjekt (siehe Abschnitt _Fehlerbehandlung_).          |

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die beste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK kümmert sich um die Low-Level-Details und lässt Sie sich auf Ihre Projektaufgaben konzentrieren. Besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webservices mithilfe verschiedener SDKs durchgeführt werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetPageCount.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetPageCount.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetPageCount.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetPageCount.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82deb2e4189bc27ae92abf73c36b4df0" "Example_GetPageCount.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetPageCount.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetPageCount.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetPageCount.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Fehlerbehandlung

| HTTP-Status | Beschreibung                              | Beispiel-JSON-Body                                                                           |
| ----------- | ----------------------------------------- | -------------------------------------------------------------------------------------------- |
| 401         | Ungültiges oder fehlendes JWT-Token.      | `{ "Code": "InvalidAuthenticationToken", "Message": "Zugriffstoken fehlt oder ist ungültig." }` |
| 404         | Die angegebene Arbeitsmappe konnte nicht gefunden werden. | `{ "Code": "FileNotFound", "Message": "Die angeforderte Datei existiert nicht." }` |
| 400         | Ungültige Anforderung – erforderliche Parameter fehlen. | `{ "Code": "BadRequest", "Message": "Erforderlicher Parameter 'name' fehlt." }` |
| 500         | Interner Serverfehler.                    | `{ "Code": "InternalError", "Message": "Ein unerwarteter Fehler ist aufgetreten." }` |