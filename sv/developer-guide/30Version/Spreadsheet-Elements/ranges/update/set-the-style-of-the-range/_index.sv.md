---
title: "Ställ in intervallstil – Aspose.Cells Cloud API"
second_title: "Dokumentation"
linktitle: "Ställ in intervallstil"
type: docs
url: /ranges/update/style/
aliases: [/set-the-style-of-the-range/]
keywords: "Aspose.Cells, intervallstil, API, Excel, moln"
description: "Lär dig hur du ställer in stilen för ett cellintervall i ett Excel-ark med Aspose.Cells Cloud REST API. Inkluderar autentiseringssteg, begäranformat, svarsdetaljer och SDK-exempel för .NET, Java, Python, Go och mer."
weight: 70
---

## **Introduktion**
Detta exempel visar hur du ställer in stilen för ett intervall med Aspose.Cells Cloud API. Du kan anropa API:t från många programmeringsspråk, såsom .NET, Java, PHP, Ruby, Python, JavaScript (jQuery) och andra.

## **API-info**

| API                                                   | Typ  | Beskrivning                              | Resurslänk                                                                                                                                      |
| ----------------------------------------------------- | ---- | ---------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- |
| /cells/{name}/worksheets/{sheetName}/ranges/style     | POST | Ställ in cellstilen för ett namngivet intervall | [PostWorksheetCellsRangeStyle](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeStyle) |

### **cURL-exempel**  

{{< tabs tabTotal="2" tabID="1" tabName1="Begäran" tabName2="Svar" >}}

{{< tab tabNum="1" >}}

**Förutsättningar**  
1. Skaffa en åtkomsttoken via OAuth2-klientautentisering (`POST https://api.aspose.cloud/connect/token`).  
2. Inkludera headern `Authorization: Bearer <access_token>` i varje begäran.  

**Begäran**  

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

*Objektet `Range` anger övre vänstra cellen och storleken på intervallet. Objektet `Style` innehåller formateringsalternativen som ska tillämpas.*

{{< /tab >}}

{{< tab tabNum="2" >}}

**Svar**  

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Felhantering** – Vid misslyckade anrop returnerar API:t lämplig HTTP-statuskod (t.ex. 400, 401, 500) tillsammans med en JSON-kropp som innehåller fälten `Error` och `Message`. Kontrollera värdet på `Code`; alla resultat som inte är 200 bör loggas och hanteras enligt din felhanteringspolicy.

{{< /tab >}}

{{< /tabs >}}

## **SDK-källa**  
Aspose.Cells Cloud SDK:er kan laddas ner från följande sida: [Tillgängliga SDK:er](/cells/available-sdks/)

### **SDK-exempel**  
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