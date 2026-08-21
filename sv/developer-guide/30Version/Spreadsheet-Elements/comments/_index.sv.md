---
title: "Arbeta med Excel-kommentarer"
second_title: "Dokument"
linktitle: "Kommentarer"
type: docs
url: /sv/comments/
aliases: [/sv/working-with-comments/]
keywords: "Aspose.Cells Cloud, Excel-kommentar-API, kalkylarkskommentarer, REST-API"
description: "Lär dig hur du lägger till, hämtar, uppdaterar och tar bort Excel-kommentarer med Aspose.Cells Cloud REST API v3.0, inklusive kodexempel, förutsättningar och felhantering."
weight: 100
ArticleTitle: "Arbeta med Excel-kommentarer – Aspose.Cells Cloud API-guide"
---

När du skapar en Excel-arbetsbok kan användare lägga till kommentarer av olika skäl. Ett vanligt användningsområde är att förklara en formel i en cell, särskilt om filen kommer att delas med andra. Kommentarer kan också fungera som påminnelser, anteckningar för samarbetspartners eller som ett medel för att hänvisa till andra arbetsböcker. När en kommentar har lagts till tillåter Excel användarna att ändra storlek, form och format på kommentarboxen så att den passar deras önskade stil. Att mastera hantering av kommentarer hjälper användare att få ut det mesta av denna funktion.

**Förutsättningar**

- Ett aktivt Aspose.Cells Cloud-konto.  
- En giltig **åtkomsttoken** som erhållits via OAuth 2.0.  
- API-version **v3.0** (de slutpunkter som används i den här guiden tillhör denna version).  
- Valfritt: Aspose.Cells SDK för ditt föredragna programspråk för att förenkla skapandet av förfrågningar.

**Version**

Exemplen nedan riktas till **Aspose.Cells Cloud REST API v3.0**. Kommande API-utgåvor kan införa ytterligare parametrar eller ändra svarsstrukturer; konsultera alltid den senaste API-referensen för uppdaterade detaljer.

**Lägg till en kommentar**

För att lägga till en kommentar, skicka en **POST**-förfrågan till följande slutpunkt:

```
POST https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments
Authorization: Bearer {access_token}
Content-Type: application/json
```

**Sökvägsparametrar**

| Parameter | Typ    | Obligatorisk | Beskrivning                                |
|-----------|--------|--------------|--------------------------------------------|
| `file`    | string | Ja           | Namn på arbetsboksfilen (inklusive tillägg). |
| `sheet`   | string | Ja           | Kalkylbladsnamn där kommentaren ska läggas till. |

**Schemat för begärandetexten**

| Fält      | Typ    | Obligatorisk | Beskrivning                               |
|-----------|--------|--------------|-------------------------------------------|
| `CellName`| string | Ja           | Adress i A1-stil för cellen (t.ex. **B2**). |
| `Comment` | string | Ja           | Kommentartext som ska lagras.             |
| `Author`  | string | Nej          | Namn på kommentarens författare.          |

**Exempel på begärandetext**

```json
{
  "CellName": "B2",
  "Comment": "Granskning behövs",
  "Author": "John Doe"
}
```

**Exempel på lyckad svarsåterställning** (`200 OK`)

```json
{
  "Code": 200,
  "Status": "OK",
  "Comment": {
    "CellName": "B2",
    "Author": "John Doe",
    "HtmlComment": "Granskning behövs",
    "Note": "Granskning behövs"
  }
}
```

**Vanliga felkoder**

| Kod | Betydelse                               |
|-----|-----------------------------------------|
| 400 | Ogiltig celladress eller begärandetext  |
| 401 | Auktorisering saknas – ogiltig/bristfällig token |
| 404 | Arbetsbok eller kalkylblad hittades inte |

**Hämta kommentarer**

Hämta alla kommentarer från ett kalkylblad:

```
GET https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments
Authorization: Bearer {access_token}
```

**Sökvägsparametrar**

| Parameter | Typ    | Obligatorisk | Beskrivning                     |
|-----------|--------|--------------|---------------------------------|
| `file`    | string | Ja           | Namn på arbetsboksfilen.        |
| `sheet`   | string | Ja           | Kalkylbladsnamn.                |

**Exempel på svar**

```json
{
  "Code": 200,
  "Status": "OK",
  "Comments": [
    {
      "CellName": "A1",
      "Author": "Alice",
      "HtmlComment": "Initialt värde",
      "Note": "Initialt värde"
    },
    {
      "CellName": "B2",
      "Author": "John Doe",
      "HtmlComment": "Granskning behövs",
      "Note": "Granskning behövs"
    }
  ]
}
```

**Uppdatera en kommentar**

För att ändra en befintlig kommentar, skicka en **PUT**-förfrågan. Kommentaren identifieras av dess **index** i kalkylbladets samling av kommentarer (börjar på 0).

```
PUT https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments/{commentIndex}
Authorization: Bearer {access_token}
Content-Type: application/json
```

**Sökvägsparametrar**

| Parameter      | Typ   | Obligatorisk | Beskrivning                            |
|----------------|-------|--------------|----------------------------------------|
| `file`         | string | Ja          | Namn på arbetsboksfilen.               |
| `sheet`        | string | Ja          | Kalkylbladsnamn.                       |
| `commentIndex` | int    | Ja          | Nollbaserat index för den kommentar som ska uppdateras. |

**Schemat för begärandetexten**

| Fält     | Typ    | Obligatorisk | Beskrivning                         |
|----------|--------|--------------|-------------------------------------|
| `Comment`| string | Ja           | Ny kommentartext.                   |
| `Author` | string | Nej          | Uppdaterat författarnamn (valfritt).|

**Exempel på begärandetext**

```json
{
  "Comment": "Uppdaterad text för anteckning",
  "Author": "John Doe"
}
```

Svaret följer samma struktur som svaret för **Lägg till en kommentar**.

**Ta bort en kommentar**

Ta bort en enskild kommentar med dess index:

```
DELETE https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments/{commentIndex}
Authorization: Bearer {access_token}
```

**Sökvägsparametrar**

| Parameter      | Typ   | Obligatorisk | Beskrivning                            |
|----------------|-------|--------------|----------------------------------------|
| `file`         | string | Ja          | Namn på arbetsboksfilen.               |
| `sheet`        | string | Ja          | Kalkylbladsnamn.                       |
| `commentIndex` | int    | Ja          | Nollbaserat index för den kommentar som ska tas bort. |

Ett lyckat borttagningssvar returnerar:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Ta bort alla kommentarer**

För att rensa alla kommentarer från ett kalkylblad:

```
DELETE https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments
Authorization: Bearer {access_token}
```

**Sökvägsparametrar**

| Parameter | Typ    | Obligatorisk | Beskrivning                     |
|-----------|--------|--------------|---------------------------------|
| `file`    | string | Ja           | Namn på arbetsboksfilen.        |
| `sheet`   | string | Ja           | Kalkylbladsnamn.                |

**Riktlinjer för felhantering**

- **404 Not Found** – Kontrollera att arbetsbokens ID, kalkylbladsnamn och kommentarsindex är korrekta.  
- **400 Bad Request** – Kontrollera JSON-syntaxen och obligatoriska fält (`CellName`, `Comment`).  
- **429 Too Many Requests** – Implementera exponentiell backoff och respektera `Retry-After`-headern.

**Sammanfattning**

- Excel-kommentarer används för att [lägga till en anteckning eller förklara en formel i en cell](/sv/comments/add/).  
- Excel ger användarna flexibiliteten att [redigera](/sv/comments/update/), [ta bort](/sv/comments/delete/) och [visa](/sv/comments/get/) eller [dölja](/sv/comments/update/) kommentarer i ett kalkylblad.  
- Användare kan också [ändra storlek](/sv/comments/update/) och [flytta](/sv/comments/update/) på kommentarboxen.  

För mer information om arbetet med andra kalkylarksobjekt, se guiden om [arbeta med celler](/sv/working-with-cells/).