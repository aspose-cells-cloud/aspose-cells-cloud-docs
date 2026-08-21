---
title: "Ta bort tecken i fjärrkalkylark"
ArticleTitle: "Ta bort tecken i fjärrkalkylark – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Ta bort tecken i fjärrkalkylark"
type: docs
url: /sv/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/characters
aliases: []
keywords: "Aspose.Cells, ta bort tecken, textbearbetning"
description: "Tar bort användardefinierade tecken, fördefinierade symboluppsättningar eller valfri delsträng från varje cell i det valda intervallet, samtidigt som formler, formatering och datavalidering för ett fjärrkalkylark bevaras."
weight: 100
---

## Ta bort tecken i fjärrkalkylark med Aspose.Cells Cloud Webbtjänster

Tar bort användardefinierade tecken, fördefinierade symboluppsättningar eller valfri delsträng från varje cell i det valda intervallet, samtidigt som formler, formatering och datavalidering för ett fjärrkalkylark bevaras.

### Webb-API-slutpunkt

```http
PUT https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/characters
```

### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### Begäranparametrar

| Parameternamn       | Typ     | Sökväg/Frågesträng/HTTP-kropp | Beskrivning                                                                                                                                                                      |
|---------------------|---------|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| name                | string  | Sökväg                        | (Obligatoriskt) Namnet på arbetsboksfilen som ska hämtas.                                                                                                                       |
| worksheet           | string  | Sökväg                        | Ange kalkylbladet i kalkylarket.                                                                                                                                               |
| range               | string  | Sökväg                        | Ange intervallet i kalkylbladet.                                                                                                                                               |
| removeTextMethod    | string  | Fråga                         | Ange typen av metod för textborttagning.                                                                                                                                        |
| characterSets       | string  | Fråga                         | Ange teckenuppsättningarna.                                                                                                                                                      |
| removeCustomValue   | string  | Fråga                         | Ange det anpassade värde som ska tas bort.                                                                                                                                      |
| caseSensitive       | boolean | Fråga                         | Påverkar läget `Substring` och `CustomChars` när aktiverat.                                                                                                                    |
| folder              | string  | Fråga                         | (Valfritt) Sökvägen till mappen där arbetsboken lagras. Standardvärdet är null.                                                                                                 |
| storageName         | string  | Fråga                         | (Valfritt) Namnet på lagringsutrymmet vid användning av anpassat molnlagringsutrymme. Använd standardlagringsutrymmet om utelämnat.                                            |
| region              | string  | Fråga                         | Region/språkinställning för kalkylark (t.ex. `sv-SE`, `en-US`, `fr-FR`). Påverkar formatering av tal, tolkning av datum och språkspecifika beteenden.                          |
| password            | string  | Fråga                         | Lösenordet för öppning av kalkylarksfilen.                                                                                                                                       |

### Begärandekroppparameter

| Parameternamn | Typ  | Beskrivning |
| ------------- | ---- | ----------- |
| *Ingen*       | *Ingen* | Denna åtgärd kräver ingen begärandekropp. |

### **Svar**

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "Tecken har tagits bort framgångsrikt.",
  "Data": {
    "RequestId": "string",
    "Workbook": {
      "Name": "string",
      "Path": "string"
    }
  }
}
```

**Svarsstatuskoder**

| Kod | Betydelse | Beskrivning |
|-----|-----------|-------------|
| 200 | OK        | Tecknen har tagits bort framgångsrikt och arbetsboken har uppdaterats. |
| 400 | Felaktig begäran | En eller flera parametrar saknas eller är ogiltiga. |
| 401 | Oautentiserad | Autentisering misslyckades – JWT-token saknas eller är ogiltig. |
| 413 | Begäran för stor | Begärans storlek överskrider tillåten gräns. |
| 500 | Internt serverfel | Ett oväntat fel uppstod på serversidan. |

## Hur du använder Ta bort tecken i fjärrkalkylark med SDK:er

### Specifikation för Ta bort tecken i fjärrkalkylark

[Specifikationen för Ta bort tecken i fjärrkalkylark API](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/{TextProcessingController}/RemoveCharactersInRemoteSpreadsheet) definierar ett offentligt tillgängligt programmeringsgränssnitt och låter dig utföra REST-interaktioner direkt från en webbläsare.

Du kan använda cURL-kommandoradsverktyget för enkelt att komma åt Aspose.Cells-webbtjänster. Följande exempel visar hur man gör anrop till Cloud API med cURL.

{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}

{< tab tabNum="1" >}

```bash
# Använd HTTPS för en säker anslutning
curl -v "https://api.aspose.cloud/v4.0/cells/{name}/worksheets/{worksheet}/range/{range}/content/remove/characters?removeTextMethod={removeTextMethod}&characterSets={characterSets}&removeCustomValue={removeCustomValue}&caseSensitive={caseSensitive}&folder={folder}&storageName={storageName}&region={region}&password={password}" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{< /tab >}

{< tab tabNum="2" >}

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "Tecken har tagits bort framgångsrikt.",
  "Data": {
    "RequestId": "3f5e2c1a-9b7d-4a6e-8c2f-1d5e9b7a6c4f",
    "Workbook": {
      "Name": "Sample.xlsx",
      "Path": "/documents/Sample.xlsx"
    }
  }
}
```

{< /tab >}

{< /tabs >}

### Använd Aspose Cells Cloud SDK:er

Att använda en SDK är det snabbaste sättet att påskynda utvecklingen. En SDK abstraher bort detaljer på låg nivå och låter dig fokusera på dina projektuppgifter. Besök <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub-lagret</a> för en komplett lista över Aspose.Cells Cloud SDK:er.

Följande kodexempel visar hur man anropar Aspose Cells Cloud-webbtjänster med olika SDK:er:
`[TBD]`
---