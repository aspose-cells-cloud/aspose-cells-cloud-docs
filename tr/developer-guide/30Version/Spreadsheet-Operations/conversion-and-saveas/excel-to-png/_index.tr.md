---
title: "Excel'den PNG'ye"
second_title: "Belge"
linktitle: "Excel'den PNG'ye"
type: docs
url: /tr/trconvert-excel-file-to-png-file/
keywords: "Excel'den PNG'ye, Aspose.Cells Cloud, REST API, elektronik tablo dönüşümü, PNG formatı"
description: "Aspose.Cells Cloud REST API ile Excel elektronik tablolarını PNG görüntülerine dönüştürün. Birden fazla SDK'yı destekler ve çeşitli programlama dilleri için detaylı örnekler sunar."
weight: 90
---

Bu REST API, bir elektronik tablo dosyasını PNG formatına dönüştürür.

## REST API Specification (REST API Spesifikasyonu)

```
POST https://api.aspose.cloud/v3.0/cells/convert/png
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### **Sorgu Parametresi**

| Parametre Adı         | Tür    | Açıklama                                                                                     |
| --------------------- | ------ | -------------------------------------------------------------------------------------------- |
| password              | string | Excel dosyasını açmak için gereken şifre.                                                    |
| storageName           | string | Dosyanın bulunduğu depo adı.                                                                 |
| checkExcelRestriction | bool   | Hücreleri veya ilgili nesneleri değiştirirken Excel dosyası kısıtlamalarının denetlenip denetlenmeyeceğini belirler. |

### **İstek Gövdesi Parametresi**

| Parametre Adı | Tür       | Açıklama                                                                |
| -------------- | --------- | ----------------------------------------------------------------------- |
| datafile       | data file | Çok parçalı isteğin ilk kısmında yer alan elektronik tablo dosyası.      |

### **Yanıt**

API, oluşturulan PNG dosyasını içeren bir **FileInfo** nesnesi döndürür.

| Alan            | Tür    | Açıklama                                      |
| --------------- | ------ | --------------------------------------------- |
| **Filename**    | string | PNG dosyasının adı (örneğin, `example.png`). |
| **FileSize**    | int    | Dosyanın bayt cinsinden boyutu.               |
| **FileContent** | string | PNG dosyasının Base64 ile kodlanmış içeriği.  |

[FileInfo](/cells/file-info/)


**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                         |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK (Tamam)                  | Sü 필 적용 성공; yanıt işlem ayrıntılarını içerir. |
| 400  | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401  | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci. |
| 413  | Payload Too Large (Çok Büyük Yük) | Yüklenecek dosya boyut sınırını aşıyor. |
| 500  | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası. |
## SDK'lar ile PostConvertWorkbookToPNG API'sini Nasıl Kullanılır

### PostConvertWorkbookToPNG API Spesifikasyonu


[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/#/Conversion/PostConvertWorkbookToPNG), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

**cURL** komut satırı aracını kullanarak Aspose.Cells web hizmetlerine kolayca erişebilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'ye nasıl istekte bulunulacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/convert/png" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: curl" \
     -d {"File":{}}
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Filename": "xxxxxx.png",
  "FileSize": xxxx,
  "FileContent": "File Content: base64_encoded_string"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK'larını Kullanma

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoludur. SDK, düşük seviye detayları yönetir, böylece projenizin görevlerine odaklanabilirsiniz. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanılarak Aspose.Cells web hizmetlerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example_PostConvertWorkbookToPNG.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostConvertWorkbookToPNG.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostConvertWorkbookToPNG.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostConvertWorkbookToPNG.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostConvertWorkbookToPNG.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostConvertWorkbookToPNG.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostConvertWorkbookToPNG.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostConvertWorkbookToPNG.go" >}}

{{< /tab >}}

{{< /tabs >}}

## Benzer İşlevleri Gerçekleştiren Diğer API'ler

- **[POST /cells/{name}/saveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)** – Bir Excel dosyasını CSV (veya diğer formatlar) olarak ek ayarlarla kaydeder ve sonucu depolar.
- **[PUT /cells/convert](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook)** – Bir Excel dosyasını CSV (veya diğer formatlar) formatına dönüştürür, isteğe bağlı parametreler alır ve sonucu yanıtta döndürür.
- **[GET /cells/{name}](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)** – Bir Excel dosyasını alır ve anında CSV (veya diğer formatlar) formatına dönüştürebilir.