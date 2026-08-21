---
title: "Dateiinformationen"
second_title: "Dokument"
linktitle: "Dateiinformationen"
type: docs
url: /de/file-info/
keywords: "Datei, Information, Excel, Aspose.Cells, Cloud API, Metadaten, Base64"
description: "Rufen Sie den Dateinamen, die Größe und den Base64-Inhalt einer Excel-Datei mithilfe der Aspose.Cells Cloud API ab. Enthält Anforderungssyntax, Beispielcode und Fehlerbehandlung."
weight: 79
ArticleTitle: "Dateiinformationen – Excel-Dateimetadaten und Base64-Inhalt (Aspose.Cells Cloud API)"
---

## FileInfo-Eigenschaften


| Name            | Typ    | Beschreibung                                                |
| --------------- | ------ | ----------------------------------------------------------- |
| **FileName**    | string | Der Name der Datei einschließlich ihrer Erweiterung.       |
| **FileSize**    | long   | Die Größe der Datei in Bytes.                               |
| **FileContent** | string | Enthält die rohen Excel-Dateidaten in Base64-codierter Form. |

Die Antwort wird als JSON mit denselben drei in der obigen Tabelle aufgeführten Eigenschaften zurückgegeben, beispielsweise:

```json
{
  "FileName": "MeineArbeitsmappe.xlsx",
  "FileSize": 254312,
  "FileContent": "UEsDBBQABgAIAAAAIQD..."
}
```

### Fehler

| HTTP-Code | Bedeutung               | Eintrittsbedingung                              |
| --------- | ----------------------- | ----------------------------------------------- |
| 200       | OK – Anforderung erfolgreich. | Normale Antwort.                                |
| 401       | Nicht autorisiert       | Fehlender oder ungültiges Authentifizierungstoken. |
| 404       | Nicht gefunden          | Die angegebene Datei existiert nicht.           |
| 500       | Interner Serverfehler   | Unerwarteter Serverfehler.                      |

Stellen Sie für jeden Fehler sicher, dass das Authentifizierungstoken gültig ist (401), überprüfen Sie den Dateipfad (404) oder konsultieren Sie die allgemeine Anleitung zur Fehlerbehandlung für Wiederholungsstrategien (500).

## Siehe auch

- [Arbeitsmappe abrufen](https://docs.aspose.cloud/cells/get-workbook) – Abrufen eines Arbeitsmappenobjekts und seiner Arbeitsblätter.  
- [Datei herunterladen](https://docs.aspose.cloud/cells/download-file) – Herunterladen der rohen Dateibytes ohne Base64-Codierung.  
- [Authentifizierungsübersicht](https://docs.aspose.cloud/cells/authentication) – Wie Sie Zugriffstoken erhalten und verwenden.  
---