---
title: "Excel Çalışma Sayfasında Bir Pivot Tablo Alın"
second_title: "Belge"
linktitle: Al
type: docs
url: /pivot-tables/get/
aliases: [/get-worksheet-pivot-table-information-by-index/]
keywords: "Aspose.Cells, pivot tablo, Excel, REST API, çalışma sayfası pivot tablosu al"
description: "Aspose.Cells Cloud REST API aracılığıyla bir Excel çalışma sayfasından bir pivot tablo alın. İstek söz dizimi, parametreler, kimlik doğrulama, yanıt şeması, hata işleme ve SDK örneklerini içerir."
weight: 10
ArticleTitle: "Excel Çalışma Sayfasında Bir Pivot Tablo Alın"
---

Bu REST API, dizinine göre bir çalışma sayfasının **pivot tablo** bilgilerini getirir.

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulamayı</a> gerektirir.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivottableIndex}
```

### İstek parametreleri

| Parametre Adı       | Tür      | Konum   | Açıklama                                                   |
| ------------------- | -------- | ------- | ---------------------------------------------------------- |
| **name**            | string   | path    | Excel dosyasının adı.                                      |
| **sheetName**       | string   | path    | Pivot tabloyu içeren çalışma sayfasının adı.              |
| **pivottableIndex** | integer  | path    | Çalışma sayfasındaki pivot tablonun sıfır tabanlı indeksi. |
| **folder**          | string   | query   | Belgenin bulunduğu klasör.                                 |
| **storageName**     | string   | query   | Aspose Cloud depo adı.                                     |

Aspose.Cells web hizmetlerine kolayca erişmek için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile API’yi nasıl çağıracağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Status": "string",
  "PivotFilters": [
    {
      "AutoFilter": {
        "link": {
          "Href": "string",
          "Rel": "string",
          "Title": "string",
          "Type": "string"
        },
        "FilterColumns": [
          {
            "FieldIndex": 0,
            "FilterType": "string",
            "MultipleFilters": {
              "MatchBlank": true,
              "MultipleFilterList": [{}]
            },
            "ColorFilter": {
              "FilterByFillColor": "string",
              "Pattern": "string",
              "Color": {
                "Color": {
                  "A": 0,
                  "R": 0,
                  "G": 0,
                  "B": 0
                },
                "ColorIndex": 0,
                "IsShapeColor": true,
                "ThemeColor": {
                  "ColorType": "string",
                  "Tint": 0
                },
                "Type": "string"
              },
              "ForegroundColorColor": {
                "Color": {
                  "A": 0,
                  "R": 0,
                  "G": 0,
                  "B": 0
                },
                "ColorIndex": 0,
                "IsShapeColor": true,
                "ThemeColor": {
                  "ColorType": "string",
                  "Tint": 0
                },
                "Type": "string"
              },
              "BackgroundColor": {
                "Color": {
                  "A": 0,
                  "R": 0,
                  "G": 0,
                  "B": 0
                },
                "ColorIndex": 0,
                "IsShapeColor": true,
                "ThemeColor": {
                  "ColorType": "string",
                  "Tint": 0
                },
                "Type": "string"
              }
            },
            "CustomFilters": [
              {
                "FilterOperatorType": "string"
              }
            ],
            "DynamicFilter": {
              "DynamicFilterType": "string"
            },
            "IconFilter": {
              "IconId": 0,
              "IconSetType": "string"
            },
            "Top10Filter": {
              "Criteria": "string",
              "IsPercent": true,
              "IsTop": true,
              "Items": 0
            },
            "VisibleDropdown": "string"
          }
        ],
        "Range": "string",
        "Sorter": {
          "CaseSensitive": true,
          "HasHeaders": true,
          "KeyList": [
            {
              "Key": 0,
              "SortOrder": "string",
              "CustomList": "string"
            }
          ],
          "SortLeftToRight": true
        }
      },
      "EvaluationOrder": 0,
      "FieldIndex": 0,
      "FilterType": "string",
      "MeasureFldIndex": 0,
      "MemberPropertyFieldIndex": 0,
      "Name": "string",
      "Value1": "string",
      "Value2": "string"
    }
  ]
}
```

**Yanıt Şeması**

| Alan            | Tür     | Açıklama                                               |
|-----------------|---------|--------------------------------------------------------|
| Status          | string  | İşlem durumu metni (örn. “OK”).                       |
| PivotFilters    | array   | Pivot filtre tanımlarının koleksiyonu.                 |
| └─ AutoFilter   | object  | Pivot tabloya uygulanan otomatik filtreleme detayları. |
|    └─ link      | object  | Filtre için bağlantı (hyperlink) bilgisi.             |
|    └─ FilterColumns | array | Bireysel sütun filtre ayarları.                   |
|    └─ Range     | string  | Filtrenin uygulandığı hücre aralığı.                  |
|    └─ Sorter    | object  | Filtrelenmiş veriler için sıralama yapılandırması.    |
| (ekstra iç içe geçmiş alanlar, yukarıdaki örnek JSON'da gösterilen yapıya uyar) |

{{< /tab >}}

{{< /tabs >}}

### Hata işleme

API, standart HTTP durum kodlarını takip eder. Tipik yanıtlar şunları içerir:

| Durum Kodu | Anlam                                                              | Örnek JSON (hata)                                   |
| ---------- | ------------------------------------------------------------------ | --------------------------------------------------- |
| 200        | Başarılı – pivot tablo döndürüldü                                 | —                                                   |
| 401        | Yetkisiz – geçersiz veya eksik belirteç                           | `{"code":401,"message":"Invalid access token."}`   |
| 404        | Bulunamadı – dosya, çalışma sayfası veya pivot tablo indeksi yok   | `{"code":404,"message":"Pivot table not found."}`  |
| 500        | Sunucu hatası – beklenmeyen durum                                 | `{"code":500,"message":"Internal server error."}`  |

**Notlar:** API, 150 MB’a kadar olan Excel dosyalarını destekler ve Excel 2007–2021 formatlarıyla çalışır. Çalışma sayfası adının büyük/küçük harfe duyarlı olduğunu lütfen unutmayın.

## Bulut SDK Geliştirme Takımı

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. SDK, düşük seviye detayları yöneterek size proje görevlerinize odaklanma imkânı sunar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposunu](https://github.com/aspose-cells-cloud) kontrol edin.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web hizmetlerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Objective C" tabName8="Android" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-GetWorksheetPivotTableByIndex-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-GetWorksheetPivotInfoByIndex-1.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "GetWorksheetPivotTablesInformationByIndex.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-GetWorksheetPivotTableByIndex-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Examples-Android-pivottables-GetPivotTableIndexWorksheet-get-pivottable-index-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-GetWorksheetPivotTableByIndex-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "3ff21d138764aa6b6fd51fbaab8cdb95" >}}

{{< /tab >}}

{{< /tabs >}}