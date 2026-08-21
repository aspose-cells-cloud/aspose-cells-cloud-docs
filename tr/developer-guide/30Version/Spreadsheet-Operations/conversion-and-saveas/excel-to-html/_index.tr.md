---
title: Excel Dosyasını HTML'ye Dönüştür  
description: Aspose.Cells Cloud API'sini kullanarak bir Excel çalışma kitabını HTML dosyasına dönüştürün.  
api_version: v3.0  
base_url: https://api.aspose.cloud/v3.0  
---

# Excel Dosyasını HTML'ye Dönüştür  

Aspose.Cells Cloud, bir Excel çalışma kitabını (XLS, XLSX, CSV vb.) bir HTML belgesine dönüştüren güçlü bir REST uç noktası sağlar. İşlem, oluşturulan HTML dosyasını (adı, boyutu ve Base64 ile kodlanmış içeriği) içeren bir **FileInfo** nesnesi döndürür.

---

## Ön Gereksinimler

| Gereksinim | Nasıl Karşılanır |
|------------|------------------|
| **Aspose Cloud hesabı** | [aspose.cloud](https://www.aspose.cloud) adresinde kaydolun. |
| **JWT erişim belirteci** | OAuth 2.0 `POST /connect/token` uç noktasından bir bearer belirteci edinin. |
| **Depolama (isteğe bağlı)** | API’nin belirli bir depodan dosya okumasını/yazmasını istiyorsanız, önce oluşturun (örneğin Amazon S3, Azure Blob veya Aspose Cloud deposu). |
| **cURL / SDK** | Multipart/form-data destekleyen herhangi bir HTTP istemcisi (cURL, Postman veya Aspose.Cells SDK’larından biri). |

---

## Kimlik Doğrulama

Tüm Aspose.Cells Cloud istekleri **JWT belirteci tabanlı kimlik doğrulama** gerektirir.

```http
Authorization: Bearer <erişim-belirteci>
```

Belirteç, her isteğin `Authorization` başlığına eklenmelidir.

---

## Uç Nokta

```
POST https://api.aspose.cloud/v3.0/cells/convert/html
```

> **Not** – İstek `multipart/form-data` olarak gönderilmelidir. Excel dosyası, çok parçalı gövdenin ilk parçası olarak sağlanmalıdır.

---

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

## İstek Parametreleri  

### Sorgu Parametreleri  

| Ad                      | Tür     | Gerekli | Varsayılan | Açıklama |
|-------------------------|---------|---------|------------|----------|
| `password`              | string  | Hayır   | –          | Korumalı bir çalışma kitabını açmak için şifre. |
| `storageName`           | string  | Hayır   | –          | Kaynak dosyanın bulunduğu depo adı. |
| `checkExcelRestriction` | boolean | Hayır   | `true`     | `true` olarak ayarlandığında, hizmet Excel’e özgü kısıtlamaları (örneğin korunmuş sayfalar) doğrular. |
| `region`                | string  | Hayır   | –          | Çalışma kitabının bölgesel ayarları (örneğin `tr-TR`). |
| `FontsLocation`         | string  | Hayır   | –          | İşlem sırasında ihtiyaç duyulan özel fontları içeren klasörün URL’si veya yolu. |

### Form Verisi (Multipart)  

| Ad   | Tür  | Gerekli | Açıklama |
|------|------|---------|----------|
| **File** | dosya | **Evet** | Dönüştürülecek Excel çalışma kitabını belirtir. Çok parçalı isteğin ilk parçası olarak verilmelidir. |

---

## İstek Örneği (cURL)

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/html?checkExcelRestriction=true" \
     -H "accept: multipart/form-data" \
     -H "Authorization: Bearer <erişim-belirteci>" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@/yolunuz/your_workbook.xlsx"
```

---

## Başarılı Yanıt  

**Durum Kodu:** `200 OK`

| Alan         | Tür    | Açıklama |
|--------------|--------|----------|
| `Filename`   | string | Oluşturulan HTML dosyasının adı (örneğin `ornek.html`). |
| `FileSize`   | int    | HTML dosyasının bayt cinsinden boyutu. |
| `FileContent`| string | Base64 ile kodlanmış HTML içeriği. |

```json
{
  "Filename": "ornek.html",
  "FileSize": 12345,
  "FileContent": "base64_kodlu_metin"
}
```

Yanıt şeması, **FileInfo** modeli tarafından tanımlanır: [/cells/file-info](/cells/file-info/).

---

## Hata Yanıtları  

| Kod | Anlam                  | Örnek Yük |
|-----|------------------------|-----------|
| `400` | Geçersiz İstek – eksik/geçersiz parametreler | ```json { "Code": "BadRequest", "Message": "'File' parçası gereklidir." } ``` |
| `401` | Yetkisiz – geçersiz veya eksik JWT belirteci | ```json { "Code": "InvalidToken", "Message": "Erişim belirteci eksik veya süresi dolmuş." } ``` |
| `404` | Bulunamadı – kaynak dosya belirtilen depoda yok | ```json { "Code": "FileNotFound", "Message": "'my.xlsx' adlı dosya 'MyStorage' adlı depoda bulunmuyor." } ``` |
| `413` | Yük Çok Büyük – yüklenen dosya izin verilen boyutu aşıyor | ```json { "Code": "RequestEntityTooLarge", "Message": "Yüklenen dosya 100 MB sınırını aşıyor." } ``` |
| `429` | Çok Fazla İstek – hız sınırı aşıldı | ```json { "Code": "TooManyRequests", "Message": "Dakikada 60 istek sınırı aşıldı." } ``` |
| `500` | Sunucu İç Hatası – beklenmeyen sunucu durumu | ```json { "Code": "InternalError", "Message": "Beklenmeyen bir hata oluştu. Lütfen daha sonra tekrar deneyin." } ``` |

---

## Hız Sınırları  

| Sınır | Açıklama |
|-------|----------|
| **Hesap başına 60 istek/dakika** (varsayılan) | Bu sınırın aşılması `429 Too Many Requests` hatasını döndürür. İstemci mantığınızı ayarlayın veya Aspose Cloud portalından daha yüksek bir kota talep edin. |

---

## SDK Desteği  

Aspose, bu uç noktayı sarmalayan birden fazla dil için birinci sınıf SDK’lar sağlar. Aşağıdaki örnekler, aynı dönüşümü resmi SDK’lar kullanarak göstermektedir.

| Dil      | Örnek |
|----------|-------|
| C#       | <details><summary>Örneği göster</summary>```csharp\nusing Aspose.Cells.Cloud.SDK.Api;\nusing Aspose.Cells.Cloud.SDK.Model;\n\nvar apiInstance = new ConversionApi();\nvar file = File.ReadAllBytes("your.xlsx");\nvar result = apiInstance.PostConvertWorkbookToHtml(file, password: null, checkExcelRestriction: true);\nConsole.WriteLine(result.Filename);\n```</details> |
| Java     | <details><summary>Örneği göster</summary>```java\nConversionApi api = new ConversionApi();\nFile file = new File("your.xlsx");\nFileInfo info = api.postConvertWorkbookToHtml(file, null, true);\nSystem.out.println(info.getFilename());\n```</details> |
| Python   | <details><summary>Örneği göster</summary>```python\nfrom asposecellscloud import ConversionApi\napi = ConversionApi()\nwith open('your.xlsx', 'rb') as f:\n    file_info = api.post_convert_workbook_to_html(file=f.read())\nprint(file_info.filename)\n```</details> |
| Node.js  | <details><summary>Örneği göster</summary>```javascript\nconst { ConversionApi } = require('asposecellscloud');\nconst api = new ConversionApi();\nconst fs = require('fs');\napi.postConvertWorkbookToHtml({ File: fs.createReadStream('your.xlsx') })\n   .then(info => console.log(info.Filename));\n```</details> |
| Go       | <details><summary>Örneği göster</summary>```go\nimport (\n    "asposecellscloud"\n    "os"\n)\nfunc main() {\n    api := asposecellscloud.NewConversionApi()\n    f, _ := os.Open("your.xlsx")\n    info, _ := api.PostConvertWorkbookToHtml(f, nil, true)\n    fmt.Println(info.Filename)\n}\n```</details> |
| PHP      | <details><summary>Örneği göster</summary>```php\nuse Aspose\Cells\ConversionApi;\n$api = new ConversionApi();\n$file = fopen('your.xlsx', 'r');\n$info = $api->postConvertWorkbookToHtml($file);\necho $info->getFilename();\n```</details> |
| Ruby     | <details><summary>Örneği göster</summary>```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::ConversionApi.new\nfile = File.open('your.xlsx')\ninfo = api.post_convert_workbook_to_html(file: file)\nputs info.filename\n```</details> |
| Perl     | <details><summary>Örneği göster</summary>```perl\nuse Aspose::Cells::ConversionApi;\nmy $api = Aspose::Cells::ConversionApi->new();\nopen my $fh, '<', 'your.xlsx' or die $!;\nmy $info = $api->post_convert_workbook_to_html(file => $fh);\nprint $info->{Filename};\n```</details> |

Desteklenen tüm SDK’ların tam listesi ve kurulum talimatları için lütfen **Aspose.Cells Cloud SDK’ları** deposuna bakın: <https://github.com/aspose-cells-cloud>.

---

## İlgili Uç Noktalar  

| Uç Nokta | Açıklama |
|----------|----------|
| `POST /cells/{name}/saveAs` | Mevcut bir Excel dosyasını doğrudan depoya HTML (veya diğer formatlar) olarak kaydeder. |
| `PUT /cells/convert` | Ek dönüştürme seçenekleriyle bir çalışma kitabını HTML’ye dönüştürür; sonuç yanıt gövdesinde döndürülür. |
| `GET /cells/{name}` | Zaten depoda bulunan (veya diğer formatlarda kaydedilmiş) bir çalışma kitabını, isteğe bağlı sorgu parametreleriyle birlikte alır. |

---

## Sık Sorulan Sorular  

**S:** *Excel’den HTML’e dönüştürme API’sini çağırırken nasıl kimlik doğrulama yaparım?*  
**C:** OAuth 2.0 `/connect/token` uç noktasından elde edilen `Authorization: Bearer <erişim-belirteci>` başlığını ekleyin.

**S:** *`FileInfo` yanıtı hangi bilgileri içerir?*  
**C:** Üç alandan oluşur – `Filename` (string), `FileSize` (byte türünden tamsayı) ve `FileContent` (Base64 ile kodlanmış HTML içeriği).

**S:** *Hangi hata kodlarıyla karşılaşabilirim?*  
**C:** `400` (Geçersiz İstek), `401` (Yetkisiz), `404` (Dosya Bulunamadı), `413` (Yük Çok Büyük), `429` (Çok Fazla İstek), `500` (Sunucu İç Hatası). Her biri `Code` ve `Message` alanlarını içeren bir JSON yükü döndürür.

**S:** *Özel bir font konumu belirleyebilir miyim?*  
**C:** Evet. Gerekli fontları içeren klasörün veya URL'nin bulunduğu `FontsLocation` sorgu parametresini kullanın.

**S:** *Bu işlem için bir hız sınırı var mı?*  
**C:** Varsayılan sınır **hesap başına dakikada 60 istek**tir. Bu sınırın aşılması `429 Too Many Requests` hatasını döndürür.

---

## JSON-LD Breadcrumb (Yapılandırılmış Veri)

Bu bloğu eklemek, arama sonuçlarında zengin snippet breadcrumb’ların görünmesini sağlayarak SEO’yu artırır.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    { "@type": "ListItem", "position": 1, "name": "Ana Sayfa", "item": "https://docs.aspose.cloud/" },
    { "@type": "ListItem", "position": 2, "name": "Geliştirici Merkezi", "item": "https://docs.aspose.cloud/cells/" },
    { "@type": "ListItem", "position": 3, "name": "Dönüştürme", "item": "https://docs.aspose.cloud/cells/conversion/" },
    { "@type": "ListItem", "position": 4, "name": "Excel'den HTML'ye", "item": "https://docs.aspose.cloud/cells/convert-excel-file-to-html-file/" }
  ]
}
</script>
```

---

## Değişiklik Günlüğü  

| Sürüm | Tarih       | Değişiklikler |
|-------|-------------|---------------|
| **v3.0** | 2024‑10‑01 | `PostConvertWorkbookToHtml` fonksiyonunun ilk genel sürümü. |
| **v3.1** | 2025‑04‑15 | `region` ve `FontsLocation` sorgu parametreleri eklendi; hata yükü formatı güncellendi. |
| **v3.2** | 2026‑03‑20 | Hız sınırı belgeleri ve örnek hata yanıtları eklendi. |

--- 

*Ek yardım için lütfen Aspose desteğiyle iletişime geçin veya resmi API referansını ziyaret edin:* <https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToHtml>  
---