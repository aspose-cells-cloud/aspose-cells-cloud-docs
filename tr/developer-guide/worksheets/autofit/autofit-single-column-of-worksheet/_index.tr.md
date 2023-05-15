---
title: Excel çalışma sayfasında bir sütunu otomatik sığdırma
second_title: Aspose.Cells Cloud Documen
linktitle: Sütun
type: docs
url: /tr/worksheets/autofit/column/
aliases: [/autofit-single-column-of-worksheet/]
keywords: Autofit a column on an Excel workshee
description: Aspose.Cells Cloud REST API, bir Excel çalışma sayfasında bir sütunu otomatik sığdırmayı destekler. SDK, geliştirme dili türlerini destekler. Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve Swift'i içerir
weight: 10
---
Bu REST API, bir Excel çalışma sayfasına bir sütunun otomatik sığdırılacağını gösterir.
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autofitcolumns
 
```
 İstek parametreleri şunlardır:
 
| Parametre adı| Tip| Yol/Sorgu Dizesi/HTTPBody|Tanım|
|:- |:- |:- |:- |
| isim| sicim| yol||
| sayfaAdı| sicim| yol||
| ilk sütun| tamsayı| sorgu||
| son Sütun| tamsayı| sorgu||
| otomatikFitterSeçenekleri|| vücut||
| ilk sıra| tamsayı| sorgu||
| son satır| tamsayı| sorgu||
| dosya| sicim| sorgu||
| depolamaAdı| sicim| sorgu| depolama adı.|
 
 bu[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Worksheets/PostAutofitWorksheetColumns) herkesin erişebileceği bir programlama arabirimi tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.
 
Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'e nasıl çağrı yapılacağını gösterir.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/sampleAutoFit.xlsx/worksheets/Sheet1/autofitcolumns?lastColumn=2&firstColumn=2" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-d '{"AutoFitMergedCells" : true, "IgnoreHidden" : true, "OnlyAuto" : true}' 

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


{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "9b4ccf2e3ba7d0f1d2a625d6cd40d2fd" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "3f17376a8d99f16f703fdb52c08a05ff" >}}

{{< /tab >}}

{{< /tabs >}}




