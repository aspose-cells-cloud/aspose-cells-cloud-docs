---
title: Dosyayı Taşı
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/file/move/
keywords: Learn how to download file with Aspose Cells Cloud REST API
description: Aspose Cells Cloud REST API SDK destekli geliştirme dili türleriyle dosya indirmeyi öğrenin. Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve Swift'i içerir
weight: 100
---
Bu REST API, `move file`'i gösterir.
 
## RSET API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/storage/file/move/{srcPath}
 
```
 İstek parametreleri şunlardır:
 
| Parametre adı| Tip| Yol/Sorgu Dizesi/HTTPBody|Tanım|
|:- |:- |:- |:- |
| kaynakYol| sicim| yol| Kaynak dosya yolu, örneğin '/src.ext'|
| hedefYol| sicim| sorgu| Hedef dosya yolu, örneğin '/dest.ext'|
| srcDepolamaAdı| sicim| sorgu| Kaynak depolama adı|
| hedefDepoAdı| sicim| sorgu| Hedef depolama adı|
| sürüm kimliği| sicim| sorgu| Taşınacak dosya sürümü kimliği|
 
 bu[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/File/MoveFile) herkesin erişebileceği bir programlama arabirimi tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.
 
Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'e nasıl çağrı yapılacağını gösterir.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/move/Book2.xlsx?destPath=MoveBook2.xlsx" \
-X PUT \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
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
 
 