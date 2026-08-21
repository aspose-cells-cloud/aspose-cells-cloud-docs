---
title: "Spara kalkylark i ett annat format – Aspose.Cells Cloud API (v4.0)"
second_title: "Dokument"
ArticleTitle: "Så här sparar du ett kalkylark i ett annat filformat i molnlagring: Steg-för-steg-guide"
linktype: "Spara kalkylark som"
type: docs
url: /sv/save-spreadsheet-as/
keywords: "Aspose Cells, konvertering av kalkylark, spara som, API, XLSX till PDF, molnlagring, Excel till PDF, CSV-export, molnkonvertering"
description: "Lär dig hur du sparar ett kalkylark som lagras i Aspose Cloud i ett annat format (t.ex. XLSX, PDF, CSV etc.) med Aspose.Cells Cloud Save Spreadsheet API. Inkluderar begärsyntax, parametrar, cURL-exempel och SDK-kod."
weight: 100
---

Spara ett molnkalkylark eller Excel-fil i ett annat format i molnlagring.

## **Save Spreadsheet as API**

### Web-API

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/saveas
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Begärparametrar**

| Parametername   | Typ    | Plats  | Beskrivning                                                                                      |
| :-------------- | :----- | :----- | :----------------------------------------------------------------------------------------------- |
| name            | Sträng | Sökväg | **Obligatoriskt.** Namnet på arbetsboken som ska konverteras.                                   |
| format          | Sträng | Fråga  | **Obligatoriskt.** Önskat utdataformat (t.ex. `Xlsx`, `PDF`, `CSV`).                            |
| saveOptionsData | Klass  | Brödtext | Valfri data för spalternativ. Om utelämnas blir standardvärdet `null`.                          |
| folder          | Sträng | Fråga  | Valfri mappkatalog där källarbetsboken lagras. Om utelämnas blir standardvärdet `null`.          |
| storageName     | Sträng | Fråga  | Valfritt namn på en anpassad lagring. Om utelämnas används standardlagringen.                   |
| outPath         | Sträng | Fråga  | Valfri utdatapath för den konverterade filen. Om utelämnas blir standardvärdet `null`.          |
| outStorageName  | Sträng | Fråga  | Valfritt lagringsnamn för utdatafilen.                                                          |
| fontsLocation   | Sträng | Fråga  | Valfri plats för anpassade typsnitt.                                                            |
| region          | Sträng | Fråga  | Valfritt inställningsvärde för kalkylarkregion.                                                |
| password        | Sträng | Fråga  | Valfritt lösenord för öppning av kalkylarksfilen.                                               |

**Stödda utdataformat**

| Format   | Filändelse                                       |
| :------- | :----------------------------------------------- |
| Xlsx     | .xlsx                                            |
| Pdf      | .pdf                                             |
| Csv      | .csv                                             |
| Html     | .html                                            |
| Ods      | .ods                                             |
| Xls      | .xls                                             |
| Txt      | .txt                                             |
| Mhtml    | .mhtml                                           |
| Tiff     | .tiff                                            |
| Pptx     | .pptx                                            |
| … (mer)  | Se API-specifikationen för hela listan (över 20 format) |

### **Svar**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Exempel på felaktigt svar (400 Bad Request)**

```json
{
  "Code": 400,
  "Message": "Ogiltiga begärparametrar."
}
```

**HTTP-statuskoder**

| Kod | Betydelse             | Beskrivning                                                              |
|-----|-----------------------|--------------------------------------------------------------------------|
| 200 | OK                    | Filter tillämpades framgångsrikt; svaret innehåller åtgärdsdetaljer.    |
| 400 | Bad Request           | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).         |
| 401 | Unauthorized          | Ogiltig eller saknad JWT-token.                                          |
| 413 | Payload Too Large     | Den uppladdade filen överskrider storleksgränsen.                        |
| 500 | Internal Server Error | Oväntat serverfel.                                                       |

## Var bör du använda Save Spreadsheet API?

### Enterprise-dokumenthanteringssystem

- Spara finansrapporter automatiskt som PDF-arkiv.
- Säkerhetskopiera försäljningsdata regelbundet i CSV-format.
- Spara projektplaner som skrivskyddade filer för att förhindra oavsiktliga ändringar.

### Dataintegrering och ETL-processer

- Exportera data från CRM-system och spara dem som en standard-Excel-mall.
- Konvertera ERP-data till CSV för import till andra system.
- Spara rådata som JSON för API-överföring.

### Utveckling och automatiseringsscenarier

- Backend-processning för webbapplikationer.
- Automatiserade system för rapportgenerering.
- Molnsamarbetsplattformar.
- Integration i godkännandeprocesser.
- Säkerhetskopiering och migrering av data.

## Varför bör du använda Save Spreadsheet API?

- **Utvecklarvänlig** – Erbjuder SDK:er för flera språk med detaljerad dokumentation, vilket förenklar integrationen.
- **Arbetsbesparande** – Hanterar konverteringen på servern, vilket minskar behovet av anpassad konverteringskod.
- **Användningsbaserad prissättning** – Fakturerar endast för utförda API-anrop, utan förskottsbaserade licensavgifter.
- **Ingen serverunderhållning** – Tjänsten körs i molnet, vilket innebär att du slipper hantera konverteringsinfrastruktur.
- **Brett formatstöd** – Stöder konvertering mellan över 20 kalkylarksformat.
- **Dataintegritet** – Bevarar layout, formler och formatering vid konvertering.

## Hur använder du Save Spreadsheet as API med SDK:er?

### Save Spreadsheet as API-specifikation

[Save Spreadsheet as API-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/SaveSpreadsheetAs) definierar ett offentligt tillgängligt programmeringsgränssnitt, vilket gör att du kan utföra REST-interaktioner direkt från en webbläsare.

**Exempel med begärcode och cURL**

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur du gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/saveas?format=pdf&outPath=output.pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{"SaveOptions":{"SaveFormat":"pdf"}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att utveckla, eftersom den abstraher bort detaljer på lägre nivå och låter dig spara ett kalkylark i ett annat format med minimal kod. Se [GitHub-arkivet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du anropar Aspose.Cells webbtjänster med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_WorkbookSaveAs.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_WorkbookSaveAs.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_WorkbookSaveAs.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_WorkbookSaveAs.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_WorkbookSaveAs.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_WorkbookSaveAs.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_WorkbookSaveAs.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_WorkbookSaveAs.go" >}}
{{</tab>}}
{{< /tabs >}}