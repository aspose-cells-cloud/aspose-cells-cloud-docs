---
title: Importieren Sie JSON-Daten in Exce
second_title: Aspose.Cells Cloud Documen
linktitle: JSO importieren
type: docs
url: /de/import/json/
keywords: Import Json data into Excel
description: Aspose.Cells Cloud REST API unterstützt das Importieren von String-Array-Daten in Excel Dateien. SDK unterstützt verschiedene Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift
weight: 40
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdwon, Json-Daten importieren in Excel
---
Dieses REST API `import json data` in Excel Arbeitsblatt.


## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/{name}/importjson

```

Die wichtigen Parameter werden in der folgenden Tabelle beschrieben:


**ImportStringArrayOption**

|Parametername|Typ|Beschreibung|
|:- |:- |:- |
| Name| Schnur| Der Arbeitsmappenname|
| Importieren von Json-Anfragen| Klasse| JSON-Anfrage importieren.|
| Passwort| Schnur| Das Kennwort der Arbeitsmappe.|
| Ordner| Schnur| Original-Arbeitsmappenordner.|
| Speichername| Schnur| Speichername.|
| Ausgangspfad| Schnur| Ausgabedateipfad.|
| Name des Ausgangsspeichers| Schnur|Speichername für die Ausgabedatei.|
| checkExcelRestriction| Schnur| Überprüfen Sie die Einschränkung Excel.|


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

 Die Verwendung eines SDK ist der beste Weg, um die Entwicklung zu beschleunigen. Ein SDK kümmert sich um Details auf niedriger Ebene und ermöglicht es Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Bitte lesen Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mit verschiedenen SDKs Aufrufe an die Webdienste Aspose.Cells tätigen:





