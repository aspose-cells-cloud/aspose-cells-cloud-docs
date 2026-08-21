---
title: "Erweiterte Excel-Dateikonvertierung"
second_title: "Dokument"
linktype: "Erweiterte Konvertierung"
type: docs
url: /advanced-convert-excel/
keywords: "Aspose.Cells, Excel-Konvertierung, Cloud-API, SDK"
description: "Die Aspose.Cells Cloud REST-API bietet leistungsstarke Funktionen zur Konvertierung von Excel-Arbeitsmappen in eine Vielzahl von Formaten sowie zur Konfiguration von Seitenformatierung, Speicheroptionen und Druckeinstellungen. SDKs sind für Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby und Swift verfügbar, was eine nahtlose Integration über verschiedene Plattformen hinweg ermöglicht."
weight: 50
ArticleTitle: "Erweiterte Excel-Dateikonvertierung – Aspose.Cells Cloud API-Anleitung"
---

## Erweiterte Cloud-API für Excel-Konvertierung

Die erweiterte Konvertierungsfunktion ermöglicht es Ihnen, eine Excel-Arbeitsmappe in verschiedene Ausgabeformate (PDF, HTML, CSV usw.) zu konvertieren und dabei eine detaillierte Kontrolle über die Seitenformatierung, Speicheroptionen und Druckeinstellungen auszuüben.

**Voraussetzungen / Authentifizierung**  
Um diesen Endpunkt nutzen zu können, müssen Sie einen Zugriffstoken von Aspose.Cells Cloud erhalten und diesen im `Authorization`-Header als Bearer-Token übermitteln.

**API-Referenz**  
- **Methode:** `PUT`  
- **Endpunkt:** `/cells/convert`  
- **Parameter:**  
  - `format` (Zeichenfolge, erforderlich) – Gewünschtes Ausgabeformat (z. B. `pdf`, `html`).  
  - `outPath` (Zeichenfolge, optional) – Pfad im Cloud-Speicher, unter dem die konvertierte Datei gespeichert wird.  
  - `options` (Objekt, optional) – JSON-Objekt mit erweiterten Konvertierungsoptionen wie `pageSetup`, `saveOptions` und `printSettings`.  
- **Beispiel für Anforderungstext:**  
  ```json
  {
    "format": "pdf",
    "outPath": "output/converted.pdf",
    "options": {
      "pageSetup": {
        "orientation": "Landscape",
        "paperSize": "A4"
      },
      "saveOptions": {
        "compress": true
      },
      "printSettings": {
        "printHeadings": false
      }
    }
  }
  ```  
- **Antwort:**  
  - `200 OK` – Konvertierung erfolgreich; Antwort enthält den konvertierten Dateistream oder einen Verweis auf die gespeicherte Datei.  
  - `400 Bad Request` – Ungültige Parameter oder fehlerhafter Anforderungstext.  
  - `401 Unauthorized` – Authentifizierung fehlgeschlagen oder Token fehlt.  
  - `500 Internal Server Error` – Serverseitiger Fehler während der Konvertierung.  

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                     |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK                          | Konvertierung erfolgreich; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiger oder fehlender JWT-Token. |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet die maximale Dateigröße. |
| 500  | Internal Server Error       | Unerwarteter Serverfehler. |

**Hinweise**  
* Einige Ausgabeformate weisen spezifische Einschränkungen auf (z. B. werden bei der HTML-Konvertierung Makros nicht beibehalten). Weitere Informationen finden Sie in der formatabhängigen Dokumentation.

### Die Fähigkeit, Tabellendateien aus verschiedenen Datenquellen zu laden

### Festlegen der Seitenformatierung und Speicheroptionen

## Cloud SDK-Familie

Die Verwendung eines SDK beschleunigt die Entwicklung, da darin niedrigere Details abstrahiert werden, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Besuchen Sie das <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub-Repository</a>, um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mithilfe verschiedener SDKs durchgeführt werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbook.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbook.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbook.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbook.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbook.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbook.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbook.go" >}}

{{< /tab >}}

{{< /tabs >}}

<script type="application/ld+json">
{
  "@context":"https://schema.org",
  "@type":"WebAPI",
  "name":"Aspose.Cells Cloud Erweiterte Konvertierung",
  "description":"Konvertieren Sie eine Excel-Arbeitsmappe in PDF/HTML/CSV mit erweiterten Optionen.",
  "url":"https://api.aspose.cloud/v3.0/cells/convert",
  "documentation":"https://docs.aspose.cloud/cells/advanced-convert-excel/",
  "endpointDescription":"PUT /cells/convert",
  "input":{
    "@type":"PropertyValueSpecification",
    "valueRequired":true,
    "valueName":"format",
    "description":"Gewünschtes Ausgabeformat (pdf, html, csv, …)"
  },
  "target":{
    "@type":"EntryPoint",
    "urlTemplate":"https://api.aspose.cloud/v3.0/cells/convert?format={format}",
    "httpMethod":"PUT"
  }
}
</script>