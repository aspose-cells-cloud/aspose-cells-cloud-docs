---
title: "Arbeta med Excel-bilder"
second_title: "Dokument"
linktitle: "Bilder"
type: docs
url: /sv/pictures/
aliases: [  /sv/working-with-pictures/ ]
keywords: "Excel, bild, Aspose.Cells Cloud, REST API, bildhantering, Excel-bilder"
description: "Lär dig hur du hämtar, lägger till, uppdaterar och raderar bilder i Excel-ark med Aspose.Cells Cloud REST API. Inkluderar kodexempel för C#, Java, Python och mer."
weight: 100
ArticleTitle: "Arbeta med Excel-bilder – Aspose.Cells Cloud-dokumentation"
---

## Arbeta med bilder i en Excel-fil

Den här guiden förklarar hur du arbetar med **bilder** (även kallade bilder) i Excel-ark via Aspose.Cells Cloud REST API. Den täcker de viktigaste bildrelaterade åtgärderna – att hämta, lägga till, uppdatera och radera Excel-bilder – och pekar på detaljerade exempel för varje uppgift.

**Förutsättningar**: ett Aspose.Cells Cloud-konto, en giltig API-nyckel och det lämpliga SDK:t installerat för din valda programmeringsspråk.

- [Hämta en bild i ett specifikt format från ett Excel-ark.](/sv/cells/pictures/get/) – Hämta en enskild bild i det begärda formatet (PNG, JPEG, etc.) från ett ark.  
- [Hämta all bildinformation från ett Excel-ark.](/sv/cells/pictures/get-all/) | Lista metadata för alla bilder i ett ark.  
- [Lägg till en bild i ett Excel-ark.](/sv/cells/pictures/add/) – Infoga en ny bild i ett ark och ange dess position och storlek.  
- [Uppdatera en specifik bild i ett Excel-ark.](/sv/cells/pictures/update/) – Ändra egenskaperna (t.ex. dimensioner, placering) för en befintlig bild.  
- [Radera alla bilder från ett Excel-ark.](/sv/cells/pictures/clear/) – Ta bort alla bildobjekt från ett ark med ett enda anrop.  
- [Radera en bild från ett Excel-ark.](/sv/cells/pictures/delete/) – Radera en enskild bild identifierad med dess index.  

**API-referens**

**Hämta en bild i ett specifikt format**  

| HTTP-metod | Endpoint | Nödvändiga parametrar | Exempel på begäran | Exempel på svar | Statuskoder |
|-------------|----------|---------------------|----------------|----------------|--------------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName` (sökväg), `sheetName` (sökväg), `pictureIndex` (sökväg), `format` (frågeparameter) | `GET https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures/0?format=png` | Binär bilddata (PNG, JPEG, etc.) | 200 OK, 400 Ogiltig begäran, 401 Auktorisering krävs, 404 Hittades inte, 500 Serverfel |

**Hämta all bildinformation**  

| HTTP-metod | Endpoint | Nödvändiga parametrar | Exempel på begäran | Exempel på svar | Statuskoder |
|-------------|----------|---------------------|----------------|----------------|--------------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName` (sökväg), `sheetName` (sökväg) | `GET https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures` | JSON-array med bildmetadata (index, namn, position, storlek) | 200 OK, 400, 401, 404, 500 |

**Lägg till en bild**  

| HTTP-metod | Endpoint | Nödvändiga parametrar | Exempel på begärans kropp | Exempel på svar | Statuskoder |
|-------------|----------|---------------------|---------------------|----------------|--------------|
| POST | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName` (sökväg), `sheetName` (sökväg) | `{ "image": "<base64-kodad-bild>", "upperLeftRow": 5, "upperLeftColumn": 2, "width": 200, "height": 150 }` | `{ "code": 200, "status": "OK", "pictureIndex": 3 }` | 201 Skapades, 400, 401, 404, 500 |

**Uppdatera en bild**  

| HTTP-metod | Endpoint | Nödvändiga parametrar | Exempel på begärans kropp | Exempel på svar | Statuskoder |
|-------------|----------|---------------------|---------------------|----------------|--------------|
| PUT | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName` (sökväg), `sheetName` (sökväg), `pictureIndex` (sökväg) | `{ "upperLeftRow": 10, "upperLeftColumn": 4, "width": 300, "height": 250 }` | `{ "code": 200, "status": "OK" }` | 200 OK, 400, 401, 404, 500 |

**Radera alla bilder**  

| HTTP-metod | Endpoint | Nödvändiga parametrar | Exempel på begäran | Exempel på svar | Statuskoder |
|-------------|----------|---------------------|----------------|----------------|--------------|
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName` (sökväg), `sheetName` (sökväg) | `DELETE https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures` | `{ "code": 200, "status": "Alla bilder raderade." }` | 200 OK, 400, 401, 404, 500 |

**Radera en specifik bild**  

| HTTP-metod | Endpoint | Nödvändiga parametrar | Exempel på begäran | Exempel på svar | Statuskoder |
|-------------|----------|---------------------|----------------|----------------|--------------|
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName` (sökväg), `sheetName` (sökväg), `pictureIndex` (sökväg) | `DELETE https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures/2` | `{ "code": 200, "status": "Bild raderad." }` | 200 OK, 400, 401, 404, 500 |

**Relaterade ämnen**

Utforska andra bildrelaterade åtgärder i Aspose.Cells Cloud:  
- [Arbeta med former](/sv/cells/shapes/) – lägg till, redigera och radera ritningsformer.  
- [Arbeta med diagram](/sv/cells/charts/) – skapa och manipulera diagramobjekt.  
- [Arbeta med bilder i ark](/sv/cells/images/) – bädda in och hantera råa bildfiler.

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Arbeta med Excel-bilder – Aspose.Cells Cloud-dokumentation",
  "description": "Guide för att hämta, lägga till, uppdatera och radera Excel-bilder via Aspose.Cells Cloud REST API.",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Aspose",
    "logo": {
      "@type": "ImageObject",
      "url": "https://cms.admin.containerize.com/templates/asposecloud/images/logo.png"
    }
  },
  "datePublished": "2026-07-30",
  "keywords": "Excel-bilder, Aspose.Cells Cloud, REST API, bildhantering",
  "url": "https://docs.aspose.cloud/cells/pictures/"
}
</script>