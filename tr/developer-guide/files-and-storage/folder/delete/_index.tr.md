---
title: Klasörü Sil
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/folder/delete/
keywords: Learn how to delete folder with Aspose Cells Cloud REST API
description: Aspose Cells Cloud REST API SDK destekli geliştirme dili türleri ile klasörü nasıl sileceğinizi öğrenin. Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve Swift'i içerir
weight: 100
---
Bu REST API, `delete folder`'i gösterir.
 
## RSET API
 
```bash
 
DELETE http://api.aspose.cloud/v3.0/cells/storage/folder/{path}
 
```
 İstek parametreleri şunlardır:
 
| Parametre adı| Tip| Yol/Sorgu Dizesi/HTTPBody|Tanım|
|:- |:- |:- |:- |
| yol| sicim| yol| Klasör yolu, örneğin '/klasör'|
| depolamaAdı| sicim| sorgu| Depolama adı|
| özyinelemeli| mantıksal| sorgu| YANLIŞ|

 
 bu[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Folder/DeleteFolder) herkesin erişebileceği bir programlama arabirimi tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.
 
Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'e nasıl çağrı yapılacağını gösterir.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/desfolder" \
-X DELETE \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
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
 
 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, alt düzey ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanızı sağlar. Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.
 
Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanılarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını gösterir:
 

