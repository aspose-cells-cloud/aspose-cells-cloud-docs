---
title: "Konvertera Excel-område till PDF med Aspose.Cells Cloud API"
second_title: "Dokument"
ArticleTitle: "Hur man konverterar lokalt kalkylbladsområde till en PDF-fil: Steg-för-steg-guide"
linktype: "Konvertera område till PDF"
type: docs
url: /sv/convert-range-to-pdf/
keywords: "Aspose.Cells Cloud, konvertera Excel-område till PDF, Excel till PDF, molnkonvertering"
description: "Konvertera ett specifikt område från en lokal Excel-fil till PDF med Aspose.Cells Clouds REST API."
weight: 100
---

Exportera ett dataområde från en lokal Excel-fil till en [PDF](https://docs.fileformat.com/pdf/) fil med Cloud API:et.

**Förutsättningar**: Innan du använder detta API behöver du ett giltigt Aspose.Cells Cloud-konto, ett JWT-åtkomsttoken och eventuellt en Aspose.Cells Cloud SDK för din programmeringsspråk. Se till att mållagret (standard eller anpassat) är konfigurerat om du planerar att använda parametern `outStorageName`.

## **Konvertera område till PDF API**

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/pdf
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Förfrågningsparametrar:**

| Parameternamn  | Typ    | Sökväg/Frågesträng/HTTP-brödtext | Beskrivning                                                                   |
| -------------- | ------ | ------------------------------- | ----------------------------------------------------------------------------- |
| Spreadsheet    | Fil    | FormData                        | Ladda upp kalkylbladsfilen.                                                   |
| worksheet      | Sträng | Fråga                           | Kalkylbladsnamnet inom kalkylbladsfilen.                                      |
| range          | Sträng | Fråga                           | Cellområdet som ska konverteras, t.ex. A1:C10.                                |
| outPath        | Sträng | Fråga                           | (Valfritt) Mappens sökväg där arbetsboken lagras. Standard är null.          |
| outStorageName | Sträng | Fråga                           | Lagringsnamn för utdatafilen.                                                 |
| fontsLocation  | Sträng | Fråga                           | Plats för anpassade teckensnitt för hemanvändning.                            |
| region         | Sträng | Fråga                           | Inställning för kalkylbladsregion.                                            |
| password       | Sträng | Fråga                           | Lösenord för öppnande av kalkylbladsfilen.                                    |

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

_Typeligt svar är en binär PDF-ström som returneras som filnedladdning._

**HTTP-statuskoder**

| Kod | Betydelse             | Beskrivning                                                       |
| --- | --------------------- | ----------------------------------------------------------------- |
| 200 | OK                    | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig förfrågan    | Saknade eller ogiltiga parametrar (t.ex. filformat som inte stöds). |
| 401 | Obehörig              | Ogiltig eller saknad JWT-token.                                   |
| 413 | För stor nyttolast    | Den uppladdade filen överskrider storleksgränsen.                 |
| 500 | Internt serverfel     | Oväntat serverfel.                                                |

## **Var bör du använda API:et för att konvertera område till PDF?**

- **Ekonomiska rapporter**: Konvertera balansräkningar, resultaträkningar (specifika områden) till PDF för revisionsklar dokumentation.
- **Försäljningsrapporter**: Omvandla försäljningsinstrumentpaneler eller provisionberäkningar till distribuerbara PDF-filer.
- **Driftsmässiga mått**: Exportera KPI-tabeller och prestandamått som formella PDF-rapporter.
- **Kontraktsdata**: Exportera prislistor och avtal om servicegrad från kalkylblad till PDF-bilagor.
- **Revisions Spår**: Bevara ekonomiska dataområden som oföränderlig PDF-bevismaterial.
- **Portföljöversikter**: Exportera investeringsprestandaområden som kundklara PDF-rapporter.
- **Kvalitetskontrollrapporter**: Exportera inspektionsdataområden till PDF för efterlevnadsdokumentation.
- **Lageröversikter**: Omvandla lagerinformationstabeller till PDF för ledningsöversikt.

## **Varför bör du använda API:et för att konvertera område till PDF?**

- **Utvecklarvänlig**: Aspose.Cells Cloud erbjuder SDK-bibliotek i flera språk, vilket möjliggör snabb utveckling och omfattande dokumentation. Jämfört med att bygga egna lösningar för diagramrendering minskar detta utvecklingsarbetet betydligt.
- **Kostnadseffektiv**: Du kan konvertera dataområden utan att först ladda upp hela arbetsboken, vilket sparar lagringsutrymme och minskar kostnaderna.
- **Bevarar komplex Excel-formattering** i ett universellt tillgängligt PDF-format.

## **Hur använder du API:et för att konvertera område till PDF med SDK:er?**

### **API-specifikation för att konvertera område till PDF**

[API-specifikationen för att konvertera område till PDF](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToPDF) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för att enkelt komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Förfrågan" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/pdf?worksheet=Blad1&range=A1:C10" \
  -H "Authorization: Bearer {access_token}" \
  -F "Spreadsheet=@/sökväg/till/fil.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="result.pdf"
Content-Length: 8423

```

{{< /tab >}}

{{< /tabs >}}

### **Använd Aspose.Cells Cloud SDK:er**

Att använda SDK är det snabbaste sättet att utveckla, eftersom den abstraher bort detaljer på låg nivå och låter dig konvertera ett dataområde till en PDF-fil med koncist kod. Kontrollera [GitHub-lagringsplatsen](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man gör anrop till Aspose.Cells webbtjänster med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToPDF.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToPDF.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToPDF.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToPDF.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToPDF.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToPDF.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToPDF.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToPDF.go" >}}
{{</tab>}}
{{< /tabs >}}