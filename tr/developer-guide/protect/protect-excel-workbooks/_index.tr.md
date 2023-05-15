---
title: Excel Workboo'yu koruyun
second_title: Aspose.Cells Cloud Documen
linktitle: Korumak
type: docs
url: /tr/workbook/protect/
aliases: [/protect-excel-workbooks/]
keywords: Protect Excel files
description: Aspose.Cells Cloud REST API, Excel dosyalarının korunmasını destekler. SDK, geliştirme dili türlerini destekler. Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve Swift'i içerir
weight: 30
---
Bu REST API, bir Excel `workbook`'i korur.

**Sorgu Parametresi**

|Parametre adı|Tip|Tanım|
|:- |:- |:- |
|dosya|sicim|Orijinal çalışma kitabı klasörü.|
|depolamaAdı|sicim|Depolama adı.|

**İstek Gövde Parametresi**

|Parametre adı|Tip|Tanım|
|:- |:- |:- |
|koruma|Çalışma Kitabı Koruma Talebi||

**Çalışma Kitabı Koruma Talebi**

|Parametre adı|Tip|Tanım|
|:- |:- |:- |
|Koruma Türü|sicim|TÜMÜ/ İÇİNDEKİLER/HİÇBİRİ/NESNELER/SENARYOLAR/YAPI/PENCERELER|
|Şifre|sicim||



## DİNLENME API

|**API**|**Tip**|**Tanım**|**Havalı Bağlantı**|
|:- |:- |:- |:- |
|/hücreler/{isim}/koruma|POSTALAMAK|Bir belgeyi koruyun|[Koruma Sonrası Belgesi](https://apireference.aspose.cloud/cells/#/Workbook/PostProtectDocument)|

 bu[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Workbook/PostProtectDocument) herkesin erişebileceği bir programlama arabirimi tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

 Kullanabilirsiniz**cURL** Aspose.Cells web hizmetlerine kolayca erişmek için komut satırı aracı. Aşağıdaki örnek, cURL ile Cloud API'e nasıl çağrı yapılacağını gösterir.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/protection" -H "accept: application/json" -H "Content-Type: application/json" -d "{ \"ProtectionType\": \"all\", \"Password\": \"aspose\"}"

```

{{< /tab >}}

{{< tab tabNum="2" >}}

```java

{

  "Code":"200",

  "Status":"OK"

}

```

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Ailesi

 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, alt düzey ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanızı sağlar. Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanılarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını gösterir:

{{< tabs tabTotal="11" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" tabName11="Swift" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorkbookPostProtectDocument.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-workbook-ProtectWorkbook-protect-excel-workbook.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Workbook-PostProtectDocument-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Document-protect_document-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "ProtectExcelWorkbooks.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Workbook-ProtectWorkbook-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-workbook-ProtectWorkbook-protect-excel-workbook.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "example-encrypt-with-password.go" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Workbook-ProtectWorkbook-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "81821b7ead61ba5371d2b1130aba0c2f" >}}

{{< /tab >}}

{{< tab tabNum="11" >}}

{{< gist "aspose-cells-cloud-gists" "5a57805e300750236fa567e015f1677b" >}}

{{< /tab >}}

{{< /tabs >}}
