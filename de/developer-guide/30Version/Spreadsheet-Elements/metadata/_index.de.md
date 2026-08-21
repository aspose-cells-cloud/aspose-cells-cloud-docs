---
title: "Arbeiten mit Excel-Metadaten und -Eigenschaften"
second_title: "Dokument"
linktype: "docs"
url: /de/metadata/
aliases:
  - /de/document-properties/
  - /de/working-with-document-properties/
keywords: "Aspose.Cells Cloud, Excel-Metadaten, Dokumenteigenschaften-API, REST-API, Metadaten abrufen, Excel-Eigenschaften aktualisieren, Excel-Metadaten löschen"
description: "Erfahren Sie, wie Sie mithilfe der Aspose.Cells Cloud REST-API Excel-Dateimetadaten lesen, hinzufügen, aktualisieren und löschen. Enthält Beispiele für cURL und SDKs für Java, .NET, Python, Node.js und mehr."
ArticleTitle: "Arbeiten mit Excel-Metadaten und Dokumenteigenschaften – Aspose.Cells Cloud"
weight: 100
---

Excel-Dateien können eine Vielzahl von Metadaten speichern, die zur Identifizierung, Organisation und Verwaltung der Dokumente beitragen. Aspose.Cells Cloud bietet eine einfache REST-API zum Lesen, Hinzufügen, Aktualisieren und Löschen dieser Metadaten, sodass Entwickler die Verwaltung von Dokumenteigenschaften nahtlos in ihre Anwendungen integrieren können. Dieser Leitfaden behandelt die beiden Hauptkategorien von Eigenschaften – Standard- und benutzerdefinierte – erläutert deren Verwendung und enthält direkte Links zu den entsprechenden API-Endpunkten. Außerdem finden Sie eine übersichtliche API-Referenztabelle mit Anforderungsdetails, um die Implementierung zu beschleunigen.

**Zuletzt aktualisiert:** 8. Juli 2026  

**Arten von Dokumenteigenschaften**

Bevor wir lernen, wie Sie mit Aspose.Cells Cloud-APIs Dokumenteigenschaften (Metadaten) in Excel anzeigen, ändern und entfernen, klären wir die Arten von Eigenschaften, die ein Excel-Dokument enthalten kann.

- **Standard-Eigenschaften** sind allgemein bei Excel verfügbar. Sie enthalten grundlegende Informationen wie Titel, Betreff, Autor, Kategorie usw. Sie können benutzerdefinierte Textwerte für diese Eigenschaften festlegen, um die Datei leichter auffindbar zu machen.

- **Benutzerdefinierte Eigenschaften** werden vom Nutzer erstellt. Sie ermöglichen das Hinzufügen zusätzlicher Metadaten zu Ihrer Excel-Datei.

**So arbeiten Sie mit Dokumenteigenschaften in einer Excel-Datei**

- [So rufen Sie eine bestimmte Dokumenteigenschaft mit Speicher ab](/de/cells/document-properties/get/)
- [So rufen Sie Dokumenteigenschaften ohne Speicher ab](/de/cells/metadata/get/)
- [So rufen Sie alle Dokumenteigenschaften mit Speicher ab](/de/cells/document-properties/get-all/)
- [So aktualisieren Sie eine bestimmte Dokumenteigenschaft mit Speicher](/de/cells/document-properties/update/)
- [So aktualisieren Sie eine bestimmte Dokumenteigenschaft ohne Speicher](/de/cells/metadata/update/)
- [So entfernen Sie eine bestimmte Dokumenteigenschaft mit Speicher](/de/cells/document-properties/delete/)
- [So entfernen Sie Dokumenteigenschaften ohne Speicher](/de/cells/metadata/delete/)
- [So entfernen Sie alle Dokumenteigenschaften mit Speicher](/de/cells/document-properties/clear/)

**API-Referenz (ohne Speicher)**  

| Methode | Endpunkt | Beschreibung |
|--------|----------|-------------|
| **GET** | `GET https://api.aspose.cloud/v3.0/cells/metadata` | Ruft alle Dokumenteigenschaften der im Cloud-Speicher gespeicherten Arbeitsmappe ab. |
| **GET** | `GET https://api.aspose.cloud/v3.0/cells/metadata/{propertyName}` | Ruft den Wert einer bestimmten Eigenschaft (Standard oder benutzerdefiniert) ab, identifiziert über `propertyName`. |
| **PUT** | `PUT https://api.aspose.cloud/v3.0/cells/metadata/{propertyName}` | Aktualisiert den Wert einer bestehenden Eigenschaft. Der Anforderungstext enthält den neuen Wert im JSON-Format. |
| **DELETE** | `DELETE https://api.aspose.cloud/v3.0/cells/metadata/{propertyName}` | Löscht eine bestimmte Eigenschaft aus der Arbeitsmappe. |
| **DELETE** | `DELETE https://api.aspose.cloud/v3.0/cells/metadata` | Entfernt alle benutzerdefinierten und Standard-Eigenschaften aus der Arbeitsmappe. |

*Alle Anfragen erfordern ein OAuth 2.0-Zugriffstoken und können optionale Abfrageparameter wie `storage` und `folder` enthalten, sofern ein bestimmter Speicherort verwendet wird.*