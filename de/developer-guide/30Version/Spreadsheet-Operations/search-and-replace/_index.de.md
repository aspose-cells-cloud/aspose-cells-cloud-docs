---
title: "Suchen und Ersetzen von Textinhalten in Excel-Dateien"
second_title: "Dokumentation"
linktitle: "Suchen und Ersetzen"
type: docs
url: /de/search-and-replace/
aliases: [  /de/working-with-text/ , /de/text/ ]
description: "Erfahren Sie, wie Sie Text in Excel-Arbeitsmappen und -Arbeitsblättern mithilfe der Aspose.Cells Cloud REST-API suchen und ersetzen können. Enthält Anforderungsformat, Beispielscode für .NET, Java, Python sowie Fehlerbehandlung."
keywords: "Aspose.Cells Cloud, Excel, Suchen und Ersetzen, REST-API, .NET, Java, Python"
weight: 20
ArticleTitle: "Suchen und Ersetzen von Text in Excel-Dateien mithilfe der Aspose.Cells Cloud API"
---

Textoperationen sind komplexe Prozesse für Excel-Dateien. Viele Faktoren tragen zu dieser Komplexität bei und sollten während der Verarbeitung berücksichtigt werden. Aspose.Cells Cloud bietet eine zuverlässige Möglichkeit, Text in einer Vielzahl von Tabellenkalkulationsformaten zu suchen und zu ersetzen.

Die Arbeit mit Text in Excel-Arbeitsmappen erfordert häufig das Auffinden spezifischer Zeichenfolgen und das Aktualisieren dieser über mehrere Arbeitsblätter hinweg. Die Aspose.Cells Cloud API vereinfacht diese Aufgabe durch eine einheitliche **Such- und Ersetzungsoperation**, die in allen unterstützten Tabellenkalkulationsformaten funktioniert.

## Übersicht

Mit der Such- und Ersetzungsfunktion können Sie spezifische Zeichenfolgen in einer Arbeitsmappe oder einem bestimmten Arbeitsblatt suchen und durch neue Werte ersetzen. Der Vorgang funktioniert mit allen von Aspose.Cells Cloud unterstützten Formaten wie **XLS, XLSX, XLSM, XLSB, ODS, CSV** und weiteren. Mithilfe der **Such- und Ersetzungsfunktion** können Sie Daten schnell bereinigen, wiederholte Tippfehler korrigieren oder mithilfe von Massenbenennungskonventionen在整个 Arbeitsmappe anwenden.

## Voraussetzungen

- Ein aktiver Aspose.Cloud-Account mit gültiger **Client‑Id** und **Client‑Secret**.
- Zugriffstoken, das über den OAuth 2.0-Authentifizierungsfluss erhalten wurde.
- Die Zielarbeitsmappe muss im Aspose Cloud-Speicher gespeichert oder über eine öffentliche URL erreichbar sein.
- Erforderliches SDK installiert (z. B. Aspose.Cells‑Cloud für .NET, Java oder Python).

## API-Referenz

**Methode:** `POST`  
**Endpunkt**

```
POST https://api.aspose.cloud/v3.0/cells/{fileName}/searchreplace
```

| Parameter        | Typ     | Erforderlich | Beschreibung                                                                                      |
| ---------------- | ------- | ------------ | ------------------------------------------------------------------------------------------------- |
| `fileName`       | string  | Ja           | Name der Arbeitsmappe (einschließlich Dateierweiterung).                                          |
| `folder`         | string  | Nein         | Pfad zum Cloud-Speicherordner.                                                                    |
| `storage`        | string  | Nein         | Speichername, sofern nicht der Standard verwendet wird.                                          |
| `sheetName`      | string  | Nein         | Name des spezifischen Arbeitsblatts; falls weggelassen, gilt der Vorgang für die gesamte Mappe.  |
| `searchString`   | string  | Ja           | Zu suchender Text.                                                                                |
| `replaceString`  | string  | Ja           | Text, durch den die gefundenen Vorkommen ersetzt werden sollen.                                  |
| `ignoreCase`     | boolean | Nein         | Auf `true` setzen, um eine groß-/kleinschreibungunabhängige Suche durchzuführen.                |
| `matchWholeCell` | boolean | Nein         | Auf `true` setzen, um nur ganze Zellübereinstimmungen zu ersetzen.                               |

**Header**

- `Authorization: Bearer {access_token}`
- `Content-Type: application/json`

**Anforderungstext (JSON)**

```json
{
  "searchString": "AlterWert",
  "replaceString": "NeuerWert",
  "ignoreCase": false,
  "matchWholeCell": false,
  "sheetName": "Tabelle1"
}
```

**Erfolgreiche Antwort (JSON)**

```json
{
  "status": "OK",
  "replacedCount": 3,
  "updatedFileUrl": "https://api.aspose.cloud/v3.0/storage/file/updatedWorkbook.xlsx"
}
```

## Unterstützte Formate

| Format                                | Erweiterung               |
| ------------------------------------- | ------------------------- |
| Excel-Arbeitsmappe                    | .xls, .xlsx, .xlsm, .xlsb |
| OpenDocument Tabellenkalkulation      | .ods                      |
| CSV                                   | .csv                      |
| Weitere (wie von Aspose.Cells unterstützt) | —                         |

## Codebeispiele

Im Folgenden finden Sie minimale Beispiele für drei gängige SDKs. Ersetzen Sie `{clientId}`, `{clientSecret}` und andere Platzhalter durch Ihre tatsächlichen Werte. Diese Beispiele zeigen, wie Sie einen **Such- und Ersetzungs**vorgang programmgesteuert durchführen.

## Fehlerbehandlung und Randfälle

| HTTP-Code | Bedeutung                                           | Empfohlene Maßnahme                                                 |
| --------- | --------------------------------------------------- | ------------------------------------------------------------------- |
| 400       | Bad Request – fehlende oder ungültige Parameter    | Überprüfen Sie erforderliche Felder und Datentypen.                |
| 401       | Unauthorized – ungültiges oder abgelaufenes Token  | Aktualisieren Sie den Zugriffstoken.                               |
| 404       | Not Found – Arbeitsmappe oder Arbeitsblatt nicht vorhanden | Überprüfen Sie Dateiname, Ordnerpfad und `sheetName`.             |
| 415       | Unsupported Media Type – ungültiges Dateiformat    | Stellen Sie sicher, dass die hochgeladene Datei ein unterstütztes Excel- oder CSV-Format hat. |
| 202       | Accepted – Anfrage zur Verarbeitung akzeptiert     | Pollen Sie den Vorgangsstatus, falls asynchrone Verarbeitung verwendet wird. |
| 204       | No Content – Vorgang erfolgreich ohne Antwortbody  | Die Ersetzung wurde angewendet; es werden keine weiteren Daten zurückgegeben. |
| 500       | Internal Server Error – unerwarteter Fehler        | Wiederholen Sie den Vorgang nach einer kurzen Verzögerung; kontaktieren Sie den Aspose-Support, falls das Problem bestehen bleibt. |

**Hinweise:**  
- Große Arbeitsmappen können die Anforderungsgrößenbeschränkungen überschreiten; erwägen Sie daher, die Datei zuerst in den Cloud-Speicher hochzuladen.  
- Wenn `ignoreCase` auf `true` gesetzt ist, beachten Sie, dass länderspezifische Groß-/Kleinschreibungsumordnungen die Ergebnisse beeinflussen können.  
- Die Verwendung von `matchWholeCell` bei Formeln ersetzt keine Teilübereinstimmungen innerhalb des Formeltextes.

## Suchen und Ersetzen in Excel-Dateien

- [So erhalten Sie Textelemente aus einer Excel-Arbeitsmappe.](/de/cells/workbook/get-text-items/)
- [So erhalten Sie Textelemente aus einem Excel-Arbeitsblatt.](/de/cells/worksheets/get-text-items/)
- [So finden Sie Text aus einer Excel-Arbeitsmappe.](/de/cells/workbook/find-text/)
- [So finden Sie Text aus einem Excel-Arbeitsblatt.](/de/cells/worksheets/find-text/)
- [So finden Sie Text aus Excel-Dateien, ohne eine Datei hochzuladen.](/de/cells/search/)
- [So ersetzen Sie Text aus einer Excel-Arbeitsmappe.](/de/cells/workbook/replace-text/)
- [So ersetzen Sie Text aus einem Excel-Arbeitsblatt.](/de/cells/worksheets/replace-text/)
- [So ersetzen Sie Text aus Excel-Dateien, ohne eine Datei hochzuladen.](/de/cells/replace/)

<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "TechArticle",
  "headline": "Suchen und Ersetzen von Text in Excel-Dateien mithilfe der Aspose.Cells Cloud API",
  "description": "Dokumentation für den Such- und Ersetzungs-Endpunkt von Aspose.Cells Cloud, einschließlich Anforderungsformat, Parametern, Beispielen und Fehlerbehandlung.",
  "url": "https://docs.aspose.cloud/de/cells/search-and-replace/",
  "author": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Aspose"
  },
  "datePublished": "2026-07-30",
  "keywords": "Aspose.Cells Cloud, Excel, Suchen und Ersetzen, API, REST"
}
</script>
---