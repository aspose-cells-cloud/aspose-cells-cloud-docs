---
title: Importieren Sie JSON-Daten in Excel
second_title: Documen
linktitle: JSO importieren
type: docs
url: /de/import-json-data-into-excel/
aliases: [ /import/json/]
keywords: Import Json data into Excel
description: Aspose.Cells Cloud REST API unterstützt den Import von String-Array-Daten in Excel Dateien. SDK unterstützt verschiedene Entwicklungssprachen. Dazu gehören Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby und Swift
weight: 40
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdown, Json-Daten importieren in Excel
---
Dieses REST API `import json data` in Excel Arbeitsblatt.

## RSET API

```bash

POST https://api.aspose.cloud/v3.0/cells/{name}/importjson

```

Die wichtigen Parameter sind in der folgenden Tabelle beschrieben:

**ImportStringArrayOption**

|Parametername| Pfad/Abfragezeichenfolge/HTTPBody|Typ|Beschreibung|
|:- |:- |:- |:- |
| Name| Weg| Schnur| Der Arbeitsmappenname|
| importJsonRequest| HTTPBody| Klasse| JSON-Anfrage importieren.|
| Passwort| Abfragezeichenfolge| Schnur| Das Kennwort der Arbeitsmappe.|
| Ordner| Abfragezeichenfolge| Schnur| Original-Arbeitsmappenordner.|
| Speichername| Abfragezeichenfolge| Schnur| Speichername.|
| Ausgangspfad| Abfragezeichenfolge| Schnur| Pfad der Ausgabedatei.|
|outStorageName| Abfragezeichenfolge| Schnur| Speichername für die Ausgabedatei.|
| checkExcelRestriction| Abfragezeichenfolge| Schnur| Überprüfen Sie die Einschränkung Excel.|

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

 Die Verwendung eines SDKs beschleunigt die Entwicklung am besten. Ein SDK kümmert sich um die Details auf niedriger Ebene und ermöglicht es Ihnen, sich auf Ihre Projektaufgaben zu konzentrieren. Bitte beachten Sie die[GitHub-Repository](https://github.com/aspose-cells-cloud) für eine vollständige Liste der Aspose.Cells Cloud SDKs.

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:
