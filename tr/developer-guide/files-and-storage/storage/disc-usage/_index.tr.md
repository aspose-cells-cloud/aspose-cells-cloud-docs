---
title: Disk Kullanımı
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/storage/disc-usage/
keywords: Learn how to get disc-usage with Aspose Cells Cloud REST API
description: Aspose Cells Cloud REST API SDK desteği geliştirme dili türleri ile disk kullanımını nasıl alacağınızı öğrenin. Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve Swift'i içerir
weight: 100
---
Bu REST API, `get disc usage`'i gösterir.
 
## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/storage/disc
 
```
 İstek parametreleri şunlardır:
 
| Parametre adı| Tip| Yol/Sorgu Dizesi/HTTPBody|Tanım|
|:- |:- |:- |:- |
| depolamaAdı| sicim| sorgu| Depolama adı|

 
 bu[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Storage/GetDiscUsage) herkesin erişebileceği bir programlama arabirimi tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.
 
Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'e nasıl çağrı yapılacağını gösterir.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName21="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/disc" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="12" >}}
 
```bash
{
  "UsedSize": 0,
  "TotalSize": 0
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Bulut SDK Ailesi
 
 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, alt düzey ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanızı sağlar. Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.
 
Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanılarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını gösterir:
 
 