---
title: "Arbeiten mit Excel OLE-Objekten"
second_title: "Dokument"
linktitle: "OleObjects"
type: docs
url: /de/oleobjects/
aliases: [  /de/working-with-oleobjects/ ]
keywords: "OLE, Excel, Aspose.Cells, API, Cloud"
description: "Verwenden Sie die Aspose.Cells Cloud REST API, um OLE-Objekte in Excel-Arbeitsblättern abzurufen, hinzuzufügen, zu aktualisieren, zu löschen und in andere Formate zu konvertieren. SDKs sind für Java, .NET, Python, PHP, Ruby, Go, Node.js, Perl, Swift und Android verfügbar."
weight: 100
ArticleTitle: "Arbeiten mit Excel OLE-Objekten – Anleitung zum Abrufen, Hinzufügen, Aktualisieren, Löschen und Konvertieren von OLE-Objekten"
---

**Arbeiten mit OLE-Objekten in einem Excel-Arbeitsblatt**

Die Aspose.Cells Cloud REST API stellt eine vollständige Reihe von Operationen zur programmgesteuerten Verwaltung von OLE-Objekten bereit. Im Folgenden finden Sie eine knappe Übersicht zu jeder Operation, einschließlich der HTTP-Methode, dem Endpoint-Muster, den erforderlichen Parametern und einem kurzen Beispiel für die Antwort.

- [Abrufen eines OLE-Objekts aus einem Excel-Arbeitsblatt](/cells/oleobjects/get/)
  - **Methode:** `GET`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **Parameter:** `fileName` (String), `sheetName` (String), `oleObjectIndex` (Integer)  
  - **Beispiel-Antwort:**  
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

- [Hinzufügen eines OLE-Objekts zu einem Excel-Arbeitsblatt](/cells/oleobjects/add/)
  - **Methode:** `POST`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects`  
  - **Parameter:** `fileName`, `sheetName`, `oleObject` (binär oder base64), `imageFormat` (optional)  
  - **Beispiel-Anforderungstext:** multipart/form-data mit dem Dateistream.  
  - **Beispiel-Antwort:** `201 Created` mit dem Location-Header des neuen OLE-Objekts.

- [Aktualisieren eines bestimmten OLE-Objekts in einem Excel-Arbeitsblatt](/cells/oleobjects/update/)
  - **Methode:** `PUT`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **Parameter:** `fileName`, `sheetName`, `oleObjectIndex`, `oleObject` (aktualisierter Inhalt)  
  - **Beispiel-Antwort:** `200 OK` mit aktualisierten Objekt-Metadaten.

- [Konvertieren eines OLE-Objekts in ein Bild innerhalb eines Excel-Arbeitsblatts](/cells/oleobjects/convert/)
  - **Methode:** `GET`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}/convert`  
  - **Parameter:** `fileName`, `sheetName`, `oleObjectIndex`, `format` (z. B. `png`, `jpeg`)  
  - **Beispiel-Antwort:** Binärer Bildstream des konvertierten OLE-Objekts.

- [Löschen aller OLE-Objekte in einem Excel-Arbeitsblatt](/cells/oleobjects/clear/)
  - **Methode:** `DELETE`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects`  
  - **Parameter:** `fileName`, `sheetName`  
  - **Beispiel-Antwort:** `204 No Content`, was angibt, dass alle OLE-Objekte entfernt wurden.

- [Löschen eines bestimmten OLE-Objekts in einem Excel-Arbeitsblatt](/cells/oleobjects/delete/)
  - **Methode:** `DELETE`  
  - **Endpoint:** `/cells/{fileName}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  
  - **Parameter:** `fileName`, `sheetName`, `oleObjectIndex`  
  - **Beispiel-Antwort:** `204 No Content`, bestätigt, dass das Objekt gelöscht wurde.
---