---
title: "Excel till TIFF"
second_title: "Dokument"
linketitle: "Excel till TIFF"
type: docs
url: /convert-excel-file-to-tiff-file/
aliases: [/convert-excel-file-to-tiff-in-cloud/, /convert/excel-to-tiff/]
keywords: "Aspose.Cells Cloud, konvertering av Excel till TIFF, REST API, cURL, SDK, .NET, Java, Python, bildexport"
description: "Lär dig hur du konverterar Excel-arbetsböcker till TIFF-bilder med hög kvalitet med Aspose.Cells Cloud API. Detaljerade cURL-kommandon, SDK-exempel (C#, Java, Python, …), autentiseringssteg och felhantering."
weight: 90
---

**Konvertera**, **Spara som** och **Exportera**-ändpunkterna i Aspose.Cells Cloud möjliggör för dig att omvandla en Excel-arbetsbok till en TIFF-bild.  
Du kan anropa dessa ändpunkter direkt med **cURL** eller via någon av de SDK:er som stöds.

## REST API

| **API**                | **Metod** | **Syfte**                                                                                     | **Swagger-länk**                                                                            |
| ---------------------- | --------- | --------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `/cells/convert`       | PUT       | Konverterar en arbetsbok som anges i begärandetexten till det angivna formatet (TIFF).         | [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) |
| `/cells/{name}`        | GET       | Exporterar den namngivna arbetsboken till ett annat format (TIFF) och returnerar resultatet i svaret. | [GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)               |
| `/cells/{name}/saveAs` | POST      | Sparar arbetsboken i ett valt format (TIFF) och lagrar resultatet i molnlagringen.            | [PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)   |

Dessa ändpunkter är offentligt tillgängliga och kan anropas direkt från en webbläsare eller någon HTTP-klient.

### cURL-exempel

{{< tabs tabTotal="3" tabID="11" tabName11="convert" tabName12="saveas" tabName13="export">}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/convert?format=tiff" \
     -X PUT \
     -d '{"File":{"Name":"book1.xlsx","Data":"<base64‑content>"},"SaveFormat":"tiff"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="12" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx/saveas?newfilename=book1.tiff" \
     -X POST \
     -d '{"SaveFormat":"tiff","ImageFormat":"tiff"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< tab tabNum="13" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=tiff" \
     -X GET \
     -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}
{{< /tabs >}}

> **Obs:**
>
> - Begärandetexten för **Konvertera** måste innehålla filen (eller en referens till en lagrad fil) samt önskat `SaveFormat`.
> - Begäran för **Export** kräver inte någon begärandetext; formatet anges via fristrengen (`format=tiff`).

## Felhantering

| **Statuskod** | **Betydelse**        | **Vanlig orsak**                            |
| ------------- | -------------------- | ------------------------------------------- |
| 200           | Lyckades             | TIFF-bilden returneras (binär ström).      |
| 400           | Felaktig begäran     | Saknade eller felaktiga parametrar.         |
| 401           | Inte auktoriserad    | Ogiltigt eller saknat JWT-token.            |
| 404           | Hittades inte        | Den angivna arbetsboken finns inte.         |
| 500           | Internt serverfel    | Oväntat tillstånd på serversidan.           |

När ett fel uppstår returnerar API:et en JSON-payload med `Code`, `Message` och eventuellt `Description`.

## Moln-SDK-familj

Att använda en SDK är det snabbaste sättet att utveckla. En SDK hanterar detaljer på låg nivå så att du kan fokusera på ditt projekt. Kontrollera [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbookToTiff.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbookToTiff.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbookToTiff.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbookToTiff.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbookToTiff.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbookToTiff.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbookToTiff.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbookToTiff.go" >}}

{{< /tab >}}

{{< /tabs >}}