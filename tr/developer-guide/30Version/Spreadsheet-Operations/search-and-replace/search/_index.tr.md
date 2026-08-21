---
title: "Excel Dosyalarında Metin Bul – Aspose.Cells Cloud API"
description: "Aspose.Cells Cloud API kullanarak Excel (XLS, XLSX, XLSM, XLSB) ve ODS dosyalarında belirli bir metni arayın. İstek detaylarını, cURL ve SDK örneklerini ve hata işleme içerir."
keywords: "Aspose.Cells, Excel, arama, API, REST"
type: docs
url: /tr/cells/search/
aliases:
  - /search/
  - /search-without-using-storage/
  - /search-without-storage/
weight: 50
---

# Excel Dosyalarında Metin Bul – Aspose.Cells Cloud API

## Genel Bakış
Aspose.Cells Cloud, Excel çalışma kitaplarında (XLS, XLSX, XLSM, XLSB) ve OpenDocument Spreadsheet (ODS) dosyalarında belirli bir metin dizgisini aramak için bir **POST** uç noktası sağlar. API, istenen metni içeren tüm hücreleri ve eşleşmenin bulunduğu çalışma sayfasına bir bağlantı ile birlikte döndürür.

> **Kullanım Senaryoları**  
> - Daha fazla işlem yapmadan önce bir raporda belirli bir değerin mevcut olduğunu doğrulayın.  
> - Önce tüm eşleşmeleri listeleyen hızlı bir “bul ve değiştir” aracı oluşturun.  
> - Bir spreadsheet topluluğu boyunca anahtar terimlerin bir dizinini oluşturun.

---

## Ön Gereksinimler
| Gereksinim | Detaylar |
|-------------|---------|
| **Kimlik Doğrulama** | Aspose Cloud OAuth akışı ile elde edilen JWT belirteci. Belirteç **Cells** kapsamını içermelidir. |
| **Desteklenen formatlar** | XLS, XLSX, XLSM, XLSB, ODS |
| **Maksimum dosya boyutu** | 150 MB (sıkıştırılmış). 150 MB’yi aşan dosyalar **413 Payload Too Large** hatası döndürür. |
| **Gerekli başlıklar** | `Authorization: Bearer <jwt-token>`  <br> `Accept: application/json` |
| **İzinler** | Belirteç, hedef depolama alanı kullanılıyorsa (uzak depolama), okuma iznine sahip olmalıdır – dosya `multipart/form-data` olarak yükleniyorsa bu gerekli değildir. |

*İpucu:* JWT belirtecini oluşturmak için **/connect/token** uç noktasını kullanın. Ayrıntılar için [Kimlik Doğrulama Kılavuzu](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) sayfasını ziyaret edin.

---

## Uç Nokta

| Öğe | Değer |
|------|-------|
| **HTTP Yöntemi** | `POST` |
| **URL** | `https://api.aspose.cloud/v3.0/cells/search` |
| **Amaç** | Yüklü bir Excel çalışma kitabında belirli metni arayın. |
| **Güvenlik** | JWT belirteci (Bearer) – yukarıdaki *Ön Gereksinimler* bölümüne bakın. |

---

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulamayı</a> gerektirir.

## İstek Parametreleri

| İsim | Tür | Konum | Gerekli | Açıklama |
|------|-----|-------|---------|----------|
| `file` | **file** | `formData` (multipart) | **Evet** | Yüklenmesi gereken spreadsheet dosyası. |
| `text` | **string** | Sorgu dizgisi | **Evet** | Aranacak metin dizgisi. |
| `password` | **string** | Sorgu dizgisi | Hayır | Gerekliyse korumalı bir çalışma kitabını açmak için şifre. |
| `sheetname` | **string** | Sorgu dizgisi | Hayır | Aramayı sınırlamak için çalışma sayfasının adı. Atlanırsa tüm çalışma sayfaları aranır. |
| `checkExcelRestriction` | **boolean** | Sorgu dizgisi | Hayır (varsayılan: `true`) | `true` olarak ayarlandığında, API aramadan önce Excel’e özgü kısıtlamaları (örneğin salt okunur hücreler) doğrular. |

---

## İstek Örneği (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/search?text=Fatura&sheetname=Sayfa1" \
  -X POST \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt-token>" \
  -F "file=@InvoiceReport.xlsx"
```

`<jwt-token>` ifadesini geçerli bir belirteç ile değiştirin ve sorgu parametrelerini gerektiği şekilde ayarlayın.*

---

## Başarılı Yanıt

**HTTP 200 – Arama başarılı; yanıt, bulunan metin ögelerini içerir.**

```json
{
  "Status": "OK",
  "Code": 200,
  "TextItems": {
    "link": {
      "Href": "string",
      "Rel": "string",
      "Title": "string",
      "Type": "string"
    },
    "TextItemList": [
      {
        "Text": "Fatura #12345",
        "link": {
          "Href": "InvoiceReport.xlsx/worksheets/Sayfa1",
          "Rel": "parent",
          "Title": "Sayfa1",
          "Type": "string"
        }
      },
      {
        "Text": "Fatura #12346",
        "link": {
          "Href": "InvoiceReport.xlsx/worksheets/Sayfa1",
          "Rel": "parent",
          "Title": "Sayfa1",
          "Type": "string"
        }
      }
    ]
  }
}
```

### Yanıt Alanları

| Alan | Tür | Açıklama |
|------|-----|----------|
| `Status` | string | Genel istek durumu (başarı için `OK`). |
| `Code` | integer | HTTP durum kodu (200). |
| `TextItems.link` | object | Kaynak koleksiyonuna yönlendiren hiperbağlantı. |
| `TextItems.TextItemList` | array | Eşleşmelerin listesi. Her öge şunları içerir: |
| `Text` | string | Arama metniyle eşleşen hücre değeri. |
| `link` | object | Eşleşmenin bulunduğu çalışma sayfasına yönlendiren hiperbağlantı (`Href`, `Workbook/worksheets/SheetName` yolunu gösterir). |

---

## Hata Yanıtları

| HTTP Kodu | Anlamı | Tipik Neden | Örnek Gövde |
|-----------|--------|-------------|--------------|
| **400** | İstek Hatalı | Eksik gerekli parametreler, desteklenmeyen dosya türü veya geçersiz sorgu değerleri. | `{ "Status":"Error","Code":400,"Message":"'text' sorgu parametresi gerekli." }` |
| **401** | Yetkisiz | Eksik veya geçersiz JWT belirteci. | `{ "Status":"Error","Code":401,"Message":"Geçersiz veya süresi dolmuş erişim belirteci." }` |
| **413** | Gövde Çok Büyük | Yüklenen dosya 150 MB sınırını aşıyor. | `{ "Status":"Error","Code":413,"Message":"Dosya boyutu izin verilen sınırı aşıyor." }` |
| **500** | Sunucu İç Hatası | Beklenmeyen sunucu tarafı sorunu. | `{ "Status":"Error","Code":500,"Message":"Beklenmeyen bir hata oluştu." }` |

---

## SDK Örnekleri

Aşağıda, resmi Aspose.Cells Cloud SDK’ları kullanılarak **PostSearch** işlemi için minimal kod parçacıkları verilmiştir. `YOUR_JWT_TOKEN` ve dosya yolunu kendi değerlerinizle değiştirin.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;
using System;
using System.IO;

class Program
{
    static void Main()
    {
        var config = new Configuration
        {
            AccessToken = "YOUR_JWT_TOKEN",
            BaseUrl = "https://api.aspose.cloud"
        };
        var cellsApi = new CellsApi(config);

        using var stream = File.OpenRead("InvoiceReport.xlsx");
        var result = cellsApi.PostSearch(
            file: stream,
            text: "Fatura",
            sheetname: "Sayfa1",
            password: null,
            checkExcelRestriction: true
        );

        foreach (var item in result.TextItems.TextItemList)
        {
            Console.WriteLine($"{item.Text}  ->  {item.Link.Href}");
        }
    }
}
```

### Java

```java
import com.aspose.cells.cloud.sdk.api.CellsApi;
import com.aspose.cells.cloud.sdk.model.*;
import java.io.File;

public class PostSearchDemo {
    public static void main(String[] args) throws Exception {
        CellsApi api = new CellsApi("YOUR_JWT_TOKEN");
        File file = new File("InvoiceReport.xlsx");

        TextItemsResponse response = api.postSearch(
                file,
                "Fatura",
                null,          // password
                "Sayfa1",      // sheetname
                true           // checkExcelRestriction
        );

        response.getTextItems().getTextItemList()
                .forEach(item -> System.out.println(item.getText() + " -> " + item.getLink().getHref()));
    }
}
```

### Python

```python
import asposecellscloudsdk
from asposecellscloudsdk import CellsApi, ApiException, Configuration
from asposecellscloudsdk.models import TextItemsResponse
import pathlib

config = Configuration()
config.access_token = "YOUR_JWT_TOKEN"
config.host = "https://api.aspose.cloud"

api_instance = CellsApi(configuration=config)

file_path = pathlib.Path("InvoiceReport.xlsx")
with open(file_path, "rb") as f:
    result: TextItemsResponse = api_instance.post_search(
        file=f,
        text="Fatura",
        password=None,
        sheetname="Sayfa1",
        check_excel_restriction=True
    )

for item in result.text_items.text_item_list:
    print(f"{item.text} -> {item.link.href}")
```

### Node.js (TypeScript)

```typescript
import { CellsApi, Configuration } from "@asposecells-cloud/sdk";

const config = new Configuration({
    accessToken: "YOUR_JWT_TOKEN",
    basePath: "https://api.aspose.cloud"
});

const api = new CellsApi(config);

api.postSearch({
    file: fs.createReadStream("InvoiceReport.xlsx"),
    text: "Fatura",
    sheetname: "Sayfa1",
    checkExcelRestriction: true
}).then(response => {
    response.textItems?.textItemList?.forEach(item => {
        console.log(`${item.text} -> ${item.link?.href}`);
    });
}).catch(err => console.error(err));
```

*(PHP, Ruby, Go ve Perl için SDK’lar [Aspose.Cells Cloud GitHub deposunda](https://github.com/aspose-cells-cloud) mevcuttur.)*

---

## Ek Notlar

- **`checkExcelRestriction`** varsayılan olarak `true`’dır. Çalışma kitabında aramayı engelleyebilecek korumalı hücreler olmadığından eminseniz `false` olarak ayarlayın.
- API, diğer Aspose.Cells uç noktalarıyla kullanılabilecek **hiperbağlantıları** (`Href`) döndürür (örneğin, çalışma sayfasını indirmek veya hücre formatını almak için).
- Büyük çalışma kitaplarında arama yaparken yanıt süresini artırmak için `sheetname` parametresi ile arama kapsamını daraltmayı düşünün.

---

## İlgili Bağlantılar

- **Kimlik Doğrulama Kılavuzu** – <https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/>
- **PostSearch için OpenAPI Spesifikasyonu** – <https://apireference.aspose.cloud/cells/#/LightCells/PostSearch>
- **Aspose.Cells Cloud SDK’ları** – <https://github.com/aspose-cells-cloud>
- **Ortam Sınırları ve Kotalar** – <https://docs.aspose.cloud/total/getting-started/limits/>

---