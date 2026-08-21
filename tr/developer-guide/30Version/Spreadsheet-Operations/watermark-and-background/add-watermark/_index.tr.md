---
title: "Excel dosyalarına filigran ekleme"
second_title: "Belge"
linktitle: "Excel Dosyalarına Filigran Ekleme"
type: docs
url: /tr/add-watermark-into-excel-files/
aliases: [  /tr/watermark/ ]
keywords: "Excel dosyasına filigran ekleme, Aspose.Cells Cloud, REST API, SDK, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go"
description: "Aspose.Cells Cloud REST API (v3.0) kullanarak Excel çalışma kitaplarına metin filigranı nasıl ekleyeceğinizi öğrenin. cURL örneği, gerekli parametreler ve yanıt ayrıntılarını içerir."
weight: 39
ArticleTitle: "Excel Dosyalarına Filigran Ekle – Aspose.Cells Cloud Dokümantasyonu"
---

Bu REST API, Excel dosyalarına bir **filigran** ekler.

**Önkoşullar:** Geçerli bir JWT erişim belirteci edinmelisiniz ve Excel dosyasının desteklenen bir formatta olduğundan emin olmalısınız (örneğin, `.xlsx`, `.xls`).  
**Arka plan:** Filigran, sahipliği veya gizliliği belirtmek için her çalışma sayfasına uygulanan yarı saydam bir metin katmanıdır.

## PostWatermark API

```http
POST https://api.aspose.cloud/v3.0/cells/watermark
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulamayı</a> gerektirir.

### **İstek Parametreleri**

| Parametre Adı | Tür   | Konum                     | Açıklama                                                    |
| -------------- | ------ | ------------------------- | ----------------------------------------------------------- |
| `file`         | dosya  | formData (multipart body) | Filigranın uygulanacağı Excel dosyası.                       |
| `text`         | string | sorgu                     | Görüntülenecek filigran metni.                              |
| `color`        | string | sorgu                     | ARGB hex formatında filigran rengi (örneğin, `004433ff`). |

### **Yanıt**

JSON yanıtı, bir **Files** dizisi içerir. Her dosya nesnesi için:

- **Filename** – işlenmiş çalışma kitabının adı.  
- **FileSize** – dosyanın bayt cinsinden boyutu.  
- **FileContent** – filigranlı Excel dosyasının Base64 ile kodlanmış içeriği; gerçek dosyayı elde etmek için bunu çözmeniz gerekir.

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Files": [
        {
            "Filename" : "[dosya1_adı]",
            "Filesize" : [dosya boyutu],
            "FileContent" : "[Base64Dizesi]"
        },        {
            "Filename" : "[dosya2_adı]",
            "Filesize" : [dosya boyutu],
            "FileContent" : "[Base64Dizesi]"
        },        {
            "Filename" : "[dosya3_adı]",
            "Filesize" : [dosya boyutu],
            "FileContent" : "[Base64Dizesi]"
        }
    ]
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                         |
|------|-----------------------------|--------------------------------------------------|
| 200  | Tamam                       | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400  | Hatalı İstek                | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401  | Yetkisiz                    | Geçersiz veya eksik JWT belirteci. |
| 413  | Yük Çok Büyük               | Yüklenen dosya boyut sınırını aşıyor. |
| 500  | İç Sunucu Hatası            | Beklenmeyen sunucu hatası. |

## PostWatermark API’yi SDK’larla Nasıl Kullanılır

### PostWatermark API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/LightCells/PostWatermark), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

**cURL** komut satırı aracını kullanarak Aspose.Cells web hizmetlerini çağırabilirsiniz. Aşağıdaki örnek, gerekli kimlik doğrulama başlığını içeren tam bir isteği göstermektedir. `<your-jwt-token>` yerine Aspose kimlik doğrulama uç noktasından elde ettiğiniz geçerli bir JWT erişim belirteci yazın.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/watermark?text=aspose.cells.cloud&color=004433ff" \
  -X POST \
  -H "Content-Type: multipart/form-data" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <your-jwt-token>" \
  -F "file=@Sample.xlsx"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "Sample_watermarked.xlsx",
      "FileSize": 274022,
      "FileContent": "-----Base64Dizesi--------"
    }
  ]
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme yapmanın en hızlı yoludur. Bir SDK, düşük seviyeli ayrıntıları soyutlayarak iş mantığınıza odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK’ları kullanarak Aspose.Cells web hizmetlerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWatermark.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWatermark.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWatermark.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWatermark.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWatermark.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWatermark.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWatermark.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWatermark.go" >}}

{{< /tab >}}

{{< /tabs >}}
---