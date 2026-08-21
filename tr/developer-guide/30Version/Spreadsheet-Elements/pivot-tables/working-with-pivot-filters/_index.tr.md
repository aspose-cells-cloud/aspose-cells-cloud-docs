---
title: "Pivot Filtreleriyle Çalışma"
second_title: "Belge"
linktitle: "Filtreler"
type: docs
url: /tr/pivot-tables/add-filters/
aliases: [  /tr/working-with-pivot-filters/ ]
keywords: "Aspose.Cells, Pivot Tablosu, Filtre, REST API, Bulut"
description: "Aspose.Cells Cloud REST API kullanarak pivot tablo filtrelerinin nasıl ekleneceğini, alınacağını ve silineceğini öğrenin. İstek sözdizimi, gerekli parametreler, cURL örneği ve C# ile Go için SDK kod parçacıklarını içerir."
weight: 50
ArticleTitle: "Pivot Filtreleriyle Çalışma – Aspose.Cells Cloud Dokümantasyonu"
---

Bu REST API, belirtilen dizindeki pivot tablosuna bir **pivot filtresi** ekler.

**Ön Gereksinimler**  
Bu uç noktayı çağırmadan önce şunları yapmanız gerekir:

- Geçerli bir OAuth/JWT erişim belirteci oluşturun ve `Authorization` başlığına ekleyin.  
- Hedef çalışma kitabının, erişiminiz olan bir bulut klasöründe depolandığından emin olun (`folder` ve isteğe bağlı olarak `storageName` belirtin).  
- Aspose.Cells Cloud API sürümü 3.0 veya üzeri olmalıdır.

## PutWorksheetPivotTableFilter API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotFilters
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı      | Tür      | Konum  | Açıklama                                                                                     |
| ------------------- | -------- | ------ | -------------------------------------------------------------------------------------------- |
| **name**            | string   | path   | Excel dosyasının adı.                                                                        |
| **sheetName**       | string   | path   | Pivot tabloyu içeren çalışma sayfası.                                                        |
| **pivotTableIndex** | integer  | path   | Filtrenin uygulanacağı pivot tablonun sıfır tabanlı indeksi.                                 |
| **filter**          | object   | body   | Filtre ayarlarını tanımlayan JSON nesnesi. Aşağıdaki **filter schema (filtre şeması)** tablosuna bakın. |
| **needReCalculate** | boolean  | query  | **true** olarak ayarlandığında, filtre eklendikten sonra çalışma kitabının yeniden hesaplanmasını zorlar. Varsayılan **false**. |
| **folder**          | string   | query  | Dosyanın bulunduğu bulut depolama klasörü.                                                   |
| **storageName**     | string   | query  | Bulut depolama adı.                                                                          |

**Filtre Şeması (filter schema)**

| Özellik                      | Tür      | Açıklama                                                                                    |
| ---------------------------- | -------- | ------------------------------------------------------------------------------------------- |
| **AutoFilter**               | object   | Otomatik Filtre için ayarlar; kullanılmıyorsa atlanabilir.                                 |
| **EvaluationOrder**          | integer  | Filtrenin değerlendirilme sırası.                                                            |
| **FieldIndex**               | integer  | Filtrenin uygulanacağı alanın sıfır tabanlı indeksi.                                       |
| **FilterType**               | string   | Filtre türü (örn. `Value`, `Count`, `Label`).                                               |
| **MeasureFldIndex**          | integer  | Uygulanıyorsa ölçü alanı indeksi.                                                           |
| **MemberPropertyFieldIndex** | integer  | Uygulanıyorsa üye özelliği alanı indeksi.                                                   |
| **Name**                     | string   | İsteğe bağlı filtre adı.                                                                    |
| **Value1**                   | string   | Filtre tarafından kullanılan ilk değer (örn. bir aralık için alt sınır).                    |
| **Value2**                   | string   | Filtre tarafından kullanılan ikinci değer (örn. bir aralık için üst sınır).                 |
| **CustomFilters**            | array    | Özel filtre nesnelerinin koleksiyonu (her biri `FilterOperatorType`, `Value1`, `Value2` içerir). |
| **DynamicFilter**            | object   | Dinamik filtre için ayarlar (örn. Top10, Bottom10).                                        |
| **IconFilter**               | object   | Simge tabanlı filtre için ayarlar.                                                          |
| **Top10Filter**              | object   | Top10/Bottom10 filtresi için ayarlar.                                                       |
| **ColorFilter**              | object   | Renk tabanlı filtre için ayarlar.                                                           |
| **Visibledropdown**          | boolean  | Filtre açılır listesinin görünür olup olmadığını gösterir.                                 |

> **Not:** Yukarıda listelenen tüm parametreler, API referansında açıkça "isteğe bağlı" olarak belirtilmedikçe zorunludur.

### Yanıt Kodları

| Kod | Anlam                                        |
| --- | -------------------------------------------- |
| 200 | Filtre başarıyla eklendi.                    |
| 400 | Geçersiz istek – geçersiz parametreler.      |
| 401 | Yetkisiz erişim – eksik veya geçersiz belirteç. |
| 404 | Bulunamadı – çalışma kitabı veya pivot tablo eksik. |
| 500 | İç sunucu hatası.                            |

**En İyi Uygulamalar**  
- Filtre nesnelerini mümkün olduğunca küçük tutun; büyük filtre tanımları istek gecikmesini artırabilir.  
- Çağrılar idempotent’tir — aynı filtreyi iki kez eklemek, kopyalar oluşturmaz.  
- Hesap başına dakikada 100 istek olan API hız sınırlamalarına uyun.  

*Ek Notlar:*  
- Bir filtre tanımının maksimum boyutu 1 MB’tir; daha büyük yükler 400 hatasıyla reddedilir.  
- `needReCalculate=true` kullanıldığında, büyük çalışma kitaplarında yanıt süresi artabilir.  

Tam OpenAPI tanımını buradan inceleyebilirsiniz:  
[OpenAPI Specification (OpenAPI Tanımlaması)](https://apireference.aspose.cloud/cells/#/PivotTables/PutWorksheetPivotTableFilter)

### Örnek cURL İsteği

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/pivottables/0/PivotFilters?needReCalculate=true" \
  -X PUT \
  -d '{
        "AutoFilter": {
          "link": { "Href": "https://example.com", "Rel": "self", "Title": "AutoFilter Link", "Type": "application/json" },
          "FilterColumns": [
            {
              "FieldIndex": 0,
              "FilterType": "Value",
              "MultipleFilters": {
                "MatchBlank": true,
                "MultipleFilterList": [ { "Value": "example" } ]
              },
              "ColorFilter": {
                "FilterByFillColor": "FF0000",
                "Pattern": "Solid",
                "Color": {
                  "Color": { "A": 255, "R": 255, "G": 0, "B": 0 },
                  "ColorIndex": 3,
                  "IsShapeColor": false,
                  "ThemeColor": { "ColorType": "Accent1", "Tint": 0 },
                  "Type": "Rgb"
                },
                "ForegroundColorColor": null,
                "BackgroundColor": null
              },
              "CustomFilters": [ { "FilterOperatorType": "Equals", "Value1": "Example" } ],
              "DynamicFilter": { "DynamicFilterType": "Top10" },
              "IconFilter": { "IconId": 1, "IconSetType": "3Arrows" },
              "Top10Filter": { "Criteria": "Top", "IsPercent": true, "IsTop": true, "Items": 10 },
              "Visibledropdown": "true"
            }
          ],
          "Range": "A1:D100",
          "Sorter": {
            "CaseSensitive": false,
            "HasHeaders": true,
            "KeyList": [ { "Key": 0, "SortOrder": "Ascending", "CustomList": null } ],
            "SortLeftToRight": false
          }
        },
        "EvaluationOrder": 0,
        "FieldIndex": 0,
        "FilterType": "Value",
        "MeasureFldIndex": 0,
        "MemberPropertyFieldIndex": 0,
        "Name": "MyFilter",
        "Value1": "10",
        "Value2": "20"
      }' \
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

## Bulut SDK Ailesi

Aspose.Cells Cloud’a karşı hızlıca geliştirme yapmanın en iyi yolu SDK kullanmaktır. SDK’lar düşük seviye ayrıntıları ele alır ve iş mantığınıza odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub Deposu](https://github.com/aspose-cells-cloud)'na bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web hizmetlerine nasıl istek yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

```csharp
using System;
using System.Threading.Tasks;
using Aspose.Cells.Cloud.Sdk.Api;
using Aspose.Cells.Cloud.Sdk.Model;

public class PivotFilterExample
{
    public static async Task AddPivotFilterAsync()
    {
        // API istemcisini başlatın (kimlik bilgilerinizle değiştirin)
        var config = new Configuration
        {
            ClientId = "YOUR_CLIENT_ID",
            ClientSecret = "YOUR_CLIENT_SECRET"
        };
        var apiInstance = new CellsApi(config);

        // Filtre nesnesini oluşturun
        var filter = new PivotFilter
        {
            AutoFilter = null,
            EvaluationOrder = 0,
            FieldIndex = 1,
            FilterType = "Count"
        };

        // İsteği hazırlayın
        var request = new PutWorksheetPivotTableFilterRequest(
            name: "Book1.xlsx",
            sheetName: "PivotSheet",
            pivotTableIndex: 0,
            filter: filter,
            needReCalculate: true,
            folder: "Temp",
            storageName: null);

        // İsteği yürütün
        var response = await apiInstance.PutWorksheetPivotTableFilterAsync(request);
        Console.WriteLine($"Durum: {response.Status}");
    }
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "2a2aa16c2d9fd7e46b1b19f5fea5842b" >}}

{{< /tab >}}

{{< /tabs >}}

Pivot tablolarla ilgili ek işlemler için **Ekle**, **Sil** ve **Temizle** filtre dokümantasyonuna bakın.