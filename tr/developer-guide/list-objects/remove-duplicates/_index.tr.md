---
title:  Liste nesnesi kopyaları kaldır
second_title: Aspose.Cells Cloud Documen
linktitle: Kopyayı kaldır
type: docs
keywords: list object(table) remove duplicates 
url: /tr/list-objects/remove-duplicates/
description:  Liste nesnesindeki kopyaları kaldırın.
weight: 20
---
 Bu REST API, liste nesnesindeki kopyaların kaldırıldığını gösterir.

## RSET API


```bash

POST http://api.aspose.cloud/v3.0//cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates

```

 İstek parametreleri şunlardır:

| Parametre adı| Tip| Yol/Sorgu Dizesi/HTTPBody| Tanım|
|:- |:- |:- |:- |
|isim|Sicim|Yol||
|sayfaAdı|Sicim|Yol||
|listObjectIndex|Tamsayı|Yol||
|dosya|Sicim|Sorgu||
|depolamaAdı|Sicim|Sorgu||



[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/ListObjectsController/PostWorksheetListObjectRemoveDuplicates) herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnekte, cURL ile Cloud API'e nasıl çağrı yapılacağı gösterilmektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}
```powershell
curl -v "http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/RemoveDuplicates" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
```
{{< /tab >}}
{{< tab tabNum="2" >}}
```powershell

```
{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Ailesi

SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, düşük düzeyli ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanıza olanak tanır. Aspose.Cells Bulut SDK'larının tam listesi için lütfen GitHub deposuna göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını gösterir:
