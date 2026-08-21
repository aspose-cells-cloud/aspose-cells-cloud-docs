---
title: "Beräkna formel"
ArticleTitle: "Beräkna formel – Aspose.Cells Cloud API"
second_title: "Dokument"
linktype: "docs"
url: /cells/calculate/formula
aliases: []
keywords: "Aspose Cells, beräkna formel, kalkylark, API"
description: "Beräkna formel i ett kalkylark med Aspose.Cells Cloud API."
weight: 100
---

## Beräkna formel med Aspose.Cells Cloud-webbtjänster

Beräknar en angiven formel i ett angivet kalkylblad i en uppladdad kalkylarksfil och returnerar det resulterande kalkylarket som en filström. Denna åtgärd stöder platsbaserad bearbetning via parametern **region** och kan öppna lösenordsskyddade filer.

### Slutpunkt för webb-API

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/formula
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begärparametrar

| Parameter Name | Typ    | Sökväg/Frågesträng/HTTP-brödtext | Beskrivning |
|----------------|--------|----------------------------------|-------------|
| Spreadsheet    | Fil    | FormData                         | Ladda upp kalkylarksfil. |
| worksheet      | Sträng | Fråga                            | Namn på kalkylbladet som innehåller formeln. |
| formula        | Sträng | Fråga                            | Formeln som ska beräknas (t.ex. `=SUM(A1:B2)`). |
| region         | Sträng | Fråga                            | Kalkylarksregion/språkinställning (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar nummerformatering, datumtolkning och platsbaserat beteende. |
| password       | Sträng | Fråga                            | Lösenord för att öppna kalkylarksfilen. |

### Brödtextparameter för begäran

| Parameter Name | Typ | Beskrivning |
| -------------- | --- | ----------- |
| [TBD] | [TBD] | [TBD] |

### **Svar**

```json
{
  "File": "<binär ström av det resulterande kalkylarket>"
}
```

**Svarsstatuskoder**

| Kod | Betydelse | Beskrivning |
|-----|-----------|-------------|
| 200 | OK | Beräkningen lyckades; det resulterande kalkylarkfilen returneras. |
| 400 | Felaktig begäran | En eller flera begärparametrar saknas eller är ogiltiga. |
| 401 | Otillåten | Autentisering misslyckades eller JWT-token saknas/är ogiltig. |
| 413 | För stor nyttolast | Den uppladdade filen överskrider den tillåtna storleksgränsen. |
| 500 | Internt serverfel | Ett oväntat fel inträffade på servern. |

## Hur du använder Beräkna formel med SDK:er

### Specificering av Beräkna formel

[API-specificeringen för Beräkna formel](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Calculate/CalculationFormula) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör att du kan utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose Cells Cloud-webbtjänster. Följande exempel visar hur du gör anrop till Cloud-API:et med cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}

{< tab tabNum="1" >}

```bash
# Använd HTTPS för en säker anslutning
curl -v "https://api.aspose.cloud/v4.0/cells/calculate/formula?worksheet=Sheet1&formula=%3DSUM(A1%3AB2)&region=sv-SE&password=MyPassword" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F "Spreadsheet=@sample.xlsx"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "File": "<binär ström av det resulterande kalkylarket>"
}
```

{< /tab >}

{< /tabs >}

### Använd Aspose Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att påskynda utvecklingen. En SDK abstraher bort detaljer på låg nivå, vilket gör att du kan fokusera på dina projektuppgifter. Se <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-lagringsplatsen</a> för en fullständig lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose Cells Cloud-webbtjänster med olika SDK:er:
 `[TBD]`
---