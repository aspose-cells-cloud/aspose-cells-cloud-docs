---
title: "Konvertera kalkylblad till HTML-tabell"
ArticleTitle: "Konvertera kalkylblad till HTML-tabell – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "KonverteraKalkylbladTillHtmlTabell"
type: docs
url: /cells/convert/worksheet/html-table
aliases: []
keywords: "Aspose.Cells, KonverteraKalkylbladTillHtmlTabell, HTML-tabell, API"
description: "Konverterar ett kalkylblad i en kalkylfil på en lokal enhet till en HTML-tabellfil med hjälp av Aspose.Cells Cloud."
weight: 100
---

## Konvertera kalkylblad till HTML-tabell hos Aspose.Cells Cloud-webbtjänster

Denna åtgärd läser en kalkylfil från det lokala filsystemet, konverterar det angivna kalkylbladet till en HTML-tabell och returnerar det konverterade resultatet som en filström. Konverteringen sker helt på molnservern, så ingen mellanliggande uppladdning till molnlagring krävs. Den stöder valfria lokalinställningar och lösenordsskyddade arbetsböcker.

### Slutpunkt för webb-API

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/worksheet/html-table
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begäranparametrar

| Parameternamn | Typ   | Sökväg/Frågesträng/HTTP-kropp | Beskrivning |
|---------------|-------|-------------------------------|-------------|
| Kalkylfil     | Fil   | FormData                      | Ladda upp kalkylfil. |
| kalkylblad    | Sträng | Fråga                         | Namn på kalkylblad i kalkylfilen. (obligatoriskt) |
| region        | Sträng | Fråga                         | Region-/språkinställning för kalkylfilen (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar nummerformatering, datumtolkning och lokalspecifik beteende. |
| lösenord      | Sträng | Fråga                         | Lösenord för att öppna kalkylfilen. |

### Parametrar i begäranskroppen

| Parameternamn | Typ | Beskrivning |
| ------------- | --- | ----------- |
| *Ingen*       | *Ingen* | *Ingen JSON-kropp krävs; filen skickas som multipart/form-data.* |

### **Svar**

```json
{
  "File": "binär ström av den genererade HTML-tabellen"
}
```

**Svarsstatuskoder**

| Kod | Betydelse | Beskrivning |
|-----|-----------|-------------|
| 200 | OK        | Kalkylbladet konverterades framgångsrikt till HTML-tabell och returnerades som filström. |
| 400 | Felaktig begäran | Ogiltig begäran-URL eller obligatoriska parametrar saknas. |
| 401 | Inte auktoriserad | Autentisering misslyckades, eller så angavs inga autentiseringsuppgifter. |
| 404 | Hittades inte | Källfilen är inte tillgänglig. |
| 500 | Internt serverfel | Kalkylfilen stötte på ett fel vid hämtning av konverteringsdata. |
| 413 | För stor nyttolast | Den uppladdade filen överskrider den tillåtna storleksgränsen. |

## Hur man använder Konvertera kalkylblad till HTML-tabell med SDK:er

### Specifikation för Konvertera kalkylblad till HTML-tabell

[Specifikation för Konvertera kalkylblad till HTML-tabell API](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertWorksheetToHtmlTable) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur du gör anrop till moln-API:et med cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}

{< tab tabNum="1" >}

```bash
# Använd HTTPS för en säker anslutning
curl -v "https://api.aspose.cloud/v4.0/cells/convert/worksheet/html-table?worksheet={worksheet}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Kalkylfil=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "File": "binär ström av den genererade HTML-tabellen"
}
```

{< /tab >}

{< /tabs >}

### Använd Aspose Cells Cloud SDK:er

Att använda ett SDK är det snabbaste sättet att påskynda utvecklingen. Ett SDK abstraher bort detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Ta en titt på <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-lagringsplatsen</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose.Cells Cloud-webbtjänster med olika SDK:er:
`[TBD]`
---