---
title: "Akıllı İşaretleyici Şablonları ile Excel Raporları Oluşturun"
second_title: "Belge"
linktype: "Akıllıİşaretleyici"
type: docs
url: /build-report-with-smart-marker/
aliases:
  - /create-excel-workbook-from-a-smartmarker-template/
  - /workbook/smartmarker/
  - /workbook/create/smartmarker/
keywords: "Excel, Akıllı İşaretleyici, Aspose.Cells Cloud, REST API, Çalışma Kitabı, SDK, API, Rapor Oluşturma"
description: "Aspose.Cells Cloud REST API ile Akıllı İşaretleyici şablonlarından Excel çalışma kitaplarını nasıl oluşturacağınızı öğrenin. İsteğe/yanıta ayrıntılarını, cURL örneğini, önkoşulları, notları ve SDK kod örneklerini içerir."
weight: 40
ArticleTitle: "Akıllı İşaretleyici Şablonları ile Excel Raporları Oluşturun – Aspose.Cells Cloud API Kılavuzu"
---

Bu REST API, Akıllı İşaretleyici şablonunu kullanarak bir çalışma kitabı oluşturur.

## Çalışma Kitabı Akıllı İşaretleyici (SmartMarker) API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/smartmarker
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### **Akıllı İşaretleyici Nedir?**

Akıllı İşaretleyici, XML (veya JSON) dosyasındaki veri alanlarını bir Excel şablonundaki hücrelere eşleyen yer tutucu sözdizimidir. Çalışma zamanında Aspose.Cells, bu işaretleyicileri ilgili verilerle değiştirerek programatik olarak tamamen doldurulmuş raporlar oluşturmanızı sağlar.

### **Sorgu Parametreleri**

| Parametre Adı | Tür   | Açıklama                                                    |
| ------------- | ----- | ----------------------------------------------------------- |
| outPath       | string | Oluşturulan çalışma kitabının kaydedileceği hedef yol.     |
| folder        | string | Orijinal çalışma kitabının bulunduğu klasör.               |
| storageName   | string | Kullanılacak depolama hizmetinin adı.                      |

### **İstek Gövdesi Parametresi**

| Parametre Adı | Tür | Açıklama                                           |
| ------------- | --- | -------------------------------------------------- |
| xmlFile       | file | İsteğe eklenen Akıllı İşaretleyici XML veri dosyası. |

### **Yanıt**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**Notlar / Sınırlamalar:**  
- API, boyutu **50 MB**'a kadar olan Excel dosyalarını destekler.  
- Kabul edilen formatlar yalnızca **.xlsx**, **.xlsm** ve **.xlsb** formatlarıdır.  
- Hesap başına **saniyede 20 istek** hız sınırı uygulanır.

**HTTP Durum Kodları**

| Kod | Anlamı                      | Açıklama                                           |
|-----|-----------------------------|----------------------------------------------------|
| 200 | OK (Tamam)                  | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci.                |
| 413 | Payload Too Large (Çok Büyük Yük) | Yüklenen dosya boyut sınırını aşıyor.          |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu tarafı hatası.          |

## Çalışma Kitabı Akıllı İşaretleyici API Nasıl Kullanılır?

### Çalışma Kitabı Akıllı İşaretleyici API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookGetSmartMarkerResult), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

### Aspose.Cells Cloud SDK’larını Kullanın

Aspose.Cells web hizmetlerine kolayca erişmek için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'ye nasıl istek yapıldığını göstermektedir.

**Hızlı tek satırlık örnek**

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/{name}/smartmarker?outPath={outPath}" -H "Authorization: Bearer {access_token}" -F "xmlFile=@Sample_SmartMarker_Data.xml"
```

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/newworkbook_14.xlsx/smartmarker?outPath=GeneratedReport.xlsx" \
    -H "accept: multipart/form-data" \
    -H "x-aspose-client: Containerize.Swagger" \
    -F "xmlFile=@Sample_SmartMarker_Data.xml"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```text
HTTP/1.1 200 OK
Content-Type: application/json

{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### **Hata Yönetimi**

| HTTP Durumu | Açıklama             | Tipik Neden                                           |
| ----------- | -------------------- | ----------------------------------------------------- |
| 400         | Bad Request (Hatalı İstek) | Eksik şablon, hatalı XML veya geçersiz parametreler. |
| 401         | Unauthorized (Yetkisiz)    | Geçersiz veya eksik kimlik doğrulama belirteci.     |
| 404         | Not Found (Bulunamadı)     | Belirtilen çalışma kitabına veya depolama konumuna ulaşılamadı. |
| 500         | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu tarafı hatası.          |

**Hata yanıtına örnek (400)**

```json
{
  "Code": 400,
  "Message": "XML veri dosyası eksik veya hatalı."
}
```

## Bulut SDK Ailesi

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. Bir SDK, düşük seviye detayları ele alır ve böylece projenizin görevlerine odaklanabilirsiniz. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web hizmetlerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookCreate.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookCreate.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookCreate.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookCreate.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookCreate.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookCreate.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookCreate.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookCreate.go" >}}

{{< /tab >}}

{{< /tabs >}}