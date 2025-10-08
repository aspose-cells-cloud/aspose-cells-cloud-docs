---
title: Aspose.Cells Cloud Web API – Eine Tabelle in eine andere einfügen.
second_title: Aspose.Cells Cloud"
ArticleTitle: Merge one spreadsheet into anothe
linktitle: Remote-Tabellen zusammenführen
type: docs
url: /de/merge-remote-spreadsheet/
keywords: Merge spreadsheets, cloud storage, Aspose.Cells Cloud Web API, spreadsheet merging, XLSX, CSV, PD
description: Kombinieren Sie eine in einem Cloud-Speicher gespeicherte Tabellenkalkulationsdatei mit einer anderen Tabellenkalkulation und Sie können das Format und den Speicherort der Datenausgabe angeben.
weight: 100
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, JSON, Markdown, leere Zellen zusammenführen, Cloud-Verarbeitung
---
Kombinieren Sie eine in einem Cloud-Speicher gespeicherte Tabellenkalkulationsdatei mit einer anderen Tabellenkalkulation und Sie können das Format und den Speicherort der Datenausgabe angeben.

## **Remote-Tabelle zusammenführen API**

```http
PUT http://api.aspose.cloud/v4.0/cells/{name}/merge/spreadsheet
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:- |:- |:- |:- |
|Name|Zeichenfolge|Weg|Der Name der zusammenzuführenden Arbeitsmappendatei.|
|zusammengeführteTabelle|Zeichenfolge|Abfrage|Die Liste der zusammenzuführenden Tabellenkalkulationsdateien.|
|Ordner|Zeichenfolge|Abfrage|Der Ordnerpfad, in dem die Arbeitsmappe gespeichert ist.|
|Ausgabeformat|Zeichenfolge|Abfrage|Das Ausgabedateiformat (z. B. XLSX, PDF).|
|mergeInOneSheet|Boolescher Wert|Abfrage|Ob alle Daten in einem einzigen Arbeitsblatt zusammengefasst werden sollen.|
|Speichername|Zeichenfolge|Abfrage|(Optional) Der Name des Speichers bei Verwendung eines benutzerdefinierten Cloud-Speichers. Wird dieser Name weggelassen, wird standardmäßig der Standardspeicher verwendet.|
|Ausgangspfad|Zeichenfolge|Abfrage|(Optional) Der Ordnerpfad für die zusammengeführte Arbeitsmappe. Der Standardwert ist null.|
|outStorageName|Zeichenfolge|Abfrage|Der Name des Speichers für die Ausgabedatei.|
|SchriftartenStandort|Zeichenfolge|Abfrage|Benutzerdefinierter Schriftartenspeicherort.|
|Region|Zeichenfolge|Abfrage|Die Tabellenbereichseinstellung.|
|Passwort|Zeichenfolge|Abfrage|Das Kennwort für den Zugriff auf die Tabellenkalkulationsdatei.|

### **Antwort**

```json
[
    {
        "Name": "ResponseFile",
        "DataType": {
            "Identifier": "File",
            "Reference": "Stream"
        }
    }
]
```

### Fehlercodes

- **400 Ungültige Anfrage**: Ungültige Apose.Cells Cloud API-URI.
- **401 Nicht autorisiert**: Ungültiges Zugriffstoken. Oder ungültige Client-ID und ungültiges Geheimnis.
- **404 Nicht gefunden**: Auf die Tabellenkalkulationsdatei kann nicht zugegriffen werden.
- **500 Serverfehler**: Beim Abrufen der Berechnungsdaten ist in der Tabelle eine Anomalie aufgetreten.

## Wo sollten wir das Merge Remote Spreadsheet API verwenden?

- Wenn Sie mehrere Datendateien im Cloud-Speicher zusammenführen müssen.


## Warum sollten Sie das Merge Remote Spreadsheet API verwenden?

- Dateien aus dem Cloud-Speicher müssen nicht heruntergeladen werden und können direkt in der Cloud zusammengeführt werden.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## So verwenden Sie die Merge Remote-Tabelle API mit SDKs

### Merge Remote Spreadsheet API Spezifikation

 Der[Merge Remote Spreadsheet API Spezifikation](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeRemoteSpreadsheet) bietet eine öffentlich zugängliche Programmierschnittstelle zum Ausführen von REST-Interaktionen direkt von einem Webbrowser aus.

## Excel API SDK

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK ist die schnellste Art der Entwicklung, da es die Details auf niedriger Ebene abstrahiert und es Ihnen ermöglicht, eine Tabelle mit einem kurzen Code in eine andere Tabelle einzufügen.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.
Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs mit Aspose.Cells-Webdiensten interagieren:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeRemoteSpreadsheet.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeRemoteSpreadsheet.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeRemoteSpreadsheet.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeRemoteSpreadsheet.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeRemoteSpreadsheet.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeRemoteSpreadsheet.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeRemoteSpreadsheet.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeRemoteSpreadsheet.go" >}}
{{< /tab >}}
{{< /tabs >}}
