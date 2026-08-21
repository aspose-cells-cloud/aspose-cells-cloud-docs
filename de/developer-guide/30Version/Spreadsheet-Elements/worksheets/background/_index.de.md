---
title: "Hintergrundbild für Arbeitsblatt hinzufügen oder entfernen – Aspose.Cells Cloud API"
second_title: "Dokument"
linktitle: "Hintergrund"
type: docs
url: /de/worksheets/background/
keywords: "Aspose.Cells Cloud, Hintergrundbild für Arbeitsblatt, Excel-API, Hintergrundbild hinzufügen, Hintergrundbild entfernen, SDK-Beispiele"
description: "Erfahren Sie, wie Sie mit der Aspose.Cells Cloud REST-API ein Hintergrundbild für ein Excel-Arbeitsblatt hinzufügen oder entfernen. Enthält Anforderungssyntax, SDK-Beispiele für Java, .NET, Python, PHP sowie Fehlerbehandlung."
weight: 20
ArticleTitle: "Hintergrundbild für Arbeitsblatt mit Aspose.Cells Cloud API hinzufügen oder entfernen"
---

## Arbeiten mit Hintergrund in einem Excel-Arbeitsblatt

**Übersicht:** Ein Hintergrund für ein Arbeitsblatt ist ein Bild, das hinter den Zellen eines Arbeitsblatts angezeigt wird und zur Markenpräsenz oder als visueller Hinweis dienen kann. Mit der Aspose.Cells Cloud API können Sie dieses Hintergrundbild programmgesteuert hinzufügen oder entfernen.

**Voraussetzungen:**  
- Gültiges Aspose.Cells Cloud-Zugriffstoken (OAuth 2.0).  
- Eine im Cloudspeicher gespeicherte Excel-Arbeitsmappe.  
- Eine Bilddatei (PNG, JPEG, BMP) für den Hintergrund.

- **Hintergrund hinzufügen** – Legen Sie ein Hintergrundbild für ein Arbeitsblatt fest. Weitere Informationen finden Sie im ausführlichen Leitfaden [So legen Sie ein Hintergrundbild für ein Excel-Arbeitsblatt fest](/cells/worksheets/background/add/).  
- **Hintergrund entfernen** – Entfernen Sie ein vorhandenes Hintergrundbild von einem Arbeitsblatt. Weitere Informationen finden Sie im ausführlichen Leitfaden [So entfernen Sie ein Hintergrundbild von einem Excel-Arbeitsblatt](/cells/worksheets/background/delete/).

Die Verwendung eines Hintergrundbilds für ein Arbeitsblatt kann die Markenpräsenz stärken, wichtige Bereiche hervorheben oder visuelle Hinweise für Endbenutzer liefern. Die Aspose.Cells Cloud API macht es einfach, dieses Hintergrundbild direkt aus Ihrer Anwendung heraus festzulegen oder zu löschen.

### API-Referenz

| Vorgang | HTTP-Methode | Endpoint | Pfadparameter | Anforderungstext | Erfolgsantwort |
|---------|--------------|----------|----------------|----------------|----------------|
| Hintergrund hinzufügen | PUT | `/cells/{name}/worksheets/{sheetName}/background` | `name` – Name der Arbeitsmappe<br>`sheetName` – Zielarbeitsblatt | Bilddatei (PNG, JPEG, BMP) als multipart/form‑data | `200 OK` – Hintergrund angewendet |
| Hintergrund entfernen | DELETE | `/cells/{name}/worksheets/{sheetName}/background` | `name` – Name der Arbeitsmappe<br>`sheetName` – Zielarbeitsblatt | *kein* | `200 OK` – Hintergrund entfernt |

#### Beispiel (Java SDK)

```java
// Hintergrundbild hinzufügen
CellsApi cellsApi = new CellsApi("client_id", "client_secret");
File image = new File("path/to/background.png");
cellsApi.putWorksheetBackground("Book1.xlsx", "Sheet1", image, null);

// Hintergrundbild entfernen
cellsApi.deleteWorksheetBackground("Book1.xlsx", "Sheet1", null);
```

#### Beispiel (Python SDK)

```python
import asposecellscloud
api = asposecellscloud.CellsApi(client_id="YOUR_CLIENT_ID", client_secret="YOUR_CLIENT_SECRET")

# Hintergrund hinzufügen
with open("background.png", "rb") as img:
    api.put_worksheet_background("Book1.xlsx", "Sheet1", img)

# Hintergrund entfernen
api.delete_worksheet_background("Book1.xlsx", "Sheet1")
```

Weitere Sprachbeispiele (C#, PHP, Ruby) finden Sie in der SDK-Dokumentation.

**Verwandte Themen**  
- Erfahren Sie mehr über die Verwaltung von Arbeitsblättern im Allgemeinen: [Übersicht über Arbeitsblätter](/cells/worksheets/).  
- Informieren Sie sich über die Authentifizierung bei Aspose.Cells Cloud: [Leitfaden zur API-Authentifizierung](/cells/authentication/).  
- Entdecken Sie andere Tabellenelemente wie Diagramme, Tabellen und Formeln: [Index der Tabellenelemente](/cells/elements/).
---