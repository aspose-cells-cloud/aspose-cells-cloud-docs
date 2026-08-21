---
title: "Acceptera alla ändringsförslag"
ArticleTitle: "Acceptera alla ändringsförslag – Aspose.Cells Cloud"
second_title: "Dokument"
linktitle: "Acceptera alla ändringsförslag"
type: docs
url: /sv/cells/spreadsheet/accept-all-revisions
aliases: []
keywords: "Aspose.Cells, AcceptAllRevisions, kalkylark, ändringsförslag"
description: "Acceptera alla ändringsförslag i ett kalkylarksdokument med Aspose.Cells Cloud API."
weight: 100
---

## AcceptAllRevisions i Aspose.Cells Cloud-webbtjänster

Acceptera alla ändringsförslag i den uppladdade kalkylarksfilen och returnera den bearbetade arbetsboken.

### Endpoint för webb-API

```http
PUT https://api.aspose.cloud/v4.0/cells/spreadsheet/accept-all-revisions
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud API är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Requestparametrar

| Parametername | Typ   | Path/Query String/HTTP Body | Beskrivning |
|---------------|-------|-----------------------------|-------------|
| Spreadsheet   | Fil   | FormData (HTTP Body)        | Ladda upp kalkylarksfil. |
| outPath       | sträng | Frågesträng                 | (Valfritt) Mappsökvägen där arbetsboken lagras. Standard är null. |
| outStorageName| sträng | Frågesträng                 | Lagringsnamn för utdatafil. |
| fontsLocation | sträng | Frågesträng                 | Använd anpassade typsnitt. |
| region        | sträng | Frågesträng                 | Inställning för kalkylarkets region/språk (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar formatering av tal, tolkning av datum och lokalbundet beteende. |
| password      | sträng | Frågesträng                 | Lösenord för att öppna kalkylarksfilen. |

### Request Body-parameter

| Parametername | Typ | Beskrivning |
| ------------- | --- | ----------- |
| Spreadsheet   | Fil | Ladda upp kalkylarksfil. |

### **Svar**

```json
{
  "File": "Binär ström av den bearbetade kalkylarksfilen"
}
```

**Svarsstatuskoder**

| Kod | Betydelse | Beskrivning |
|-----|-----------|-------------|
| 200 | OK | Ändringsförslagen accepterades framgångsrikt och den bearbetade filen returnerades. |
| 400 | Felaktig förfrågan | Förfrågan är ogiltig (t.ex. saknar nödvändig fil eller ogiltiga parametrar). |
| 401 | Oautentiserad | Autentisering misslyckades eller JWT-token saknas/är ogiltig. |
| 413 | För stor nyttolast | Den uppladdade filen överskrider den tillåtna storleksgränsen. |
| 500 | Internt serverfel | Ett oväntat fel uppstod på servern. |

## Hur man använder AcceptAllRevisions med SDK:er

### AcceptAllRevisions-specifikation

[AcceptAllRevisions API-specifikationen](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Management/AcceptAllRevisions) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda kommandoradsverktyget cURL för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Förfrågan" tabName2="Svar" >}

{< tab tabNum="1" >}

```bash
# Använd HTTPS för en säker anslutning
curl -v "https://api.aspose.cloud/v4.0/cells/spreadsheet/accept-all-revisions?outPath=outputFolder&outStorageName=MyStorage&fontsLocation=/fonts&region=sv-SE&password=12345" \
  -X PUT \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/octet-stream" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'Spreadsheet=@sample.xlsx'
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "File": "Binär ström av den bearbetade kalkylarksfilen"
}
```

{< /tab >}

{< /tabs >}

### Använd Aspose Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att påskynda utvecklingen. En SDK abstraher bort detaljer på lägre nivå och låter dig fokusera på dina projektuppgifter. Se <a href="[TBD]" rel="noopener noreferrer">GitHub-lagringsplatsen</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose Cells Cloud-webbtjänster med olika SDK:er:
 `[TBD]`