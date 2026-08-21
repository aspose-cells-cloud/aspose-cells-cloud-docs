---
title: "Aspose.Cells Cloud – Mathematische Berechnungs-API (Addieren, Subtrahieren, Multiplizieren, Dividieren, %)"
second_title: "Dokument"
ArticleTitle: "Addieren, Subtrahieren, Multiplizieren, Dividieren und Prozentwerte in Tabellenkalkulationen/Excel"
linktitle: "Mathematische Berechnung"
type: docs
url: /de/math-calculate/
keywords: "Mathematische Berechnungs-API, Aspose.Cells Cloud, Excel-Berechnungen, Addieren, Subtrahieren, Multiplizieren, Dividieren, Prozent, Massenverarbeitung in Excel, REST-API"
description: "Erfahren Sie, wie Sie die Aspose.Cells Cloud Mathematische Berechnungs-API verwenden, um Additions-, Subtraktions-, Multiplikations-, Divisions- oder Prozentsatzoperationen auf Excel-Bereiche in Massen anzuwenden. Enthält Anforderungsformat, Beispielcode und Fehlerbehandlung."
weight: 100
---

## **Einführung**: Schnellberechnung in Tabellenkalkulationen – Addieren, Multiplizieren, Subtrahieren, Dividieren und Prozentsatzformeln in einer laufenden API

_Führen Sie Massenberechnungen über ganze Spalten, Zeilen oder Tabellen durch, ohne eine Formel schreiben zu müssen._

- **Grundlegende Mathematik**: Addieren, Subtrahieren, Multiplizieren oder Dividieren Sie jede Zelle in einem Bereich um eine beliebige Zahl
- **Prozentsätze**: Erhöhen/Vermindern um % oder Ermitteln von % eines Wertes (z. B. +15 %, -8 %, 20 % von…)
- **Massenverarbeitung**: Wenden Sie dies sofort auf Tausende von Zellen an – kein Ausfüllen per Ziehen, keine Arrayformel, kein VBA

| **Berechnungsvorgang** | Beschreibung |
| :--------------------- | :----------- |
| **Addieren**           | +            |
| **Subtrahieren**       | -            |
| **Multiplizieren**     | \*           |
| **Dividieren**         | /            |
| **Prozent**            | %            |

## **Mathematische Berechnungs-API**

```http
PUT https://api.aspose.cloud/v4.0/cells/calculate/math
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter:**

| Parametername | Typ    | Pfad/Abfragezeichenfolge/HTTP-Body | Beschreibung                                                                                      |
| :------------ | :----- | :--------------------------------- | :------------------------------------------------------------------------------------------------ |
| Spreadsheet   | Datei  | FormData                           | Laden Sie die zu verarbeitende Tabellenkalkulationsdatei hoch.                                   |
| operation     | Zeichenfolge | Abfrage                        | Der durchzuführende mathematische Vorgang (Addieren, Subtrahieren, Multiplizieren, Dividieren, Prozent). |
| value         | Zeichenfolge | Abfrage                        | Ein Wert, der bei Bedarf in der Berechnung verwendet werden soll.                               |
| worksheet     | Zeichenfolge | Abfrage                        | Der Name des Arbeitsblatts, auf dem der Vorgang ausgeführt werden soll.                          |
| range         | Zeichenfolge | Abfrage                        | Der Bereich von Zellen, der in die Berechnung einbezogen werden soll.                            |
| region        | Zeichenfolge | Abfrage                        | Die Regionseinstellung der Tabellenkalkulation.                                                  |
| password      | Zeichenfolge | Abfrage                        | Das Passwort zum Öffnen der geschützten Tabellenkalkulationsdatei (sofern vorhanden).             |

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

**HTTP-Statuscodes**

| Code | Bedeutung             | Beschreibung                                                     |
| ---- | --------------------- | ---------------------------------------------------------------- |
| 200  | OK                    | Filter erfolgreich angewendet; Antwort enthält Vorgangsdetails. |
| 400  | Ungültige Anforderung | Fehlende oder ungültige Parameter (z. B. nicht unterstützter Dateityp). |
| 401  | Nicht autorisiert     | Ungültiges oder fehlendes JWT-Token.                             |
| 413  | Anforderungstext zu groß | Die hochgeladene Datei überschreitet die Größenbeschränkung.  |
| 500  | Interner Serverfehler | Unerwarteter Serverfehler.                                       |

## Wofür sollte die Mathematische Berechnungs-API verwendet werden?

- **Finanzen**: Fügen Sie einer ganzen Spalte mit Einkaufspreisen 13 % MwSt hinzu.
- **Inventar**: Multiplizieren Sie die kg-Spalte mit 2,2046, um Massen in Pfund umzurechnen.
- **Lohnabrechnung**: Fügen Sie allen Mitarbeitern einen pauschalen Bonus von 1.000 zur Bonusspalte hinzu.
- **Devisenumrechnung**: Dividieren Sie die Umsatzspalte durch den aktuellen Wechselkurs, um Beträge in USD zu erhalten.
- **Bewertung**: Ziehen Sie von jeder Schülernote 5 Punkte ab, um eine Anwesenheitsstrafe anzuwenden.
- **E-Commerce**: Wenden Sie einen 15 %igen Werbe-Rabatt an, indem Sie Produktpreise mit einem Klick reduzieren.

## Warum sollten Sie die Mathematische Berechnungs-API verwenden?

- **Schnelle Excel-Berechnungen** – Monatsabschlussberichte in Sekundenschnelle fertigstellen.
- **Massenprozentsatz-Erhöhung in Excel** – Preise, Prognosen, Provisionen mit einem Klick aktualisieren.
- **Gleiche Zahl zur gesamten Spalte hinzufügen** – Inventar, Währungsumrechnung, Einheitenumrechnung.
- **Excel ohne Formeln** – Nicht-Techniker schätzen die Einfachheit.
- Die Entwicklung kann schnell über die vorhandenen SDKs abgeschlossen werden.

**Hinweise**  
Die maximal unterstützte Dateigröße beträgt 200 MB. Der `range`-Parameter muss eine gültige Excel-Adressangabe sein (z. B. A1:B10). Sehr große Arbeitsblätter können zusätzliche Verarbeitungszeit erfordern.

## So verwenden Sie die Mathematische Berechnungs-API mit SDKs

### Spezifikation der Mathematischen Berechnungs-API

Die [Spezifikation der Mathematischen Berechnungs-API](https://reference.aspose.cloud/cells/#/CalculateController/MathCalculate) definiert eine öffentlich zugängliche Programmierschnittstelle, die Entwicklern ermöglicht, direkt über einen Webbrowser mit der API zu interagieren.

### Verwenden der Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist der schnellste Weg zur Entwicklung, da sie die Low-Level-Details abstrahieren und es Ihnen ermöglichen, mathematische Berechnungen pro Zelle mit nur wenigen Codezeilen durchzuführen.  
Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie auf [GitHub bei Aspose.Cells Cloud](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aufrufe an Aspose.Cells-Webdienste mit verschiedenen SDKs durchgeführt werden:

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MathCalculate.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MathCalculate.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MathCalculate.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MathCalculate.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MathCalculate.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MathCalculate.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MathCalculate.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MathCalculate.go" >}}
{{</tab>}}
{{< /tabs >}}