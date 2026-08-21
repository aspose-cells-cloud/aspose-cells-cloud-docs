---
title: "Excel Çalışma Sayfasında Satırların Gruplamasını Kaldırma"
second_title: "Belge"
linktitle: "Gruplama Kaldır"
type: docs
url: /tr/rows/ungroup/
aliases: [  /tr/ungroup-rows-in-excel-worksheet/ ]
keywords: "satırların gruplamasını kaldırma, Excel, Aspose.Cells Cloud, REST API, SDK, elektronik tablo"
description: "Aspose.Cells Cloud REST API ve çeşitli programlama dilleri için SDK'larını kullanarak Excel çalışma sayfasında satırların gruplamasını nasıl kaldıracağını öğrenin."
weight: 70
---

Bu REST API, Excel çalışma sayfasındaki satırların gruplamasını kaldırır.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/ungroup
```

### **İstek Parametreleri**

| Parametre Adı | Tür      | Konum  | Açıklama                                                                 |
| ------------- | -------- | ------ | ------------------------------------------------------------------------ |
| name          | string   | path   | Çalışma kitabının adı.                                                    |
| sheetName     | string   | path   | Çalışma sayfasının adı.                                                   |
| firstIndex    | integer  | query  | Gruplaması kaldırılacak ilk satırın sıfır tabanlı indeksi.               |
| lastIndex     | integer  | query  | Gruplaması kaldırılacak son satırın sıfır tabanlı indeksi.               |
| isAll         | boolean  | query  | **true** ise, belirtilen aralıktaki tüm satırların gruplaması kaldırılır. |
| folder        | string   | query  | Çalışma kitabının bulunduğu klasör.                                       |
| storageName   | string   | query  | Çalışma kitabının bulunduğu depo adı.                                     |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/PostUngroupWorksheetRows), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'ye nasıl istek gönderileceğini göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/ungroup?firstIndex=1&lastIndex=5&isAll=true" \
 -X POST \
 -H "Content-Type: application/json" \
 -H "Accept: application/json" \
 -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Topluluğu

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoludur. Bir SDK, düşük seviye detayları yönetir ve projenizdeki görevlere odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK’ları kullanarak Aspose.Cells web hizmetlerine nasıl istek gönderileceğini göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUngroupWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUngroupWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUngroupWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUngroupWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUngroupWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUngroupWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUngroupWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUngroupWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}