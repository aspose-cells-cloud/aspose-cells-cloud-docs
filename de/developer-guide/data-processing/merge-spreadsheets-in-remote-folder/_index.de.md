---
title: Aspose.Cells Cloud Web API - Zusammenführen übereinstimmender Tabellenkalkulationsdateien in einer Datei in einem Remote-Ordner
second_title: Documen
ArticleTitle: Merge matching spreadsheet files into a file in a remote Folder
linktitle: Tabellenkalkulationen in Remote-Ordnern zusammenführen
type: docs
url: /de/merge-spreadsheets-in-remote-folder/
keywords: Merge spreadsheets, cloud storage, Excel API, remote processing, spreadsheet formats, REST AP
description: Kombinieren Sie die im Cloud-Speicher gespeicherten Tabellenkalkulationsdateien in einer Datei. Das Dateiformat unterstützt 30 Ausgabeformate, z. B. PDF, CSV, JSON und andere gängige Formate.
weight: 100
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, JSON, Markdown, Tabellenkalkulationen zusammenführen, Cloud-Verarbeitung, Remote-Dateiverwaltung
---
Fügen Sie passende Tabellenkalkulationsdateien in Dateien im Remote-Ordner zusammen. Das Ausgabedateiformat unterstützt über 30 Formate wie PDF, CSV, JSON und andere gängige Formate.


## **Tabellenkalkulationen im Remote-Ordner zusammenführen API**

```http
PUT http://api.aspose.cloud/v4.0/cells/merge/remote-spreadsheets
```

### **Anforderungsparameter:**

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:- |:- |:- |:- |
| Ordner| Zeichenfolge| Abfrage|Der Ordner, in dem die zusammengeführten Dateien gespeichert werden.|
| Dateiübereinstimmungsausdruck| Zeichenfolge| Abfrage| Ausdruck zum Abgleichen von Dateien zum Zusammenführen.|
| Ausgabeformat| Zeichenfolge| Abfrage| Das gewünschte Ausgabedateiformat.|
| mergeInOneSheet| Boolescher Wert| Abfrage| Gibt an, ob alle Daten in einem einzigen Arbeitsblatt zusammengefasst werden sollen.|
| Speichername| Zeichenfolge| Abfrage| (Optional) Der Name des benutzerdefinierten Cloud-Speichers; wird standardmäßig der Standardspeicher verwendet, wenn er weggelassen wird.|
| Ausgangspfad| Zeichenfolge| Abfrage| (Optional) Der Ordnerpfad zum Speichern der Arbeitsmappe; der Standardwert ist null.|
|outStorageName| Zeichenfolge| Abfrage| Der Name des Speichers für die Ausgabedatei.|
| SchriftartenStandort| Zeichenfolge| Abfrage| Gibt benutzerdefinierte Schriftarten an.|
| Region| Zeichenfolge| Abfrage| Legt den Tabellenbereich fest.|
| Passwort| Zeichenfolge| Abfrage| Das Kennwort zum Öffnen der Tabellenkalkulationsdatei.|

## **Antwort**

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

## Wo sollten wir die Zusammenführungstabelle im Remote-Ordner API verwenden?

Wenn Sie mehrere Datendateien zusammenführen müssen, können Sie diese API verwenden.

## Warum sollten Sie die Merge-Tabelle im Remote-Ordner API verwenden?

- Dateien aus dem Cloud-Speicher müssen nicht heruntergeladen werden und können direkt in der Cloud zusammengeführt werden.
- Stapelweises Zusammenführen mehrerer Tabellenkalkulationsdateien. Unterstützung für übereinstimmende Ausdrücke.
- Die Entwicklung kann über das vorhandene SDK schnell abgeschlossen werden.

## So verwenden Sie die Merge-Tabelle im Remote-Ordner API mit SDKs

### Tabelle im Remote-Ordner zusammenführen API Spezifikation

 Der[Tabelle im Remote-Ordner zusammenführen API Spezifikation](https://reference.aspose.cloud/cells/#/DataProcessingController/MergeSpreadsheetsInRemoteFolder) bietet eine öffentlich zugängliche Programmierschnittstelle, die REST-Interaktionen direkt von einem Webbrowser aus ermöglicht.

### Verwenden Sie Aspose.Cells Cloud SDKs

Die Verwendung des SDK ist die schnellste Art der Entwicklung, da es die Details auf niedriger Ebene abstrahiert und es Ihnen ermöglicht, passende Tabellenkalkulationsdateien mit einem kurzen Code in Dateien in einem Remote-Ordner zusammenzuführen.
 Bitte schauen Sie sich die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele veranschaulichen die Interaktion mit Aspose.Cells-Webdiensten mithilfe verschiedener SDKs:
{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MergeSpreadsheetsInRemoteFolder.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MergeSpreadsheetsInRemoteFolder.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MergeSpreadsheetsInRemoteFolder.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MergeSpreadsheetsInRemoteFolder.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MergeSpreadsheetsInRemoteFolder.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MergeSpreadsheetsInRemoteFolder.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MergeSpreadsheetsInRemoteFolder.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MergeSpreadsheetsInRemoteFolder.go" >}}
{{< /tab >}}
{{< /tabs >}}
