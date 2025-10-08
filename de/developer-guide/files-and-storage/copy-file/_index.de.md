---
title: Datei kopieren - Excel AP
second_title: Documen
linktitle: Datei kopieren
type: docs
url: /de/copy-file/
keywords: Excel API, Office Cloud, REST API, Spreadsheet Copy, PDF Conversion, CSV Export, JSON Handling, Markdown Support, Copy Excel File, Match Blank Cell
description: Erfahren Sie, wie Sie mit CopyFile API für Excel Tabellenkalkulationen effizient duplizieren und verschiedene Dateiformate verarbeiten können
weight: 100
kwords: Excel API, Office Cloud, REST API, Tabellenkopie, PDF Konvertierung, CSV-Export, JSON-Verarbeitung, Markdown-Unterstützung, Excel Datei kopieren, Leere Zelle abgleichen
---
## **Excel API: Datei kopieren**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/file/copy/{srcPath}
```

### **Funktionsbeschreibung**

 Der**Datei kopieren** API ermöglicht Benutzern das Duplizieren einer Excel-Datei von einem angegebenen Quellpfad in einen Zielpfad und unterstützt verschiedene Speicheroptionen.

###  Die Anfrageparameter von**Datei kopieren** API sind

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|-------------- ||--------------------- |-------------------------------------- |
| Quellpfad| Zeichenfolge| Weg| Der Quellpfad der zu kopierenden Datei.|
| Zielpfad| Zeichenfolge| Abfrage| Der Zielpfad, in dem die Datei gespeichert wird.|
| srcStorageName| Zeichenfolge| Abfrage| Der Name des Quellspeichers.|
| Zielspeichername| Zeichenfolge| Abfrage| Der Name des Zielspeichers.|
| Versions-ID| Zeichenfolge| Abfrage| Optionale Versions-ID der zu kopierenden Datei.|

### **Antwortbeschreibung**

```json
{
Void
}
```

## OpenAPI-Spezifikation

 Der[OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/FileController/CopyFile) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen die Durchführung von REST-Interaktionen direkt von einem Webbrowser aus.

## Excel API SDK

 Die Verwendung eines SDKs beschleunigt die Entwicklung. Ein SDK verwaltet Details auf niedriger Ebene, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Bitte beachten Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_CopyFile.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_CopyFile.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_CopyFile.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_CopyFile.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_CopyFile.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_CopyFile.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_CopyFile.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_CopyFile.go" >}}
{{< /tab >}}
{{< /tabs >}}
