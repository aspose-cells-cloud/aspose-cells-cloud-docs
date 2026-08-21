---
title: "Aspose.Cells Cloud Web API – Excel Dosyaları İçin Açma ve Düzenleme Şifresi Belirleme/Güncelleme"
second_title: "Kapsamlı Geliştirici Kılavuzu"
ArticleTitle: "Elektronik Tablo Koruması – Açma Şifresi ve Düzenleme Şifresi Belirleme"
linktitle: "Koruma"
type: docs
url: /tr/protection/
keywords: "Aspose.Cells, Bulut, API, Elektronik Tablo, Koruma, Açma Şifresi, Okuma-Yazma Şifresi, Excel"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma kitabını açma veya okuma-yazma şifresi ile nasıl koruyacağınızı öğrenin. İstek sözdizimi, kod örnekleri ve hata işleme içerir."
weight: 60
---

Bu kılavuzda, Aspose.Cells Cloud Web API’sini kullanarak elektronik tablolarda **açma şifresi** ve **okuma-yazma şifresi** belirlemeyi, değiştirmeyi ve kaldırmayı öğreneceksiniz. Bu özellikler, Excel çalışma kitaplarınızdaki hassas verilerin korunmasına yardımcı olur.

**Ön Gereksinimler**  
- Geçerli bir API anahtarı ve SID ile aktif bir Aspose.Cells Cloud hesabı.  
- Korumak istediğiniz çalışma kitabının Aspose Bulut depolama alanına yüklenmiş olması veya herkese açık bir URL üzerinden erişilebilir olması gerekir.  

**API Referansı**  

| **HTTP Yöntemi** | **Uç Nokta** | **Sorgu / Yol Parametreleri** | **Açıklama** |
|-----------------|--------------|----------------------------|-----------------|
| `PUT` | `/cells/{fileName}/protection` | `fileName` (yol) – çalışma kitabının adı<br>`openPassword` (sorgu, isteğe bağlı) – dosyayı açmak için gerekli şifre<br>`readWritePassword` (sorgu, isteğe bağlı) – dosyayı değiştirmek için gerekli şifre | Belirtilen çalışma kitabının açma ve/veya okuma-yazma şifrelerini ayarlar veya günceller. |
| `DELETE` | `/cells/{fileName}/protection` | `fileName` (yol) – çalışma kitabının adı | Çalışma kitabını koruyan tüm şifreleri kaldırır. |

**İstek Gövdesi Örneği (JSON)**  

```json
{
  "OpenPassword": "AçmaSifrem123",
  "ReadWritePassword": "DüzenlemeSifrem456"
}
```

**Yanıt Örneği (JSON)**  

```json
{
  "Code": 200,
  "Status": "OK",
  "Message": "Çalışma kitabı koruması başarıyla güncellendi."
}
```

**HTTP Durum Kodları**

| Kod | Anlamı                     | Açıklama                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | Tamam (OK)                  | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400  | Hatalı İstek (Bad Request)  | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401  | Yetkisiz (Unauthorized)     | Geçersiz veya eksik JWT belirteci. |
| 413  | Yük Çok Büyük (Payload Too Large) | Yüklenen dosya boyut sınırlarını aşıyor. |
| 500  | Sunucu İç Hatası (Internal Server Error) | Beklenmeyen sunucu hatası. |

**Kod Örnekleri**

*C# (Aspose.Cells Cloud SDK)*  

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var apiInstance = new CellsApi("YOUR_CLIENT_ID", "YOUR_CLIENT_SECRET");
var request = new SetWorkbookProtectionRequest(
    name: "Sample.xlsx",
    openPassword: "AçmaSifrem123",
    readWritePassword: "DüzenlemeSifrem456"
);
apiInstance.SetWorkbookProtection(request);
```

*Python (Aspose.Cells Cloud SDK)*  

```python
import asposecellscloud
from asposecellscloud.apis.cells_api import CellsApi
from asposecellscloud.models import SetWorkbookProtectionRequest

api = CellsApi(client_id="YOUR_CLIENT_ID", client_secret="YOUR_CLIENT_SECRET")
request = SetWorkbookProtectionRequest(
    name="Sample.xlsx",
    open_password="AçmaSifrem123",
    read_write_password="DüzenlemeSifrem456"
)
api.set_workbook_protection(request)
```

**Hata İşleme**  
Bir hata oluştuğunda API, `Code`, `Message` ve isteğe bağlı olarak `Description` içeren bir JSON yükü döndürür. Durum kodunu kontrol edin ve uygulama mantığınıza uygun şekilde işlem yapın.

**İlgili Konular**  

- **[Aspose.Cells Cloud ile bir elektronik tabloyu şifreyle nasıl koruyacağınız](https://docs.aspose.cloud/cells/protect-spreadsheet/).**  
- **[Aspose.Cells Cloud ile bir elektronik tablonun korumasını nasıl kaldıracakğınız](https://docs.aspose.cloud/cells/unprotect-spreadsheet/).**  
---