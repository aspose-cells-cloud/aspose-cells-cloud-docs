---
title: "Arbeiten mit dem Löschen von Zeilen in einem Excel-Arbeitsblatt"
second_title: "Dokument"
linktitle: "Löschen"
type: docs
url: /rows/delete/
keywords: "Aspose.Cells, Zeile löschen, Excel-API, REST, Cloud, Tabellendokument, Excel, SDK"
description: "Erfahren Sie, wie Sie einzelne oder mehrere Zeilen in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API löschen. Enthält Codebeispiele für Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby und Swift."
weight: 20
ArticleTitle: "Arbeiten mit dem Löschen von Zeilen in einem Excel-Arbeitsblatt – Aspose.Cells Cloud API-Anleitung"
---

## Verfügbare Löschvorgänge

Die folgenden Beispiele zeigen, wie Sie mithilfe der Aspose.Cells Cloud REST API eine einzelne leere Zeile oder mehrere Zeilen aus einem Excel-Arbeitsblatt löschen.

- [So löschen Sie eine leere Zeile in einem Excel-Arbeitsblatt](/cells/rows/delete/row/)
- [So löschen Sie mehrere Zeilen in einem Excel-Arbeitsblatt](/cells/rows/delete/rows/)

**API-Referenz**

| Element               | Details |
|-----------------------|---------------------------------------------------------------|
| **HTTP-Methode**      | DELETE |
| **Endpunkt**          | `/cells/{fileName}/worksheets/{sheetName}/rows` |
| **Pfadparameter**     | `fileName` – Name der Excel-Datei (erforderlich)<br>`sheetName` – Name des Arbeitsblatts (erforderlich) |
| **Abfrageparameter**  | `startrow` – Index der ersten zu löschenden Zeile (erforderlich)<br>`totalRows` – Anzahl der zu löschenden Zeilen (erforderlich)<br>`storage` – Name des Cloud-Speichers (optional)<br>`folder` – Ordnerpfad im Speicher (optional) |
| **Anforderungstext**  | *Keiner* |
| **Antwortbeispiel**   | ```json<br>{<br>  "Code": 200,<br>  "Status": "OK",<br>  "RowsDeleted": 1<br>}<br>``` |
| **Mögliche Statuscodes** | 200 OK – Zeilen erfolgreich gelöscht<br>400 Bad Request – ungültige Parameter<br>401 Unauthorized – Authentifizierungsfehler<br>404 Not Found – Datei oder Arbeitsblatt nicht gefunden<br>500 Internal Server Error – serverseitiges Problem |

**Siehe auch**

- [Zeile hinzufügen](/cells/rows/add/)
- [Zeile abrufen](/cells/rows/get/)
- [Zeile kopieren](/cells/rows/copy/)
- [Zeile ausblenden](/cells/rows/hide/)
- [Übersicht über Zeilen](/cells/rows/)