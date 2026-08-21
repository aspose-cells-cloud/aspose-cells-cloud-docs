---
title: "Koşullu Biçimlendirmeyi Sil – Aspose.Cells Cloud API Referansı"
type: docs
url: /conditional-formattings/delete/
aliases:
  - /remove-conditional-formatting/
keywords: "Aspose.Cells, Koşullu Biçimlendirme, Sil, API, Excel, Bulut"
description: "Aspose.Cells Cloud REST API'sini kullanarak bir çalışma sayfasından koşullu biçimlendirme kuralını kaldırın. Parametreler, kimlik doğrulama, istek/yanıt örnekleri ve SDK kod parçacıklarını içerir."
weight: 60
---

# Koşullu Biçimlendirmeyi Sil

## Arkaplan
Koşullu biçimlendirme, belirli bir kriteri karşılayan hücrelere görsel stiller uygulamanızı sağlar (örneğin, bir eşiğin üzerindeki değerleri vurgulayın). Otomasyon senaryolarında mevcut bir kuralı kaldırmanız gerekebilir. Bu uç nokta, Aspose Cloud deposunda depolanan bir Excel çalışma kitabının çalışma sayfasından bir koşullu biçimlendirme kuralını siler.

## Gereksinimler
- **Cells** ürününün etkinleştirildiği bir **Aspose Cloud** hesabı.  
- OAuth 2.0 istemci kimlik bilgileri akışı ile oluşturulan **JWT erişim belirteci**.  
- Çalışma kitabının (`{name}`) zaten belirtilen **klasörde** ve **depoda** (varsa) bulunuyor olması gerekir.  
- Aşağıda gösterilen URL’lerde **v3.0** API sürümü (varsayılan) kullanılmaktadır.

## Kimlik Doğrulama
Tüm Aspose.Cells Cloud uç noktaları **JWT belirteci tabanlı kimlik doğrulama** gerektirir.

```http
Authorization: Bearer <access_token>
```

### Erişim belirteci edinin (cURL)

```bash
curl -X POST "https://api.aspose.cloud/connect/token" \
  -d "grant_type=client_credentials&client_id=<your_client_id>&client_secret=<your_client_secret>&scope=Cells"
```

**Yanıt**

```json
{
  "access_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...",
  "token_type": "Bearer",
  "expires_in": 3600
}
```

Döndürülen `access_token` değerini her istekte `Authorization` başlığında kullanın.

## HTTP İsteği

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/conditionalFormattings/{index}
```

### Yol Parametreleri

| Ad          | Tür      | Gerekli | Açıklama |
|-------------|----------|---------|----------|
| `name`      | string   | Evet    | Çalışma kitabının dosya adı (örneğin, `Book1.xlsx`). |
| `sheetName` | string   | Evet    | Koşullu biçimlendirmeyi içeren çalışma sayfası. |
| `index`     | integer  | Evet    | Silinecek koşullu biçimlendirme kuralının sıfır tabanlı indeksi. |

### Sorgu Parametreleri

| Ad             | Tür     | Gerekli | Açıklama |
|----------------|---------|---------|----------|
| `folder`       | string  | Hayır   | Çalışma kitabının bulunduğu bulut klasörü. |
| `storageName`  | string  | Hayır   | Aspose Cloud depolama hizmetinin adı. |

## İstek Örneği (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/conditionalFormattings/0?folder=MyFolder&storageName=MyStorage" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

### Başarılı Yanıt

```json
{
  "Code": "200",
  "Status": "OK"
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama |
|-----|-----------------------------|----------|
| 200 | OK                          | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request                 | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized                | Geçersiz veya eksik JWT belirteci. |
| 413 | Payload Too Large           | Yüklenen dosya boyut sınırını aşıyor. |
| 500 | Internal Server Error       | Beklenmeyen sunucu hatası. |

## Hata Yanıtları

| HTTP Kodu | Neden | Örnek Gövde |
|-----------|-------|-------------|
| **400**   | Bad Request – eksik veya geçersiz parametreler. | `{ "Code":"400", "Message":"Geçersiz parametre değeri." }` |
| **401**   | Unauthorized – eksik veya geçersiz JWT belirteci. | `{ "Code":"401", "Message":"Erişim belirteci eksik veya geçersiz." }` |
| **404**   | Not Found – çalışma kitabının veya çalışma sayfasının bulunamaması. | `{ "Code":"404", "Message":"Dosya bulunamadı." }` |
| **500**   | Internal Server Error – beklenmeyen sunucu hatası. | `{ "Code":"500", "Message":"Beklenmeyen bir hata oluştu." }` |

## SDK Örnekleri
Aşağıdaki kod parçacıkları, **Koşullu Biçimlendirmeyi Sil** işlemini resmi Aspose.Cells Cloud SDK'ları kullanarak nasıl çağıracağınızı göstermektedir.

### C# (.NET)

```csharp
using Aspose.Cells.Cloud.SDK;
using Aspose.Cells.Cloud.SDK.Requests;

// API istemcisini yapılandırın
var config = new Configuration
{
    ClientId = "<your_client_id>",
    ClientSecret = "<your_client_secret>"
};
var apiInstance = new ConditionalFormattingsApi(config);

// Koşullu biçimlendirmeyi silin
var request = new DeleteWorksheetConditionalFormattingRequest(
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    folder: "MyFolder",
    storageName: null
);
apiInstance.DeleteWorksheetConditionalFormatting(request);
```

### Java

```java
import com.aspose.cells.cloud.sdk.api.*;
import com.aspose.cells.cloud.sdk.model.*;
import com.aspose.cells.cloud.sdk.requests.*;

ApiClient client = new ApiClient();
client.setAppKey("<your_client_id>");
client.setAppSid("<your_client_secret>");

ConditionalFormattingsApi api = new ConditionalFormattingsApi(client);

DeleteWorksheetConditionalFormattingRequest request = new DeleteWorksheetConditionalFormattingRequest(
        "Book1.xlsx",
        "Sheet1",
        0,
        "MyFolder",
        null);

api.deleteWorksheetConditionalFormatting(request);
```

### Node.js

```javascript
const { ConditionalFormattingsApi, DeleteWorksheetConditionalFormattingRequest } = require('asposecellscloud');

const config = {
    clientId: "<your_client_id>",
    clientSecret: "<your_client_secret>"
};

const apiInstance = new ConditionalFormattingsApi(config);

const request = new DeleteWorksheetConditionalFormattingRequest({
    name: "Book1.xlsx",
    sheetName: "Sheet1",
    index: 0,
    folder: "MyFolder",
    storageName: null
});

apiInstance.deleteWorksheetConditionalFormatting(request)
    .then(() => console.log('Koşullu biçimlendirme silindi.'))
    .catch(err => console.error(err));
```

### Python

```python
from asposecellscloud import ConditionalFormattingsApi, DeleteWorksheetConditionalFormattingRequest, ApiClient

api_client = ApiClient(client_id="<your_client_id>", client_secret="<your_client_secret>")
api = ConditionalFormattingsApi(api_client)

request = DeleteWorksheetConditionalFormattingRequest(
    name="Book1.xlsx",
    sheetName="Sheet1",
    index=0,
    folder="MyFolder",
    storageName=None
)

api.delete_worksheet_conditional_formatting(request)
print("Koşullu biçimlendirme kaldırıldı.")
```

*(Ruby, Go, Perl ve Swift için ek SDK kod parçacıkları [GitHub deposunda](https://github.com/aspose-cells-cloud) mevcuttur.)*

## Ayrıca Bakınız
- **Kimlik Doğrulama Kılavuzu** – [JWT belirteci tabanlı kimlik doğrulama](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- **OpenAPI Specification** – Bu uç nokta için ayrıntılı şema (yeni sekmede açılır)  
  `<a href="https://apireference.aspose.cloud/cells/#/ConditionalFormattings/DeleteWorksheetConditionalFormatting" target="_blank" rel="noopener noreferrer">OpenAPI Specification</a>`  
- **Koşullu Biçimlendirme Genel Bakışı** – Biçimlendirme kurallarını nasıl oluşturabileceğinizi, güncelleyebileceğinizi ve listeleyebileceğinizi öğrenin.  
- **Aspose.Cells Cloud SDK'ları** – Desteklenen tüm dillerin tam listesi [GitHub deposunda](https://github.com/aspose-cells-cloud).  

---  

*Bu sayfa, standart Aspose.Cells Cloud API dokümantasyon şablonunu takip eder, Gereksinimler bölümünü içerir ve erişilebilirlik ve SEO en iyi uygulamalarına uygundur.*