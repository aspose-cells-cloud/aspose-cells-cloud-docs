﻿---
title: Ge
type: docs
url: /tr/comments/get/
aliases: [/get-comment-from-a-worksheet/]
keywords: REST API, spreadsheets, excel, get commen
description: "Cells.Cloud API için Excel çalıştır: yorum al"
weight: 10
kwords: Excel, Office Bulut, REST API, Elektronik Tablo, PDF, CSV, Json, Markdwon, Al
---
Bu REST API, hücre adına göre çalışma sayfası yorumunu al anlamına gelir.
 
## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/comments/{cellName}
 
```
 İstek parametreleri şunlardır:
 
| Parametre adı| Tip| Yol/Sorgu Dizesi/HTTPBody|Tanım|
|:- |:- |:- |:- |
| isim| sicim| yol| Belge adı.|
| sayfaAdı| sicim| yol| Çalışma sayfası adı.|
| hücreAdı| sicim| yol| Hücre adı|
| dosya| sicim| sorgu| Belge klasörü.|
| depolamaAdı| sicim| sorgu| depolama adı.|
 
[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetComment) herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.
 
Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnekte, cURL ile Cloud API'e nasıl çağrı yapılacağı gösterilmektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}

{{< tab tabNum="11" >}}

```java

curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/comments/A1" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"


```

{{< /tab >}}

{{< tab tabNum="12" >}}

```java

{
    "Comment":{

    "CellName":"A1",

    "Author":"roy.wang",

    "HtmlNote": "",

    "Note": "Aspose.Cells Cloud.",

    "AutoSize": "True",

    "IsVisible": "True",

    "Width": 30,

    "Height": 10,

    "TextHorizontalAlignment": "Bottom",

    "TextOrientationType": "TopToBottom",

    "TextVerticalAlignment": "Bottom"

    },
 
   "Code": 200,

   "Status": "OK"

}

```

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Ailesi
 
 SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, düşük düzeyli ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanıza olanak tanır. Lütfen şuraya göz atın:[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.
 
Aşağıdaki kod örnekleri, çeşitli SDK'ları kullanarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını gösterir:

{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "0f1e96858d650d16d9c09ca61723c335" >}}

{{< /tab >}}

{{< /tabs >}}
