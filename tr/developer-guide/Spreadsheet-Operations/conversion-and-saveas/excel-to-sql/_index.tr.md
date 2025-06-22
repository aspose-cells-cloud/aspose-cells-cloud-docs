---
title: Excel SQ'ya
second_title: Aspose.Cells Cloud Documen
linktitle: Excel SQ'ya
type: docs
url: /tr/convert-excel-file-to-sql-file/
keywords: Convert excel files to sql files
description: Aspose.Cells Cloud REST API excel dosyalarını sql dosyalarına dönüştürmeyi destekler. SDK çeşitli geliştirme dillerini destekler. Bunlara Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve swift dahildir
weight: 100
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, Json, Markdown, Excel'den SQL'e
---
Bu REST API, `convert`'e bir elektronik tablo dosyasının sql formatlı bir dosyaya dönüştürüldüğünü gösterir.

**Sorgu Parametresi**

|Parametre Adı|Tip|Tanım|
|:- |:- |:- |
|şifre|sicim| Excel dosyasını açmak için gereken şifre.|
|depolamaAdı|sicim| Dosyanın bulunduğu depolama adı.|
|checkExcelKısıtlama|bool| Kullanıcı hücrelerle ilgili nesneleri değiştirdiğinde Excel dosyasının kısıtlamasını kontrol edin.|

**İstek Gövde Parametresi**

|Parametre Adı|Tip|Tanım|
|:- |:- |:- |
|veri dosyası| veri dosyası|Veri dosyası çok parçalı içeriğin ilk bölümüne kaydedilir.|

**Cevap**

[Dosya bilgisi](/cells/tr/file-info/)

## REST API Şartname

|**API**|**Tip**|**Tanım**|**Swagger Bağlantısı**|
|:- |:- |:- |:- |
|/hücreler/dönüştür/sql|POSTALAMAK|Bir elektronik tabloyu sql dosyasına dönüştürün.|[PostConvertWorkbookToSQL](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToSQL)|

 The[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToSQL) herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

 Kullanabilirsiniz**cURL** Aspose.Cells web servislerine kolayca erişmek için komut satırı aracı. Aşağıdaki örnek, cURL ile Cloud API'e nasıl çağrı yapılacağını gösterir.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/sql" 
     -H "accept: multipart/form-data" 
     -H "Content-Type: multipart/form-data" 
     -H "x-aspose-client: curl" 
     -d {"File":{}}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```

{
  "Filename": "xxxxxx.json",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}

```

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Ailesi

 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, düşük seviyeli ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanızı sağlar. Lütfen şuraya göz atın:[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:
{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToSQL.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToSQL.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToSQL.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToSQL.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToSQL.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToSQL.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToSQL.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToSQL.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Diğer API'ler bu işlevi uygular

[POST /hücreler/{isim}/kaydet](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs) API, MS Excel dosyasını ek ayarlarla HTML dosyası olarak kaydetmenizi ve sonucu depolama alanına kaydetmenizi sağlar.

Bu REST API `convert` excel dosyasını HTML'e kopyalayın.

[PUT /hücreler/dönüştür](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) API, MS Excel dosyasını ek ayarlarla HTML dosyasına dönüştürmenizi ve sonucu yanıta kaydetmenizi sağlar.

Bu REST API `export` excel dosyasını HTML'e kopyalayın.

[GET /hücreler/{isim}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook  ) API, MS Excel dosyasını ek ayarlarla HTML dosyasına dönüştürmenizi ve sonucu yanıta kaydetmenizi sağlar.
