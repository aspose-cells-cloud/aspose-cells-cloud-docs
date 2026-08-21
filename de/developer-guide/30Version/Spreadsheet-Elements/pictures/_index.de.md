---
title: "Arbeiten mit Excel-Bildern"
second_title: "Dokument"
linktitle: "Bilder"
type: docs
url: /pictures/
aliases: [/working-with-pictures/]
keywords: "Excel, Bild, Aspose.Cells Cloud, REST API, Bildverarbeitung, Excel-Bilder"
description: "Erfahren Sie, wie Sie Bilder in Excel-Arbeitsblättern mithilfe der Aspose.Cells Cloud REST API abrufen, hinzufügen, aktualisieren und löschen. Enthält Codebeispiele für C#, Java, Python und mehr."
weight: 100
ArticleTitle: "Arbeiten mit Excel-Bildern – Aspose.Cells Cloud-Dokumentation"
---

## Arbeiten mit Bildern in einer Excel-Datei

Dieser Leitfaden erklärt, wie Sie mit **Bildern** (auch als Bilder bezeichnet) in Excel-Arbeitsblättern über die Aspose.Cells Cloud REST API arbeiten. Er behandelt die wichtigsten bildbezogenen Vorgänge – Abrufen, Hinzufügen, Aktualisieren und Löschen von Excel-Bildern – und verweist auf detaillierte Beispiele für jede Aufgabe.

**Voraussetzungen**: Ein Aspose.Cells Cloud-Konto, ein gültiger API-Schlüssel und das für Ihre gewählte Sprache geeignete SDK installiert.

- [So rufen Sie ein Bild in einem bestimmten Format aus einem Excel-Arbeitsblatt ab.](/cells/pictures/get/) – Abrufen eines einzelnen Bilds im gewünschten Format (PNG, JPEG usw.) aus einem Arbeitsblatt.  
- [So rufen Sie alle Bildinformationen aus einem Excel-Arbeitsblatt ab.](/cells/pictures/get-all/) – Auflisten der Metadaten aller im Arbeitsblatt enthaltenen Bilder.  
- [So fügen Sie ein Bild zu einem Excel-Arbeitsblatt hinzu.](/cells/pictures/add/) – Einfügen eines neuen Bilds in ein Arbeitsblatt mit Angabe von Position und Größe.  
- [So aktualisieren Sie ein bestimmtes Bild aus einem Excel-Arbeitsblatt.](/cells/pictures/update/) – Ändern der Eigenschaften (z. B. Abmessungen, Platzierung) eines vorhandenen Bilds.  
- [So löschen Sie alle Bilder aus einem Excel-Arbeitsblatt.](/cells/pictures/clear/) – Entfernen aller Bildobjekte aus einem Arbeitsblatt mit einem einzigen Aufruf.  
- [So löschen Sie ein Bild aus einem Excel-Arbeitsblatt.](/cells/pictures/delete/) – Löschen eines einzelnen Bilds, das durch seinen Index identifiziert wird.  

**API-Referenz**

**Abrufen eines Bilds in einem bestimmten Format**  

| HTTP-Methode | Endpunkt | Erforderliche Parameter | Beispielanfrage | Beispielantwort | Statuscodes |
|-------------|----------|-----------------------|----------------|----------------|--------------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName` (Pfad), `sheetName` (Pfad), `pictureIndex` (Pfad), `format` (Abfrage) | `GET https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures/0?format=png` | Binäre Bilddaten (PNG, JPEG usw.) | 200 OK, 400 Bad Request, 401 Unauthorized, 404 Not Found, 500 Server Error |

**Abrufen aller Bildinformationen**  

| HTTP-Methode | Endpunkt | Erforderliche Parameter | Beispielanfrage | Beispielantwort | Statuscodes |
|-------------|----------|-----------------------|----------------|----------------|--------------|
| GET | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName` (Pfad), `sheetName` (Pfad) | `GET https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures` | JSON-Array mit Bildmetadaten (Index, Name, Position, Größe) | 200 OK, 400, 401, 404, 500 |

**Hinzufügen eines Bilds**  

| HTTP-Methode | Endpunkt | Erforderliche Parameter | Beispielanfragetext | Beispielantwort | Statuscodes |
|-------------|----------|-----------------------|---------------------|----------------|--------------|
| POST | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName` (Pfad), `sheetName` (Pfad) | `{ "image": "<base64-codiertes-Bild>", "upperLeftRow": 5, "upperLeftColumn": 2, "width": 200, "height": 150 }` | `{ "code": 200, "status": "OK", "pictureIndex": 3 }` | 201 Created, 400, 401, 404, 500 |

**Aktualisieren eines Bilds**  

| HTTP-Methode | Endpunkt | Erforderliche Parameter | Beispielanfragetext | Beispielantwort | Statuscodes |
|-------------|----------|-----------------------|---------------------|----------------|--------------|
| PUT | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName` (Pfad), `sheetName` (Pfad), `pictureIndex` (Pfad) | `{ "upperLeftRow": 10, "upperLeftColumn": 4, "width": 300, "height": 250 }` | `{ "code": 200, "status": "OK" }` | 200 OK, 400, 401, 404, 500 |

**Löschen aller Bilder**  

| HTTP-Methode | Endpunkt | Erforderliche Parameter | Beispielanfrage | Beispielantwort | Statuscodes |
|-------------|----------|-----------------------|----------------|----------------|--------------|
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/pictures` | `fileName` (Pfad), `sheetName` (Pfad) | `DELETE https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures` | `{ "code": 200, "status": "All pictures deleted." }` | 200 OK, 400, 401, 404, 500 |

**Löschen eines bestimmten Bilds**  

| HTTP-Methode | Endpunkt | Erforderliche Parameter | Beispielanfrage | Beispielantwort | Statuscodes |
|-------------|----------|-----------------------|----------------|----------------|--------------|
| DELETE | `/cells/{fileName}/worksheets/{sheetName}/pictures/{pictureIndex}` | `fileName` (Pfad), `sheetName` (Pfad), `pictureIndex` (Pfad) | `DELETE https://api.aspose.cloud/v3.0/cells/myBook.xlsx/worksheets/Sheet1/pictures/2` | `{ "code": 200, "status": "Picture deleted." }` | 200 OK, 400, 401, 404, 500 |

**Verwandte Themen**

Weitere bildbezogene Vorgänge in Aspose.Cells Cloud:  
- [Arbeiten mit Formen](/cells/shapes/) – Hinzufügen, Bearbeiten und Löschen von Zeichnungsformen.  
- [Arbeiten mit Diagrammen](/cells/charts/) – Erstellen und Bearbeiten von Diagrammobjekten.  
- [Arbeiten mit Bildern in Arbeitsblättern](/cells/images/) – Einfügen und Verwalten von rohen Bilddateien.

---

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Arbeiten mit Excel-Bildern – Aspose.Cells Cloud-Dokumentation",
  "description": "Leitfaden zum Abrufen, Hinzufügen, Aktualisieren und Löschen von Excel-Bildern über die Aspose.Cells Cloud REST API.",
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
  "keywords": "Excel-Bilder, Aspose.Cells Cloud, REST API, Bildverarbeitung",
  "url": "https://docs.aspose.cloud/cells/pictures/"
}
</script>