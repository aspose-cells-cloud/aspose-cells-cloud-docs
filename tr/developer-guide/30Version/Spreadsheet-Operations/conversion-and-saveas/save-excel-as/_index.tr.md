---
title: "Excel Çalışma Kitabını Kaydet – Aspose.Cells Cloud API"
second_title: "Belge"
linktitle: "Farklı Kaydet"
type: docs
url: /save-an-excel-file-as-other-formats-files/
aliases:
  - /convert-excel-workbook-to-different-file-formats/
  - /saveas-other-formats/
keywords: "Aspose Cells, Excel, Farklı Kaydet, PDF, CSV, JSON, Markdown, REST API"
description: "Aspose.Cells Cloud REST API kullanarak Excel çalışma kitaplarını PDF, CSV, JSON, Markdown ve diğer formatlara kaydedin."
weight: 30
---

Bu REST API, bir Excel dosyasını farklı formatlarda **kaydetmenizi** sağlar.  
Bu uç noktayı çağırmadan önce, geçerli bir OAuth 2.0 erişim belirtecinizin olduğunu ve kaynak çalışma kitabının Aspose Cloud depolama alanınızda saklandığını doğrulayın.

**Gereksinimler**  
1. Bir JWT erişim belirteci edinin ve her isteğin `Authorization: Bearer <token>` başlığına ekleyin.  
2. Kaynak çalışma kitabını Aspose Cloud depolama alanına yükleyin (veya zaten mevcut olduğunu doğrulayın).  
3. Çalışma kitabının bulunduğu depo adını ve klasör yolunu bilin.

## PostWorkbookSaveAs API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/saveAs
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulamayı</a> gerektirir.

### **Yol Parametresi**

| Parametre Adı | Tür   | Açıklama                      |
| -------------- | ------ | --------------------------- |
| name           | string | Excel dosyasının adı. |

### **Sorgu Parametresi**

| Parametre Adı         | Tür    | Açıklama                                                                                 |
| --------------------- | ------ | ---------------------------------------------------------------------------------------- |
| newfilename           | string | Kaydedilecek belge için yeni dosya adı.                                                  |
| isAutoFitRows         | string | Doğruysa, çalışma kitabındaki tüm satırları otomatik olarak sığdırır. Varsayılan değer `false`'tir. |
| isAutoFitColumns      | string | Doğruysa, çalışma kitabındaki sütun genişliklerini otomatik olarak sığdırır. Varsayılan değer `false`'tir. |
| folder                | string | Orijinal çalışma kitabının bulunduğu klasör.                                              |
| storageName           | string | Kaynak dosyanın bulunduğu depo adı.                                                       |
| outStorageName        | string | Çıktı dosyasının kaydedileceği depo adı.                                                  |
| checkExcelRestriction | bool   | Hücreleri veya ilgili nesneleri değiştirirken Excel kısıtlamalarının uygulanıp uygulanmayacağını belirtir. |
| region                | string | Çalışma kitabına uygulanacak bölgesel ayarlar.                                            |
| pageWideFitOnPerSheet | bool   | Dönüştürme sırasında sayfa genişliğini her bir çalışma sayfasına sığdırır.                |
| pageTallFitOnPerSheet | bool   | Dönüştürme sırasında sayfa yüksekliğini her bir çalışma sayfasına sığdırır.               |
| sheetName             | string | Dönüştürülecek çalışma sayfasının adı.                                                    |
| pageIndex             | string | Belirtilen çalışma sayfası içinde dönüştürülecek sayfanın dizini (`sheetName` gerekli).   |
| onePagePerSheet       | bool   | PDF'e dönüştürürken her çalışma sayfası için bir sayfa oluşturur.                          |

### **İstek Gövdesi Parametresi**

| Parametre Adı | Tür    | Açıklama                                                       |
| -------------- | ------ | -------------------------------------------------------------- |
| SaveOptions    | Object | İkinci kısım olarak multipart isteğin içine sağlanan kaydetme seçenekleri. |

**Örnek istek gövdesi (multipart isteğin JSON kısmı)**

```json
{
  "SaveOptions": {
    "SaveFormat": "pdf",
    "CompressionLevel": 9
  }
}
```

### Yanıt

API, bir `SaveResponse` nesnesi döndürür.

```json
{
  "Status": "OK",
  "Code": 200,
  "SaveResult": {
    "Documents": [
      {
        "Name": "sample.pdf",
        "Size": 10240,
        "Folder": "output",
        "Storage": "MyStorage"
      }
    ]
  }
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                             |
|------|-----------------------------|------------------------------------------------------|
| 200  | Tamam (OK)                  | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400  | Hatalı İstek (Bad Request)  | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401  | Yetkisiz (Unauthorized)     | Geçersiz veya eksik JWT belirteci.                   |
| 413  | İçerik Çok Büyük (Payload Too Large) | Yüklenen dosya boyut sınırını aşıyor.               |
| 500  | Sunucu İç Hatası (Internal Server Error) | Beklenmeyen sunucu hatası.                      |

## SDK'lar ile PostWorkbookSaveAs API Nasıl Kullanılır

### PostWorkbookSaveAs API Belirtimi

[OpenAPI Belirtimi](https://reference.aspose.cloud/cells/#/Conversion/PostWorkbookSaveAs), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web hizmetlerine kolayca erişmek için **cURL** kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'yi nasıl çağıracağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/sampleBook.xlsx/SaveAs?newfilename=sample.pdf&isAutoFitRows=true&isAutoFitColumns=true" \
  -H "accept: multipart/form-data" \
  -H "Authorization: Bearer <your_jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "SaveResult": {
    "Documents": [
      {
        "Name": "sample.pdf",
        "Size": 10240,
        "Folder": "output",
        "Storage": "MyStorage"
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK'larını Kullanma

SDK kullanmak, geliştirme hızını en hızlı şekilde artıracaktır. SDK, düşük seviye detayları kendisi yönetir ve size proje görevlerinize odaklanma imkanı verir. Aspose.Cells Cloud SDK'larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub deposuna</a> bakın.

Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanılarak Aspose.Cells web hizmetlerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSaveAs.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSaveAs.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSaveAs.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSaveAs.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSaveAs.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSaveAs.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSaveAs.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookSaveAs.go" >}}

{{< /tab >}}

{{< /tabs >}}

Diğer dönüşüm senaryoları için [Excel’i PDF’e Dönüştür](/convert-excel-to-pdf/) ve [Excel’i CSV’ye Dışa Aktar](/export-excel-to-csv/) kılavuzlarına bakın.