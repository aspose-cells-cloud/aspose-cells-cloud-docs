---
title: "Bild exportieren"
second_title: "Dokument"
linktitle: "Bild"
type: docs
url: /export-excel-picture-to-different-formats/
aliases: [/export/excel-picture-to-different-formats/]
keywords: "Bild exportieren, Aspose.Cells Cloud, REST-API, Excel, Bildformate, PNG, GIF, JPEG, BMP, SVG, TIFF, EMF, WMF"
description: "Exportieren Sie Excel-Bilder in verschiedene Bildformate mithilfe der Aspose.Cells Cloud REST-API. Der Dienst unterstützt SDKs für mehrere Sprachen, darunter C#, Java, PHP, Ruby, Node.js, Python, Perl, Go und Swift."
weight: 20
---

Sie können Bilder in die folgenden Formate exportieren: [PNG](https://docs.fileformat.com/Image/png/), [GIF](https://docs.fileformat.com/image/gif/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), und [WMF](https://docs.fileformat.com/image/Wmf/).

## REST-API


```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.


### Anforderungsparameter

| Parameter       | Ort         | Typ  | Erforderlich | Beschreibung                                                                 |
| --------------- | ----------- | ---- | ------------ | ---------------------------------------------------------------------------- |
| `file`          | Form‑data   | file | Ja           | Die Excel-Arbeitsmappe (`.xlsx`, `.xls`, usw.), die die OLE-Objekte enthält. |
| `outputFormat`  | Query       | string | Ja         | Zielformat für die exportierten Objekte (`pdf`, `png`, `jpeg`, `docx`, `pptx`). |
| `objectType`    | Query       | string | Ja         | Fester Wert `oleobject`.                                                     |


### Antwort

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet6_Pictures_0.tif",
      "FileSize": 21680,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet6_Pictures_1.tif",
      "FileSize": 21286,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet2_Pictures_0.tif",
      "FileSize": 130084,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet2_Pictures_1.tif",
      "FileSize": 120062,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                      |
|------|-----------------------------|-------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Details zum Vorgang. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Unauthorized                | Ungültiges oder fehlendes JWT-Token.                             |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.            |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                        |
## Verwendung der PostExport-API mit SDKs

### PostExport-API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

Sie können das Kommandozeilentool **cURL** verwenden, um problemlos auf Aspose.Cells-Webdienste zuzugreifen. Das folgende Beispiel zeigt, wie ein Aufruf der Cloud-API mit cURL erfolgt.


```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=picture&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Verwendung der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist die effizienteste Methode, um die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf die Logik Ihres Projekts konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportPicture.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportPicture.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportPicture.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportPicture.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportPicture.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportPicture.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportPicture.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportPicture.go" >}}
{{< /tab >}}

{{< /tabs >}}