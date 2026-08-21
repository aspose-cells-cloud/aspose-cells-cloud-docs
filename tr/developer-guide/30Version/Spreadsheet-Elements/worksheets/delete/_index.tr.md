---
title: "Excel çalışma kitabında çalışma sayfalarını silme ile çalışma"
second_title: "Belge"
linktitle: "Sil"
type: docs
url: /tr/worksheets/delete/
keywords: "Aspose.Cells, Bulut, REST API, Çalışma Sayfası Sil, Excel, C#, Java, Python"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma kitabından tek veya birden fazla çalışma sayfasını nasıl sileceğinizi öğrenin. C#, Java ve Python örneklerini, önkoşulları, hata ayıklama ipuçlarını ve ilgili işlemleri içerir."
weight: 20
ArticleTitle: "Aspose.Cells Cloud API ile Excel Çalışma Kitabında Çalışma Sayfası(lar) Silme"
---

## Excel Çalışma Kitabında Çalışma Sayfalarını Silme ile Çalışma

Bir uygulama dinamik olarak Excel dosyaları oluşturduğunda veya değiştirdiğinde, geçici raporlar, yer tutucu sayfalar veya güncel olmayan veriler gibi artık gerekli olmayan çalışma sayfalarını kaldırmanız gerekebilir. Aspose.Cells Cloud API, tek bir istekte tek veya birden fazla çalışma sayfasını silmeyi kolaylaştırır.

**API Referansı**  

| Öğe | Detaylar |
|------|---------|
| **HTTP Yöntemi** | `DELETE` |
| **Uç Nokta** | `/cells/{dosyaAdı}/worksheets` |
| **Yol Parametreleri** | `dosyaAdı` – Excel dosyasının adı (zorunludur) |
| **Sorgu Parametreleri** | `sayfaAdı` – silinecek çalışma sayfasının adı (isteğe bağlı, tek sayfa silme için) <br> `klasör` – depolamadaki kaynak klasör (isteğe bağlı) <br> `depolar` – kullanılacak depo adı (isteğe bağlı) |
| **İstek Gövdesi** | *Yok* |
| **Başarılı Yanıt** | `200 OK` – çalışma sayfası(lar) başarıyla silindi. İşlem durumunu içeren bir JSON nesnesi döndürür. |
| **Hata Yanıtları** | `400 Bad Request` – geçersiz parametreler <br> `401 Unauthorized` – kimlik doğrulama hatası <br> `404 Not Found` – dosya veya çalışma sayfası bulunamadı <br> `500 Internal Server Error` – sunucu tarafında sorun |

**İstek**  

Bir veya daha fazla çalışma sayfasını silmek için yukarıdaki uç noktaya bir `DELETE` isteği gönderin; zorunlu `dosyaAdı` parametresini ve tek bir sayfa silme için isteğe bağlı `sayfaAdı` sorgu parametresini ekleyin. `sayfaAdı` belirtilmezse, API çalışma kitabındaki tüm çalışma sayfalarını siler.

**Parametreler**  

- `dosyaAdı` (dize, zorunludur): Uzantısıyla birlikte Excel dosyasının adı.  
- `sayfaAdı` (dize, isteğe bağlı): Silinecek belirli çalışma sayfasının adı. Belirtilmezse API tüm çalışma sayfalarını siler.  
- `klasör` (dize, isteğe bağlı): Depolamadaki dosyayı içeren klasörün yolu.  
- `depolar` (dize, isteğe bağlı): Kullanılacak Aspose Cloud depo adı.

**Yanıtlar**  

- **200 OK** – Örnek JSON:  
  ```json
  {
    "code": 200,
    "status": "OK",
    "message": "Çalışma sayfası(lar) başarıyla silindi."
  }
  ```
- **400 Bad Request** – Geçersiz istek parametreleri.  
- **401 Unauthorized** – Kimlik doğrulama belirteci eksik veya geçersiz.  
- **404 Not Found** – Belirtilen dosya veya çalışma sayfası mevcut değil.  
- **500 Internal Server Error** – Beklenmeyen sunucu hatası.

**Örnekler**  

*Aşağıda, silme uç noktasını üç popüler dil kullanarak çağırma yöntemini gösteren kısa kod parçacıkları yer almaktadır.*

**C# Örneği**  
```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Client;
using Aspose.Cells.Cloud.SDK.Model;

var api = new CellsApi("client_id", "client_secret");
var fileName = "Sample.xlsx";
var sheetName = "TempSheet";

try
{
    var response = api.DeleteWorksheet(fileName, sheetName);
    Console.WriteLine($"Durum: {response.Status}");
}
catch (Exception ex)
{
    Console.WriteLine($"Hata: {ex.Message}");
}
```

**Java Örneği**  
```java
import com.aspose.cloud.cells.api.CellsApi;
import com.aspose.cloud.cells.model.ResponseMessage;

public class DeleteWorksheetDemo {
    public static void main(String[] args) throws Exception {
        CellsApi api = new CellsApi("client_id", "client_secret");
        String fileName = "Sample.xlsx";
        String sheetName = "TempSheet";

        try {
            ResponseMessage response = api.deleteWorksheet(fileName, sheetName, null, null);
            System.out.println("Durum: " + response.getStatus());
        } catch (Exception e) {
            System.err.println("Hata: " + e.getMessage());
        }
    }
}
```

**Python Örneği**  
```python
from asposecellscloud import CellsApi, ApiException

api = CellsApi(client_id="client_id", client_secret="client_secret")
file_name = "Sample.xlsx"
sheet_name = "TempSheet"

try:
    response = api.delete_worksheet(file_name, sheet_name)
    print(f"Durum: {response.status}")
except ApiException as e:
    print(f"Hata: {e}")
```

**Hata Yönetimi**  

- İsteği göndermeden önce kimlik doğrulama belirtecini geçerli olduğundan emin olun.  
- Yanıt durum kodunu kontrol edin; `400`, `401`, `404` ve `500` durumlarını uygun şekilde işleyin.  
- Ağ veya SDK özel durumlarını yakalamak için try-catch bloklarını (veya eşdeğerlerini) kullanın.

**İlgili İşlemler**  

- [Çalışma sayfası ekle](/worksheets/add/) – Mevcut bir çalışma kitabına yeni bir çalışma sayfası oluşturun.  
- [Çalışma sayfası kopyala](/worksheets/copy/) – Mevcut bir çalışma sayfasını kopyalayın.  
- [Çalışma sayfası yeniden adlandır](/worksheets/rename/) – Bir çalışma sayfasının adını değiştirin.  
- [Çalışma sayfasını taşı](/worksheets/move/) – Çalışma sayfalarını bir çalışma kitabında yeniden sıralayın.  
---