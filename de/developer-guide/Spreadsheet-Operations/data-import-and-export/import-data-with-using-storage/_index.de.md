﻿---
title: Daten importieren mit Storage
second_title: Aspose.Cells Cloud Documen
linktitle: Daten mit Speicher importieren
type: docs
url: /de/import-data-with-using-storage/
aliases: [/import-data-into-excel-worksheet/, /import-data-into-worksheet/ , /import-data-in-excel-worksheet/, /import-data/,/import/with-using-storage/]
description: "Cells.Cloud API für Excel bedienen: Daten in Excel Arbeitsblatt importieren"
weight: 10
kwords: Excel, Office Cloud, REST API, Tabellenkalkulation, PDF, CSV, Json, Markdown, Datenimport mit Speicher
---
Dieser REST API gibt `import data` in der Datei Excel an.

## RSET API

```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/importdata
 
```

Die Anforderungsparameter sind:

| Parametername| Typ| Pfad/Abfragezeichenfolge/HTTPBody|Beschreibung|
|:- |:- |:- |:- |
| Name| Schnur| Weg||
| Ordner| Schnur| Abfrage||
| Speichername| Schnur| Abfrage| Speichername.|
| Importdaten|| Körper||

**Die Parameter für die Importdatenoptionen** sind beschrieben in[der Referenzlink](/cells/de/import/#import-data-option-parameter).

 Der[OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht Ihnen die Durchführung von REST-Interaktionen direkt von einem Webbrowser aus.

Mit dem Befehlszeilentool cURL können Sie problemlos auf die Webdienste Aspose.Cells zugreifen. Das folgende Beispiel zeigt, wie Sie mit cURL Aufrufe an die Cloud API tätigen.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/importdata" \
-X POST \
-D "{\"Data\":[1,2,4],\"DestinationWorksheet\":\"Sheet1\",\"FirstRow\":1,\"FirstColumn\":2,\"IsVertical\":true,\"IsInsert\":true,\"importDataType\":\"IntArray\"}" \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
 
```

{{< /tab >}}

{{< /tabs >}}

Die folgenden Codebeispiele zeigen, wie Sie mithilfe verschiedener SDKs Aufrufe an Aspose.Cells-Webdienste tätigen:
