---
title: Toplu Bölme
second_title: Documen
type: docs
url: /tr/batch/split
keywords: Batch split Excel file
description: Aspose.Cells Cloud API, toplu bölme dosyasını destekler. SDK, çeşitli geliştirme dillerini destekler. Bunlar arasında Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve Swift bulunur.
weight: 100
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, Json, Markdown, Toplu Bölme
---
Bu REST API uygun dosyanın `batch split` olduğunu gösterir.

## RSET API

```bash
 
POST http://api.aspose.cloud/v3.0/cells/batch/split
 
```

İstek parametreleri şunlardır:

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi|Tanım|
|:- |:- |:- |:- |
| Toplu Bölme İsteği|| vücut||

**BatchSplitRequest Özellikleri**

Adı | Türü | Açıklama | Notlar
------------ | ------------- | ------------- | -------------
 KaynakKlasörü | dize | | [isteğe bağlı]KaynakDepolama | dize | | [isteğe bağlı]EşleşmeKoşulu | EşleşmeKoşuluİsteği | | [isteğe bağlı]Biçim | dize | | [isteğe bağlı]KaynakDizin | tamsayı | | [isteğe bağlı]İndeks | tamsayı | | [isteğe bağlı]ÇıkışKlasörü | dize | | [isteğe bağlı]KaydetmeSeçenekleri | KaydetmeSeçenekleri | | [isteğe bağlı]**MatchConditionRequest Özellikleri**

Adı | Türü | Açıklama | Notlar
------------ | ------------- | ------------- | -------------
 RegexPattern | dize | | [isteğe bağlı]FullMatchConditions | dize[]| | [isteğe bağlı][OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/Batch/PostBatchSplit) herkesin erişebileceği bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

cURL komut satırı aracını kullanarak Aspose.Cells web servislerine kolayca erişebilirsiniz. Aşağıdaki örnek, cURL ile API Cloud'a nasıl çağrı yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/batch/split" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
-D "{\"SourceFolder\":\"CellsTests\",\"OutFolder\":\"Output\",\"MatchCondition\":{\"RegexPattern\":\"(^Book)(.+)(xlsx$)\"},\"Format\":\"pdf\"}" 
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```bash
{
"Code": 200,
"Status": "OK"
}
 
```

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Ailesi

 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, düşük seviyeli ayrıntılarla ilgilenir ve bölünmüş görevlerinize odaklanmanızı sağlar. Lütfen şuraya göz atın:[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.

Aşağıdaki kod örnekleri çeşitli SDK'ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

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
