---
title: "Arbeitsblatt in PDF, PNG, CSV und mehr konvertieren – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Arbeitsblatt konvertieren"
type: docs
url: /worksheets/conversion/
aliases:
  - /convert-worksheet-to-image/
  - /worksheets/to-image/
keywords: "Aspose.Cells, Arbeitsblatt-Konvertierung, REST-API, cURL, SDK, PDF, PNG, CSV"
description: "Erfahren Sie, wie Sie ein einzelnes Arbeitsblatt aus einer Excel-Arbeitsmappe in PDF, PNG, CSV und über 15 weitere Formate mit der Aspose.Cells Cloud REST-API konvertieren können. Enthält cURL-Beispiel, SDK-Snippets und eine vollständige Parameterreferenz."
weight: 130
ArticleTitle: "Arbeitsblatt in PDF, PNG, CSV und mehr konvertieren – Aspose.Cells Cloud API"
---

**Worksheet-Conversion-API** – Der Endpunkt `GET /cells/{name}/worksheets/{sheetName}` konvertiert ein einzelnes Arbeitsblatt (ein Blatt innerhalb einer Excel-Arbeitsmappe) in ein anderes Dateiformat.

> **Voraussetzung:** Sie müssen über ein gültiges JWT-Token verfügen und die Arbeitsmappe in einem unterstützten Aspose-Cloud-Speicherort gespeichert haben, bevor Sie diesen Endpunkt aufrufen.

Unterstützte **zu lesende** Formate (das Arbeitsblatt kann gelesen werden aus):

- XLS, XLSX, XLSB, CSV, TSV, XLSM, ODS, TXT

Unterstützte **nur zum Speichern**-Formate (das Arbeitsblatt kann gespeichert werden als):

- PDF, OTS, XPS, DIF, PNG, JPEG, BMP, SVG, TIFF, EMF, NUMBERS, FODS

## REST-API

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetWithFormat) beschreibt die öffentlich zugängliche Schnittstelle.

### **Anfrageparameter**

| Parameter                | Typ     | Erforderlich | Standardwert | Zulässige Werte                                                    | Beschreibung                                          |
| ------------------------ | ------- | ------------ | ------------ | ------------------------------------------------------------------ | ----------------------------------------------------- |
| **format**               | string  | Ja           | –            | pdf, png, jpeg, bmp, svg, tiff, emf, csv, txt, … (siehe Liste)    | Ziel-Ausgabeformat.                                   |
| **verticalResolution**   | integer | Nein         | 96           | 72‑600                                                             | Vertikale DPI für Bildausgabe.                        |
| **horizontalResolution** | integer | Nein         | 96           | 72‑600                                                             | Horizontale DPI für Bildausgabe.                      |
| **password**             | string  | Nein         | –            | –                                                                  | Passwort zum Öffnen einer geschützten Arbeitsmappe.   |
| **folder**               | string  | Nein         | –            | –                                                                  | Cloud-Ordner, in dem die Quell-Arbeitsmappe gespeichert ist. |
| **storage**              | string  | Nein         | –            | –                                                                  | Name des Speichers (z. B. „Default“).                 |

### Antwort

| Statuscode | Beschreibung                                                             | Rückgabetyp                |
| ---------- | ------------------------------------------------------------------------ | -------------------------- |
| **200**    | Konvertierung erfolgreich; Binärstream der konvertierten Datei wird zurückgegeben. | `application/octet-stream` |
| **400**    | Ungültige Anfrage – fehlende oder ungültige Parameter.                  | JSON-Fehlerobjekt          |
| **401**    | Nicht autorisiert – ungültiges oder fehlendes JWT-Token.                | JSON-Fehlerobjekt          |
| **404**    | Nicht gefunden – Arbeitsmappe oder Arbeitsblatt existiert nicht.        | JSON-Fehlerobjekt          |
| **500**    | Interner Serverfehler – unerwarteter Fehler.                             | JSON-Fehlerobjekt          |

#### Beispielanfrage (cURL)

```bash
curl -v "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1?format=png&verticalResolution=96&horizontalResolution=96" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

#### Beispielantwort

```
Konvertiertes Bild (Binärstream)
```

## Cloud SDK-Familie

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf Ihr Projekt konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mit verschiedenen SDKs aufgerufen werden:

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