---
title: "Arbeta med Excel-OLE-objekt"
second_title: "Dokument"
linktitle: "OleObjects"
type: docs
url: /oleobjects/
aliases: [/working-with-oleobjects/]
keywords: "OLE, Excel, Aspose.Cells, API, moln"
description: "Använd Aspose.Cells Cloud REST API för att hämta, lägga till, uppdatera, ta bort och konvertera OLE-objekt i Excel-arbetsblad. SDK:er finns för Java, .NET, Python, PHP, Ruby, Go, Node.js, Perl, Swift och Android."
weight: 100
ArticleTitle: "Arbeta med Excel-OLE-objekt – Guide för att hämta, lägga till, uppdatera, ta bort och konvertera OLE-objekt"
---

**Så här arbetar du med OLE-objekt i ett Excel-arbetsblad**

Aspose.Cells Cloud REST API erbjuder en komplett uppsättning åtgärder för att hantera OLE-objekt programmatiskt. Nedan finns en kompakt referens för varje åtgärd, inklusive HTTP-metod, slutpunktsmönster, nödvändiga parametrar och ett exempel på respons.

- [Hur man hämtar ett OLE-objekt från ett Excel-arbetsblad](/cells/oleobjects/get/)
  - **Metod:** `GET`  
  - **Slutpunkt:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **Parametrar:** `fileName` (sträng), `sheetName` (sträng), `oleObjectIndex` (heltal)  
  - **Exempel på respons:**  
    ```json
    {
      "OleObject": {
        "Name": "Chart1",
        "ContentType": "image/png",
        "Width": 400,
        "Height": 300
      }
    }
    ```

- [Hur man lägger till ett OLE-objekt i ett Excel-arbetsblad](/cells/oleobjects/add/)
  - **Metod:** `POST`  
  - **Slutpunkt:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects`  
  - **Parametrar:** `fileName`, `sheetName`, `oleObject` (binär eller base64-kodad), `imageFormat` (valfritt)  
  - **Exempel på begärandetext:** multipart/form-data med filströmmen.  
  - **Exempel på respons:** `201 Created` med platsheader för det nya OLE-objektet.

- [Hur man uppdaterar ett specifikt OLE-objekt i ett Excel-arbetsblad](/cells/oleobjects/update/)
  - **Metod:** `PUT`  
  - **Slutpunkt:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **Parametrar:** `fileName`, `sheetName`, `oleObjectIndex`, `oleObject` (uppdaterat innehåll)  
  - **Exempel på respons:** `200 OK` med metadata för det uppdaterade objektet.

- [Hur man konverterar ett OLE-objekt till en bild i ett Excel-arbetsblad](/cells/oleobjects/convert/)
  - **Metod:** `GET`  
  - **Slutpunkt:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}/convert`  
  - **Parametrar:** `fileName`, `sheetName`, `oleObjectIndex`, `format` (t.ex. `png`, `jpeg`)  
  - **Exempel på respons:** Binär bildström för det konverterade OLE-objektet.

- [Hur man tar bort alla OLE-objekt i ett Excel-arbetsblad](/cells/oleobjects/clear/)
  - **Metod:** `DELETE`  
  - **Slutpunkt:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects`  
  - **Parametrar:** `fileName`, `sheetName`  
  - **Exempel på respons:** `204 No Content` vilket indikerar att alla OLE-objekt har tagits bort.

- [Hur man tar bort ett specifikt OLE-objekt i ett Excel-arbetsblad](/cells/oleobjects/delete/)
  - **Metod:** `DELETE`  
  - **Slutpunkt:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **Parametrar:** `fileName`, `sheetName`, `oleObjectIndex`  
  - **Exempel på respons:** `204 No Content` vilket bekräftar att objektet har tagits bort.