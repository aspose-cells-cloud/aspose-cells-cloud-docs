---
title: "Bir Excel Çalışma Sayfasından Satır Açıklaması Alın"
second_title: "Belge"
linktitle: "Satır"
type: docs
url: /tr/rows/get/row/
aliases: [  /tr/get-row-from-a-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel satır API'si, Çalışma Sayfası Satırı Al, REST API, .NET SDK, Java SDK, Python SDK"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasındaki belirli bir satırın (yükseklik, stil, gizli durumu vb.) ayrıntılı bilgilerini alın. cURL örneği, SDK kod parçacıkları ve hata yönetimi içerir."
weight: 10
ArticleTitle: "Bir Excel Çalışma Sayfasından Satır Açıklaması Alın – Aspose.Cells Cloud API"
---

**Ön Gereksinimler:**
- Geçerli bir JWT erişim belirteci edinin ve bunu `Authorization: Bearer <jwt token>` başlığına ekleyin.
- Çalışma kitabının Aspose Cloud deposunda depolandığından emin olun veya yer aldığı klasör yolunu belirtin.
- Uç nokta URL'inde gösterildiği gibi API sürümünü **v3.0** olarak kullanın.

Bu REST API, bir Excel çalışma sayfasındaki satır verilerini indeksine göre alır.

## GetWorksheetRow API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### **İstek Parametreleri**

| Parametre Adı | Tür      | Konum | Açıklama                                              |
|---------------|----------|-------|-------------------------------------------------------|
| name          | string   | path  | Çalışma kitabının dosya adı.                          |
| sheetName     | string   | path  | Çalışma kitabındaki çalışma sayfasının adı.          |
| rowIndex      | integer  | path  | Alınacak satırın sıfır tabanlı indeksi.              |
| folder        | string   | query | Çalışma kitabını içeren klasör.                       |
| storageName   | string   | query | Çalışma kitabının bulunduğu depo adı.                |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetRow), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'ye istek nasıl atılacağını göstermektedir. İsteği kimlik doğrulamak için `Authorization: Bearer <jwt token>` başlığını ekleyin.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/0" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Row": {
    "GroupLevel": 0,
    "Height": 13.5,
    "Index": 0,
    "IsBlank": false,
    "IsHeightMatched": true,
    "IsHidden": false,
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/rows/0",
      "Rel": "self"
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

**Yanıt şeması**

| Özellik           | Tür       | Açıklama                                                              |
|--------------------|-----------|-----------------------------------------------------------------------|
| `GroupLevel`       | integer   | Satırın taslak düzeyi (gruplama için kullanılır).                     |
| `Height`           | number    | Satırın nokta cinsinden yüksekliği.                                   |
| `Index`            | integer   | Döndürülen satırın sıfır tabanlı indeksi.                             |
| `IsBlank`          | boolean   | Satırda herhangi bir veri olup olmadığını gösterir.                   |
| `IsHeightMatched`  | boolean   | Satır yüksekliği varsayılan satır yüksekliğiyle eşleşiyorsa `true`.   |
| `IsHidden`         | boolean   | Satır gizliyse `true`.                                                |
| `Style`            | object    | Satır için stil bilgilerini içeren nesne.                             |
| `link`             | object    | Satır kaynağına yönelik hiperbağlantı referansı.                      |
| `Code`             | integer   | Yanıtın HTTP durum kodu.                                              |
| `Status`           | string    | Durumun metinsel açıklaması (örneğin, “OK”).                         |

{{< /tab >}}

{{< /tabs >}}

**Notlar / Hata Yönetimi:** API aşağıdaki HTTP durum kodlarından birini döndürebilir:

- **200** – Başarılı; satır verileri döndürülür.  
- **401** – Yetkisiz; JWT belirteci eksik veya geçersiz.  
- **404** – Bulunamadı; belirtilen çalışma kitabı, çalışma sayfası veya satır mevcut değil.  
- **500** – Sunucu iç hatası; beklenmeyen bir durum oluştu.

| Kod  | Açıklama                                      | Giderme                                  |
|------|-----------------------------------------------|------------------------------------------|
| 200  | Başarılı – satır verileri döndürüldü.         | –                                        |
| 401  | Yetkisiz – eksik veya geçersiz JWT belirteci. | Geçerli bir JWT belirteci sağlayın.      |
| 404  | Bulunamadı – çalışma kitabı, çalışma sayfası veya satır eksik.| Adları ve satır indeksini kontrol edin. |
| 500  | Sunucu iç hatası – beklenmeyen durum.         | Aspose desteğiyle iletişime geçin.       |

Hata kodlarının tam listesi için Aspose.Cells Cloud [Hata Kodları belgesine](https://docs.aspose.cloud/cells/) bakın.

## Cloud SDK Ailesi

SDK kullanmak geliştirmenin en hızlı yoludur. Bir SDK, düşük seviyeli ayrıntıları soyutlayarak proje görevlerinize odaklanmanıza olanak tanır. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK'lar kullanılarak Aspose.Cells web hizmetlerine nasıl istek atılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetRow.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetRow.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetRow.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetRow.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetRow.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetRow.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetRow.go" >}}

{{< /tab >}}

{{< /tabs >}}