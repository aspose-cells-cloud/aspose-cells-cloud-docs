---
title: "Aspose.Cells Cloud API v3.0 ile Excel Dosyasını PPTX'e Dönüştürme"
second_title: "Belge"
linktitle: "Excel'den PPTX'e"
type: docs
url: /tr/convert-excel-file-to-pptx-file/
keywords: "Aspose, Cells, Excel, PPTX, dönüştürme, REST API, bulut"
description: "Aspose.Cells Cloud REST API v3.0 ile Excel çalışma kitaplarını PPTX sunumlara nasıl dönüştüreceğinizi öğrenin. cURL isteği, SDK kod örnekleri, kimlik doğrulama ve hata yönetimi içerir."
weight: 90
ArticleTitle: "Aspose.Cells Cloud API v3.0 ile Excel Dosyasını PPTX'e Dönüştürme"
---

Bu REST API, bir elektronik tablo dosyasını PPTX formatına dönüştürür.

## PostConvertWorkbookToPptx API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/pptx
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### Sorgu Parametreleri

| Parametre Adı         | Tür    | Açıklama                                                                                   |
| --------------------- | ------ | ------------------------------------------------------------------------------------------ |
| `password`            | string | Excel çalışma kitabını açmak için gereken parola.                                           |
| `storageName`         | string | Kaynak dosyanın bulunduğu depo adı.                                                        |
| `checkExcelRestriction` | bool | Hücreyle ilgili nesneleri değiştirirken Excel dosyası kısıtlamalarının uygulanıp uygulanmayacağını belirtir. |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür       | Açıklama                                                          |
| ------------- | --------- | ----------------------------------------------------------------- |
| `datafile`    | veri dosyası | Çok parçalı istek gövdesinin ilk bölümünde yer alan Excel dosyası. |

**Örnek çok parçalı istek gövdesi (basitleştirilmiş):**

```
--boundary
Content-Disposition: form-data; name="File"; filename="input.xlsx"
Content-Type: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet

<input.xlsx dosyasının ikili içeriği>
--boundary
Content-Disposition: form-data; name="password"

MyPwd
--boundary--
```

### Yanıt

API, oluşturulan pptx dosyasını içeren bir **FileInfo** nesnesi döndürür.

| Alan            | Tür    | Açıklama                                        |
| --------------- | ------ | ----------------------------------------------- |
| **Filename**    | string | PPTX dosyasının adı (örn. `example.pptx`).      |
| **FileSize**    | int    | Dosyanın bayt cinsinden boyutu.                 |
| **FileContent** | string | PPTX dosyasının Base64 ile kodlanmış içeriği.   |

[FileInfo](/cells/file-info/)


**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                         |
|-----|-----------------------------|--------------------------------------------------|
| 200 | Tamam                       | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir. |
| 400 | Geçersiz İstek              | Eksik veya geçersiz parametreler (örn., desteklenmeyen dosya türü). |
| 401 | Yetkisiz                    | Geçersiz veya eksik JWT belirteci.              |
| 413 | İçerik Çok Büyük            | Yüklenecek dosya boyut sınırını aşıyor.         |
| 500 | İç Sunucu Hatası            | Beklenmeyen sunucu hatası.                      |

*Notlar:* Uç nokta, yaygın Excel formatlarını (`.xlsx`, `.xls`, `.xlsm`) destekler. Maksimum dosya boyutu 50 MB ile sınırlıdır. Makrolar veya korumalı sayfalar içeren çalışma kitaplarında uygun parametreler sağlanmazsa dönüştürme kısıtlanabilir.

## SDK’lar ile PostConvertWorkbookToPptx API’yi Nasıl Kullanılır

### PostConvertWorkbookToPptx API Spesifikasyonu

<a href="https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPptx" rel="noopener noreferrer">OpenAPI Spesifikasyonu</a>, herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

**cURL** komut satırı aracını kullanarak Aspose.Cells web servislerine kolayca erişebilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’yi nasıl çağıracağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/pptx?storageName=MyStorage" \
     -H "Authorization: Bearer {access_token}" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -F "File=@/path/to/input.xlsx" \
     -F "password=MyPwd"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.pptx",
  "FileSize": 123456,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme yapmanın en hızlı yoludur. SDK, düşük seviye detayları soyutlayarak projenize odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud" rel="noopener noreferrer") bakın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web servislerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPptx.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPptx.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPptx.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPptx.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPptx.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1c" "Example_PostConvertWorkbookToPptx.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPptx.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPptx.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Bu İşlevi Gerçekleyen Diğer API’ler

- **[POST /cells/convert/pdf](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPdf)** – Excel dosyasını PDF’e dönüştürür.
- **[POST /cells/convert/png](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPng)** – Excel dosyasını PNG görüntülere dönüştürür.
- **[POST /cells/convert/svg](https://apireference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToSvg)** – Excel dosyasını SVG formatına dönüştürür.
---