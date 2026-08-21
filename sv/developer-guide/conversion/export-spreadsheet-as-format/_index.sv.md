---
title: "Aspose.Cells Cloud Web API – Exportera fjärr-Excel-arbetsblad till andra format – Gratis onlineverktyg"
second_title: "Dokument"
ArticleTitle: "Hur man exporterar ett fjärrstyrkt kalkylblad till andra format: Steg-för-steg-guide"
linktitle: "Exportera kalkylark till format"
type: docs
url: /export-spreadsheet-as-format/
keywords: "Aspose.Cells, konvertering av kalkylark, API, export, PDF, CSV, JSON, XLSX"
description: "Konvertera Excel-arbetsböcker lagrade i Aspose Cloud till PDF, XLSX, CSV, JSON eller HTML via en enda REST-slutpunkt. Lär dig begärsyntax, parametrar och se SDK-exempel i C#, Java, Python och mer."
weight: 100
---

Exportera ett molnbaserat kalkylark (Excel) till ett annat filformat.

## **Exportera kalkylark till format – API**

### Web-API

```http
GET https://api.aspose.cloud/v4.0/cells/{name}?format={format}&folder={folder}&storageName={storageName}&outPath={outPath}&outStorageName={outStorageName}&fontsLocation={fontsLocation}&region={region}&password={password}
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Begärandeparametrar:**

| Parameter_name | Typ    | Path/Query String/HTTP Body | Beskrivning                                                                                                                                           |
| :------------- | :----- | :-------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------- |
| name           | String | Path                        | (Obligatoriskt) Namnet på arbetsbokens fil som ska hämtas.                                                                                           |
| format         | String | Query                       | (Obligatoriskt) Önskat utdataformat (t.ex. “Xlsx”, “PDF”, “CSV”).                                                                                    |
| folder         | String | Query                       | (Valfritt) Sökvägen till mappen där arbetsboken är lagrad. Standardvärdet är null.                                                                   |
| storageName    | String | Query                       | (Valfritt) Namnet på lagringen om du använder anpassad molnlagring. Använd standardlagring om utelämnas.                                             |
| outPath        | String | Query                       | (Valfritt) Sökvägen till mappen där arbetsboken kommer att sparas. Standardvärdet är null.                                                           |
| outStorageName | String | Query                       | (Valfritt) Lagringsnamn för utdatafilen.                                                                                                             |
| fontsLocation  | String | Query                       | (Valfritt) Plats för anpassade typsnitt.                                                                                                             |
| region         | String | Query                       | (Valfritt) Kalkylarkets regionspråkinställning (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar nummerformatering, datumtolkning och språkspecifika beteenden. |
| password       | String | Query                       | (Valfritt) Lösenordet för att öppna kalkylarksfilen.                                                                                                |

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

Svaret innehåller ett enda objekt som representerar den konverterade fillström.

**HTTP-statuskoder**

| Kod | Betydelse             | Beskrivning                                                       |
| ---- | --------------------- | ----------------------------------------------------------------- |
| 200  | OK                    | Filter tillämpades framgångsrikt; svaret innehåller åtgärdens detaljer. |
| 400  | Felaktig begäran      | Saknade eller ogiltiga parametrar (t.ex. filtyp som inte stöds).  |
| 401  | Oauktoriserad         | Ogiltig eller saknad JWT-token.                                   |
| 413  | För stor nyttolast    | Den uppladdade filen överskrider storleksgränsen.                 |
| 500  | Internt serverfel     | Oväntat serverfel.                                                |

## Var bör du använda API:et för att exportera kalkylark till andra format?

- **Migrering av äldre system**: Konvertera tusentals äldre XLS-filer till XLSX för moderna system.
- **Standardisering av arkivering**: Normalisera olika kalkylarksformat (XLS, XLSM, ODS, CSV) till ett enda format för arkivering.
- **Interoperabilitet med kontorspaket**: Konvertera Excel-filer till format som är kompatibla med LibreOffice, Google Sheets eller Apple Numbers.
- **Normalisering av datakällor**: Konvertera olika kalkylarksformat till CSV eller JSON för att kunna mata in data i databaser.
- **Webbpublicering**: Konvertera finansiella modeller till HTML för visning på webben.

## Varför bör du använda API:et för att exportera kalkylark till andra format?

- **Utvecklarvänligt**: Aspose.Cells Cloud erbjuder SDK-bibliotek i flera språk, vilket möjliggör snabb utveckling och är tillämpligt med omfattande dokumentation. Jämfört med att bygga egna lösningar för diagramvisning minskas utvecklingsarbetet avsevärt.
- **Lägre arbetskostnad**: Minimerar behovet av att tilldela personal till dokumentkonsolidering.
- **Betala per användning**: Ingen upfront-investering; du betalar bara för de API-anrop som faktiskt används.
- **Ingen underhållsbehov på serversidan**: Du behöver inte underhålla servrar, uppdatera programvara eller hantera kompatibilitetsproblem.
- **Omfattande formatsupport**: Konvertera mellan över 20 olika kalkylarksformat.
- **Bevara dataintegritet och formatering**: Behåller originalutseendet, formler och stil vid konvertering.

## Hur använder man API:et för att exportera kalkylark till format med SDK:er?

### Specifikation för API:et för att exportera kalkylark till format

<a href="https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ExportSpreadsheetAsFormat" rel="noopener noreferrer">Specifikation för API:et för att exportera kalkylark till format</a> tillhandahåller ett offentligt tillgängligt programmeringsgränssnitt för att utföra REST-interaktioner sömlöst.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="11" tabName11="Begäran" tabName12="Svar" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v4.0/cells/MyWorkbook.xlsx/worksheets?format=pdf" \
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

Att använda en SDK är det snabbaste sättet att utveckla, eftersom den abstraher bort detaljer på låg nivå och tillåter dig att exportera ett kalkylark till ett filformat med kort kod.  
Innan du anropar API:et, måste du skaffa en OAuth 2.0-åtkomsttoken och inkludera den i `Authorization: Bearer <token>`-huvudet.

Ta en titt på <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-lagret</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel illustrerar hur man interagerar med Aspose.Cells-webbtjänster via olika SDK:er:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ExportSpreadsheetAsFormat.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ExportSpreadsheetAsFormat.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ExportSpreadsheetAsFormat.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ExportSpreadsheetAsFormat.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ExportSpreadsheetAsFormat.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ExportSpreadsheetAsFormat.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ExportSpreadsheetAsFormat.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ExportSpreadsheetAsFormat.go" >}}
{{</tab>}}
{{< /tabs >}}
---