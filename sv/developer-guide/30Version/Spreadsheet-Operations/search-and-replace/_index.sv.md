---
title: "Sök och ersätt textinnehåll i Excel-filer"
second_title: "Dokumentation"
linktitle: "Sök och ersätt"
type: docs
url: /sv/search-and-replace/
aliases: [/sv/working-with-text/, /sv/text/]
description: "Lär dig hur du söker och ersätter text i Excel-arbetsböcker och -arbetsblad med Aspose.Cells Cloud REST API. Inkluderar begäranformat, exempelkod för .NET, Java, Python samt felhantering."
keywords: "Aspose.Cells Cloud, Excel, sök och ersätt, REST API, .NET, Java, Python"
weight: 20
ArticleTitle: "Sök och ersätt text i Excel-filer med Aspose.Cells Cloud API"
---

Textåtgärder är komplexa processer för Excel-filer. Många faktorer bidrar till denna komplexitet och bör beaktas vid bearbetning. Aspose.Cells Cloud tillhandahåller ett pålitligt sätt att söka efter och ersätta text i ett stort antal kalkylarksfiler.

Arbete med text i Excel-arbetsböcker kräver ofta att man hittar specifika strängar och uppdaterar dem på flera arbetsblad. Aspose.Cells Cloud API förenklar denna uppgift genom att tillhandahålla en enhetlig **sök- och ersätt**-åtgärd som fungerar med alla format som stöds av Aspose.Cells Cloud.

## Översikt

Sök och ersätt låter dig hitta specifika strängar i en arbetsbok eller ett visst arbetsblad och ersätta dem med nya värden. Åtgärden fungerar med alla format som stöds av Aspose.Cells Cloud, såsom **XLS, XLSX, XLSM, XLSB, ODS, CSV** och andra. Med **sök- och ersätt**-funktionen kan du snabbt städa upp data, korrigera upprepade stavfel eller tillämpa bulknamngivningskonventioner i hela en arbetsbok.

## Förutsättningar

- Ett aktivt Aspose.Cloud-konto med giltigt **Client‑Id** och **Client‑Secret**.
- Åtkomsttoken erhållen via OAuth 2.0-autentiseringsflödet.
- Målarbetsboken måste lagras i Aspose Cloud-lagring eller vara tillgänglig via en offentlig URL.
- Nödvändigt SDK installerat (t.ex. Aspose.Cells‑Cloud för .NET, Java eller Python).

## API-referens

**Metod:** `POST`  
**Endpoint**

```
POST https://api.aspose.cloud/v3.0/cells/{fileName}/searchreplace
```

| Parameter        | Typ     | Nödvändig | Beskrivning                                                                      |
| ---------------- | ------- | --------- | -------------------------------------------------------------------------------- |
| `fileName`       | string  | Ja        | Namn på arbetsboken (inklusive tillägg).                                        |
| `folder`         | string  | Nej       | Mappväg i molnlagring.                                                          |
| `storage`        | string  | Nej       | Lagringsnamn om det inte är standard.                                            |
| `sheetName`      | string  | Nej       | Specifikt arbetsbladsnamn; om utelämnas appliceras åtgärden på hela arbetsboken. |
| `searchString`   | string  | Ja        | Text att söka efter.                                                             |
| `replaceString`  | string  | Ja        | Text att ersätta hittade förekomster med.                                       |
| `ignoreCase`     | boolean | Nej       | Ställ in till `true` för att utföra skiftlägesokänslig sökning.                 |
| `matchWholeCell` | boolean | Nej       | Ställ in till `true` för att endast ersätta helcellmatchningar.                 |

**Headers**

- `Authorization: Bearer {access_token}`
- `Content-Type: application/json`

**Request Body (JSON)**

```json
{
  "searchString": "OldValue",
  "replaceString": "NewValue",
  "ignoreCase": false,
  "matchWholeCell": false,
  "sheetName": "Sheet1"
}
```

**Lyckad svar (JSON)**

```json
{
  "status": "OK",
  "replacedCount": 3,
  "updatedFileUrl": "https://api.aspose.cloud/v3.0/storage/file/updatedWorkbook.xlsx"
}
```

## Format som stöds

| Format                      | Filändelse                |
| --------------------------- | ------------------------- |
| Excel-arbetsbok             | .xls, .xlsx, .xlsm, .xlsb |
| OpenDocument-kalkylark      | .ods                      |
| CSV                         | .csv                      |
| Övriga (som stöds av Aspose.Cells) | —                         |

## Kodexempel

Nedan finns minimala exempel för tre populära SDK:er. Ersätt `{clientId}`, `{clientSecret}` och andra platshållare med dina faktiska värden. Dessa exempel visar hur man utför en **sök- och ersätt**-åtgärd programmässigt.

## Felhantering och gränssnittsfall

| HTTP-kod | Betydelse                                         | Rekommenderad åtgärd                                                 |
| -------- | ------------------------------------------------- | -------------------------------------------------------------------- |
| 400      | Felaktig begäran – saknade eller ogiltiga parametrar | Kontrollera nödvändiga fält och datatyper.                          |
| 401      | Auktorisering misslyckades – ogiltig eller utgången token | Uppdatera åtkomsttoken.                                             |
| 404      | Hittades inte – arbetsbok eller arbetsblad finns inte | Kontrollera filnamn, mappväg och `sheetName`.                       |
| 415      | Formatet stöds inte – ogiltigt filformat          | Se till att den uppladdade filen är i ett stöds Excel- eller CSV-format. |
| 202      | Godkänd – begäran accepterad för bearbetning      | Fråga efter åtgärdens status om asynkron bearbetning används.       |
| 204      | Inget innehåll – åtgärden lyckades utan svarsbody | Ersättningen tillämpades; inga ytterligare data returnerades.      |
| 500      | Internt serverfel – oväntat fel                    | Försök igen efter en kort fördröjning; kontakta Aspose-stöd om felet kvarstår. |

**Anteckningar:**  
- Stora arbetsböcker kan överskrida gränsen för begärandestorlek; överväg att först ladda upp filen till molnlagring.  
- När `ignoreCase` är inställt på `true` bör du vara medveten om att lokalberoende skiftlägessättning kan påverka resultaten.  
- Om `matchWholeCell` används med formler ersätts inte delmatchningar i formeltexten.

## Sök och ersätt i Excel-filer

- [Hur man får textobjekt från en Excel-arbetsbok.](/sv/cells/workbook/get-text-items/)
- [Hur man får textobjekt från ett Excel-arbetsblad.](/sv/cells/worksheets/get-text-items/)
- [Hur man hittar text från en Excel-arbetsbok.](/sv/cells/workbook/find-text/)
- [Hur man hittar text från ett Excel-arbetsblad.](/sv/cells/worksheets/find-text/)
- [Hur man hittar text från Excel-filer utan att ladda upp en fil.](/sv/cells/search/)
- [Hur man ersätter text från en Excel-arbetsbok.](/sv/cells/workbook/replace-text/)
- [Hur man ersätter text från ett Excel-arbetsblad.](/sv/cells/worksheets/replace-text/)
- [Hur man ersätter text från Excel-filer utan att ladda upp en fil.](/sv/cells/replace/)

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Sök och ersätt text i Excel-filer med Aspose.Cells Cloud API",
  "description": "Dokumentation för sök- och ersätt-endpoint i Aspose.Cells Cloud, inklusive begäranformat, parametrar, exempel och felhantering.",
  "url": "https://docs.aspose.cloud/cells/sv/search-and-replace/",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2026-07-30",
  "keywords": "Aspose.Cells Cloud, Excel, sök och ersätt, API, REST"
}
</script>