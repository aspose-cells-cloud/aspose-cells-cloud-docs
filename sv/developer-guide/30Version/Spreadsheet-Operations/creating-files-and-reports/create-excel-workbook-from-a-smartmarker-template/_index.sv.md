---
title: "Skapa Excel-rapporter med Smart Marker-mallar"
second_title: "Dokument"
linktitle: "SmartMarker"
type: docs
url: /build-report-with-smart-marker/
aliases:
  - /create-excel-workbook-from-a-smartmarker-template/
  - /workbook/smartmarker/
  - /workbook/create/smartmarker/
keywords: "Excel, Smart Marker, Aspose.Cells Cloud, REST API, Arbetsbok, SDK, API, Rapportgenerering"
description: "Lär dig hur du genererar Excel-arbetsböcker från Smart Marker-mallar med Aspose.Cells Cloud REST API. Innehåller information om begäran/svar, cURL-exempel, förutsättningar, anteckningar och SDK-kodexempel."
weight: 40
ArticleTitle: "Skapa Excel-rapporter med Smart Marker-mallar – Aspose.Cells Cloud API-guide"
---

Denna REST API skapar en arbetsbok med hjälp av en Smart Marker-mall.

## Workbook SmartMarker API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/smartmarker
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Vad är en Smart Marker?**

En Smart Marker är en platsmarkör-syntax som kopplar datafält i en XML- (eller JSON-) fil till celler i en Excel-mall. Vid körning ersätter Aspose.Cells markörerna med motsvarande data, vilket gör att du kan generera helt ifyllda rapporter programmerat.

### **Frågeparametrar**

| Parameternamn | Typ   | Beskrivning                                                  |
| ------------- | ----- | ------------------------------------------------------------ |
| outPath       | string | Målsökväg dit den genererade arbetsboken kommer att sparas. |
| folder        | string | Mapp som innehåller den ursprungliga arbetsboken.            |
| storageName   | string | Namn på den lagringstjänst som ska användas.                 |

### **Parametrar för begärandetext**

| Parameternamn | Typ | Beskrivning                                      |
| ------------- | --- | ------------------------------------------------ |
| xmlFile       | fil | Smart Marker-XML-datafilen som laddats upp med begäran. |

### **Svar**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**Anteckningar / Begränsningar:**  
- API:et stöder Excel-filer upp till **50 MB** i storlek.  
- Endast formatet **.xlsx**, **.xlsm** och **.xlsb** accepteras.  
- En hastighetsbegränsning på **20 begäranden per sekund** per konto tillämpas.

**HTTP-statuskoder**

| Kod | Betydelse                   | Beskrivning                                           |
|-----|-----------------------------|-------------------------------------------------------|
| 200 | OK                          | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig begäran            | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Auktoriseringsfel           | Ogiltig eller saknad JWT-token.                      |
| 413 | Payload för stor            | Den uppladdade filen överskrider storleksgränsen.    |
| 500 | Internt serverfel           | Oväntat serverfel.                                   |

## Hur man använder Workbook SmartMarker API

### Workbook SmartMarker API-specifikation

[OpenAPI-specifikationen](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookGetSmartMarkerResult) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Du kan använda kommandoradsverktyget **cURL** för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

**Snabb rad-exempel**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/{name}/smartmarker?outPath={outPath}" -H "Authorization: Bearer {access_token}" -F "xmlFile=@Sample_SmartMarker_Data.xml"
```

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/newworkbook_14.xlsx/smartmarker?outPath=GeneratedReport.xlsx" \
    -H "accept: multipart/form-data" \
    -H "x-aspose-client: Containerize.Swagger" \
    -F "xmlFile=@Sample_SmartMarker_Data.xml"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```text
HTTP/1.1 200 OK
Content-Type: application/json

{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### **Felhantering**

| HTTP-status | Beskrivning       | Vanlig orsak                                           |
| ----------- | ----------------- | ------------------------------------------------------ |
| 400         | Felaktig begäran  | Saknad mall, felaktig XML eller ogiltiga parametrar. |
| 401         | Auktoriseringsfel | Ogiltig eller saknad autentiseringstoken.             |
| 404         | Hittades inte     | Angiven arbetsbok eller lagringsplats finns inte.     |
| 500         | Internt serverfel | Oväntat serverfel.                                    |

**Exempel på felaktigt svar (400)**

```json
{
  "Code": 400,
  "Message": "XML-datafilen saknas eller är felaktig."
}
```

## Cloud SDK-familj

Att använda ett SDK är det bästa sättet att påskynda utvecklingen. Ett SDK hanterar detaljer på låg nivå så att du kan fokusera på dina projektuppgifter. Kolla in [GitHub-lagret](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookCreate.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookCreate.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookCreate.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookCreate.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookCreate.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookCreate.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookCreate.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookCreate.go" >}}

{{< /tab >}}

{{< /tabs >}}