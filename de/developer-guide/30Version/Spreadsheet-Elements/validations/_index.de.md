---
title: "Arbeiten mit Excel-Datenvalidierung"
second_title: "Dokument"
linktype: "Validierungen"
type: docs
url: /validations/
keywords: "Excel-Datenvalidierung, Aspose.Cells Cloud, REST API, Tabellenkalkulation, Office Cloud"
description: "Erfahren Sie, wie Sie Excel-Datenvalidierungsregeln programmgesteuert mit der Aspose.Cells Cloud REST API hinzufügen, abrufen, aktualisieren, löschen und löschen können. Enthält Beispiele für .NET, Java, Python und PHP."
weight: 100
ArticleTitle: "Arbeiten mit Excel-Datenvalidierung – Aspose.Cells Cloud API-Dokumentation"
---

Die Excel-Datenvalidierung ist eine Funktion in Microsoft Excel, mit der gesteuert wird, was ein Benutzer in eine Zelle eines Arbeitsblatts eingeben darf. Sie kann Eingaben auf einen bestimmten Datumsbereich, nur ganzzahlige Werte oder sogar Dropdown-Listen beschränken, die Platz sparen und Werte in einer einzelnen Zelle anzeigen. Sie können auch eine benutzerdefinierte Nachricht definieren, die angezeigt wird, wenn ein Benutzer einen falschen Wert oder ein ungültiges Format eingibt.

Beispielsweise kann ein Benutzer ein Meeting festlegen, das zwischen 9:00 Uhr und 18:00 Uhr stattfindet.

Datenvalidierung kann verwendet werden, um sicherzustellen, dass ein Wert eine positive Zahl ist, ein Datum zwischen dem 15. und 30. eines Monats, ein Datum innerhalb der nächsten 30 Tage oder ein Texteintrag mit weniger als 25 Zeichen usw.

### API-Übersicht

| Vorgang | HTTP-Methode | Endpunkt | Beschreibung |
|---------|--------------|----------|--------------|
| Hinzufügen | POST | `/cells/{file}/worksheets/{sheet}/validations` | Erstellt eine Validierungsregel |
| Abrufen | GET | `/cells/{file}/worksheets/{sheet}/validations/{index}` | Ruft eine spezifische Regel ab |
| Alle abrufen | GET | `/cells/{file}/worksheets/{sheet}/validations` | Listet alle Regeln auf |
| Aktualisieren | PUT | `/cells/{file}/worksheets/{sheet}/validations/{index}` | Ändert eine Regel |
| Löschen | DELETE | `/cells/{file}/worksheets/{sheet}/validations/{index}` | Entfernt eine Regel |
| Löschen (alle) | POST | `/cells/{file}/worksheets/{sheet}/validations/clear` | Entfernt alle Regeln |

## Arbeiten mit Validierungen in einer Excel-Datei

- [Wie Sie einer Excel-Arbeitsmappe eine Validierungsregel hinzufügen](/cells/validations/add/)
- [Wie Sie eine Validierungsregel aus einer Excel-Arbeitsmappe abrufen](/cells/validations/get/)
- [Wie Sie alle Validierungsregeln aus einer Excel-Arbeitsmappe abrufen](/cells/validations/get-all/)
- [Wie Sie eine Validierungsregel aus einer Excel-Arbeitsmappe löschen](/cells/validations/delete/)
- [Wie Sie alle Validierungsregeln aus einer Excel-Arbeitsmappe löschen](/cells/validations/clear/)
- [Wie Sie eine Validierungsregel in einer Excel-Arbeitsmappe aktualisieren](/cells/validations/update/)