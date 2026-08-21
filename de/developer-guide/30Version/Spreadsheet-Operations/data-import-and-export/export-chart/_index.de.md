---
title: "Excel-Diagramm exportieren"
second_title: "Dokument"
linktitle: "Diagramm"
type: docs
url: /export-excel-chart-to-different-formats/
aliases: [/export/excel-chart-to-different-formats/]
description: "Exportieren Sie Excel-Diagrammobjekte in gängige Formate wie PNG, JPEG, PDF, SVG, TIFF, EMF, WMF und weitere mithilfe der Aspose.Cells Cloud REST API oder SDKs. Enthält Authentifizierung, ein cURL-Beispiel und Codebeispiele für mehrere Sprachen."
keywords: "Aspose.Cells, Diagramm exportieren, Excel-Diagramm exportieren, REST API, cURL, PDF, PNG, JPEG, SVG, TIFF, EMF, WMF, SDK, Diagrammformate, Aspose Cells Cloud"
weight: 20
ArticleTitle: "Excel-Diagramm exportieren – Dokument"
---

Das Exportieren von Diagrammobjekten aus einer Excel-Arbeitsmappe in verschiedene Bild- und Dokumentformate ist eine häufige Anforderung für Berichte und Veröffentlichungen. Aspose.Cells Cloud bietet eine einfache REST-Schnittstelle, mit der Diagramme direkt in gängige Formate wie PNG, JPEG, PDF, SVG, TIFF, EMF, WMF und weitere konvertiert werden können.

Sie können Diagramme in die folgenden Formate exportieren: [PNG](https://docs.fileformat.com/Image/png/), [GIF](https://docs.fileformat.com/image/gif/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [WMF](https://docs.fileformat.com/image/Wmf/) und [PDF](https://docs.fileformat.com/pdf/).

**Voraussetzungen:**  
- Ein gültiges Aspose.Cells Cloud-Konto mit aktiver Subskription.  
- Ein OAuth 2.0 Bearer-Token (JWT), das über den Authentifizierungsfluss erworben wurde.  
- Die hochzuladende Arbeitsmappe (maximale Größe < 50 MB).  

## **REST API**

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### Anforderungsparameter

| Parametername | Typ   | Pfad/Abfragezeichenfolge/HTTP-Body | Erforderlich | Beschreibung                                                                                                                     |
|---------------|--------|------------------------------------|--------------|----------------------------------------------------------------------------------------------------------------------------------|
| file          | file   | formData                           | True         | Die hochzuladende Datei                                                                                                          |
| objectType    | string | query                              | True         | Der Typ des zu exportierenden Objekts. Für den Diagrammexport verwenden Sie `chart`. Weitere mögliche Werte sind `worksheet`, `picture` usw. |
| format        | string | query                              | True         | Gewünschtes Ausgabeformat. Unterstützte Werte: `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf`.                 |

### **Antwort**

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_0.tif",
      "FileSize": 10040,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_1.tif",
      "FileSize": 12978,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_2.tif",
      "FileSize": 7002,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet4_Charts_3.tif",
      "FileSize": 11532,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet6_Charts_0.tif",
      "FileSize": 8270,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3_Charts_0.tif",
      "FileSize": 42570,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3_Charts_1.tif",
      "FileSize": 12102,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet3_Charts_2.tif",
      "FileSize": 8290,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                 | Beschreibung                                                                 |
|------|---------------------------|------------------------------------------------------------------------------|
| 200  | OK                        | Filter erfolgreich angewendet; die Antwort enthält Details zum Vorgang.     |
| 400  | Bad Request               | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp).    |
| 401  | Unauthorized              | Ungültiges oder fehlendes JWT-Token.                                        |
| 413  | Payload Too Large         | Die hochgeladene Datei überschreitet das Größenlimit.                      |
| 500  | Internal Server Error     | Unerwarteter Serverfehler.                                                  |

## So verwenden Sie die PostExport-API mit SDKs

### PostExport-API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Alle Anfragen müssen ein gültiges OAuth 2.0 Bearer-Token im `Authorization`-Header enthalten. Das folgende Beispiel zeigt, wie die API mit **cURL** aufgerufen und eine Arbeitsmappe mithilfe von multipart/form‑data hochgeladen wird.

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=chart&format=tiff" \
  -H "Authorization: Bearer {access_token}" \
  -H "Accept: multipart/form-data" \
  -H "Content-Type: multipart/form-data" \
  -H "x-aspose-client: Containerize.Swagger" \
  -F "File=@/path/to/your/workbook.xlsx"
```

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details und ermöglicht es Ihnen, sich auf Ihre ProjektAufgaben zu konzentrieren. Bitte besuchen Sie das [GitHub-Repository](https://github.com/aspose-cells-cloud), um eine vollständige Liste der Aspose.Cells Cloud SDKs zu erhalten.

Die folgenden Codebeispiele zeigen, wie Aufrufe an die Aspose.Cells-Webdienste mithilfe verschiedener SDKs durchgeführt werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportChart.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportChart.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportChart.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportChart.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportChart.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportChart.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportChart.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportChart.go" >}}

{{< /tab >}}

{{< /tabs >}}
---