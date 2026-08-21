---
title: "Lägg till eller ta bort bakgrundsbild i kalkylblad – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Bakgrund"
type: docs
url: /sv/worksheets/background/
keywords: "Aspose.Cells Cloud, kalkylbladsbakgrund, Excel-API, lägg till bakgrundsbild, ta bort kalkylbladsbakgrund, SDK-exempel"
description: "Lär dig hur du lägger till eller tar bort en bakgrundsbild i ett Excel-kalkylblad med Aspose.Cells Cloud REST API. Inkluderar begärsyntax, SDK-exempel för Java, .NET, Python, PHP samt felhantering."
weight: 20
ArticleTitle: "Lägg till eller ta bort bakgrundsbild i kalkylblad med Aspose.Cells Cloud API"
---

## Arbeta med bakgrund i ett Excel-kalkylblad

**Översikt:** En kalkylbladsbakgrund är en bild som visas bakom cellerna i ett kalkylblad, vilket är användbart för märkning eller visuella ledtrådar. Aspose.Cells Cloud API låter dig lägga till eller ta bort denna bakgrundsbild programmatiskt.

**Förutsättningar:**  
- Giltig Aspose.Cells Cloud-åtkomsttoken (OAuth 2.0).  
- En Excel-arbetsbok lagrad i molnet.  
- En bildfil (PNG, JPEG, BMP) som ska användas som bakgrund.

- **Lägg till bakgrund** – Ställ in en bakgrundsbild på ett kalkylblad. Se den detaljerade guiden [Hur man ställer in bakgrund i ett Excel-kalkylblad](/cells/worksheets/background/add/).  
- **Ta bort bakgrund** – Ta bort en befintlig bakgrundsbild från ett kalkylblad. Se den detaljerade guiden [Hur man tar bort bakgrund i ett Excel-kalkylblad](/cells/worksheets/background/delete/).

Att använda en kalkylbladsbakgrund kan förbättra märkning, lyfta fram viktiga delar eller tillhandahålla visuella ledtrådar för slutanvändare. Aspose.Cells Cloud API gör det enkelt att ställa in eller rensa denna bakgrundsbild direkt från din applikation.

### API-referens

| Åtgärd | HTTP-metod | Endpoint | Path-parametrar | Begärandetext | Lyckad svarskod |
|--------|------------|----------|----------------|---------------|-----------------|
| Lägg till bakgrund | PUT | `/cells/{name}/worksheets/{sheetName}/background` | `name` – arbetsbokens filnamn<br>`sheetName` – målkalkylbladet | Bildfil (PNG, JPEG, BMP) som multipart/form‑data | `200 OK` – bakgrund tillagd |
| Ta bort bakgrund | DELETE | `/cells/{name}/worksheets/{sheetName}/background` | `name` – arbetsbokens filnamn<br>`sheetName` – målkalkylbladet | *ingen* | `200 OK` – bakgrund borttagen |

#### Exempel (Java SDK)

```java
// Lägg till en bakgrundsbild
CellsApi cellsApi = new CellsApi("client_id", "client_secret");
File image = new File("path/to/background.png");
cellsApi.putWorksheetBackground("Book1.xlsx", "Sheet1", image, null);

// Ta bort bakgrundsbilden
cellsApi.deleteWorksheetBackground("Book1.xlsx", "Sheet1", null);
```

#### Exempel (Python SDK)

```python
import asposecellscloud
api = asposecellscloud.CellsApi(client_id="DIN_KLIENT_ID", client_secret="DIN_KLIENT_HEMliga_NYCKEL")

# Lägg till bakgrund
with open("background.png", "rb") as img:
    api.put_worksheet_background("Book1.xlsx", "Sheet1", img)

# Ta bort bakgrund
api.delete_worksheet_background("Book1.xlsx", "Sheet1")
```

För ytterligare språkexempel (C#, PHP, Ruby), hänvisas till SDK-dokumentationen.

**Relaterade ämnen**  
- Läs mer om hantering av kalkylblad i allmänhet: [Översikt över kalkylblad](/cells/worksheets/).  
- Förstå hur du autentiserar med Aspose.Cells Cloud: [API-autentiseringsguide](/cells/authentication/).  
- Utforska andra kalkylbladselement såsom diagram, tabeller och formler: [Index över kalkylbladselement](/cells/elements/).
---