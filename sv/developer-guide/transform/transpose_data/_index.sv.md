---
title: "TransposeData"
ArticleTitle: "TransposeData – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "TransposeData"
type: docs
url: /cells/transpose
aliases: ["/cells/transpose"]
keywords: "TransposeData, Aspose.Cells, molnbaserat API, kalkylark, transponera"
description: "Byt rader och kolumner i kalkylarket."
weight: 1000
---

## TransposeData i Aspose.Cells Cloud-webbtjänster

Byt rader och kolumner i kalkylarket.

### Slutpunkt för webb-API

```http
PUT https://api.aspose.cloud/v4.0/cells/transpose
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärparametrar

| ParameterNamn    | Typ    | Sökväg/Frågesträng/HTTP-body | Beskrivning                                                                                                                         |
|------------------|--------|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| Spreadsheet      | Fil    | FormData                     | Ladda upp kalkylarksfil.                                                                                                            |
| worksheet        | Sträng | Fråga                        | Kalkylbladets namn.                                                                                                                 |
| cellArea         | Sträng | Fråga                        | Ett angivet dataområde.                                                                                                             |
| outPath          | Sträng | Fråga                        | (Valfritt) Mappsökvägen där arbetsboken lagras. Standardvärdet är null.                                                             |
| outStorageName   | Sträng | Fråga                        | Lagringsnamn för utdatafil.                                                                                                         |
| region           | Sträng | Fråga                        | Kalkylarksregion/språkinställning (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar nummerformatering, datumtolkning och lokalbaserat beteende. |
| password         | Sträng | Fråga                        | Lösenord för att öppna kalkylarksfilen.                                                                                            |

### Begäran body-parameter

| ParameterNamn | Typ | Beskrivning |
| -------------- | --- | ----------- |
| [TBD]          | [TBD] | [TBD]       |

### **Svar**

```json
{
  "file": "binärström för det transponerade kalkylarket"
}
```

**Svarsstatuskoder**

| Kod | Betydelse | Beskrivning |
|-----|-----------|-------------|
| 200 | OK | Det transponerade kalkylarksfilen returneras. |
| 400 | Felaktig begäran | Ogiltiga indataparametrar eller felaktigt formaterad begäran. |
| 401 | Inte auktoriserad | Autentisering misslyckades eller JWT-token saknas/är ogiltig. |
| 413 | För stor payload | Uppladdad fil överskrider tillåten filstorlek. |
| 500 | Internt serverfel | Oväntat serverfel. |

## Hur du använder TransposeData med SDK:er

### TransposeData-specifikation

[TransposeData API-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{Transform}/{TransposeData}) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose Cells Cloud-webbtjänster. Följande exempel visar hur du gör anrop till moln-API:et med cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}

{< tab tabNum="1" >}

```bash
# Använd HTTPS för en säker anslutning
curl -v "https://api.aspose.cloud/v4.0/cells/transpose?worksheet=Blad1&cellArea=A1:C10&outPath=output%2Ffolder&outStorageName=MyStorage&region=sv-SE&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@exempel.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "file": "binärström för det transponerade kalkylarket"
}
```

{< /tab >}

{< /tabs >}

### Använd Aspose Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att påskynda utvecklingen. En SDK abstraher bort detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-lagringsplatsen</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose Cells Cloud-webbtjänster med hjälp av diverse SDK:er:
`[TBD]`
---