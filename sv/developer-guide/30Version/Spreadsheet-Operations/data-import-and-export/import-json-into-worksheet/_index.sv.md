---
title: "Importera JSON-data till Excel"
second_title: "Dokument"
linktitle: "Importera JSON"
type: docs
url: /sv/import-json-data-into-excel/
aliases: [  /sv/import/json/ ]
keywords: "Aspose.Cells Cloud, JSON-import, Excel-API, REST-import av JSON, SDK-exempel"
description: "Lär dig hur du importerar JSON-data till ett Excel-ark med Aspose.Cells Cloud REST API. Innehåller detaljerade endpoint-uppgifter, exempel på förfrågan/svar och SDK-kod för .NET, Java och Python."
weight: 40
---

Denna REST API **importerar JSON-data** till ett Excel-ark.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/importjson
```
### **Säkerhet och autentisering**

Aspose.Cells Cloud-API:er är säkra och kräver <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-tokenbaserad autentisering</a>.

### **Förfrågningsparametrar**

| Parameternamn         | Plats        | Typ    | Beskrivning                                                                                          |
| --------------------- | ------------ | ------ | ---------------------------------------------------------------------------------------------------- |
| name                  | Sökväg       | sträng | Namnet på arbetsbokens fil.                                                                          |
| importJsonRequest     | HTTP-nyttja  | klass  | Begäran som innehåller information om JSON-importen.                                                |
| password              | Frågesträng  | sträng | Lösenord för att öppna arbetsboken (om den är skyddad).                                              |
| folder                | Frågesträng  | sträng | Mappen som innehåller den ursprungliga arbetsboken.                                                  |
| storageName           | Frågesträng  | sträng | Namnet på lagringen där arbetsboken finns.                                                          |
| outPath               | Frågesträng  | sträng | Sökväg för utdatafilen efter import. Om den utelämnas returneras den uppdaterade arbetsboken i svaret. |
| outStorageName        | Frågesträng  | sträng | Lagringsnamn för utdatafilen.                                                                        |
| checkExcelRestriction | Frågesträng  | sträng | Flagga som anger om Excel-specifika restriktioner ska tillämpas (true/false).                        |

### **Exempel på begäran**

```json
{
  "JsonFileSource": {
    "FilePath": "string"
  },
  "ImportPosition": {
    "SheetName": "string",
    "RowIndex": 0,
    "ColumnIndex": 0
  },
  "JsonContent": "string"
}
```

### Svar

En lyckad begäran returnerar **HTTP 200** med ett JSON-svar enligt:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Möjliga statuskoder:

| Kod | Betydelse                               |
| --- | --------------------------------------- |
| 200 | Importen lyckades                       |
| 400 | Felaktig begäran – saknad eller ogiltig data |
| 401 | Autentisering krävs – ogiltig eller saknad token |
| 500 | Internt serverfel                       |


## Hur du använder PostWorkbookImportJson-API:et med SDK:er

### PostWorkbookImportJson API-specifikation

[OpenAPI-specifikationen](https://reference.aspose.cloud/cells/#/DataProcessing/PostWorkbookImportJson) definierar ett offentligt tillgängligt programmeringsgränssnitt och gör att du kan utföra REST-interaktioner direkt från en webbläsare.

### Använd Aspose.Cells Cloud SDK:er

Att använda en SDK är det mest effektiva sättet att påskynda utvecklingen. SDK:er hanterar detaljer på lågnivå, så att du kan fokusera på din affärslogik. För en komplett lista över Aspose.Cells Cloud SDK:er, besök [GitHub-förrådet](https://github.com/aspose-cells-cloud).

Följande kodexempel visar hur man anropar Aspose.Cells-webbtjänster med olika SDK:er:

---