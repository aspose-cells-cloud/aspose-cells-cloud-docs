﻿---
title:  Aralık Sıralaması
second_title: Aspose.Cells Cloud Documen
linktitle: Sor
type: docs
keywords: Range Sort
url: /tr/ranges/sort/
description:  Bir hücre aralığının etrafındaki ana hat kenarlığını ayarlar.
weight: 20
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, Json, Markdwon, Aralık Sıralaması
---
 Bu REST API, aralık sıralamasını gösterir.

## RSET API


```bash

POST http://api.aspose.cloud/v3.0//cells/{name}/worksheets/{sheetName}/ranges/sort

```

 İstek parametreleri şunlardır:

| Parametre adı| Tip| Yol/Sorgu Dizesi/HTTPBody| Tanım|
|:- |:- |:- |:- |
|isim|Sicim|Yol|Çalışma kitabı adı.|
|sayfaAdı|Sicim|Yol|Çalışma sayfası adı.|
|aralıkİşlet|Sınıf|Vücut| Aralık Sıralama İsteği|
|dosya|Sicim|Sorgu|Orijinal çalışma kitabı klasörü.|
|depolamaAdı|Sicim|Sorgu|Depolama adı.|



[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/RangesController/PostWorksheetCellsRangeSort) herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnekte, cURL ile Cloud API'e nasıl çağrı yapılacağı gösterilmektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
{{< tab tabNum="1" >}}
```powershell
curl -v "http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/sort" \
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

