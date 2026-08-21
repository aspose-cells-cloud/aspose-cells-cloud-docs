---
---
title: "Exportera kalkylblad – Aspose.Cells Cloud API v4 (PDF, PNG, SVG, CSV)"
second_title: "Dokument"
ArticleTitle: "Så här exporterar du ett fjärrladdat kalkylblad till ett annat format: Steg-för-steg-guide"
linktitle: "Exportera kalkylblad"
type: docs
url: /export-worksheet-as-format/
keywords: "Aspose Cells, exportera kalkylblad, moln-API, PDF, PNG, CSV, Excel-omvandling"
description: "Konvertera ett kalkylblad lagrat i Aspose.Cells Cloud till PDF, PNG, SVG, CSV eller andra format via en enda GET-begäran. Inkluderar kodexempel för C#, Java, Python med mera."
weight: 100
---

Exportera ett molnbaserat kalkylark/Excel-kalkylblad till en fil i ett annat format med Aspose.Cells Cloud Web API.

## **Exportera kalkylblad som format-API**

### Web-API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-token-baserad autentisering</a>.

```bash
-H "Authorization: Bearer {access_token}"
```

### **Begärandeparametrar**

| Parameternamn      | Typ    | Path/Query String/HTTPBody | Beskrivning                                                                                                                                        |
| :----------------- | :----- | :------------------------- | :------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**           | String | Path                       | (Nödvändigt) Namnet på den arbetsboksfil som ska hämtas.                                                                                           |
| **worksheet**      | String | Path                       | (Nödvändigt) Det specifika kalkylblad som ska konverteras.                                                                                        |
| **format**         | String | Query                      | (Nödvändigt) Önskat utdataformat (t.ex. `png`, `pdf`, `svg`).                                                                                      |
| **folder**         | String | Query                      | (Valfritt) Mappsökvägen där arbetsboken lagras. Standardvärdet är `null`.                                                                          |
| **storageName**    | String | Query                      | (Valfritt) Namnet på den anpassade molnlagringen. Använd standardlagring om utelämnas.                                                            |
| **outPath**        | String | Query                      | (Valfritt) Sökvägen till utdatamappen. Standardvärdet är `null`.                                                                                  |
| **outStorageName** | String | Query                      | (Valfritt) Lagringsnamn för utdatafilen.                                                                                                           |
| **fontsLocation**  | String | Query                      | (Valfritt) Angiv anpassade teckensnitt vid behov.                                                                                                  |
| **region**         | String | Query                      | (Valfritt) Kalkylarksregion/språkinställning (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar nummerformatering, datumtolkning och språkspecifikt beteende. |
| **password**       | String | Query                      | (Valfritt) Lösenordet för åtkomst till kalkylarkfilen.                                                                                             |

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

| Kod | Betydelse              | Beskrivning                                                       |
| ---- | ---------------------- | ----------------------------------------------------------------- |
| 200  | OK                     | Filter tillämpades framgångsrikt; svaret innehåller åtgärdsdetaljer. |
| 400  | Felaktig begäran       | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).  |
| 401  | Oautentiserad          | Ogiltig eller saknad JWT-token.                                   |
| 413  | För stor nyttolast     | Den uppladdade filen överskrider storleksgränsen.                 |
| 500  | Internt serverfel      | Oväntat serverfel.                                                |

## **Var bör du använda API:et för export av kalkylblad till ett annat format?**

- **Migrering av äldre system** – Konvertera tusentals äldre XLS-filer till XLSX för moderna system.
- **Arkiveringsstandardisering** – Normalisera diverse kalkylarksformat (XLS, XLSM, ODS, CSV) till ett enskilt format för arkivering.
- **Interoperabilitet i kontorsprogramsviter** – Konvertera Excel-filer till format som är kompatibla med LibreOffice, Google Sheets eller Apple Numbers.
- **Normalisering av datakällor** – Konvertera diverse kalkylarksformat till CSV eller JSON för inläsning till databaser.
- **Webbpublicering** – Konvertera finansiella modeller till HTML för visning på webben.

## Varför använda API:et för export av kalkylblad till ett annat format?

- **SDK-stöd för flera språk** – Erbjuder klientbibliotek för flera programmeringsspråk, vilket gör att utvecklare kan anropa API:et direkt från sin föredragna miljö.
- **Direktkonvertering utan mellanliggande uppladdning** – Möjliggör konvertering av ett kalkylblad som lagras i molnlagring till önskat format utan att behöva ladda ner och återuppladda filen.
- **Dataendast-extraktion** – Returnerar kalkylbladsinnehållet i det valda formatet utan att bevara visuell formatering.

## Hur använder man API:et för export av kalkylblad som format med SDK:er?

### API-specifikation: Exportera kalkylblad som format

[API-specifikationen: Exportera kalkylblad som format](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportWorksheetAsFormat) tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt för att utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anrop till moln-API:et med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets/Sheet1?format=pdf" \
     -H "Authorization: Bearer {access_token}" \
     -H "Accept: application/octet-stream"
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

Att använda SDK är det snabbaste sättet att utveckla, eftersom det abstraher bort detaljerna på lågnivån, så att du kan exportera ett kalkylarkskalkylblad till en fil i ett annat format med minimal kod.  
Kolla in [GitHub-förrådet](https://github.com/aspose-cells-cloud) för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur du gör anrop till Aspose.Cells webbtjänster med hjälp av olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportWorksheetAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportWorksheetAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportWorksheetAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportWorksheetAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportWorksheetAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportWorksheetAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportWorksheetAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportWorksheetAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}