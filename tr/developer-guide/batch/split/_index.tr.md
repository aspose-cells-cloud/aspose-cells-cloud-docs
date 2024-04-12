---
title: Toplu Bölme
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/batch/split
keywords: Batch split Excel file
description: Aspose.Cells Bulut API toplu bölünmüş dosyayı destekler. SDK çeşitli geliştirme dillerini destekler. Bunlar arasında Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve Swift bulunur
weight: 100
---
Bu REST API, uygun dosyanın `batch split`'ini gösterir.
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/batch/split
 
```
 İstek parametreleri şunlardır:
 
| Parametre adı| Tip| Yol/Sorgu Dizesi/HTTPBody|Tanım|
|:- |:- |:- |:- |
| Toplu Bölme İsteği|| vücut||

**BatchSplitRequest Özellikleri**
 
İsim | Tür | Açıklama | Notlar
------------ | ------------- | ------------- | -------------
 KaynakKlasörü | dize | | [isteğe bağlı]KaynakDepolama | dize | | [isteğe bağlı]Eşleşme Durumu | Eşleşme DurumuTalebi | | [isteğe bağlı]Biçim | dize | | [isteğe bağlı]FromIndex | tamsayı | | [isteğe bağlı]ToIndex | tamsayı | | [isteğe bağlı]ÇıkışKlasörü | dize | | [isteğe bağlı]Kaydetme Seçenekleri | Seçenekleri Kaydet | | [isteğe bağlı]**MatchConditionRequest Özellikleri**
 
İsim | Tür | Açıklama | Notlar
------------ | ------------- | ------------- | -------------
 Normal Regex Deseni | dize | | [isteğe bağlı]Tam Eşleşme Koşulları | dize[]| | [isteğe bağlı][OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/Batch/PostBatchsplit) herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.
 
Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnekte, cURL ile Cloud API'e nasıl çağrı yapılacağı gösterilmektedir.
 
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
 
SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, düşük düzeyli ayrıntılarla ilgilenir ve bölünmüş görevlerinize odaklanmanıza olanak tanır. Lütfen şuraya göz atın:[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.
 
Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını gösterir:
 
 
  
{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

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

{{< tab tabNum="10" >}}


{{< /tab >}}

{{< /tabs >}}

