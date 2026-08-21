---
title: "Ganzzahl-Array in Excel-Arbeitsblatt importieren"
linktitle: "Ganzzahl-Array importieren"
type: docs
url: /de/import-integer-array-into-excel-worksheet/
aliases:
  - /import-integer-array-into-excel-worksheet/
  - /import-integer-array-into-worksheet/
  - /import-data/integer-array/
  - /import/integer-array/
keywords: "Aspose.Cells Cloud, Excel, Ganzzahl-Array importieren, REST API, SDK, C#, PHP, Ruby, Java, Python"
description: "Erfahren Sie, wie Sie ein Ganzzahl-Array mit der Aspose.Cells Cloud REST API in ein Excel-Arbeitsblatt importieren können. Enthält die Anforderungssyntax, Parameter, Beispielcode für mehrere SDKs und Antwortdetails."
weight: 30
ArticleTitle: "Ganzzahl-Array in Excel-Arbeitsblatt importieren – Aspose.Cells Cloud API"
---

Diese REST API importiert ein Ganzzahl-Array in ein Excel-Arbeitsblatt.

Die Anforderung muss ein HTTP-**POST** mit Multiteil-Inhalt sein (siehe [RFC 2046](http://tools.ietf.org/html/rfc2046#page-17) oder [RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Der erste Teil des Multiteil-Körpers enthält das JSON-Payload für **ImportIntegerArrayOption**, der zweite Teil enthält die Quelldatendatei (z. B. eine CSV- oder binäre Excel-Datei).

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

Beide Endpunkte akzeptieren denselben Multiteil-Inhalt. Der erste Endpunkt führt eine allgemeine Importoperation durch, während der zweite auf eine spezifische Arbeitsmappe mit dem Namen `{name}` abzielt.

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter**

### ImportIntegerArrayOption

| Parametername           | Typ        | Beschreibung                                                                                                                                                                                    |
| ----------------------- | ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **FirstRow**            | int        | Nullbasierter Index der ersten Zeile, in die die Daten eingefügt werden sollen.                                                                                                                |
| **FirstColumn**         | int        | Nullbasierter Index der ersten Spalte, in die die Daten eingefügt werden sollen.                                                                                                               |
| **IsVertical**          | boolean    | `true`, um das Array vertikal (einer Spalte nach unten) einzufügen; `false`, um es horizontal (einer Zeile quer) einzufügen.                                                                   |
| **Data**                | Integer[]  | Das zu importierende Ganzzahl-Array.                                                                                                                                                            |
| **DestinationWorksheet**| string     | Name des Arbeitsblatts, das die Daten empfangen soll.                                                                                                                                          |
| **IsInsert**            | boolean    | `true`, um Zeilen/Spalten einzufügen, bevor die Daten geschrieben werden; `false`, um vorhandene Zellen zu überschreiben.                                                                      |
| **ImportDataType**      | string     | Art der importierten Daten. Gültige Werte: `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`.   |
| **Source**              | FileSource | Gibt die Position der Datendatei an, wenn der Parameter **BatchData** `null` ist.                                                                                                              |

#### Beispiel für Anforderungstext

```json
{
  "Data": [1, 2, 4],
  "DestinationWorksheet": "Sheet1",
  "FirstRow": 1,
  "FirstColumn": 2,
  "IsVertical": true,
  "IsInsert": true,
  "ImportDataType": "IntArray"
}
```

### Antwort

Eine erfolgreiche Anforderung gibt **HTTP 200** mit einem JSON-Payload zurück, der folgendermaßen aussieht:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Mögliche Statuscodes:

| Code | Bedeutung                                     |
| ---- | --------------------------------------------- |
| 200  | Import erfolgreich                             |
| 400  | Ungültige Anforderung – fehlende oder ungültige Daten |
| 401  | Nicht autorisiert – ungültiges oder fehlendes Token |
| 500  | Interner Serverfehler                         |

## Verwendung der PostImportData API mit SDKs

### PostImportData API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht REST-Interaktionen direkt aus einem Webbrowser.

### Verwendung von Aspose.Cells Cloud SDKs

Die Verwendung eines SDKs ist die schnellste Möglichkeit, diese Funktion zu integrieren. SDKs verbergen die niederstufigen Details und ermöglichen es Ihnen, sich auf Ihre Geschäftslogik zu konzentrieren. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webservices mit verschiedenen SDKs aufgerufen werden:

{{< tabs tabTotal="3" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-ImportData-PostImportDataCloudFile-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostImportDataCloudFile-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-post_import_data-.rb" >}}

{{< /tab >}}

{{< /tabs >}}
---