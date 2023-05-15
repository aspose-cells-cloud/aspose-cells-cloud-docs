---
title: Klasörü Kopyala
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/folder/copy/
keywords: Learn how to copy folder with Aspose Cells Cloud REST API
description: Aspose Cells Cloud REST API SDK destekli geliştirme dili türleriyle klasörü nasıl kopyalayacağınızı öğrenin. Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve Swift'i içerir
weight: 100
---
Bu REST API, `copy folder`'i gösterir.
 
## RSET API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/storage/folder/copy/{srcPath}
 
```
 İstek parametreleri şunlardır:
 
| Parametre adı| Tip| Yol/Sorgu Dizesi/HTTPBody|Tanım|
|:- |:- |:- |:- |
| kaynakYol| sicim| yol| Kaynak klasör yolu, örneğin '/src'|
| hedefYol| sicim| sorgu| Hedef klasör yolu, örneğin '/dst'|
| srcDepolamaAdı| sicim| sorgu| Kaynak depolama adı|
| hedefDepoAdı| sicim| sorgu| Hedef depolama adı|
 
 bu[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Folder/CopyFolder) herkesin erişebileceği bir programlama arabirimi tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.
 
Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'e nasıl çağrı yapılacağını gösterir.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/folder/copy/srcfolder?destPath=desfolder" \
-X PUT \
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
 
 