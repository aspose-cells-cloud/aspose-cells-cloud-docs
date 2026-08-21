---
title: Bir Excel çalışma sayfasındaki tüm OLE nesnelerini silme
description: Aspose.Cells Cloud REST API'sini (v3.0) kullanarak bir Excel çalışma sayfasındaki tüm OLE (Nesne Bağlama ve Gömme) nesnelerini nasıl kaldıracağınızı öğrenin. Uç nokta, parametreler, istek/yanıt örnekleri, SDK kod parçacıkları, kimlik doğrulama, hata yönetimi ve SSS içerir.
keywords: Aspose.Cells Cloud, OLE nesnelerini sil, Excel API, REST API, çalışma sayfası OLE temizleme, bulut SDK
api_version: v3.0
last_updated: 2024-11-01
weight: 60
---

# Bir Excel çalışma sayfasındaki tüm OLE nesnelerini silme

**OleObjects – Clear** işlemi, belirtilen bir çalışma sayfasından **tüm** OLE (Nesne Bağlama ve Gömme) nesnelerini kaldırır, hücre verilerini ise olduğu gibi bırakır. Bu işlem, eski hesap tablolarını temizlemek veya bir çalışma kitabını yeniden dağıtım için hazırlamak için yararlıdır.

---

## Ön Gereksinimler

- Geçerli bir **Aspose Cloud JWT erişim belirteci** (OAuth 2.0).  
- Hedef çalışma kitabının Aspose Cloud depolama alanına kaydedilmiş olması gerekir (veya bulunan `klasör`/`depoadı` değerini belirtmelisiniz).  
- API sürümü **v3.0** veya üzeri.  

> **Not:** İşlem *idempotandır* – OLE nesnesi bulunmayan bir çalışma sayfasında bu işlemi yürütmek, başarılı bir `200 OK` yanıtı döndürür.

---

## HTTP İsteği

```
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects
```

### Yol parametreleri

| Ad           | Tür    | Gerekli | Açıklama                            |
|--------------|--------|---------|-------------------------------------|
| `name`       | string | ✔️      | Çalışma kitap dosyasının adı.       |
| `sheetName`  | string | ✔️      | Çalışma sayfasının adı.             |

### Sorgu parametreleri

| Ad            | Tür    | Gerekli | Açıklama                              |
|---------------|--------|---------|---------------------------------------|
| `folder`      | string | isteğe bağlı | Çalışma kitabının bulunduğu klasör. |
| `storageName` | string | isteğe bağlı | Çalışma kitabının bulunduğu depo adı. |

**İstek başlıkları**

| Başlık               | Değer                         |
|----------------------|------------------------------|
| `Authorization`      | `Bearer <jwt token>` |
| `Accept`             | `application/json` |
| `Content-Type`       | `application/json` |

---

## İstek Örneği (cURL)

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Embedded_OleObject_Sample_Book1.xlsx/worksheets/Sheet1/oleobjects?folder=Samples&storageName=MyStorage" \
     -X DELETE \
     -H "Authorization: Bearer <jwt token>" \
     -H "Accept: application/json" \
     -H "Content-Type: application/json"
```

*`<jwt token>` ifadesini geçerli bir erişim belirteci ile değiştirin ve gerekirse `folder`/`storageName` değerlerini uygun şekilde ayarlayın.*

---

## Başarılı Yanıt

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                          |
|-----|-----------------------------|---------------------------------------------------|
| 200 | OK                          | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örn., desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci. |
| 413 | Payload Too Large (Çok Büyük Yük) | Yüklenecek dosya boyut sınırını aşıyor. |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası. |
---

## SDK Örnekleri

Aşağıdaki kod parçacıkları, resmi Aspose.Cells Cloud SDK’ları ile **DeleteWorksheetOleObjects** işlemini nasıl çağıracağınızı gösterir. Yer tutucu değerleri (`<YOUR_TOKEN>`, `<FILE_NAME>` vb.) kendi verilerinizle değiştirin.

| Dil       | Örnek |
|-----------|-------|
| **C#** | <details><summary>C# örneğini göster</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar config = new Configuration { AccessToken = \"<YOUR_TOKEN>\", BasePath = \"https://api.aspose.cloud\" };\nvar api = new OleObjectsApi(config);\napi.DeleteWorksheetOleObjects(name: \"Sample.xlsx\", sheetName: \"Sheet1\", folder: \"Samples\", storageName: null);\n```</details> |
| **Java** | <details><summary>Java örneğini göster</summary>```java\nimport com.aspose.cells.cloud.api.OleObjectsApi;\nimport com.aspose.cells.cloud.client.ApiClient;\nimport com.aspose.cells.cloud.client.Configuration;\n\nConfiguration config = new Configuration();\nconfig.setAccessToken(\"<YOUR_TOKEN>\");\nconfig.setBasePath(\"https://api.aspose.cloud\");\nOleObjectsApi api = new OleObjectsApi(new ApiClient(config));\napi.deleteWorksheetOleObjects(\"Sample.xlsx\", \"Sheet1\", \"Samples\", null);\n```</details> |
| **Python** | <details><summary>Python örneğini göster</summary>```python\nfrom asposecellscloud import ApiClient, Configuration, OleObjectsApi\n\nconfig = Configuration()\nconfig.access_token = '<YOUR_TOKEN>'\nconfig.host = 'https://api.aspose.cloud'\nclient = ApiClient(configuration=config)\napi = OleObjectsApi(client)\napi.delete_worksheet_ole_objects(name='Sample.xlsx', sheet_name='Sheet1', folder='Samples')\n```</details> |
| **Node.js** | <details><summary>Node.js örneğini göster</summary>```javascript\nconst { OleObjectsApi, Configuration } = require('asposecellscloud');\n\nlet config = new Configuration({ accessToken: '<YOUR_TOKEN>', basePath: 'https://api.aspose.cloud' });\nlet api = new OleObjectsApi(config);\napi.deleteWorksheetOleObjects('Sample.xlsx', 'Sheet1', { folder: 'Samples' })\n  .then(() => console.log('All OLE objects deleted'))\n  .catch(err => console.error(err));\n```</details> |
| **Go** | <details><summary>Go örneğini göster</summary>```go\npackage main\nimport (\n    \"context\"\n    \"github.com/aspose-cells-cloud/aspose-cells-cloud-go/v3\"\n)\n\nfunc main() {\n    cfg := asposecellscloud.NewConfiguration()\n    cfg.AccessToken = \"<YOUR_TOKEN>\"\n    cfg.Host = \"https://api.aspose.cloud\"\n    api := asposecellscloud.NewOleObjectsApi(cfg)\n    _, err := api.DeleteWorksheetOleObjects(context.Background(), \"Sample.xlsx\", \"Sheet1\", map[string]interface{}{ \"folder\": \"Samples\" })\n    if err != nil { panic(err) }\n    println(\"All OLE objects deleted\")\n}\n```</details> |

*Tüm desteklenen diller için tam kaynak dosyaları [Aspose.Cells Cloud GitHub deposunda](https://github.com/aspose-cells-cloud) mevcuttur.*

---

## Hatalar ve Yönetimi

- **Idempotans** – Zaten OLE nesnesi bulunmayan bir çalışma sayfasından OLE nesnelerini silmek yine de `200 OK` döndürür.  
- **Belirteç süresinin dolması** – `401 Unauthorized` (Yetkisiz) hatası alırsanız, yeni bir JWT belirteci edinin ve işlemi yeniden deneyin.  
- **Geçersiz çalışma sayfası adı** – Çalışma sayfası adı, çalışma kitabında kullanılan büyük/küçük harfle tam olarak eşleşmelidir; aksi takdirde `400 Bad Request` (Hatalı İstek) hatası döndürülür.  

Geçici `500` hataları için üssel geri plan stratejisiyle yeniden deneme mantığı uygulayın.

---

## SSS

**S1: `folder` ve `storageName` parametrelerini belirtmem gerekiyor mu?**  
**C:** Hayır. Belirtilmezlerse Aspose Cloud, varsayılan depo ve kök klasörü kullanır.

**S2: Yalnızca belirli bir hücreden OLE nesnelerini silebilir miyim?**  
**C:** Bu uç nokta, çalışma sayfasındaki **tüm** OLE nesnelerini siler. Tek bir nesneyi kaldırmak için *Belirli bir OLE nesnesini sil* işlemini kullanın.

**S3: Çalışma kitabı düzenleme için kilitliyse ne olur?**  
**C:** API, dosyanın kilitli olduğunu belirten bir `400 Bad Request` (Hatalı İstek) hatası döndürür. Uç noktayı çağırmadan önce dosyanın başka bir yerde açılmadığından emin olun.

**S4: Çalışma kitabı için boyut sınırı var mı?**  
**C:** Hizmet, genel Aspose Cloud dosya boyutu sınırlarını (şu anda dosya başına en fazla 2 GB) uygular. Daha büyük dosyalar bölünebilir veya parça parça işlenebilir.

---

## En İyi Uygulamalar

- **Performans** – Dokümantasyon sitenizde üçüncü taraf betikleri yüklerken `async` veya `defer` özniteliklerini kullanarak ilk sayfa yükleme süresini azaltın.  
- **Güvenlik** – Yeni bir sekmede açılan tüm harici bağlantılar için `rel="noopener noreferrer"` ekleyin.  
- **Erişilebilirlik** – Dekoratif simgeler (örn., kenar çubuklarındaki aşağı doğru oklar) WCAG AA standartlarını karşılamak için `alt=""` ve `role="presentation"` özniteliklerine sahip olmalıdır.  
- **Tutarlılık** – Kodlama artefaktlarını önlemek için tarih formatlarını ISO‑8601 (`YYYY‑MM‑DD`) olarak tutun.  

---

## İlgili İşlemler

- **OLE nesnesi ekleme** – `POST /cells/{name}/worksheets/{sheetName}/oleobjects`  
- **Belirli bir OLE nesnesini silme** – `DELETE /cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}`  

Sayfanın altında yer alan gezinti bağlantılarını kullanarak ilgili API işlemlerine geçiş yapın.

---