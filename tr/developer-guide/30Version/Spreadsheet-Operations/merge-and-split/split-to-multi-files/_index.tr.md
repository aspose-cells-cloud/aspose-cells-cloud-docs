---
title: "Bir Excel dosyasını birden fazla dosyaya bölün"
second_title: "Belge"
linktype: "Bir Excel dosyasını birden fazla dosyaya bölün"
type: docs
url: /tr/split-an-excel-file-to-multi-files/
aliases: [  /tr/split-excel-workbooks/ , /tr/workbook/split/ ]
keywords: "Aspose.Cells, Bulut, Excel, Böl, API, PDF, CSV, JSON"
description: "Aspose.Cells Cloud REST API'sini kullanarak çok sayfalı Excel çalışma kitaplarını ayrı dosyalara bölün. Çıktı formatları olarak PDF, CSV ve JSON'u destekler ve Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby ve Swift için SDK'lar aracılığıyla kullanılabilir."
weight: 32
ArticleTitle: "Bir Excel dosyasını birden fazla dosyaya bölün - Aspose.Cells Cloud Dokümantasyonu"
---

Aspose.Cells Cloud REST API'si, çok sayfalı Excel çalışma kitaplarını ayrı dosyalara böler.

**Ön Gereksinimler**  
API'yi çağırmadan önce geçerli bir JWT belirteci edinmeniz ve her isteğin `Authorization` başlığına dahil etmeniz gerekir. Ayrıntılar için [kimlik doğrulama kılavuzuna](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) bakın.

## PostSplit API

```http
POST https://api.aspose.cloud/v3.0/cells/split
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.


### İstek parametreleri

| Parametre Adı | Tür   | Konum     | Açıklama                                                         |
|---------------|-------|-----------|------------------------------------------------------------------|
| file          | dosya | formData  | Yüklenecek Excel çalışma kitabını belirtir.                      |
| format        | string| query     | İstenen çıktı formatı (örneğin, `pdf`, `csv`, `json`).         |
| password      | string| query     | Şifrelenmiş bir çalışma kitabının şifresi (isteğe bağlı).        |
| from          | integer| query    | Dahil edilecek ilk sayfanın indeksi (1‑tabanlı).                |
| to            | integer| query    | Dahil edilecek son sayfanın indeksi (dahil).                    |

### **Yanıt**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Files": [
        {
            "Filename" : "[dosya1 adı]",
            "Filesize" : [dosya boyutu],
            "FileContent" : "[Base64Dizesi]"
        },        {
            "Filename" : "[dosya2 adı]",
            "Filesize" : [dosya boyutu],
            "FileContent" : "[Base64Dizesi]"
        },        {
            "Filename" : "[dosya3 adı]",
            "Filesize" : [dosya boyutu],
            "FileContent" : "[Base64Dizesi]"
        }
    ]
}
```

**HTTP Durum Kodları**

| Kod | Anlam                         | Açıklama                                                       |
|-----|-------------------------------|----------------------------------------------------------------|
| 200 | OK (Tamam)                    | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request (Hatalı İstek)    | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)       | Geçersiz veya eksik JWT belirteci. |
| 413 | Payload Too Large (Çok Büyük Yük) | Yüklenen dosya boyut sınırını aşıyor. |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası. |

## PostSplit API'sini SDK'larla Nasıl Kullanılır

### PostSplit API Belirtimi

[OpenAPI Belirtimi](https://apireference.aspose.cloud/cells/#/LightCells/PostSplit), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

**HTTP durum kodları**

| Kod | Anlam                         | Açıklama                                                                          |
|-----|-------------------------------|-----------------------------------------------------------------------------------|
| 200 | OK (Tamam)                    | Çalışma kitabı başarıyla bölündü ve yanıt dosya listesini içerir.               |
| 400 | Bad Request (Hatalı İstek)    | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen format).               |
| 401 | Unauthorized (Yetkisiz)       | Geçersiz veya eksik JWT belirteci.                                                 |
| 500 | Internal Server Error (İç Sunucu Hatası) | Sunucu tarafında beklenmeyen bir hata oluştu.                                   |

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'sine nasıl istek yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/split?format=pdf" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx' \
# xxxxx1.xlsx ve xxxxx2.xlsx dosya yollarını Excel dosyalarınızın yollarıyla değiştirin
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
    "Files": [
        {
            "Filename": "xxxxx_sheet1.pdf",
            "FileSize": 274022,
            "FileContent": "-----Base64Dizesi--------"
        },
        {
            "Filename": "xxxxx_sheet2.pdf",
            "FileSize": 274022,
            "FileContent": "-----Base64Dizesi--------"
        }
        …
    ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK'larını Kullanma

SDK kullanmak, geliştirme hızını artırmak için en iyi yoldur. Bir SDK, düşük seviye ayrıntıları yönetir ve proje görevlerinize odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK'lar kullanılarak Aspose.Cells web hizmetlerine nasıl istek yapıldığını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostSplit.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostSplit.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostSplit.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostSplit.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostSplit.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostSplit.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostSplit.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostSplit.go" >}}

{{< /tab >}}

{{< /tabs >}}
---