---
title: "Arbeitsblatt-Seiteinrichtung"
second_title: "Dokument"
linktype: "Seiteinrichtung"
type: docs
url: /de/page-setup/
keywords: "Aspose.Cells, PageSetup, Arbeitsblatt, Druckeinstellungen, Ränder, Orientierung, Papierformat, Kopfzeile, Fußzeile, Skalierung"
description: "Erfahren Sie, wie Sie das Drucklayout eines Excel-Arbeitsblatts mit dem PageSetup-Objekt von Aspose.Cells Cloud konfigurieren. Enthält eine Liste der Eigenschaften, Standardwerte, Bereichsangaben und Codebeispiele für C#, Java und Python."
weight: 20
ArticleTitle: "Arbeitsblatt-Seiteinrichtung – Konfigurieren des Drucklayouts mit Aspose.Cells Cloud"
---

# **PageSetup**

Excel-Druckseiteneinstellungen

## Übersicht

Das **PageSetup**-Objekt definiert die Layout-Optionen für den Druck eines Excel-Arbeitsblatts, wie z. B. Ränder, Orientierung, Skalierung, Kopf- und Fußzeilen sowie andere druckbezogene Einstellungen. Durch die Konfiguration dieser Eigenschaften können Entwickler druckbare Arbeitsmappen erstellen, die dem gewünschten Erscheinungsbild und der gewünschten Seitenanzahl entsprechen.

Im Folgenden finden Sie ein kurzes C#-Beispiel, das zeigt, wie gängige PageSetup-Eigenschaften mithilfe des Aspose.Cells Cloud SDK festgelegt werden:

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

// Initialisieren des API-Clients (durch eigene Anmeldedaten ersetzen)
var apiInstance = new CellsApi("IHRE_CLIENT_ID", "IHRE_CLIENT_GEHEIMNIS");

// PageSetup-Einstellungen definieren
var pageSetup = new PageSetup()
{
    Orientation = "Landscape",
    PaperSize = "A4",
    CenterHorizontally = true,
    CenterVertically = true,
    Zoom = 100
};

// Einstellungen auf das erste Arbeitsblatt der Arbeitsmappe anwenden
apiInstance.PutWorksheetPageSetup("Sample.xlsx", "Sheet1", pageSetup);
```

Dieses Snippet legt die Orientierung des Arbeitsblatts auf Querformat fest, verwendet A4-Papier, zentriert den Inhalt horizontal und vertikal und wendet einen Skalierungsfaktor von 100 % an.

## Eigenschaften

| Eigenschaftsname        | Eigenschaftstyp | Nullable | ReadOnly | Standardwert    | Beschreibung                                                                 |
| ----------------------- | --------------- | -------- | -------- | --------------- | ---------------------------------------------------------------------------- |
| BlackAndWhite           | bool            | false    | false    | false           | Druckt das Arbeitsblatt im Schwarz-Weiß-Modus.                              |
| BottomMargin            | float           | true     | false    | 2,54 cm         | Größe des unteren Randes in Zentimetern.                                     |
| CenterHorizontally      | bool            | false    | false    | false           | Zentriert das Arbeitsblatt horizontal beim Druck.                            |
| CenterVertically        | bool            | false    | false    | false           | Zentriert das Arbeitsblatt vertikal beim Druck.                              |
| FirstPageNumber         | int             | true     | false    | 1               | Die erste Seitenzahl, die beim Drucken des Arbeitsblatts verwendet wird.     |
| FitToPagesTall          | int             | false    | false    | 1               | Anzahl der Seitenhöhe, auf die das Arbeitsblatt skaliert wird.              |
| FitToPagesWide          | int             | false    | false    | 1               | Anzahl der Seitenbreite, auf die das Arbeitsblatt skaliert wird.            |
| FooterMargin            | float           | true     | false    | 2,54 cm         | Abstand vom unteren Rand der Seite bis zur Fußzeile in Zentimetern.         |
| HeaderMargin            | float           | true     | false    | 2,54 cm         | Abstand vom oberen Rand der Seite bis zur Kopfzeile in Zentimetern.         |
| IsAutoFirstPageNumber   | bool            | false    | false    | false           | Weist die erste Seitenzahl automatisch zu.                                   |
| IsHFAlignMargins        | bool            | false    | false    | true            | Wenn „true“, stimmen die Ränder für Kopf- und Fußzeile mit den Seitenrändern überein. |
| IsHFDiffFirst           | bool            | false    | false    | false           | Gibt an, dass Kopf- und Fußzeile auf der ersten Seite von den anderen Seiten abweichen. |
| IsHFDiffOddEven         | bool            | false    | false    | false           | Gibt an, dass Kopf- und Fußzeile auf ungeraden Seiten von den geraden abweichen. |
| IsHFScaleWithDoc        | bool            | false    | false    | false           | Skaliert Kopf- und Fußzeile zusammen mit dem Dokument (Excel 2007+).        |
| IsPercentScale          | bool            | false    | false    | true            | Wenn „false“, steuern „FitToPagesWide“ und „FitToPagesTall“ die Skalierung. |
| LeftMargin              | float           | true     | false    | 2,54 cm         | Größe des linken Randes in Zentimetern.                                      |
| Order                   | string          | true     | false    | "DownThenOver"  | Die Reihenfolge, die Excel beim Drucken eines großen Arbeitsblatts zur Seitennummerierung verwendet. |
| Orientation             | string          | false    | false    | "Portrait"      | Seitenorientierung: **Landscape** (Querformat) oder **Portrait** (Hochformat). |
| PaperSize               | string          | true     | false    | "A4"            | Für den Druck verwendete Papiergröße.                                        |
| PrintArea               | string          | true     | false    | (keine)         | Zellbereich, der gedruckt werden soll (z. B. `"A1:D20"`).                    |
| PrintComments           | string          | true     | false    | "NoComments"    | Art des Drucks von Kommentaren zusammen mit dem Arbeitsblatt.               |
| PrintCopies             | int             | true     | false    | 1               | Anzahl der auszudruckenden Exemplare.                                        |
| PrintDraft              | bool            | false    | false    | false           | Druckt das Arbeitsblatt im Entwurfsmodus (ohne Grafiken).                   |
| PrintErrors             | string          | true     | false    | "Display"       | Art der anzuzeigenden Druckfehler.                                           |
| PrintGridlines          | bool            | false    | false    | false           | Druckt Zellgitterlinien.                                                     |
| PrintHeadings           | bool            | false    | false    | false           | Druckt Zeilen- und Spaltenüberschriften.                                    |
| PrintQuality            | int             | true     | false    | 600             | Druckqualität (Dots per inch).                                               |
| PrintTitleColumns       | string          | true     | false    | (keine)         | Spalten, die auf der linken Seite jeder gedruckten Seite wiederholt werden. |
| PrintTitleRows          | string          | true     | false    | (keine)         | Zeilen, die oben auf jeder gedruckten Seite wiederholt werden.              |
| RightMargin             | float           | true     | false    | 2,54 cm         | Größe des rechten Randes in Zentimetern.                                     |
| TopMargin               | float           | true     | false    | 2,54 cm         | Größe des oberen Randes in Zentimetern.                                      |
| Zoom                    | int             | false    | false    | 100             | Skalierungsfaktor in Prozent (10–400 %).                                     |
| Header                  | object          | true     | false    | (keine)         | Konfiguration der Seitenkopfzeile.                                           |
| Footer                  | object          | true     | false    | (keine)         | Konfiguration der Seitenfußzeile.                                            |

## Verwandte Objekte

- **Header** – Konfiguriert die Arbeitsblatt-Kopfzeile.  
- **Footer** – Konfiguriert die Arbeitsblatt-Fußzeile.  
- **PrintOptions** – Weitere druckbezogene Einstellungen wie Seitenumbrüche und Druckbereich.  
---