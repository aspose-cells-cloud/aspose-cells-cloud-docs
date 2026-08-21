---
title: "Aspose.Cells Cloud – Konvertieren Sie Excel-Arbeitsmappen in PDF, CSV, HTML und weitere Formate (GET /cells/{name})"
second_title: "Dokumentation"
linktitle: "Excel konvertieren"
type: docs
url: /de/get-different-formats-files/
aliases:
  - /export-excel-workbook-to-different-file-formats/
  - /export-different-formats/
keywords: "Aspose.Cells, Excel-Konvertierung, Excel konvertieren, PDF, CSV, HTML, ODS, JSON, Bildformate, Tabellendokument exportieren, API, REST"
description: "Erfahren Sie, wie Sie eine Excel-Arbeitsmappe in einem beliebigen Format (PDF, CSV, HTML, PNG usw.) mithilfe der Aspose.Cells Cloud REST API abrufen. Enthält cURL-Beispiele, SDK-Beispiele, Authentifizierung und Antwortdetails."
weight: 10
ArticleTitle: "Aspose.Cells Cloud – Konvertieren Sie Excel-Arbeitsmappen in PDF, CSV, HTML und weitere Formate (GET /cells/{name})"
---

Diese REST-API ruft eine Excel-Arbeitsmappe in einem anderen Format ab.

## GetWorkBook API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Abfrageparameter**

| Parametername         | Typ    | Beschreibung                                                                                                                                                              | Standardwert |
| --------------------- | ------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ |
| format                | string | Ziel-Dateiformat (z. B. CSV, XLS, HTML, MHTML, ODS, PDF, XML, TXT, TIFF, XLSB, XLSM, XLSX, XLTM, XLTX, XPS, PNG, JPG, GIF, EMF, BMP, MD, Numbers, WMF, SVG usw.).            | –            |
| password              | string | Kennwort, das zum Öffnen der Excel-Datei erforderlich ist.                                                                                                               | –            |
| isAutoFit             | bool   | Passt die Breite von Zeilen und Spalten automatisch an.                                                                                                                  | false        |
| onlySaveTable         | bool   | Wenn **true**, wird nur Tabellendaten gespeichert. Akzeptiert `true` oder `false`.                                                                                       | false        |
| outPath               | string | Pfad zum Speichern des Ergebnisses. Bei einer einzelnen Datei inklusive Dateiname und -erweiterung; bei mehreren Dateien nur der Ordnerpfad.                               | –            |
| outStorageName        | string | Name des Speichers, in dem die Ausgabedatei gespeichert wird.                                                                                                            | –            |
| checkExcelRestriction | bool   | Prüft Excel-Einschränkungen beim Ändern von Zellen oder damit verbundenen Objekten.                                                                                      | false        |
| region                | string | Regionale Einstellungen, die auf die Arbeitsmappe angewendet werden.                                                                                                     | –            |
| pageWideFitOnPerSheet | bool   | Passt die Seitenbreite für jedes Arbeitsblatt beim Konvertieren in PDF an.                                                                                               | false        |
| pageTallFitOnPerSheet | bool   | Passt die Seitenhöhe für jedes Arbeitsblatt beim Konvertieren in PDF an.                                                                                                 | false        |
| onePagePerSheet       | bool   | Erstellt eine einzelne PDF-Seite pro Arbeitsblatt.                                                                                                                       | false        |
| folder                | string | Ordnerpfad der ursprünglichen Arbeitsmappe.                                                                                                                              | –            |
| storageName           | string | Name des Speichers, in dem sich die Quelldatei befindet.                                                                                                                 | –            |

### Antwort

**Erfolg (200)**

- Die API gibt ein **[Workbook](/cells/workbook/)**-Objekt zurück, das Strukturinformationen zur Arbeitsmappe enthält, wenn der Abfrageparameter `format` weggelassen wird.

- Die API gibt die konvertierte Datei im angeforderten Format zurück, wenn der Abfrageparameter `format` einen Dateityp angibt.

```http
HTTP/1.1 200 OK
Content-Type: application/pdf
Content-Disposition: attachment; filename="book1.pdf"
Content-Length: 123456

(binäre PDF-Daten)
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                                 |
|------|-----------------------------|------------------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang.         |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstütztes Dateiformat).  |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                                        |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet die Größeinschränkung.                 |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                                  |

> **Hinweise:**  
> - Große Arbeitsmappen können länger zum Konvertieren benötigen; erwägen Sie, das Timeout für die Anfrage zu erhöhen.  
> - Einige Formate (z. B. `ODS`) unterstützen bestimmte Excel-Funktionen wie Makros nicht.

## Verwenden der GetWorkBook API mit SDKs

> **Voraussetzungen:**  
> - Ein gültiges **JWT-Zugriffstoken**, das über den Aspose.Cells-Authentifizierungsfluss abgerufen wurde.  
> - Die Quell-Arbeitsmappe muss in einem unterstützten Aspose-Speicher abgelegt oder direkt in der Anfrage übermittelt werden.  
> - Stellen Sie sicher, dass die API-Version (`v3.0`) mit der neuesten veröffentlichten Version übereinstimmt.

### GetWorkBook API-Spezifikation

Die <a href="https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook" rel="noopener noreferrer">OpenAPI-Spezifikation</a> definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

### Beispielanfrage

Sie können das **cURL**-Befehlszeilentool verwenden, um auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt eine korrekte GET-Anfrage mit dem erforderlichen Autorisierungsheader.

{{< tabs tabTotal="1" tabID="11" tabName11="Anfrage" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=pdf" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger"
```

{{< /tab >}}

{{< /tabs >}}

### Verwenden der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist die schnellste Möglichkeit zur Entwicklung. Ein SDK abstractiert Low-Level-Details, sodass Sie sich auf Ihre Projekt-Aufgaben konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-Repository</a>.

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Siehe auch**

- <a href="https://apireference.aspose.cloud/cells/#/Workbook/ConvertWorkbook" rel="noopener noreferrer">Arbeitsmappe konvertieren (POST)</a>  
- <a href="https://apireference.aspose.cloud/cells/#/Workbook/SaveAs" rel="noopener noreferrer">Speichern als (GET)</a>

---

_Zuletzt aktualisiert: 2024-12-01_

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Aspose.Cells Cloud – Konvertieren Sie Excel-Arbeitsmappen in PDF, CSV, HTML und weitere Formate (GET /cells/{name})",
  "description": "Dokumentation für den Aspose.Cells Cloud GET /cells/{name}-Endpunkt, der Excel-Arbeitsmappen in verschiedene Formate wie PDF, CSV, HTML und mehr konvertiert.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2024-12-01",
  "keywords": "Aspose.Cells, Excel-Konvertierung, PDF, CSV, HTML, API, REST, Cloud",
  "url": "https://docs.aspose.cloud/cells/get-different-formats-files/",
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  }
}
</script>