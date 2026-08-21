---
title: "Bild in Excel-Arbeitsblatt importieren"
ArticleTitle: "Bild in Excel-Arbeitsblatt importieren – Aspose.Cells Cloud API-Anleitung"
second_title: "Dokument"
linktitle: "Bild importieren"
type: docs
url: /de/import-picture-into-excel-worksheet/
aliases:
  - /import-picture-into-worksheet/
  - /import-data/picture/
  - /import/picture/
keywords: "Bild importieren, Excel, Aspose.Cells Cloud, REST API, v3.0"
description: "Erfahren Sie, wie Sie Bilder mithilfe der Aspose.Cells Cloud REST API v3.0 in Excel-Arbeitsblätter importieren können. Enthält Beispiele für Multipart-Anfragen, SDK-Codebeispiele und Anleitungen zur Fehlerbehandlung. Beginnen Sie schnell und einfach mit klar strukturierten Schritten."
weight: 19
---

Das Importieren eines Bildes in ein Excel-Arbeitsblatt ermöglicht es Ihnen, Tabellenkalkulationen mit visuellen Inhalten wie Logos, Diagrammen oder Grafiken anzureichern. Diese Anleitung zeigt, wie die Aspose.Cells Cloud-**ImportPicture**-Operation, das erforderliche Anforderungsformat und die Behandlung von Antworten verwendet werden.

**Voraussetzungen:** Sie müssen über ein gültiges JWT-Authentifizierungstoken und eine bereits in Aspose Cloud Storage gespeicherte Arbeitsmappe verfügen, bevor Sie den Importvorgang ausführen können.

## PostImportData API

```http
POST https://api.aspose.cloud/v3.0/cells/import
```

### **Sicherheit und Authentifizierung**

Die Aspose.Cells Cloud APIs sind sicher und erfordern eine <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT-Token-basierte Authentifizierung</a>.

### **Anforderungsparameter**

Die Anforderung ist ein HTTP-**POST** mit **multipart/related**-Inhalt (siehe [RFC 2046](https://tools.ietf.org/html/rfc2046#page-17) oder [RFC 1341](https://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)).

- Der **erste Teil** enthält ein JSON-Objekt mit dem Namen **ImportPictureOption**, das beschreibt, wo und wie das Bild platziert werden soll.
- Der **zweite Teil** überträgt die Bilddatei (oder deren Base64-kodierten Daten).

### ImportPictureOption – Definition

```json
{
  "UpperLeftRow": 0,
  "UpperLeftColumn": 0,
  "LowerRightRow": 10,
  "LowerRightColumn": 5,
  "Filename": "logo.png",
  "Data": "iVBORw0KGgoAAAANSUhEUgAA...",
  "DestinationWorksheet": "Sheet1",
  "IsInsert": true,
  "ImportDataType": "Picture",
  "Source": { "FileSource": "Storage" }
}
```

_`IsInsert` ist ein **Boolean** – `true` fügt ein neues Bild ein, `false` ersetzt ein vorhandenes._

### Wichtige Parameter

**ImportPictureOption**

| Parametername          | Typ         | Beschreibung                                                                                                                                                                                                 |
| ---------------------- | ----------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| UpperLeftRow           | int         | Zeilenindex der oberen linken Ecke, an der das Bild platziert werden soll.                                                                                                                                   |
| UpperLeftColumn        | int         | Spaltenindex der oberen linken Ecke, an der das Bild platziert werden soll.                                                                                                                                  |
| LowerRightRow          | int         | Zeilenindex der unteren rechten Ecke, die die Grenzen des Bildes definiert.                                                                                                                                  |
| LowerRightColumn       | int         | Spaltenindex der unteren rechten Ecke, die die Grenzen des Bildes definiert.                                                                                                                                 |
| Filename               | string      | Name der Bilddatei.                                                                                                                                                                                          |
| Data                   | string      | Base64-kodiertes Binärdaten des Bildes (optional, wenn die Datei als zweiter Teil gesendet wird).                                                                                                            |
| DestinationWorksheet   | string      | Name des Arbeitsblatts, in das das Bild eingefügt werden soll.                                                                                                                                               |
| **IsInsert**           | **boolean** | `true`, um ein neues Bild einzufügen; `false`, um ein vorhandenes zu ersetzen.                                                                                                                                |
| ImportDataType         | string      | Art der zu importierenden Daten (z. B. `Picture`, `IntArray`, `DoubleArray`, `StringArray`, `TwoDimensionIntArray`, `TwoDimensionDoubleArray`, `TwoDimensionStringArray`, `BatchData`, `csvData`).         |
| Source                 | FileSource  | Gibt den Speicherort der Datendatei an, wenn der `BatchData`-Parameter null ist.                                                                                                                             |

### Antwort

Eine erfolgreiche Anforderung gibt **HTTP 200** mit einer JSON-Antwort zurück, die folgendermaßen aussieht:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Mögliche Statuscodes:

| Code | Bedeutung                               |
| ---- | --------------------------------------- |
| 200  | Import erfolgreich                      |
| 400  | Ungültige Anforderung – fehlende oder ungültige Daten |
| 401  | Nicht autorisiert – ungültiges oder fehlendes Token |
| 500  | Interner Serverfehler                   |


## Verwendung der PostImportData API mit SDKs

### PostImportData API-Spezifikation

Die [OpenAPI-Spezifikation](https://apireference.aspose.cloud/cells/#/LightCells/PostImport) definiert eine öffentlich zugängliche Programmierschnittstelle und ermöglicht es Ihnen, REST-Interaktionen direkt aus einem Webbrowser durchzuführen.

### Verwendung der Aspose.Cells Cloud SDKs


Die Verwendung eines SDKs ist die beste Möglichkeit, die Entwicklung zu beschleunigen. Ein SDK übernimmt die Low-Level-Details, sodass Sie sich auf die Aufgaben Ihres Projekts konzentrieren können. Eine vollständige Liste der Aspose.Cells Cloud SDKs finden Sie im [GitHub-Repository](https://github.com/aspose-cells-cloud).

Die folgenden Codebeispiele zeigen, wie Aspose.Cells-Webdienste mithilfe verschiedener SDKs aufgerufen werden:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js"  tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}
{{< /tab >}}

{{< /tabs >}}
---