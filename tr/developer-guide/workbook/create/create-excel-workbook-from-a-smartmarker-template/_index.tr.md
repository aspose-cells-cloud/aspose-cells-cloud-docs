---
title: Akıllı işaretçi şablonuyla Excel çalışma kitabı nasıl oluşturulur?
second_title: Aspose.Cells Cloud Documen
linktitle: akıllı marka
type: docs
url: /tr/workbook/create/smartmarker/
aliases: [/create-excel-workbook-from-a-smartmarker-template/,/workbook/smartmarker/]
keywords: How to create an Excel workbook with a smart marker template
description: Aspose.Cells Cloud REST API akıllı işaretçi şablonuyla Excel çalışma kitabı nasıl oluşturulur. SDK, geliştirme dili türlerini destekler. Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve Swift'i içerir
weight: 40
---
Bu REST API, `smart marker` ile `workbook` oluşturmayı belirtir.

**Sorgu Parametresi**

|Parametre adı|Tip|Tanım|
|:- |:- |:- |
|xmlDosyası|sicim||
|çıkış yolu|sicim||
|dosya|sicim|Orijinal çalışma kitabı klasörü.|
|depolamaAdı|sicim|Depolama adı.|

**İstek Gövde Parametresi**

|Parametre adı|Tip|Tanım|
|:- |:- |:- |
|xmlDosyası|dosya||


## DİNLENME API

|**API**|**Tip**|**Tanım**|**Havalı Bağlantı**|
|:- |:- |:- |:- |
|/hücreler/{isim}/smartmarker|POSTALAMAK|SmartMarker şablon dosyasından yeni bir Excel Çalışma Kitabı oluşturun|[PostWorkbookGetSmartMarkerResult](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookGetSmartMarkerResult)|


 bu[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookGetSmartMarkerResult) herkesin erişebileceği bir programlama arabirimi tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

 Kullanabilirsiniz**cURL** Aspose.Cells web hizmetlerine kolayca erişmek için komut satırı aracı. Aşağıdaki örnek, cURL ile Cloud API'e nasıl çağrı yapılacağını gösterir.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/newworkbook_14.xlsx/smartmarker?xmlFile=Sample_SmartMarker_Data.xml" -H "accept: multipart/form-data" -H "x-aspose-client: Containerize.Swagger"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

HttpResponseMessage with the processing result in content.

}

```

{{< /tab >}}

{{< /tabs >}}


## Bulut SDK Ailesi

 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, alt düzey ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanızı sağlar. Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanılarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını gösterir:


{{< tabs tabTotal="11" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" tabName11="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorkbookPostWorkbookGetSmartMarkerResult.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-workbook-CreateWorkbookFromSmartMarkerTemplate-create-from-smart-marker.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PutWorkbookCreate-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Workbook-create_new_workbook-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "CreateExcelWorkbookFromSmartMarkerTemplate.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Workbook-CreateWorkbookFromSmartMakerTemplate-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-workbook-CreateWorkbookFromSmartMarkerTemplate-create-from-smart-marker.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Workbook-CreateWorkbookFromSmartMakerTemplate-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "42b369351a3909d9f38916d9f6e10d9a" >}}

{{< /tab >}}

{{< tab tabNum="11" >}}

{{< gist "aspose-cells-cloud-gists" "f83596a0e742321c1a0296332804d047" >}}

{{< /tab >}}

{{< /tabs >}}
