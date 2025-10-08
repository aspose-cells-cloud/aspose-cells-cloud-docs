---
title: Aspose.Cells Cloud Web API – Addieren, Minus, Multiplizieren, Dividieren und Prozentieren in einer Reihe von Tabellenkalkulationen/Excel
second_title: Documen
ArticleTitle: Add, Minus, Multiply, Divide and Percentage in Spreadsheet/Exce
linktitle: Mathe-Rechner
type: docs
url: /de/math-calculate/
keywords: Math calculation,Cloud REST API, Add, Minus, Multiply, Divide, Percentage, Office Cloud, Aspose.Cell
description: Umfassende Anleitung zur Verwendung von Math Calculate API zum Durchführen von Berechnungen in Excel-Tabellen
weight: 100
kwords: Mathematische Berechnung, Cloud REST API, Addieren, Minus, Multiplizieren, Dividieren, Prozentsatz, Office Cloud, Aspose.Cells
---
Entwickler können diesen API verwenden, um Additions-, Subtraktions-, Multiplikations-, Divisions- und Prozentberechnungen in angegebenen Bereichen von Tabellenkalkulationen/Excel durchzuführen.

|**Berechnungsvorgang** | Beschreibung|
|:- |:- |
|**Hinzufügen** |+ |
|**Minus** |-  |
|**Multiplizieren** |*  |
|**Teilen** |/ |
|**Prozentsatz** |% |

## **Mathe berechnen API**

```http
PUT http://api.aspose.cloud/v4.0/cells/calculate/math
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTP-Text| Beschreibung|
|:- |:- |:- |:- |
| Kalkulationstabelle| Datei| FormData| Laden Sie die Tabellenkalkulationsdatei zur Verarbeitung hoch.|
| Betrieb| Zeichenfolge| Abfrage| Die auszuführende mathematische Operation (Addieren, Minus, Multiplizieren, Dividieren und Prozentieren).|
| Wert| Zeichenfolge| Abfrage| Ein Wert, der gegebenenfalls in der Berechnung verwendet werden soll.|
| Arbeitsblatt| Zeichenfolge| Abfrage| Der Name des Arbeitsblatts, auf das zu reagieren ist.|
| Reichweite| Zeichenfolge| Abfrage| Der Zellbereich, der in die Berechnung einbezogen werden soll.|
| Region| Zeichenfolge| Abfrage|Definiert den spezifischen Bereich der Tabelle.|
| Passwort| Zeichenfolge| Abfrage| Das Kennwort zum Öffnen der Tabellenkalkulationsdatei, sofern diese geschützt ist.|

### **Antwort**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
        }
    }
]
```

### Fehlercodes

- **400 Ungültige Anfrage**: Ungültige Apose.Cells Cloud API-URI.
- **401 Nicht autorisiert**: Ungültiges Zugriffstoken. Oder ungültige Client-ID und ungültiges Geheimnis.
- **404 Nicht gefunden**: Auf die Tabellenkalkulationsdatei kann nicht zugegriffen werden.
- **500 Serverfehler**: Beim Abrufen der Berechnungsdaten ist in der Tabelle eine Anomalie aufgetreten.

## Wo sollten wir den Math Calculate API verwenden?

Die mathematische Berechnung API eignet sich für Stapelberechnungen in Tabellenkalkulationen.

## Warum sollten Sie Math Calculate API verwenden?

- Führen Sie mathematische Stapelberechnungen durch.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## So verwenden Sie Math Calculate API mit SDKs

### Mathematische Berechnung API Spezifikation

 Der[Math Calculate-Spezifikation](https://reference.aspose.cloud/cells/#/CalculateController/MathCalculate) definiert eine öffentlich zugängliche Programmierschnittstelle, die es Entwicklern ermöglicht, direkt über einen Webbrowser mit API zu interagieren.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK ist die schnellste Art der Entwicklung, da es die Details auf niedriger Ebene abstrahiert und Ihnen so mathematische Berechnungen zellenweise mit nur einem kurzen Code ermöglicht.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MathCalculate.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MathCalculate.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MathCalculate.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MathCalculate.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MathCalculate.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MathCalculate.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MathCalculate.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MathCalculate.go" >}}
{{< /tab >}}
{{< /tabs >}}
