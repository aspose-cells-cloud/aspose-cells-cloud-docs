---
title: Dosyayı Kopyala
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/file/copy/
keywords: Learn how to copy file with Aspose Cells Cloud REST API
description: Aspose Cells Cloud REST API SDK destekli geliştirme dilleri ile dosyayı nasıl kopyalayacağınızı öğrenin. Bunlar arasında Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve Swift bulunur
weight: 100
---
Bu REST API, `copy file`'i gösterir.
 
## RSET API
 
```bash
 
PUT http://api.aspose.cloud/v3.0/cells/storage/file/copy/{srcPath}
 
```
 İstek parametreleri şunlardır:
 
| Parametre adı| Tip| Yol/Sorgu Dizesi/HTTPBody|Tanım|
|:- |:- |:- |:- |
| srcPath| sicim| yol| Kaynak dosya yolu örneğin '/folder/file.ext'|
| hedefYol| sicim| sorgu| Hedef dosya yolu|
| srcStorageName| sicim| sorgu| Kaynak depolama adı|
| destStorageName| sicim| sorgu| Hedef depolama adı|
| sürüm kimliği| sicim| sorgu|Kopyalanacak dosya sürüm kimliği|
 
[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/File/CopyFile) herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.
 
Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnekte, cURL ile Cloud API'e nasıl çağrı yapılacağı gösterilmektedir.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName21="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/storage/file/copy/Book1.xlsx?destPath=Book2.xlsx" \
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
 
 SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, düşük düzeyli ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanıza olanak tanır. Lütfen şuraya göz atın:[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.
 
Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını gösterir:
 
 