---
title: "Bir Excel Çalışma Sayfasından Aralık İçeriği Nasıl Alınır"
second_title: "Belge"
linktitle: "Al"
type: docs
url: /ranges/get/
keywords: "Aspose.Cells, Excel, API, al, aralık, elektronik tablo, REST"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasından aralık içeriğini nasıl alacağınızı öğrenin. İstek söz dizimini ve örnek kodu içerir."
weight: 20
ArticleTitle: "Bir Excel Çalışma Sayfasından Aralık İçeriği Nasıl Alınır – Aspose.Cells Cloud API"
---

## Bir Excel çalışma sayfasından aralık içeriğini alma

- [Adlandırılmış bir aralığa göre hücre verileri nasıl alınır](/cells/ranges/get/values/)
- [Bir Excel çalışma kitabından adlandırılmış bir aralık nasıl alınır](/cells/ranges/get/name/)

**Önkoşullar**

- Geçerli bir Aspose Cloud erişim belirteci (veya OAuth için `client_id`/`client_secret`).
- Excel dosyası, hedef depolama klasörüne yüklenmiş olmalıdır.
- Aspose.Cells Cloud SDK sürümü 3.0 veya üzeri.

**Aralığı Al** işlemi, bir çalışma sayfasındaki belirli bir aralığın içeriğini döndürür.  
Basit bir `GET` isteğidir ve aralık verilerini JSON formatında (veya talep edildiğinde diğer formatlarda) döndürür.

**İstek Genel Bakış**

| Eleman | Değer |
|---------|-------|
| **HTTP Yöntemi** | `GET` |
| **Uç Nokta** | `https://api.aspose.cloud/v3.0/cells/{fileName}/worksheets/{sheetName}/ranges/{rangeName}` |
| **Yol Parametreleri** | `fileName` – Excel dosyasının adı (uzantısı dahil) <br> `sheetName` – Çalışma sayfasının adı <br> `rangeName` – Aralığın adı (örneğin, `A1:B10`) |
| **Sorgu Parametreleri** (isteğe bağlı) | `folder` – Depolama klasörü <br> `storage` – Depolama adı <br> `outFormat` – Yanıt formatı (örneğin, `json`, `xml`) |
| **Başlıklar** | `Authorization: Bearer <access_token>` <br> `Accept: application/json` |

**Örnek cURL**

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/ranges/A1:B10?folder=Samples&storage=MyStorage" \
     -H "Authorization: Bearer YOUR_ACCESS_TOKEN" \
     -H "Accept: application/json"
```

**Örnek C#**

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model.Requests;

var apiInstance = new CellsApi("client_id", "client_secret");
var request = new GetRangeRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    rangeName: "A1:B10",
    folder: "Samples",
    storage: "MyStorage"
);
var response = apiInstance.GetRange(request);
Console.WriteLine(response);
```

**Örnek Java**

```java
import com.aspose.cells.cloud.api.CellsApi;
import com.aspose.cells.cloud.model.requests.GetRangeRequest;

CellsApi api = new CellsApi("client_id", "client_secret");
GetRangeRequest request = new GetRangeRequest(
        "Book1.xlsx",
        "Sheet1",
        "A1:B10",
        "Samples",
        "MyStorage",
        null,
        null);
var response = api.getRange(request);
System.out.println(response);
```

**Örnek Python**

```python
from asposecellscloud import CellsApi, GetRangeRequest

api = CellsApi(client_id="client_id", client_secret="client_secret")
request = GetRangeRequest(
    name="Book1.xlsx",
    sheet_name="Sheet1",
    range_name="A1:B10",
    folder="Samples",
    storage="MyStorage"
)
response = api.get_range(request)
print(response)
```

**Yanıt Şeması (JSON)**

```json
{
  "Code": 200,
  "Status": "OK",
  "Range": {
    "ColumnCount": 2,
    "RowCount": 1,
    "FirstRow": 0,
    "FirstColumn": 0,
    "Values": [
      ["Value1", "Value2"]
    ]
  }
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                         |
|------|-----------------------------|--------------------------------------------------|
| 200  | Tamam                       | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir. |
| 400  | Geçersiz İstek              | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401  | Yetkisiz                    | Geçersiz veya eksik JWT belirteci. |
| 413  | Yük Çok Büyük               | Yüklenen dosya boyut sınırını aşıyor. |
| 500  | Sunucu İç Hatası            | Beklenmeyen sunucu hatası. |

- `200 Tamam` – Aralık başarıyla alındı.  
- `400 Geçersiz İstek` – Eksik veya geçersiz parametreler.  
- `401 Yetkisiz` – Geçersiz veya eksik erişim belirteci.  
- `404 Bulunamadı` – Belirtilen dosya, çalışma sayfası veya aralık bulunamadı.  
- `500 Sunucu İç Hatası` – Beklenmeyen sunucu hatası.

**Hata Yanıt Örnekleri**

```json
// 400 Geçersiz İstek
{
  "Code": 400,
  "Message": "İstek parametreleri geçersiz veya eksik."
}
```

```json
// 401 Yetkisiz
{
  "Code": 401,
  "Message": "Geçersiz veya eksik erişim belirteci."
}
```

```json
// 404 Bulunamadı
{
  "Code": 404,
  "Message": "Belirtilen dosya, çalışma sayfası veya aralık bulunamadı."
}
```

**Ayrıca Bakınız**

- [Bir adlandırılmış aralığa göre hücre verileri nasıl alınır](/cells/ranges/get/values/)  
- [Bir Excel çalışma kitabından adlandırılmış bir aralık nasıl alınır](/cells/ranges/get/name/)  
- [Aralık içeriğini güncelleme](/cells/ranges/update/)  
- [Bir aralığı silme](/cells/ranges/delete/)  
---