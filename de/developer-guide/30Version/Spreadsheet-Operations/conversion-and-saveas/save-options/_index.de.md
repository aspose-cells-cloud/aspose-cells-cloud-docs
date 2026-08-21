---
title: "Speicheroptionen"
second_title: "Dokument"
linktitle: "Speicheroptionen"
type: docs
url: /de/save-options/
keywords: "Aspose.Cells Cloud, SaveOptions, Excel, Arbeitsmappe, REST API, Dateiformate, PDF, CSV, JSON, HTTP-Komprimierung, Diagrammzwischenspeicher, Benannte Bereiche, Verzeichniserstellung"
description: "Beschreibt die SaveOptions-Eigenschaften der Aspose.Cells Cloud REST API, die Entwicklern ermöglichen, das Speicherverhalten von Arbeitsmappen für mehrere Dateiformate und Optionen wie HTTP-Komprimierung, Aktualisierung des Diagrammzwischenspeichers und automatische Verzeichniserstellung zu konfigurieren."
weight: 79
ArticleTitle: "Speicheroptionen – Aspose.Cells Cloud REST API-Dokumentation"
---

# SaveOptions-Eigenschaften

Mit SaveOptions können Sie steuern, wie eine Arbeitsmappe beim Verwenden der Aspose.Cells Cloud REST API gespeichert wird. Durch Konfiguration dieser Optionen können Sie HTTP-Komprimierung aktivieren, das Ausgabeformat angeben, den temporären Speicher verwalten und zusätzliche Verhaltensweisen wie die Aktualisierung des Diagrammzwischenspeichers sowie die automatische Verzeichniserstellung steuern.

**Voraussetzungen**  
- Eine authentifizierte Aspose.Cells Cloud-Sitzung (OAuth 2.0 oder JWT).  
- Die Zielarbeitsmappe muss vor dem Speichern über die API geladen oder erstellt worden sein.

| Name                      | Typ        | Beschreibung                                                                                                                       | Hinweise   |
| ------------------------- | ---------- | ---------------------------------------------------------------------------------------------------------------------------------- | ---------- |
| **EnableHTTPCompression** | **bool?**  | Aktiviert HTTP-Komprimierung für die Antwort.                                                                                     | [optional] |
| **SaveFormat**            | **string** | Gibt das Zieldateiformat für das Speichern der Arbeitsmappe an.                                                                   | [optional] |
| **ClearData**             | **bool?**  | Leert die Arbeitsmappe nach dem Speichern der Datei.                                                                              | [optional] |
| **CachedFileFolder**      | **string** | Der zwischengespeicherte Dateiordner, der verwendet wird, um große Daten vorübergehend zu speichern.                              | [optional] |
| **ValidateMergedAreas**   | **bool?**  | Gibt an, ob verschmolzene Bereiche vor dem Speichern der Datei validiert werden sollen. Der Standardwert ist false.              | [optional] |
| **RefreshChartCache**     | **bool?**  | Aktualisiert die Diagrammzwischenspeicherdaten vor dem Speichern.                                                                 | [optional] |
| **CreateDirectory**       | **bool?**  | Wenn auf true gesetzt und das Verzeichnis nicht vorhanden ist, wird es vor dem Speichern der Datei automatisch erstellt.          | [optional] |
| **SortNames**             | **bool?**  | Sortiert benannte Bereiche alphabetisch beim Speichern.                                                                           | [optional] |

**Anforderung**  
- **Methode:** `POST` (oder `PUT`, je nach Vorgang)  
- **Endpunkt:** `/cells/workbook/save`  
- **Header:**  
  - `Authorization: Bearer <access_token>`  
  - `Content-Type: application/json`  
- **Rumpf:** JSON-Darstellung des `SaveOptions`-Modells (siehe Tabelle oben) kombiniert mit den Arbeitsmappendaten oder -referenz.

**Beispiel für Antwort**  
```json
{
  "status": "OK",
  "downloadUrl": "https://api.aspose.cloud/v3.0/cells/workbook/save/result.xlsx",
  "message": "Arbeitsmappe erfolgreich gespeichert."
}
```

**HTTP-Statuscodes**

| Code | Bedeutung                   | Beschreibung                                                     |
|------|-----------------------------|------------------------------------------------------------------|
| 200  | OK                          | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails. |
| 400  | Bad Request                 | Fehlende oder ungültige Parameter (z.�B. nicht unterstütztes Dateiformat). |
| 401  | Unauthorized                | Ungültiger oder fehlender JWT-Token.                             |
| 413  | Payload Too Large           | Die hochgeladene Datei überschreitet das Größenlimit.           |
| 500  | Internal Server Error       | Unerwarteter Serverfehler.                                       |

**Hinweise / Bemerkungen**  
- Wenn **CreateDirectory** auf `true` gesetzt ist, erstellt die API den Zielordner automatisch, sofern er noch nicht vorhanden ist.  
- Das Aktivieren von **EnableHTTPCompression** kann die Nutzlastgröße für große Arbeitsmappen reduzieren, vorausgesetzt der Client unterstützt das Decodieren von gzip/deflate.  
- **RefreshChartCache** sollte verwendet werden, wenn Diagramme von dynamischen Daten abhängen, die sich seit der Erstellung der Arbeitsmappe möglicherweise geändert haben.