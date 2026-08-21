---
title: "Formen exportieren"
second_title: "Dokument"
linktitle: "Form"
type: docs
url: /export-excel-shape-to-different-formats/
aliases: [/export/excel-shape-to-different-formats/]
keywords: "Formen exportieren, Aspose.Cells Cloud, Excel-Form-Export, Bildformate, REST-API, SDK"
description: "Erfahren Sie, wie Sie Excel-Formen in verschiedene Bildformate (PNG, GIF, JPEG, BMP, SVG, TIFF, EMF, WMF) mit der Aspose.Cells Cloud REST-API und SDKs exportieren können."
weight: 20
ArticleTitle: "Formen exportieren – Aspose.Cells Cloud"
---

Das Exportieren von Formen aus Excel ermöglicht die Wiederverwendung diagrammatischer Inhalte über Plattformen und Anwendungen hinweg. **Voraussetzungen:** Ein gültiges JWT-Access-Token und die zu uploadende Quell-Excel-Datei.

Sie können Formen in die folgenden Formate exportieren: **PNG**, **GIF**, **JPEG**, **BMP**, **SVG**, **TIFF**, **EMF**, **WMF**.

## PostExport API

```http
PUT https://api.aspose.cloud/v3.0/cells/export
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.


### Anforderungsparameter

| Parametername | Typ   | Pfad/Abfragezeichenfolge/HTTP-Body | Erforderlich | Beschreibung |
|---------------|-------|------------------------------------|--------------|-------------|
| file          | Datei | formData                           | Ja           | Zu uploadende Datei |
| objectType    | string | query                             | Ja           | Der Typ des zu exportierenden Objekts. Für den Chart-Export verwenden Sie `chart`. Gültige Werte sind u. a. `shape`, `worksheet`, `picture` usw. |
| format        | string | query                             | Ja           | Gewünschtes Ausgabeformat. Unterstützte Werte: `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf`. |

### **Anforderungsbeispiel**

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/export?objectType=shape&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Antwort

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet1_Shapes_0.tif",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    }
    // ... weitere Dateiobjekte ...
  ]
}
```

*Typische, Base64-kodierte Dateinutzlasten liegen im Bereich von einigen Hundert Bytes bis zu mehreren Megabytes, abhängig von Bildabmessungen und Format.*

**HTTP-Statuscodes**

| Code | Bedeutung             | Beschreibung |
|------|-----------------------|-------------|
| 200  | OK                    | Formen erfolgreich exportiert; Antwort enthält die Dateiliste. |
| 400  | Ungültige Anforderung | Fehlende oder ungültige Parameter. |
| 401  | Nicht autorisiert     | Ungültiges oder fehlendes Access-Token. |
| 413  | Nutzlast zu groß      | Die hochgeladene Datei überschreitet das Größenlimit. |
| 500  | Interner Serverfehler | Unerwarteter Serverfehler. |


## Verwendung der PostExport API mit SDKs

### PostExport API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das Befehlszeilentool **cURL** verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie die Cloud-API mit cURL aufgerufen wird.

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/export?objectType=shape&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "Authorization: Bearer <your_access_token>" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung für Aspose.Cells Cloud. Ein SDK abstrahiert die niederleveligen Details, sodass Sie sich auf die Geschäftslogik konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportShape.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportShape.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportShape.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportShape.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportShape.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportShape.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportShape.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportShape.go" >}}

{{< /tab >}}

{{< /tabs >}}
---