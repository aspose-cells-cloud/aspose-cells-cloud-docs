---
title: Ordner löschen
second_title: Documen
linktitle: Ordner löschen
type: docs
url: /de/delete-folder/
keywords: Delete folder, Aspose.Cells API, RESTful API, Excel file management, cloud storag
description: Erfahren Sie, wie Sie einen Ordner in Aspose.Cells mit dem deleteFolder API löschen, einschließlich Parametern und Codebeispielen
weight: 100
kwords: Excel API, Office Cloud, REST API, Tabellenkalkulationsverwaltung, PDF, CSV, JSON, Markdown, Ordner im Arbeitsblatt löschen Excel
---
## **Excel API : Ordner löschen**

```
DELETE http://api.aspose.cloud/v4.0/cells/storage/folder/{path}
```

### **Funktionsbeschreibung**

Mit `deleteFolder` API können Benutzer einen angegebenen Ordner aus dem mit Aspose.Cells verknüpften Cloud-Speicher entfernen. Dies kann nützlich sein, um die Organisation aufrechtzuerhalten und den Speicher effektiv zu verwalten.

###  Die Anfrageparameter von**Ordner löschen** API sind

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody| Beschreibung|
|:- |:- |:- |:- |
| Weg| Zeichenfolge| Weg| Der Pfad des zu löschenden Ordners.|
| Speichername| Zeichenfolge| Abfrage| Der Name des Speichers, in dem sich der Ordner befindet.|
| rekursiv| Boolescher Wert| Abfrage| Gibt an, ob die Löschung rekursiv erfolgen soll und dabei auch alle Inhalte im Ordner entfernt werden.|

### **Antwortbeschreibung**

```json
{
Void
}
```

## OpenAPI-Spezifikation

 Der[OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/FolderController/DeleteFolder) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen, REST-Interaktionen direkt von einem Webbrowser aus durchzuführen.

## Excel API SDK

 Die Verwendung eines SDKs beschleunigt die Entwicklung. Ein SDK verarbeitet grundlegende Details, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Bitte beachten Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:

{{< tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_DeleteFolder.cs" >}}
{{< /tab >}}
{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_DeleteFolder.java" >}}
{{< /tab >}}
{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_DeleteFolder.php" >}}
{{< /tab >}}
{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_DeleteFolder.rb" >}}
{{< /tab >}}
{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_DeleteFolder.ts" >}}
{{< /tab >}}
{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_DeleteFolder.py" >}}
{{< /tab >}}
{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_DeleteFolder.pl" >}}
{{< /tab >}}
{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_DeleteFolder.go" >}}
{{< /tab >}}
{{< /tabs >}}
