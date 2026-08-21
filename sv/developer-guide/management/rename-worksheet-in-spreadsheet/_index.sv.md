---
title: "Byt namn på kalkylblad i Excel – Aspose.Cells Cloud API"
second_title: "Dokument"
ArticleTitle: "Hur man byter namn på kalkylblad i Excel – ändra kalkylbladsnamn"
linktitle: "Byt namn på kalkylblad i kalkylark"
type: docs
url: /rename-worksheet-in-spreadsheet/
keywords: "byt namn på kalkylblad, Aspose.Cells Cloud, Excel API, kalkylark, SDK, REST API"
description: "Byt namn på Excel-kalkylblad enkelt via Aspose.Cells Cloud API. Lär dig nödvändiga parametrar, se cURL-exempel och få SDK-kod för C#, Java, Python och mer."
weight: 100
---

Byt namn på kalkylblad i Excel-arbetsböcker programmatiskt med Aspose.Cells Cloud API. Ändra kalkylbladsnamn, uppdatera fliketiketter dynamiskt och automatisera kalkylarksorganisering via RESTful API-anrop. Användbar för dokumentstandardisering och arbetsflödesautomatisering.

## Byt namn på kalkylbladsnamn i Spreadsheet API

### Web API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet?sourceName={sourceName}&targetName={targetName}&outPath={outPath}&outStorageName={outStorageName}&region={region}&password={password}
```

**cURL-exempel**

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet?sourceName=Sheet1&targetName=Report_Q1" \
     -H "Authorization: Bearer {access_token}" \
     -F "spreadsheet=@myWorkbook.xlsx"
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärparametrar

| Parameternamn      | Typ    | Plats     | Beskrivning                                                                                                                                                                                                                 |
| ------------------ | ------ | --------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Spreadsheet**    | Fil    | FormData  | **Obligatoriskt**. Excel-arbetsboksfilen (.xlsx, .xls etc.) som innehåller kalkylbladet som ska byta namn.                                                                                                                 |
| **sourceName**     | Sträng | Fråga     | **Obligatoriskt**. Det nuvarande namnet på det kalkylblad du vill byta namn på.                                                                                                                                            |
| **targetName**     | Sträng | Fråga     | **Obligatoriskt**. Det nya namn som ska tilldelas kalkylbladet. Måste följa Excel-namngivningsregler (inga `:`, `\`, `?`, `*`, `[`, `]`) och vara unikt inom arbetsboken.                                                    |
| **outPath**        | Sträng | Fråga     | **Valfritt**. Målmappens sökväg i molnlagring där den döpta om arbetsboken kommer att sparas. Om `null` eller utelämnad sparar tjänsten filen i samma mapp som källarbetsboken (eller en standard sökväg).             |
| **outStorageName** | Sträng | Fråga     | **Valfritt**. Namnidentifieraren för din konfigurerade molnlagringstjänst (t.ex. `ArchiveStorage`). Om utelämnad används standardlagringen.                                                                                |
| **region**         | Sträng | Fråga     | **Valfritt**. Det lokala inställningsvärdet (t.ex. `sv-SE`) som kan påverka teckenkodning eller regionala namngivningskonventioner.                                                                                        |
| **password**       | Sträng | Fråga     | **Valfritt**. Lösenordet som krävs för att dekryptera och redigera en lösenordsskyddad arbetsbok. Utelämna om filen inte är krypterad.                                                                                     |

**Anteckningar**: Kalkylbladsnamn är begränsade till 31 tecken och får inte innehålla tecknen `:`, `\`, `?`, `*`, `[`, eller `]`.

### Svar

Ett lyckat anrop returnerar ett JSON-objekt med statusinformation och en länk till den omdöpta filen.

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

| Kod | Betydelse             | Beskrivning                                                    |
| --- | --------------------- | -------------------------------------------------------------- |
| 200 | OK                    | Filter applicerades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400 | Felaktig förfrågan    | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds). |
| 401 | Oautentiserad         | Ogiltig eller saknad JWT-token.                                |
| 413 | För stor nyttolast    | Den uppladdade filen överskrider storleksgränsen.              |
| 500 | Internt serverfel     | Oväntat serverfel.                                             |

## Var bör vi använda Rename Worksheet in Spreadsheet API?

- **Rapportgenerering och varumärkesstandardisering** – När kundrapporter genereras automatiskt kan generiska kalkylbladsnamn (t.ex. `Sheet1`) bytas ut mot kundspecifika namn (t.ex. `AcmeCorp_Q1_Summary`) för att säkerställa ett professionellt utförande.
- **Standardisering av dataprocesseringspipeline** – I ETL-arbetsflöden kan kalkylblad som exporteras med oregelbundna namn döpas om till standardiserade namn som `Raw_Data` eller `Cleaned_Data` för att uppfylla kraven för efterföljande analys.
- **Multispråkigt innehållsleverans** – Beroende på användarens språkpreferens kan kalkylbladsnamn översättas (t.ex. `数据` eller `Data`) innan filen levereras, vilket ger en anpassad upplevelse.

## Varför bör du använda Rename Worksheet in Spreadsheet API?

- **Utvecklarvänligt** – Ger SDK:er för flera språk med omfattande dokumentation, vilket förenklar integrationen jämfört med att bygga en egen lösning.
- **Minskat arbetsinsats** – Automatiserar kalkylbladsomdöpning och minskar manuellt arbete.
- **Betala-per-användning-modell** – Fakturerar endast för API-anrop, vilket eliminierar licenskostnader i förväg.
- **Ingen serverunderhåll** – Som en molntjänst behövs ingen servervärd eller programvaruuppdateringar.
- **Stöd för automatisering** – Underlättar för automatiserad dokumentstandardisering i arbetsflöden.

## Hur man använder Rename Worksheet in Spreadsheet API med SDK:er

### OpenAPI-specifikation

<a href="https://reference.aspose.cloud/cells/#/ManagementController/RenameWorksheetInSpreadsheet" target="_blank" rel="noopener noreferrer">OpenAPI-specifikationen</a> beskriver ett offentligt tillgängligt programmeringsgränssnitt, vilket möjliggör REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/spreadsheet/rename/worksheet?sheetName=Sheet1&destName=NewSheetName" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -F "Spreadsheet=@/path/to/input.xlsx"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
{
  "type": "FileContentResult",
  "fileContents": "byte[] (Base64-kodad)",
  "contentType": "MIME-typ",
  "fileDownloadName": "valfritt filnamn"
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose.Cells Cloud SDK:er

Att använda ett SDK är det snabbaste sättet att påskynda utvecklingen. SDK:et abstraher underliggande HTTP-detaljer, så att du kan byta namn på kalkylblad med minimal kod. Se GitHub-repositoriet för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_RenameWorksheet.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_RenameWorksheet.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_RenameWorksheet.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_RenameWorksheet.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_RenameWorksheet.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_RenameWorksheet.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_RenameWorksheet.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_RenameWorksheet.go" >}}
{{</tab>}}
{{< /tabs >}}