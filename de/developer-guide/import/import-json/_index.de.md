---
title: Importieren Sie Json-Daten in Exce
second_title: Aspose.Cells Cloud Documen
linktitle: Jso importieren
type: docs
url: /de/import/json/
keywords: Import Json data into Excel
description: Aspose.Cells Cloud REST API unterstützt den Import von String-Array-Daten in Excel-Dateien. SDK unterstützt verschiedene Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift
weight: 40
---
Dieses REST API `import json data` wird in das Arbeitsblatt Excel umgewandelt.


## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/{name}/importjson

```

Die wichtigen Parameter sind in der folgenden Tabelle beschrieben:


**ImportStringArrayOption**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| Name| Zeichenfolge| Der Name der Arbeitsmappe|
| importJsonRequest| Klasse| JSON-Anfrage importieren.|
| Passwort| Zeichenfolge| Das Passwort der Arbeitsmappe.|
| Ordner| Zeichenfolge|Originaler Arbeitsmappenordner.|
| Speichername| Zeichenfolge| Speichername.|
| outPath| Zeichenfolge| Pfad der Ausgabedatei.|
| outStorageName| Zeichenfolge| Speichername für die Ausgabedatei.|
| checkExcelRestriction| Zeichenfolge| Überprüfen Sie die Einschränkung Excel.|


**Beispiel**

```json

{
  "JsonFileSource": {
    "FilePath": "string"
  },
  "ImportPosition": {
    "SheetName": "string",
    "RowIndex": 0,
    "ColumnIndex": 0
  },
  "JsonContent": "string"
}

```

## Cloud SDK-Familie

 Die Verwendung eines SDK ist der beste Weg, die Entwicklung zu beschleunigen. Ein SDK kümmert sich um Details auf niedriger Ebene und ermöglicht es Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Bitte schauen Sie sich die an[GitHub-Repository](https://github.com/aspose-cells-cloud) Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie hier.

Die folgenden Codebeispiele veranschaulichen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:





