---
title: "Dela tabell"
ArticleTitle: "Dela tabell – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Dela tabell"
type: docs
url: /sv/cells/split/table
aliases: []
keywords: "Aspose.Cells, Dela tabell, API"
description: "API för att dela en tabell i en kalkylarkfil baserat på kolumnvärden."
weight: 1
---

## SplitTable i Aspose.Cells Cloud Webbtjänster

Denna metod utför en delningsoperation på källtabellen genom att gruppera rader enligt de distinkta värdena i den angivna kolumnen. Varje datagrupp (för varje unikt delningsvärde) bearbetas sedan som en separat dataenhet. Utgångsplatsen styras av två viktiga booleska parametrar:
- Bestämmer arbetsboksstruktur. Om `true` sparas varje delningsenhet i en egen arbetsboksfil. Om `false` blir varje enhet ett nytt kalkylblad i den aktuella arbetsboken.
- Bestämmer utdatapaketering. När inställt till `true` och kombinerat med `toNewWorkbook` = `true`, genererar metoden flera individuella filer och returnerar dem som ett ZIP-arkiv. När `false` sammanfogas all data till en enda fil (antingen en arbetsbok med flera kalkylblad eller en enskild fil enligt andra inställningar).

### Web API-slutpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/split/table
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärparametrar

| Parameternamn    | Typ     | Sökväg/Frågesträng/HTTP-body | Beskrivning                                                                                                                                                       |
|------------------|---------|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | Fil     | FormData                      | Ladda upp kalkylarkfil.                                                                                                                                           |
| worksheet        | Sträng  | Fråga                         | Kalkylblad som innehåller tabellen.                                                                                                                               |
| tableName        | Sträng  | Fråga                         | Datatabell som ska delas.                                                                                                                                          |
| splitColumnName  | Sträng  | Fråga                         | Kolumnnamn att dela efter.                                                                                                                                         |
| saveSplitColumn  | Boolesk | Fråga                         | Om data i delningskolumnen ska behållas.                                                                                                                          |
| splitRowNumber   | Heltal  | Fråga                         | [TBD]                                                                                                                                                              |
| toNewWorkbook    | Boolesk | Fråga                         | Kontroll för utdataplatser: `true` – skapar nya arbetsboksfiler som innehåller den delade data; `false` – lägger till ett nytt kalkylblad i den aktuella arbetsboken. |
| toMultipleFiles  | Boolesk | Fråga                         | `true` – exporterar tabelldata som **flera separata filer** (returneras som ZIP-arkiv); `false` – lagrar all data i **en enda fil** med flera kalkylblad. Standard: `false`. |
| outPath          | Sträng  | Fråga                         | (Valfritt) Mappsökvägen där arbetsboken lagras. Standard är `null`.                                                                                               |
| outStorageName   | Sträng  | Fråga                         | Lagringsnamn för utdatafil.                                                                                                                                       |
| fontsLocation    | Sträng  | Fråga                         | Använd anpassade typsnitt.                                                                                                                                        |
| region           | Sträng  | Fråga                         | Inställning för kalkylarksregion/språk (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar nummerformatering, datumtolkning och platspecifikt beteende.                 |
| password         | Sträng  | Fråga                         | Lösenord för att öppna kalkylarkfilen.                                                                                                                            |

### Begärcodeparametrar

| Parameternamn | Typ | Beskrivning |
| ------------- | --- | ----------- |
| Spreadsheet   | Fil | Ladda upp kalkylarkfil. |

### **Svar**

```json
{
  "file": "binär ström (ZIP-arkiv eller arbetsbok beroende på parametrar)"
}
```

**Svarsstatuskoder**

| Kod | Betydelse | Beskrivning |
|-----|-----------|-------------|
| 200 | OK        | Delningsoperationen slutfördes framgångsrikt. Svaret innehåller den genererade filen (ZIP-arkiv eller arbetsbok). |
| 400 | Felaktig begäran | Ogiltig URL eller begärparametrar. |
| 401 | Ej auktoriserad | Autentisering misslyckades, eller så angavs inga autentiseringsuppgifter. |
| 404 | Hittades inte | Källfilen är inte tillgänglig. |
| 413 | Payload för stor | Begärans payload överskrider den tillåtna storleken. |
| 500 | Internt serverfel | Kalkylarket stötte på ett problem vid hämtning av data. |

## Hur man använder SplitTable med SDK:er

### SplitTable-specifikation

[SplitTable API-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/DataProcessing/SplitTable) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells Cloud-webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

```bash
# Använd HTTPS för en säker anslutning
curl -v "https://api.aspose.cloud/v4.0/cells/split/table?worksheet=Sheet1&tableName=MyTable&splitColumnName=Category&saveSplitColumn=true&splitRowNumber=1&toNewWorkbook=true&toMultipleFiles=true&outPath=output%2Ffolder&outStorageName=MyStorage&fontsLocation=%2Fcustom%2Ffonts&region=en-US&password=SecretPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "file": "binär ström (ZIP-arkiv eller arbetsbok beroende på parametrar)"
}
```

{{< /tab >}}

{{< /tabs >}}

### Använd Aspose Cells Cloud SDK:er

Att använda ett SDK är det snabbaste sättet att påskynda utvecklingen. Ett SDK abstraher bort lågnivådetaljer och låter dig fokusera på dina projektuppgifter. Kolla in <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-lagret</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose Cells Cloud-webbtjänster med olika SDK:er:
`[TBD]`
---