---
title: "Excel Çalışma Sayfasındaki Tüm Çapraz Tabloları Alın"
second_title: "Belge"
linktitle: Tümünü al
type: docs
url: /tr/pivot-tables/get-all/
aliases: [  /tr/get-worksheet-pivot-tables-information/ ]
keywords: "tüm çapraz tabloları al, Aspose.Cells Cloud API, Excel PivotTable, REST API"
description: "Aspose.Cells Cloud API aracılığıyla bir Excel çalışma sayfasındaki tüm PivotTable’ları alın. PivotTables API için uç nokta, parametreler, kimlik doğrulama adımları, cURL ve SDK örneklerini içerir."
weight: 20
ArticleTitle: "Excel Çalışma Sayfasındaki Tüm Çapraz Tabloları Alın – Aspose.Cells Cloud API"
---

**PivotTable** (Çapraz Tablo), Excel’de büyük veri setlerini yeniden düzenlemenizi ve analiz etmenizi sağlayan bir veri özetleme aracıdır. Bu REST API, belirtilen bir çalışma sayfasındaki **tüm** PivotTable’lar hakkında bilgi almanızı sağlar.

## Güvenlik ve Kimlik Doğrulama

Aspose.Cells Cloud API’leri güvenlidir ve [JWT belirteci tabanlı kimlik doğrulama](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) gerektirir.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### **İstek parametreleri**

| Parametre Adı | Tür   | Konum | Açıklama                                   |
| ------------- | ----- | ----- | ------------------------------------------ |
| name          | string | path  | Excel belgesinin adı.                     |
| sheetName     | string | path  | Çalışma sayfasının adı.                   |
| folder        | string | query | Belgenin depolandığı klasör.              |
| storageName   | string | query | Depolama hizmetinin adı.                  |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/PivotTables/GetWorksheetPivotTables), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından yapmanızı sağlar.

### İstek

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

### Yanıt

{{< tab tabNum="2" >}}

```json
{
  "PivotTables": {
    "PivotTableList": [
      {
        "link": {
          "Href": "/0",
          "Rel": "self"
        }
      }
    ],
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Hata Yanıtları

| HTTP Kodu | Açıklama                                                           | Örnek JSON Yükü                                               |
| --------- | ------------------------------------------------------------------ | ------------------------------------------------------------ |
| 400       | Geçersiz istek – gerekli parametre eksik.                         | `{ "Code": "400", "Message": "Missing required parameter." }` |
| 401       | Yetkisiz erişim – geçersiz veya eksik belirteç.                   | `{ "Code": "401", "Message": "Authentication failed." }`      |
| 404       | Bulunamadı – çalışma kitapçası, çalışma sayfası veya PivotTable mevcut değil. | `{ "Code": "404", "Message": "Resource not found." }`         |
| 500       | İç sunucu hatası – sunucuda beklenmeyen bir durum oluştu.         | `{ "Code": "500", "Message": "Server error." }`               |

## Bulut SDK Grubu

SDK kullanmak, geliştirme yapmanın en hızlı yoludur. SDK, düşük seviye detayları işler ve projenize odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web servislerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-GetWorksheetPivotTables-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-GetPivotTableWorksheet-GetPivotTableWorksheet-12345.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetWorksheetPivotTablesInformation.py" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-GetWorksheetPivotTables-1.js" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-GetPivotTableWorksheet-GetPivotTableWorksheet-12345.java" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-GetWorksheetPivotTables-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="10" >}}
{{< gist "aspose-cells-cloud-gists" "6b30a17927feeb2899283e4dbe566c42" >}}
{{< /tab >}}

{{< /tabs >}}
---