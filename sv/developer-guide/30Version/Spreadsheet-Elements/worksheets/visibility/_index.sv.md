---
title: "Hur man arbetar med synlighet i ett Excel-arbetsblad"
second_title: "Dokument"
linktitle: "Synlighet"
type: docs
url: /sv/worksheets/panes/
keywords: "Aspose.Cells Cloud, API för att dölja arbetsblad, API för att visa arbetsblad igen, synlighet för Excel-arbetsblad, REST API för Excel, Aspose.Cells v3.0"
description: "Lär dig hur du döljer eller visar Excel-arbetsblad programmatiskt med Aspose.Cells Cloud REST API. Inkluderar begärande-URL:er, exempel med cURL och .NET SDK, felhantering och versionsspecifika noteringar."
weight: 20
---

## Arbeta med synlighet i ett Excel-arbetsblad

*Arbetsbladssynlighet* avgör om ett ark visas för slutanvändaren. Med Aspose.Cells Cloud kan du dölja eller visa ett arbetsblad igen via ett enkelt REST-anrop. De använda API-slutpunkterna är:

* **Dölj ett arbetsblad** – `PUT /cells/{fileName}/worksheets/{sheetName}/visibility`  
* **Visa ett arbetsblad igen** – `PUT /cells/{fileName}/worksheets/{sheetName}/visibility`

> **Stödd API-version:** **v3.0** (från och med mars 2026)

### Förutsättningar
1. Ett aktivt **Aspose.Cells Cloud**-konto.  
2. Ett giltigt **klient-ID** och **klienthemlighet** (eller OAuth 2.0-åtkomsttoken).  
3. Arbetsboken (`{fileName}`) måste redan vara uppladdad till Aspose molnlagring.  

---

## Dölj ett arbetsblad

### Begäran
```http
PUT https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/visibility
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "Visible": false
}
```

### Svar
```json
{
  "Code": 200,
  "Status": "OK",
  "Worksheet": {
    "Name": "{sheetName}",
    "Index": 2,
    "Visible": false
  }
}
```

### Exempel med cURL
```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet2/visibility" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json" \
     -d '{ "Visible": false }'
```

### Exempel med .NET SDK
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new Visibility { Visible = false };
var response = api.PutWorksheetVisibility("MyWorkbook.xlsx", "Sheet2", request);
Console.WriteLine($"Arbetsblad dolt: {response.Worksheet.Visible}");
```

### Vanliga fel
| HTTP-kod | Beskrivning                              | Åtgärd                                                    |
|----------|------------------------------------------|-----------------------------------------------------------|
| 400      | Ogiltig JSON-kropp eller saknar `Visible` | Se till att begärandetexten är giltig JSON med nyckeln.  |
| 401      | Auktorisering misslyckades – token saknas eller har gått ut | Uppdatera OAuth-token och inkludera den i headern.       |
| 404      | Ark eller fil hittades inte              | Kontrollera att `{fileName}` och `{sheetName}` är korrekta. |
| 409      | Arket redan dolt                         | Kontrollera nuvarande synlighet innan du skickar begäran. |

---

## Visa ett arbetsblad igen

### Begäran
```http
PUT https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/visibility
Authorization: Bearer {access_token}
Content-Type: application/json

{
  "Visible": true
}
```

### Svar
```json
{
  "Code": 200,
  "Status": "OK",
  "Worksheet": {
    "Name": "{sheetName}",
    "Index": 2,
    "Visible": true
  }
}
```

### Exempel med cURL
```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/MyWorkbook.xlsx/worksheets/Sheet2/visibility" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Content-Type: application/json" \
     -d '{ "Visible": true }'
```

### Exempel med .NET SDK
```csharp
var api = new CellsApi("client_id", "client_secret");
var request = new Visibility { Visible = true };
var response = api.PutWorksheetVisibility("MyWorkbook.xlsx", "Sheet2", request);
Console.WriteLine($"Arbetsblad synligt: {response.Worksheet.Visible}");
```

### Vanliga fel
| HTTP-kod | Beskrivning                              | Åtgärd                                                    |
|----------|------------------------------------------|-----------------------------------------------------------|
| 400      | Ogiltig JSON-kropp eller saknar `Visible` | Skicka en korrekt JSON-payload med `"Visible": true`.    |
| 401      | Auktorisering misslyckades – token saknas eller har gått ut | Återskapa åtkomsttoken och försök igen.                   |
| 404      | Ark eller fil hittades inte              | Bekräfta att filen och arkets namn finns i lagringen.    |
| 409      | Arket redan synligt                     | Ingen åtgärd behövs; arbetet är redan synligt.            |

---

## Relaterade åtgärder
> *Frys rutor* | *Dela rutor* | *Zooma* – se motsvarande sidor för ytterligare kontroller för layout av arbetsblad.

---

## Vanliga frågor

<dl>
  <dt>Hur döljer jag ett arbetsblad med Aspose.Cells Cloud API?</dt>
  <dd>Skicka ett `PUT`-anrop till `/cells/{fileName}/worksheets/{sheetName}/visibility` med JSON-innehållet `{ "Visible": false }`. Inkludera en giltig OAuth 2.0-bearer-token. Ett `200 OK`-svar returnerar det uppdaterade arbetsbladsobjektet.</dd>

  <dt>Vad får jag för svar när jag visar ett arbetsblad igen?</dt>
  <dd>API:et returnerar `200 OK` med ett svarsinnehåll som innehåller arbetsbladsobjektet där `"Visible": true`. Svaret innehåller arbetsbladets `Name`, `Index` och `Visible`-egenskaper.</dd>

  <dt>Kan jag dölja flera arbetsblad i ett enda anrop?</dt>
  <dd>Nej. Synlighetsändpunkten fungerar på ett enskilt arbetsblad som identifieras av `{sheetName}`. För att dölja flera ark ska du iterera över varje namn i din klientkod.</dd>
</dl>

---

*Skrivet av Aspose Docs-teamet – över 15 års erfarenhet av att automatisera Excel-arbetsflöden.*