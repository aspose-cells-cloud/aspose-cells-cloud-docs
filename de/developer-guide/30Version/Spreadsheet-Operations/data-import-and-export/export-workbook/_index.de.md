---
title: "Arbeitsmappe exportieren"
second_title: "Dokument"
linktitle: "Arbeitsmappe"
type: docs
url: /de/export-excel-to-different-formats/
aliases: [  /de/export/excel-to-different-formats/ ]
keywords: "Aspose.Cells Cloud, Excel-Export, Arbeitsmappenkonvertierung, PDF, CSV, JSON, Bildformate, Tabellenkalkulations-API, XLSX, ODS, PNG"
description: "Eine Schritt-für-Schritt-Anleitung zum Exportieren von Excel-Arbeitsmappen in verschiedene Formate – einschließlich PDF, CSV, JSON und verschiedenen Bildtypen – mithilfe der Aspose.Cells Cloud REST-API und SDKs."
weight: 20
---

Sie können Arbeitsmappen in eines der folgenden Formate exportieren: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

## REST-API


```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.


### Anforderungsparameter

| Parametername | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Erforderlich | Beschreibung                                                                 |
|---------------|--------|------------------------------------|--------------|------------------------------------------------------------------------------|
| file          | Datei  | formData                           | Ja           | Hochzuladende Datei                                                          |
| objectType    | String | Abfrage                            | Ja           | Typ des zu exportierenden Objekts. Für den Chart-Export verwenden Sie `chart`. Weitere mögliche Werte sind `worksheet`, `picture` usw. |
| format        | String | Abfrage                            | Ja           | Gewünschtes Ausgabeformat. Unterstützte Werte: `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf`. |


### **Antwort**

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx.tif",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx.tif",
      "FileSize": 348126,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```


**HTTP-Statuscodes**

| Code | Bedeutung             | Beschreibung |
|------|-----------------------|--------------|
| 200  | OK                    | Formen erfolgreich exportiert; Antwort enthält die Dateiliste. |
| 400  | Ungültige Anforderung | Fehlende oder ungültige Parameter. |
| 401  | Nicht autorisiert     | Ungültiges oder fehlendes Zugriffstoken. |
| 413  | Anforderungstext zu groß | Hochgeladene Datei überschreitet das Größenlimit. |
| 500  | Interner Serverfehler | Unerwarteter Serverfehler. |


## Verwendung der PostExport-API mit SDKs

### PostExport-API-Spezifikation


Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) definiert eine öffentlich zugängliche Programmierschnittstelle, über die Sie REST-Interaktionen direkt aus einem Webbrowser heraus durchführen können.

Sie können das Befehlszeilentool **cURL** verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie die Cloud-API mit cURL aufgerufen wird.

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=workbook&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs beschleunigt die Entwicklung, da Low-Level-Details verwaltet werden, sodass Sie sich auf die Geschäftslogik konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie der Aspose.Cells-Webdienst mit verschiedenen SDKs aufgerufen wird:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExport.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExport.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExport.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExport.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExport.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExport.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExport.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExport.go" >}}

{{< /tab >}}

{{< /tabs >}}