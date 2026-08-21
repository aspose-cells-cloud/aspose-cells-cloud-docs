---
title: "Excel Dosyasındaki Verileri Sıkıştırın"
ArticleTitle: "Excel Dosyasındaki Verileri Sıkıştırın – Aspose.Cells Cloud API"
second_title: "Belge"
linktitle: "Excel Dosyalarını Sıkıştırın"
type: docs
url: /tr/compress-excel-files/
aliases: [  /tr/compress/ ]
keywords: "excel dosyası sıkıştırma, aspose cells cloud, excel sıkıştırma, elektronik tablo sıkıştırma, rest api, dosya sıkıştırma"
description: "Aspose.Cells Cloud REST API ile Excel dosyalarını (XLS, XLSX, XLSM, XLSB, ODS) sıkıştırın. Sıkıştırma düzeyini ayarlayın, birden fazla dosyayı işleyin ve SDK’lar aracılığıyla entegrasyon sağlayın."
weight: 39
---

## Aspose.Cells Cloud Web Servislerinin PostCompress API’si

**Ön Gereksinimler:**  
- Kimlik doğrulama için geçerli bir JWT jetonu gerekir.  
- Desteklenen dosya formatları: XLS, XLSX, XLSM, XLSB ve ODS’dir.  
- Tek istekte izin verilen maksimum dosya boyutu 500 MB’dır (hizmet sınırlarına tabidir).

Bu REST API, bir Excel dosyasındaki verileri sıkıştırır.

- XLS, XLSX, XLSM, XLSB, ODS dosyalarını sıkıştırın  
- Birden fazla Excel elektronik tablo dosyasını hızlıca sıkıştırın  
- Sıkıştırma düzeyini seçin  
- Birden fazla dosyayı destekler  

### Web API Uç Noktası

```http
POST https://api.aspose.cloud/v3.0/cells/compress
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT jeton tabanlı kimlik doğrulamayı</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür    | Yol/Sorgu Dizisi/HTTP Gövdesi | Açıklama                                      |
|---------------|--------|-------------------------------|-----------------------------------------------|
| file          | dosya  | formData                      | Yüklenecek dosya                              |
| CompressLevel | tamsayı | sorgu                         | Sıkıştırma düzeyi (0‑100); daha yüksek değerler daha güçlü sıkıştırma anlamına gelir |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür | Açıklama                                     |
|---------------|-----|----------------------------------------------|
| data          | dosya | Sıkıştırılacak çalışma kitaplığı dosyasının ikili içeriği. |

### **Yanıt**

```json
{
    "Status" : "OK",
    "Code" : 200,
    "Filename" : "[birleştirilmiş dosya adı]",
    "Filesize" : [dosya boyutu],
    "FileContent" : "[Base64Dizisi]"
}
```

*Not:* `FileContent`, Base64 dizisi olarak kodlanmış sıkıştırılmış çalışma kitabını içerir. Dizgenin uzunluğu, sıkıştırılmış dosyanın boyutuna karşılık gelir; ikili Excel dosyasını geri almak için standart Base64 araçlarını kullanarak bu dizeyi çözebilirsiniz.

**HTTP Durum Kodları**

| Kod | Anlam                      | Açıklama                                          |
|-----|----------------------------|---------------------------------------------------|
| 200 | Tamam                      | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Hatalı İstek               | Eksik veya geçersiz parametreler (örn., desteklenmeyen dosya türü). |
| 401 | Yetkisiz                   | Geçersiz veya eksik JWT jetonu. |
| 413 | İstek Gövdesi Çok Büyük    | Yüklenen dosya boyut sınırlarını aşıyor. |
| 500 | Sunucu İç Hatası           | Beklenmeyen sunucu hatası. |

## PostCompress API’sini SDK’larla Nasıl Kullanılır

### PostCompress API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/LightCells/PostCompress), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl istekte bulunacağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
# Güvenli bağlantı için HTTPS kullanın
curl -v "https://api.aspose.cloud/v3.0/cells/compress?CompressLevel=88" \
-X POST \
-H "Content-Type: multipart/form-data" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanmak, geliştirme sürecini hızlandırmanın en hızlı yoludur. Bir SDK, düşük seviye detayları soyutlayarak projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web servislerine nasıl istekte bulunacağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCompress.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCompress.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCompress.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCompress.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCompress.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCompress.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCompress.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCompress.go" >}}

{{< /tab >}}

{{< /tabs >}}