---
---
title: "Arbeta med borttagning av rader i ett Excel-ark"
second_title: "Document"
linktitle: "Ta bort"
type: docs
url: /sv/rows/delete/
keywords: "Aspose.Cells, ta bort rad, Excel API, REST, moln, kalkylark, Excel, SDK"
description: "Lär dig hur du tar bort en eller flera rader i ett Excel-ark med Aspose.Cells Cloud REST API. Innehåller kodexempel för Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby och Swift."
weight: 20
ArticleTitle: "Arbeta med borttagning av rader i ett Excel-ark – Aspose.Cells Cloud API-guide"
---

## tillgängliga borttagningsoperationer

Följande exempel visar hur du tar bort en enskild tom rad eller flera rader från ett Excel-ark med Aspose.Cells Cloud REST API.

- [Hur man tar bort en tom rad i ett Excel-ark](/sv/cells/rows/delete/row/)
- [Hur man tar bort flera rader i ett Excel-ark](/sv/cells/rows/delete/rows/)

**API-referens**

| Objekt                | Detaljer |
|---------------------|---------------------------------------------------------------|
| **HTTP-metod**     | DELETE |
| **Endpoint**        | `/cells/{fileName}/worksheets/{sheetName}/rows` |
| **Sökvägsparametrar**| `fileName` – namn på Excel-filen (obligatoriskt)<br>`sheetName` – namn på kalkylarket (obligatoriskt) |
| **Frågeparametrar**| `startrow` – index för den första rad som ska tas bort (obligatoriskt)<br>`totalRows` – antal rader som ska tas bort (obligatoriskt)<br>`storage` – namn på molnlagring (valfritt)<br>`folder` – mappsökväg i lagring (valfritt) |
| **Förfrågningsbrödtext**    | *Ingen* |
| **Exempel på svar**| ```json<br>{<br>  "Code": 200,<br>  "Status": "OK",<br>  "RowsDeleted": 1<br>}<br>``` |
| **Möjliga statuskoder**| 200 OK – rader har tagits bort utan problem<br>400 Bad Request – ogiltiga parametrar<br>401 Unauthorized – autentisering misslyckades<br>404 Not Found – fil eller kalkylark hittades inte<br>500 Internal Server Error – serverproblem |

**Se även**

- [Lägg till rad](/sv/cells/rows/add/)
- [Hämta rad](/sv/cells/rows/get/)
- [Kopiera rad](/sv/cells/rows/copy/)
- [Dölj rad](/sv/cells/rows/hide/)
- [Översikt över rader](/sv/cells/rows/)
---