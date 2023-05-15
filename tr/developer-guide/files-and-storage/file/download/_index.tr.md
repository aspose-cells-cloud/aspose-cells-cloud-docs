---
title: Dosyayı İndir
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/file/download/
keywords: Learn how to download file with Aspose Cells Cloud REST API
description: Aspose Cells Cloud REST API SDK destekli geliştirme dili türleriyle dosya indirmeyi öğrenin. Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve Swift'i içerir
weight: 100
---
Bu REST API, `download file`'i gösterir.
 
## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/storage/file/{path}
 
```
 İstek parametreleri şunlardır:
 
| Parametre adı| Tip| Yol/Sorgu Dizesi/HTTPBody|Tanım|
|:- |:- |:- |:- |
| yol| sicim| yol| Dosya yolu, örneğin '/klasör/dosya.ext'|
| depolamaAdı| sicim| sorgu| Depolama adı|
| sürüm kimliği| sicim| sorgu| İndirilecek dosya sürümü kimliği|
 
 bu[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/File/DownloadFile) herkesin erişebileceği bir programlama arabirimi tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.
 
Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'e nasıl çağrı yapılacağını gösterir.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/Book1.xlsx" \
-X GET \
-H "Content-Type: application/json" \
-H "accept: multipart/form-data" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="12" >}}
 
```bash

{
    Stream
}

```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Bulut SDK Ailesi
 
 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, alt düzey ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanızı sağlar. Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.
 
Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanılarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını gösterir:
 
 
 
 

