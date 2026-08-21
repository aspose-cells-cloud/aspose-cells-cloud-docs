---
title: "Exportieren eines Arbeitsblatts mit der Aspose.Cells Cloud API – Formate, cURL- und SDK-Beispiele"
second_title: "Dokument"
linktitle: "Arbeitsblatt-Export"
type: docs
url: /worksheets/get-worksheet/
keywords: "Aspose.Cells Cloud Get Worksheet, Arbeitsblatt exportieren, Excel-API, REST, CSV, PDF, PNG, JPEG, GIF, BMP, TIFF, EMF, XPS, OTS, XLS, XLSX, XLSB, XLSM, ODS, FODS, Numbers, Cloud-API"
description: "Erfahren Sie, wie Sie ein einzelnes Arbeitsblatt aus einer Excel-Datei mithilfe der Aspose.Cells Cloud REST-API exportieren. Enthält Endpunkt, Parameter, ein korrigiertes cURL-Beispiel, Authentifizierungsdetails, Fehlerbehandlung und SDK-Snippets für C#, Java, Python und mehr."
weight: 10
ArticleTitle: "Exportieren eines Arbeitsblatts mit der Aspose.Cells Cloud API – Formate, cURL- und SDK-Beispiele"
---

Diese REST-API ermöglicht es Ihnen, ein **Arbeitsblatt** aus einer Excel-Datei in viele verschiedene Dateiformate zu exportieren.

**Zusammenfassung** – Verwenden Sie den **Get Worksheet**-Endpunkt, um ein einzelnes Arbeitsblatt aus einer Arbeitsmappe im gewünschten Format herunterzuladen.

Sie können in die folgenden Formate exportieren:

| Format  | Erweiterung | MIME-Type                                                           |
| ------- | ----------- | ------------------------------------------------------------------- |
| XLS     | .xls        | application/vnd.ms-excel                                            |
| XLSX    | .xlsx       | application/vnd.openxmlformats-officedocument.spreadsheetml.sheet   |
| XLSB    | .xlsb       | application/vnd.ms-excel.sheet.binary.macroEnabled.12               |
| CSV     | .csv        | text/csv                                                            |
| TSV     | .tsv        | text/tab-separated-values                                           |
| XLSM    | .xlsm       | application/vnd.ms-excel.sheet.macroEnabled.12                      |
| ODS     | .ods        | application/vnd.oasis.opendocument.spreadsheet                      |
| TXT     | .txt        | text/plain                                                          |
| PDF     | .pdf        | application/pdf                                                     |
| OTS     | .ots        | application/vnd.oasis.opendocument.spreadsheet-template             |
| XPS     | .xps        | application/vnd.ms-xpsdocument                                      |
| DIF     | .dif        | application/x-dif                                                   |
| PNG     | .png        | image/png                                                           |
| JPEG    | .jpeg       | image/jpeg                                                          |
| GIF     | .gif        | image/gif                                                           |
| BMP     | .bmp        | image/bmp                                                           |
| WMF     | .wmf        | image/wmf                                                           |
| TIFF    | .tiff       | image/tiff                                                          |
| EMF     | .emf        | image/emf                                                           |
| NUMBERS | .numbers    | application/vnd.apple.numbers                                       |
| FODS    | .fods       | application/vnd.oasis.opendocument.spreadsheet-flat-xml             |

## Sicherheit und Authentifizierung
Die Aspose.Cells Cloud APIs sind sicher und erfordern eine [JWT-Token-basierte Authentifizierung](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/).

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **Anforderungsparameter**

| Parametername            | Typ     | Ort   | Beschreibung                                                                 |
| ------------------------ | ------- | ----- | ---------------------------------------------------------------------------- |
| **name**                 | string  | path  | **Erforderlich.** Name der Excel-Datei.                                     |
| **sheetName**            | string  | path  | **Erforderlich.** Name des zu exportierenden Arbeitsblatts.                 |
| **format**               | string  | query | Ziel-Dateiformat für das exportierte Arbeitsblatt (z. B. `pdf`, `png`).      |
| **verticalResolution**   | integer | query | Bild-DPI für Formate mit unterstützter Auflösung (z. B. PNG, JPEG).          |
| **horizontalResolution** | integer | query | Bild-DPI für Formate mit unterstützter Auflösung.                            |
| **area**                 | string  | query | Zellbereich zum Exportieren (z. B. `A1:D10`).                                |
| **pageIndex**            | integer | query | Seitenindex zum Exportieren, wenn das Arbeitsblatt seitenbasiert ist.        |
| **folder**               | string  | query | Ordnerpfad im Speicher, in dem sich die Quelldatei befindet.                 |
| **storageName**          | string  | query | Name des Aspose Cloud-Speichers.                                             |

Die <a href="https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet" target="_blank" rel="noopener noreferrer">OpenAPI-Spezifikation</a> definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das cURL-Befehlszeilentool verwenden, um problemlos auf die Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie die Cloud-API mit cURL aufgerufen wird.

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1?format=gif" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```http
HTTP/1.1 200 OK
Content-Type: image/gif
Content-Disposition: attachment; filename="Sheet1.gif"

<binäre Daten>
```

{{< /tab >}}

{{< /tabs >}}

## Fehlerbehandlung

Die API gibt standardmäßige HTTP-Statuscodes zurück. Gängige Antworten sind:

| Statuscode | Bedeutung                                                       | Beispiel-JSON-Body                         |
| ---------- | --------------------------------------------------------------- | ------------------------------------------ |
| **200**    | Erfolg – der Arbeitsblattstream wird zurückgegeben.             | `{ "stream": "..." }`                      |
| **400**    | Ungültige Anforderung – fehlende oder ungültige Parameter.     | `{ "error": "Ungültiger Formatparameter." }` |
| **401**    | Nicht autorisiert – ungültiges oder fehlendes JWT-Token.       | `{ "error": "Authentifizierung fehlgeschlagen." }` |
| **404**    | Nicht gefunden – die angegebene Datei oder das angegebene Arbeitsblatt existiert nicht. | `{ "error": "Arbeitsblatt nicht gefunden." }` |
| **500**    | Interner Serverfehler – unerwarteter Zustand auf dem Server.   | `{ "error": "Unerwarteter Fehler." }`      |

Behandeln Sie diese Antworten in Ihrem Clientcode, um dem Benutzer eine geeignete Rückmeldung zu geben.

## Cloud SDK-Familie

Die Verwendung eines SDKs ist die beste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details und lässt Sie sich auf Ihre Projekt Aufgaben konzentrieren. Bitte besuchen Sie das <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-Repository</a> für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Aufrufe an die Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}