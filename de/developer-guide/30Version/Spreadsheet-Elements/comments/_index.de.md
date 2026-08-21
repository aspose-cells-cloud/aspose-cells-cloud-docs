---
title: "Arbeiten mit Excel-Kommentaren"
second_title: "Dokument"
linktitle: "Kommentare"
type: docs
url: /de/comments/
aliases: [  /de/working-with-comments/ ]
keywords: "Aspose.Cells Cloud, Excel-Kommentar-API, Tabellenkalkulationskommentare, REST-API"
description: "Erfahren Sie, wie Sie Excel-Kommentare mithilfe der Aspose.Cells Cloud REST API v3.0 hinzufügen, abrufen, aktualisieren und löschen – einschließlich Codebeispielen, Voraussetzungen und Fehlerbehandlung."
weight: 100
ArticleTitle: "Arbeiten mit Excel-Kommentaren – Aspose.Cells Cloud API-Anleitung"
---

Beim Erstellen einer Excel-Arbeitsmappe können Benutzer aus verschiedenen Gründen Kommentare hinzufügen. Ein häufiger Anwendungsfall ist die Erklärung einer Formel in einer Zelle, insbesondere wenn die Datei mit anderen geteilt wird. Kommentare können zudem als Erinnerungen, Notizen für Zusammenarbeiter oder zur Querverweisung mit anderen Arbeitsmappen dienen. Sobald ein Kommentar hinzugefügt wurde, ermöglicht Excel dem Benutzer, das Kommentarfeld zu skalieren, neu zu formen und gemäß dem bevorzugten Stil zu formatieren. Eine fundierte Beherrschung der Kommentarverwaltung hilft Benutzern, das volle Potenzial dieser Funktion auszuschöpfen.

**Voraussetzungen**

- Ein aktives Aspose.Cells Cloud-Konto.  
- Ein gültiger **Zugriffstoken**, der über OAuth 2.0 ermittelt wurde.  
- API-Version **v3.0** (die in dieser Anleitung verwendeten Endpunkte gehören zu dieser Version).  
- Optional: Aspose.Cells SDK für Ihre bevorzugte Programmiersprache, um die Erstellung von Anfragen zu vereinfachen.

**Version**

Die nachfolgenden Beispiele zielen auf **Aspose.Cells Cloud REST API v3.0** ab. Zukünftige API-Veröffentlichungen können zusätzliche Parameter einführen oder Antwortstrukturen ändern; konsultieren Sie stets die aktuelle API-Dokumentation für aktuelle Details.

**Kommentar hinzufügen**

Zum Hinzufügen eines Kommentars senden Sie eine **POST**-Anfrage an folgenden Endpunkt:

```
POST https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments
Authorization: Bearer {access_token}
Content-Type: application/json
```

**Pfadparameter**

| Parameter | Typ    | Erforderlich | Beschreibung                                     |
|-----------|--------|--------------|--------------------------------------------------|
| `file`    | string | Ja           | Name der Arbeitsmappendatei (einschließlich Erweiterung). |
| `sheet`   | string | Ja           | Name des Arbeitsblatts, in das der Kommentar eingefügt wird. |

**Schema des Anforderungstexts**

| Feld       | Typ    | Erforderlich | Beschreibung                               |
|------------|--------|--------------|--------------------------------------------|
| `CellName` | string | Ja           | Zelladresse im A1-Stil (z. B. **B2**).     |
| `Comment`  | string | Ja           | Der zu speichernde Kommentartext.          |
| `Author`   | string | Nein         | Name des Kommentarautors.                  |

**Beispiel für Anforderungstext**

```json
{
  "CellName": "B2",
  "Comment": "Überprüfung erforderlich",
  "Author": "Max Mustermann"
}
```

**Beispiel für erfolgreiche Antwort** (`200 OK`)

```json
{
  "Code": 200,
  "Status": "OK",
  "Comment": {
    "CellName": "B2",
    "Author": "Max Mustermann",
    "HtmlComment": "Überprüfung erforderlich",
    "Note": "Überprüfung erforderlich"
  }
}
```

**Häufige Fehlercodes**

| Code | Bedeutung                              |
|------|----------------------------------------|
| 400  | Ungültige Zelladresse oder Anforderungstext |
| 401  | Nicht autorisiert – fehlender/ungültiger Token |
| 404  | Arbeitsmappe oder Arbeitsblatt nicht gefunden |

**Kommentare abrufen**

Rufen Sie alle Kommentare eines Arbeitsblatts ab:

```
GET https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments
Authorization: Bearer {access_token}
```

**Pfadparameter**

| Parameter | Typ    | Erforderlich | Beschreibung             |
|-----------|--------|--------------|--------------------------|
| `file`    | string | Ja           | Name der Arbeitsmappendatei. |
| `sheet`   | string | Ja           | Name des Arbeitsblatts.  |

**Beispielantwort**

```json
{
  "Code": 200,
  "Status": "OK",
  "Comments": [
    {
      "CellName": "A1",
      "Author": "Alice",
      "HtmlComment": "Initialer Wert",
      "Note": "Initialer Wert"
    },
    {
      "CellName": "B2",
      "Author": "Max Mustermann",
      "HtmlComment": "Überprüfung erforderlich",
      "Note": "Überprüfung erforderlich"
    }
  ]
}
```

**Kommentar aktualisieren**

Um einen vorhandenen Kommentar zu ändern, senden Sie eine **PUT**-Anfrage. Der Kommentar wird anhand seines **Index** in der Kommentarsammlung des Arbeitsblatts identifiziert (beginnend bei 0).

```
PUT https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments/{commentIndex}
Authorization: Bearer {access_token}
Content-Type: application/json
```

**Pfadparameter**

| Parameter      | Typ    | Erforderlich | Beschreibung                             |
|----------------|--------|--------------|------------------------------------------|
| `file`         | string | Ja           | Name der Arbeitsmappendatei.             |
| `sheet`        | string | Ja           | Name des Arbeitsblatts.                  |
| `commentIndex` | int    | Ja           | Nullbasierter Index des zu aktualisierenden Kommentars. |

**Schema des Anforderungstexts**

| Feld      | Typ    | Erforderlich | Beschreibung                    |
|-----------|--------|--------------|---------------------------------|
| `Comment` | string | Ja           | Neuer Kommentartext.            |
| `Author`  | string | Nein         | Aktualisierter Autorenname (optional). |

**Beispiel für Anforderungstext**

```json
{
  "Comment": "Aktualisierter Notiztext",
  "Author": "Max Mustermann"
}
```

Die Antwort folgt der gleichen Struktur wie bei **Kommentar hinzufügen**.

**Kommentar löschen**

Entfernen Sie einen einzelnen Kommentar anhand seines Index:

```
DELETE https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments/{commentIndex}
Authorization: Bearer {access_token}
```

**Pfadparameter**

| Parameter      | Typ    | Erforderlich | Beschreibung                             |
|----------------|--------|--------------|------------------------------------------|
| `file`         | string | Ja           | Name der Arbeitsmappendatei.             |
| `sheet`        | string | Ja           | Name des Arbeitsblatts.                  |
| `commentIndex` | int    | Ja           | Nullbasierter Index des zu löschenden Kommentars. |

Eine erfolgreiche Löschung gibt Folgendes zurück:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Alle Kommentare löschen**

Um alle Kommentare aus einem Arbeitsblatt zu entfernen:

```
DELETE https://api.aspose.cloud/v3.0/cells/{file}/worksheets/{sheet}/comments
Authorization: Bearer {access_token}
```

**Pfadparameter**

| Parameter | Typ    | Erforderlich | Beschreibung             |
|-----------|--------|--------------|--------------------------|
| `file`    | string | Ja           | Name der Arbeitsmappendatei. |
| `sheet`   | string | Ja           | Name des Arbeitsblatts.  |

**Hinweise zur Fehlerbehandlung**

- **404 Not Found** – Stellen Sie sicher, dass die Arbeitsmappen-ID, der Arbeitsblattname und der Kommentarindex korrekt sind.  
- **400 Bad Request** – Prüfen Sie die JSON-Syntax sowie die erforderlichen Felder (`CellName`, `Comment`).  
- **429 Too Many Requests** – Implementieren Sie exponentielles Backoff und beachten Sie den `Retry-After`-Header.

**Zusammenfassung**

- Excel-Kommentare dienen dem [Hinzufügen einer Notiz oder der Erklärung einer Formel in einer Zelle](/cells/comments/add/).  
- Excel bietet Benutzern die Flexibilität, Kommentare auf einem Arbeitsblatt zu [bearbeiten](/cells/comments/update/), [löschen](/cells/comments/delete/) sowie anzuzeigen oder auszublenden ([anzeigen](/cells/comments/get/), [ausblenden](/cells/comments/update/)).  
- Benutzer können das Kommentarfeld zudem [skalieren](/cells/comments/update/) und [verschieben](/cells/comments/update/).  

Weitere Informationen zum Arbeiten mit anderen Tabellenkalkulationselementen finden Sie in der Anleitung [Arbeiten mit Zellen](/cells/working-with-cells/).