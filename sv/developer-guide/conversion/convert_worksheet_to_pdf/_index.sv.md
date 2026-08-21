---
title: "ConvertWorksheetToPdf"
ArticleTitle: "Konvertera kalkylblad till PDF – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "ConvertWorksheetToPdf"
type: docs
url: /cells/convert/worksheet/pdf
aliases: []
keywords: "Aspose.Cells, Konvertera kalkylblad till PDF, API"
description: "Konverterar ett kalkylblad i en kalkylarkfil till PDF med Aspose.Cells Cloud."
weight: 10
---

## ConvertWorksheetToPdf i Aspose.Cells Cloud Webbtjänster

Denna metod läser in en kalkylarkfil från det lokala filsystemet, konverterar dess kalkylblad till en PDF-fil och returnerar det konverterade resultatet. Källfilens sökväg och målformat måste anges korrekt. Se till att nödvändiga behörigheter finns för att läsa källfilen och skriva den konverterade filen, om tillämpligt. Konverteringsprocessen sker helt på molnservern, vilket eliminerar behovet av något molnlagring eller extern nedladdning.

Nyckelfunktioner inkluderar molnnat konverteringsflöde, minskat belastningspå molnresurser och ett förenklat arbetsflöde.

### Web API-slutpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärparametrar

| Parameter namn   | Typ     | Sökväg/Frågesträng/HTTP-body | Beskrivning                                                                                                                            |
|------------------|---------|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | Fil     | FormData                     | Ladda upp kalkylarkfil.                                                                                                               |
| worksheet        | Sträng  | Frågesträng                  | Namn på kalkylbladet i kalkylarket.                                                                                                   |
| outPath          | Sträng  | Frågesträng                  | (Valfritt) Mappsökvägen där arbetsboken lagras. Standardvärdet är null.                                                               |
| outStorageName   | Sträng  | Frågesträng                  | Lagringsnamn för utdatafil.                                                                                                            |
| fontsLocation    | Sträng  | Frågesträng                  | Använd anpassade typsnitt.                                                                                                             |
| AutoRowsFit      | Boolean | Frågesträng                  | (Valfritt) Autoanpassar alla rader i kalkylblad.                                                                                      |
| AutoColumnsFit   | Boolean | Frågesträng                  | (Valfritt) Autoanpassar alla kolumner i kalkylblad.                                                                                   |
| region           | Sträng  | Frågesträng                  | Kalkylarkregion/språkinställning (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar nummerformatering, datumtolkning och regionspecifika beteenden. |
| password         | Sträng  | Frågesträng                  | Lösenord för att öppna kalkylarkfilen.                                                                                                |

### Begärandetextparameter

| Parameter namn | Typ | Beskrivning |
| -------------- | --- | ----------- |
| [TBD]          |     |             |

### **Svar**

```json
{
  "file": "<binär ström av den genererade PDF-filen>"
}
```

**Svarsstatuskoder**

| Kod | Betydelse | Beskrivning |
|-----|-----------|-------------|
| 200 | OK | Kalkylbladet har konverterats till PDF och returnerats som en filström. |
| 400 | Felaktig begäran | Ogiltiga begärparametrar eller felaktig URL. |
| 401 | Inte auktoriserad | Autentisering misslyckades, eller inga uppgifter har angetts. |
| 404 | Hittades inte | Källfilen är inte tillgänglig. |
| 413 | Payload för stor | Den uppladdade filen överskrider den tillåtna storleksgränsen. |
| 500 | Internt serverfel | Ett undantag uppstod under konvertering av kalkylarket. |

## Hur man använder ConvertWorksheetToPdf med SDK:er

### ConvertWorksheetToPdf-specifikation

[ConvertWorksheetToPdf API-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#Conversion/ConvertWorksheetToPdf) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda verktyget cURL för kommandoraden för enkelt att komma åt Aspose.Cells webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}

{< tab tabNum="1" >}

```bash
# Använd HTTPS för en säker anslutning
curl -v "https://api.aspose.cloud/v4.0/cells/convert/worksheet/pdf?worksheet=Blad1&outPath=output%2Fmapp&outStorageName=MinLagring&fontsLocation=%2Fanpassade%2Ftypsnitt&AutoRowsFit=true&AutoColumnsFit=true&region=sv-SE&password=SecretPwd" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt-token>" \
  -F "Spreadsheet=@exempel.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "<binär ström av den genererade PDF-filen>"
}
```

{< /tab >}

{< /tabs >}

### Använd Aspose Cells Cloud SDK:er

Att använda ett SDK är det snabbaste sättet att snabba upp utvecklingen. Ett SDK abstraher bort detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Kolla in <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-repositoriet</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose Cells Cloud-webbtjänster med olika SDK:er:
`[TBD]`
---