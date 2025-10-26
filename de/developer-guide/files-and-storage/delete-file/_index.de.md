---
title: Datei löschen - Excel AP
second_title: Documen
linktitle: Datei löschen
type: docs
url: /de/delete-file/
keywords: Delete file, Excel API, REST API, Office Cloud, Spreadsheet management, File deletion, Cloud storage, API usag
description: Erfahren Sie, wie Sie Dateien in Excel mit Aspose.Cells API löschen. Dieses Handbuch enthält detaillierte Informationen zum Endpunkt „deleteFile API“, zu Anforderungsparametern und zur Antwortstruktur
weight: 100
kwords: Datei löschen, Excel API, REST API, Office Cloud, Tabellenkalkulationsverwaltung, Dateilöschung, Cloud-Speicher, API usag
---
## **Excel API : Datei löschen**

```
DELETE http://api.aspose.cloud/v4.0/cells/storage/file/{path}
```

### **Funktionsbeschreibung**

 Der**Datei löschen** API ermöglicht es Benutzern, bestimmte Dateien aus dem Cloud-Speicher zu entfernen und so eine effiziente Verwaltung von Ressourcen und Daten zu gewährleisten.

###  Die Anfrageparameter für die**Datei löschen** API sind

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTP-Text| Beschreibung|
|:- |:- |:- |:- |
|Weg|Zeichenfolge|Weg|Der Pfad zur Datei, die gelöscht werden muss.|
|Speichername|Zeichenfolge|Abfrage|Der Name des Speichers, in dem sich die Datei befindet. Optional, wenn der Standardspeicher verwendet wird.|
|Versions-ID|Zeichenfolge|Abfrage|Die Versions-ID der zu löschenden Datei, falls zutreffend.|

### **Antwortbeschreibung**

```json
{
Void
}
```

## OpenAPI-Spezifikation

 Der[OpenAPI-Spezifikation](https://reference.aspose.cloud/cells/#/FileController/DeleteFile) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen die Durchführung von REST-Interaktionen direkt von einem Webbrowser aus.

## Excel API SDK

 Die Verwendung eines SDKs beschleunigt die Entwicklung. Ein SDK verwaltet Details auf niedriger Ebene, sodass Sie sich auf Ihre Projektaufgaben konzentrieren können. Bitte beachten Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:
