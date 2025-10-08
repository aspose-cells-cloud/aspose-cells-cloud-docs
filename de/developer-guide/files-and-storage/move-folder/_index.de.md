---
title: Ordner verschieben
second_title: Documen
linktitle: Ordner verschieben
type: docs
url: /de/move-folder/
keywords: Move folder API, Excel API, Folder management, REST API, Aspose.Cells, Cloud storag
description: Diese Dokumentation bietet eine umfassende Anleitung zur Verwendung des Move Folder API zum Verwalten von Ordnern innerhalb des Aspose.Cells Cloud-Speichers
weight: 100
kwords: Excel API, Ordner verschieben API, Office Cloud, REST API, Tabellenkalkulationsverwaltung, PDF, CSV, JSON, Markdown, Alle leeren Zellen in einem Excel Arbeitsblatt abgleichen
---
## **Excel API: Ordner verschieben**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/folder/move/{srcPath}
```

### **Funktionsbeschreibung**

Mit diesem API können Benutzer einen Ordner innerhalb des Aspose.Cells-Cloud-Speichers von einem Ort an einen anderen verschieben. Dies ist für die Organisation von Dateien und die effektive Verwaltung des Cloud-Speichers unerlässlich.

###  Die Anfrageparameter von**Ordner verschieben** API sind

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTP-Text| Beschreibung|
|----------------|--|------------------------|--------------------------------------------------------|
| Quellpfad| Zeichenfolge| Weg| Der Quellpfad des zu verschiebenden Ordners.|
| Zielpfad| Zeichenfolge| Abfrage| Der Zielpfad, in den der Ordner verschoben werden soll.|
| srcStorageName| Zeichenfolge| Abfrage| Der Name des Quellspeichers.|
| Zielspeichername| Zeichenfolge| Abfrage| Der Name des Zielspeichers.|

### **Antwortbeschreibung**

```json
{
Void
}
```

## OpenAPI-Spezifikation

 Der[OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/FolderController/MoveFolder) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen die Durchführung von REST-Interaktionen direkt von einem Webbrowser aus.

## Excel API SDK

 Die Verwendung eines SDKs beschleunigt die Entwicklung am besten. Ein SDK kümmert sich um die Details auf niedriger Ebene und ermöglicht es Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Bitte beachten Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_MoveFolder.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_MoveFolder.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_MoveFolder.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_MoveFolder.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_MoveFolder.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_MoveFolder.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_MoveFolder.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_MoveFolder.go" >}}
{{< /tab >}}
{{< /tabs >}}
