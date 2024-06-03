---
title: Imposta lo stile del suono
second_title: Aspose.Cells Cloud Documen
linktitle: Imposta stile
type: docs
url: /it/ranges/update/style/
aliases: [/set-the-style-of-the-range/]
keywords: Set range style on an Excel workshee
description: Aspose.Cells Cloud REST API supporta l'impostazione dello stile dell'intervallo su un foglio di lavoro Excel. L'SDK supporta tipi di linguaggi di sviluppo. Includono Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby e swift
weight: 70
kwords: Excel, Office Cloud, REST API, Foglio di calcolo, PDF, CSV, Json, Markdwon, Imposta lo stile dell'intervallo
---
## **introduzione**
Questo esempio ti consente di impostare lo stile dell'intervallo, utilizzando Aspose.Cells Cloud API nelle tue applicazioni. Puoi utilizzare il nostro REST API con qualsiasi lingua: .NET, Java, PHP, Ruby, Rails, Python, jQuery e molti altri.
## **API Informazioni**

|**API**|**Tipo**|**Descrizione**|**Collegamento alle risorse**|
|:- |:- |:- |:- |
|/cells/{nome}/worksheets/{sheetName}/ranges/style|INVIARE|Imposta lo stile della cella di un intervallo denominato|[PostWorksheetCellsRangeStyle](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeStyle)|
### **cURL Esempio**
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
## **Origine dell'SDK**
Gli SDK Cloud Aspose.Cells possono essere scaricati dalla seguente pagina:[SDK disponibili](/cells/it/available-sdks/)
### **Esempi di SDK**
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
