---
title: "Bereichsformat festlegen – Aspose.Cells Cloud API"
second_title: "Dokumentation"
linktitle: "Bereichsformat festlegen"
type: docs
url: /de/ranges/update/style/
aliases: [  /de/set-the-style-of-the-range/ ]
keywords: "Aspose.Cells, Bereichsformat, API, Excel, Cloud"
description: "Erfahren Sie, wie Sie das Format eines Zellbereichs in einem Excel-Arbeitsblatt mithilfe der Aspose.Cells Cloud REST API festlegen. Enthält Authentifizierungsschritte, Anforderungsformat, Antwortdetails und SDK-Beispiele für .NET, Java, Python, Go und weitere."
weight: 70
---

## **Einführung**
Dieses Beispiel zeigt, wie das Format eines Bereichs mithilfe der Aspose.Cells Cloud API festgelegt wird. Sie können die API aus vielen Programmiersprachen wie .NET, Java, PHP, Ruby, Python, JavaScript (jQuery) und weiteren aufrufen.

## **API-Informationen**

| API                                                   | Typ  | Beschreibung                              | Ressourcenlink                                                                                                                                 |
| ----------------------------------------------------- | ---- | ----------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| /cells/{name}/worksheets/{sheetName}/ranges/style     | POST | Format einer benannten Zellbereichs festlegen | [PostWorksheetCellsRangeStyle](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeStyle) |

### **cURL-Beispiel**

{{< tabs tabTotal="2" tabID="1" tabName1="Anforderung" tabName2="Antwort" >}}

{{< tab tabNum="1" >}}

**Voraussetzungen**  
1. Holen Sie sich ein Zugriffstoken über den OAuth2-Client-Credentials-Flow (`POST https://api.aspose.cloud/connect/token`).  
2. Fügen Sie den Header `Authorization: Bearer <access_token>` in jede Anforderung ein.  

**Anforderung**  

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/style" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{
           "Range": {
               "FirstRow": 1,
               "FirstColumn": 1,
               "RowCount": 2,
               "ColumnCount": 2,
               "Worksheet": "Sheet1"
           },
           "Style": {
               "Font": {
                   "IsBold": true,
                   "IsItalic": true,
                   "IsStrikeout": true,
                   "IsSubscript": true,
                   "IsSuperscript": true,
                   "DoubleSize": 1
               }
           }
         }'
```

*Das `Range`-Objekt gibt die obere linke Zelle und die Größe des Bereichs an. Das `Style`-Objekt enthält die anzuwendenden Formatierungsoptionen.*

{{< /tab >}}

{{< tab tabNum="2" >}}

**Antwort**  

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Fehlerbehandlung** – Bei nicht erfolgreichen Aufrufen gibt die API einen entsprechenden HTTP-Statuscode (z. B. 400, 401, 500) zusammen mit einem JSON-Text zurück, der die Felder `Error` und `Message` enthält. Prüfen Sie den `Code`-Wert; jedes Ergebnis ungleich 200 sollte protokolliert und entsprechend Ihrer Fehlerbehandlungsrichtlinie verarbeitet werden.

{{< /tab >}}

{{< /tabs >}}

## **SDK-Quellcode**
Die Aspose.Cells Cloud SDKs können von der folgenden Seite heruntergeladen werden: [Verfügbare SDKs](/cells/available-sdks/)

### **SDK-Beispiele**
{{< tabs tabTotal="4" tabID="4" tabName1="PHP" tabName2="Ruby" tabName3="Objective C" tabName4="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "81d7e60eaf43ae7192df00993997afde" >}}

{{< /tab >}}

{{< /tabs >}}
---