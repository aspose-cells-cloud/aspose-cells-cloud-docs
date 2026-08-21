---
title: "Excel'den CSV'ye"
second_title: "Belge"
linktitle: "Excel'den CSV'ye"
type: docs
url: convert-excel-file-to-CSV-file/
aliases:
  - /convert-excel-file-to-CSV-in-cloud/
  - /convert/excel-to-csv/
  - /convert-excel-file-to-CSV-file/
keywords: "Excel'den CSV'ye, Aspose.Cells Cloud, REST API, elektronik tablo dönüştürme, CSV dosyası, dosya dönüştürme"
description: "Aspose.Cells Cloud REST API ile Excel elektronik tablolarını CSV formatına dönüştürün. Kolay entegrasyon için çeşitli SDK ve programlama dillerini destekler."
weight: 90
---

Bu REST API, bir elektronik tablo dosyasını CSV formatlı bir dosyaya dönüştürür.

## REST API

```http
POST https://api.aspose.cloud/v3.0/cells/convert/csv
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.


### Sorgu Parametreleri

| Parametre Adı         | Tip    | Açıklama                                                                               |
| --------------------- | ------ | -------------------------------------------------------------------------------------- |
| `password`            | string | Excel dosyasını açmak için gerekli şifre.                                              |
| `storageName`         | string | Dosyanın bulunduğu depo adı.                                                           |
| `checkExcelRestriction` | bool   | Kullanıcı hücreyle ilgili nesneleri değiştirdiğinde Excel dosyası kısıtlamalarının denetlenip denetlenmeyeceği. |

### İstek Gövdesi Parametresi

| Parametre Adı | Tip       | Açıklama                                                            |
| ------------- | --------- | ------------------------------------------------------------------- |
| `datafile`    | veri dosyası | Çok parçalı istek gövdesinin ilk kısmında yer alan veri dosyası. |

### Yanıt

API, oluşturulan CSV dosyasını içeren bir **FileInfo** nesnesi döndürür.

| Alan             | Tip    | Açıklama                                        |
| ---------------- | ------ | ----------------------------------------------- |
| **Filename**     | string | CSV dosyasının adı (örneğin, `example.csv`).   |
| **FileSize**     | int    | Dosyanın bayt cinsinden boyutu.                 |
| **FileContent**  | string | CSV dosyasının Base64 ile kodlanmış içeriği.    |

[FileInfo](/cells/file-info/)


**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                         |
|-----|-----------------------------|--------------------------------------------------|
| 200 | Tamam                       | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Hatalı İstek                | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Yetkisiz                    | Geçersiz veya eksik JWT belirteci.              |
| 413 | Yük Çok Büyük               | Yüklenen dosya boyut sınırını aşıyor.           |
| 500 | Sunucu İç Hatası            | Beklenmeyen sunucu hatası.                      |

## PostConvertWorkbookToCSV API'yi SDK'lar ile Nasıl Kullanılır

### PostConvertWorkbookToCSV API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToCSV), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

**cURL** komut satırı aracını kullanarak Aspose.Cells web hizmetlerine erişebilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’yi nasıl çağıracağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/csv" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d '{"File":{}}'
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "example.CSV",
  "FileSize": 12345,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme yapmanın en hızlı yoludur. SDK, düşük seviye detayları ele alır ve sizin projenize odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerini çeşitli SDK’larla nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPDF.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPDF.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPDF.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPDF.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPDF.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPDF.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPDF.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPDF.go" >}}

{{< /tab >}}

{{< /tabs >}}