---
title: Datei verschieben
second_title: Documen
linktitle: Datei verschieben
type: docs
url: /de/move-file/
keywords: Move file, Aspose.Cells API, File Management, Excel API, REST API, Cloud Storage, Spreadsheet Manipulatio
description: Erfahren Sie, wie Sie mit MoveFile API Dateien im Cloud-Speicher Aspose.Cells verwalten
weight: 100
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdown, Datei verschieben, Dateiverwaltung, Cloud-Speicher
---
## **Excel API: Datei verschieben**

```
PUT http://api.aspose.cloud/v4.0/cells/storage/file/move/{srcPath}
```

### **Funktionsbeschreibung**

 Der**Datei verschieben** Mit API können Sie eine Datei innerhalb des Cloud-Speichers Aspose.Cells von einem Ort an einen anderen verschieben. Dies ist besonders nützlich, um Dateien zu organisieren und den Speicher effektiv zu verwalten.

###  Die Anfrageparameter von**Datei verschieben** API sind

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTP-Text| Beschreibung|
|---------------|--|------------------------|--------------------------------------|
| Quellpfad| Zeichenfolge| Weg| Der Quellpfad der zu verschiebenden Datei.|
| Zielpfad| Zeichenfolge| Abfrage| Der Zielpfad, in den die Datei verschoben wird.|
| srcStorageName| Zeichenfolge| Abfrage| Der Name des Quellspeichers, falls zutreffend.|
| Zielspeichername| Zeichenfolge| Abfrage|Der Zielspeichername, falls zutreffend.|
| Versions-ID| Zeichenfolge| Abfrage| Die Versions-ID der Datei, falls zutreffend.|

### **Antwortbeschreibung**

```json
{
Void
}
```

## OpenAPI-Spezifikation

 Der[OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/FileController/MoveFile) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen die Durchführung von REST-Interaktionen direkt von einem Webbrowser aus.

## Excel API SDK

 Die Verwendung eines SDKs beschleunigt die Entwicklung am besten. Ein SDK kümmert sich um die Details auf niedriger Ebene und ermöglicht es Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Bitte beachten Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:
