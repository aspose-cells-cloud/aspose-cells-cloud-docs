---
title: Ställ in stilen för Rang
second_title: Documen
linktitle: Ställ in stil
type: docs
url: /sv/ranges/update/style/
aliases: [/set-the-style-of-the-range/]
keywords: Set range style on an Excel workshee
description: Aspose.Cells Cloud REST API stöder inställning av intervallstil på ett Excel-arbetsblad. SDK stöder olika typer av utvecklingsspråk. Dessa inkluderar Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby och Swift.
weight: 70
kwords: Excel, Office Moln, REST API, Kalkylblad, PDF, CSV, Json, Markdown, Ange intervallets stil
---
## **Introduktion**
I det här exemplet kan du ställa in stilen för intervallet med hjälp av Aspose.Cells Cloud API i dina applikationer. Du kan använda vår REST API med vilket språk som helst: .NET, Java, PHP, Ruby, Rails, Python, jQuery och många fler.
## **API Information**

|**API**|**Typ**|**Beskrivning**|**Resurslänk**|
|:- |:- |:- |:- |
|/celler/{namn}/arbetsblad/{arknamn}/intervall/stil|POSTA|Ange cellstilen för ett namngivet område|[PostWorksheetCellerOmfångStil](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeStyle)|
### **cURL Exempel**
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/style" -H "accept: application/json" -H "Content-Type: application/json" -d "{ \"Range\": { \"ColumnCount\": 2, \"ColumnWidth\": 0, \"FirstColumn\": 1, \"FirstRow\": 1, \"Name\": \"string\", \"RefersTo\": \"string\", \"RowCount\": 2, \"RowHeight\": 0, \"Worksheet\": \"Sheet1\" }, \"Style\": { \"Font\": { \"DoubleSize\": 1, \"IsBold\": true, \"IsItalic\": true, \"IsStrikeout\": true, \"IsSubscript\": true, \"IsSuperscript\": true } }}"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "Code": 200,

  "Status": "OK"

}

```

{{< /tab >}}

{{< /tabs >}}
## **SDK-källa**
Cloud SDK:erna Aspose.Cells kan laddas ner från följande sida:[Tillgängliga SDK:er](/cells/sv/available-sdks/)
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
