---
title: "Aspose.Cells Cloud API – Konvertera Excel-diagram till PDF"
second_title: "Dokument"
ArticleTitle: "Hur man konverterar ett lokalt kalkylarkdiagram till en PDF-fil: Steg-för-steg-guide"
linktype: "Konvertera diagram till PDF"
type: docs
url: /sv/convert-chart-to-pdf/
keywords: "Aspose Cells, diagram, PDF, Excel, konvertering, moln-API"
description: "Exportera diagram från lokala Excel-filer till PDF-format med Aspose.Cells Cloud REST API. Stöder XLSX- och XLS-filer."
weight: 100
---

Exportera diagram från en lokal Excel-fil till [PDF](https://docs.fileformat.com/pdf/)-format med Moln-API:et.

## **Konvertera diagram till PDF Web API**

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/chart/pdf
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Förfrågningsparametrar:**

| Parameternamn    | Typ     | Path/Query String/HTTPBody | Beskrivning                                                                 |
| ---------------- | ------- | -------------------------- | --------------------------------------------------------------------------- |
| Spreadsheet      | Fil     | FormData                   | Ladda upp kalkylarkfilen.                                                   |
| worksheet        | Sträng  | Query                      | Namnet på kalkylbladet som innehåller diagrammet.                          |
| chartIndex       | Heltal  | Query                      | Indexet för det diagram som ska konverteras.                                |
| outPath          | Sträng  | Query                      | (Valfritt) Mappsökvägen dit den konverterade filen lagras. Standard är null. |
| outStorageName   | Sträng  | Query                      | Lagringsnamn för utdatafilen.                                               |
| fontsLocation    | Sträng  | Query                      | Använd anpassade typsnitt om nödvändigt.                                    |
| region           | Sträng  | Query                      | Inställning för kalkylarksregion.                                           |
| password         | Sträng  | Query                      | Lösenord för att öppna kalkylarkfilen.                                      |

### **Svar**

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

**HTTP-statuskoder**

| Kod | Betydelse             | Beskrivning                                                     |
| --- | --------------------- | --------------------------------------------------------------- |
| 200 | OK                    | Filtrering lyckades; svaret innehåller åtgärdsdetaljer.        |
| 400 | Felaktig förfrågan    | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Obehörig              | Ogiltig eller saknad JWT-token.                                 |
| 413 | För stor nyttolast    | Den uppladdade filen överskrider storleksgränsen.               |
| 500 | Internt serverfel     | Oväntat serverfel.                                              |

## Var bör du använda API:et för att konvertera diagram till PDF?

### **1. Bedriftsrapportering och automation**

- **Finansavdelningar**: Månadsrapporter med finansiella diagram → PDF-arkivering
- **Säljande team**: Diagram över prestandautveckling → PDF-kundrapporter
- **Marknadsanalys**: Diagram över kampanjprestanda → PDF-ledningsöversikter
- **Driftledning**: Diagram för produktövervakning → PDF-kompliansdokument

### **2. mjukvaruutveckling och integration**

- **SaaS-applikationer**: Diagramdata skapat av användare → laddningsbara PDF-rapporter
- **Enterprise-system**: Diagram från ERP/CRM-system → PDF-revisionsdokumentation
- **Mobilapplikationer**: In-app analysdiagram → delbara PDF-filer
- **Webbapplikationer**: Dashboarddiagram → PDF-exportfunktion

### **3. Dokumentbehandlingsarbetsflöden**

- **Batchbehandling**: Flera Excel-fildiagram konverteras till PDF samtidigt
- **Schemalagda uppgifter**: Automatiserad daglig/veckovis diagramrapportgenerering
- **Mallbaserade utdata**: Standarddiagramformat → PDF-dokument
- **Dokumentkomposition**: Kombinera diagram med annat innehåll i PDF-format

### **4. Branschspecifika applikationer**

- **Forskningsinstitut**: Diagram över experimentdata → PDF-forskningspappersfigurer
- **Utbildningssektorn**: Diagram i undervisningsmaterial → PDF-kursmaterial
- **Konsultföretag**: Analyseringsdiagram → PDF-kundleveranser
- **Tillverkningsindustrin**: Diagram för kvalitetskontroll → PDF-inspektionsrapporter
- **Hälsovård**: Patientdataplottdiagram → PDF-medical records
- **Statlig förvaltning**: Statistiska diagram → PDF-officiella publikationer

### **5. Innehållshantering och distribution**

- **Digitalt asset management**: Arkivering av diagram i standardiserat PDF-format
- **Kunskapsdatabaser**: Teknisk dokumentation med inbäddade PDF-diagram
- **Kundportaler**: Säker leverans av PDF-rapporter till intressenter
- **Regulatorisk efterlevnad**: Skapa revisionsklar PDF-dokumentation

## Varför bör du använda API:et för att konvertera diagram till PDF?

- Du kan konvertera diagram **utan att först ladda upp arbetsboken**, vilket sparar lagringsutrymme och minskar kostnaderna.
- Utveckling kan snabbt slutföras via befintliga Aspose.Cells Cloud SDK:er.
- **Enkel integration**: REST API med tydlig dokumentation.
- **Skalbar arkitektur**: Hanterar arbetsbelastningar från små till företagsstora operationer.

## Hur använder man API:et för att konvertera diagram till PDF med SDK:er?

### API-specifikation för att konvertera diagram till PDF

[API-specifikationen för att konvertera diagram till PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertChartToPDF) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

## Använd Aspose.Cells Cloud SDK:er

Att använda SDK är det snabbaste sättet att utveckla, eftersom det abstraherar bort detaljer på låg nivå och låter dig konvertera ett diagram till en PDF-fil med minimal kod.  
Följande kodexempel visar hur man gör anrop till Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertChartToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertChartToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertChartToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertChartToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertChartToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertChartToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertChartToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertChartToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}