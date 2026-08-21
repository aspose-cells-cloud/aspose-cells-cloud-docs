---
title: "Filinformation"
second_title: "Dokument"
linktitle: "Filinformation"
type: docs
url: /sv/file-info/
keywords: "Fil, information, Excel, Aspose.Cells, molntjänst, metadata, Base64"
description: "Hämta Excel-filnamn, storlek och Base64-innehåll med Aspose.Cells molntjänst. Inkluderar begärsyntax, exempelkod och felhantering."
weight: 79
ArticleTitle: "Filinformation – Excel-filmetadata och Base64-innehåll (Aspose.Cells molntjänst)"
---

## Egenskaper för filinformation


| Namn            | Typ    | Beskrivning                                              |
| --------------- | ------ | -------------------------------------------------------- |
| **FileName**    | string | Filens namn, inklusive dess tillägg.                     |
| **FileSize**    | long   | Filens storlek i byte.                                   |
| **FileContent** | string | Innehåller den råa Excel-filens data, kodad i Base64.   |

Svaret returneras som JSON med samma tre egenskaper som visas i tabellen ovan, till exempel:

```json
{
  "FileName": "MyWorkbook.xlsx",
  "FileSize": 254312,
  "FileContent": "UEsDBBQABgAIAAAAIQD..."
}
```

### Fel

| HTTP-kod | Betydelse                | När det inträffar                              |
| -------- | ------------------------ | --------------------------------------------- |
| 200      | OK – begäran lyckades.   | Normalt svar.                                 |
| 401      | Obehörig                 | Saknas eller ogiltig autentiserings-token.    |
| 404      | Hittades inte            | Den angivna filen finns inte.                 |
| 500      | Internt serverfel        | Oväntat fel på serversidan.                   |

För varje fel, se till att autentiserings-token är giltig (401), verifiera filsökvägen (404) eller konsultera den allmänna guiden för felhantering för återförsöksstrategier (500).

## Se även

- [Hämta arbetsbok](https://docs.aspose.cloud/cells/get-workbook) – hämta ett arbetsboksobjekt och dess kalkylblad.  
- [Ladda ner fil](https://docs.aspose.cloud/cells/download-file) – ladda ner råa filbyte utan Base64-kodning.  
- [Översikt över autentisering](https://docs.aspose.cloud/cells/authentication) – hur du erhåller och använder åtkomsttoken.  
---