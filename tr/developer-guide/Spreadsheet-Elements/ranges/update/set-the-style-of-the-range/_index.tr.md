﻿---
title: Çalma Tarzını Ayarla
second_title: Aspose.Cells Cloud Documen
linktitle: Stil ayarla
type: docs
url: /tr/ranges/update/style/
aliases: [/set-the-style-of-the-range/]
keywords: Set range style on an Excel workshee
description: Aspose.Cells Cloud REST API, Excel çalışma sayfasında aralık stilini ayarlamayı destekler. SDK, çeşitli geliştirme dillerini destekler. Bunlara Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve swift dahildir
weight: 70
kwords: Excel, Office Bulut, REST API, E-Tablo, PDF, CSV, Json, Markdown, Aralığın Stilini Ayarla
---
## **giriiş**
Bu örnek, uygulamalarınızda Aspose.Cells Cloud API kullanarak aralığın stilini ayarlamanıza olanak tanır. REST API'imizi herhangi bir dille kullanabilirsiniz: .NET, Java, PHP, Ruby, Rails, Python, jQuery ve daha fazlası.
## **API Bilgi**

|**API**|**Tip**|**Tanım**|**Kaynak Bağlantısı**|
|:- |:- |:- |:- |
|/hücreler/{isim}/çalışma sayfaları/{sayfaAdı}/aralıklar/stil|POSTALAMAK|Adlandırılmış bir aralığın hücre stilini ayarlayın|[PostWorksheetHücrelerAralıkStili](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeStyle)|
### **cURL Örnek**
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
## **SDK Kaynağı**
Aspose.Cells Bulut SDK'ları aşağıdaki sayfadan indirilebilir:[Mevcut SDK'lar](/cells/tr/available-sdks/)
### **SDK Örnekleri**
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
