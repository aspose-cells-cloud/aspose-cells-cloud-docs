---
title: "Excel çalışma sayfasına boş bir satır ekleme"
ArticleTitle: "Aspose.Cells Cloud API kullanarak Excel çalışma sayfasına boş bir satır ekleme"
second_title: "Belge"
linktitle: "Satır"
type: docs
url: /tr/rows/add/row/
aliases: [  /tr/add-an-empty-row-in-a-worksheet/ ]
keywords: "Aspose.Cells Cloud, Excel, boş satır ekleme, çalışma sayfası, REST API, satır ekleme, bulut tablolama"
description: "Aspose.Cells Cloud REST API'yi kullanarak Excel çalışma sayfasına boş bir satır ekleyin. Hızlı geliştirme için birden fazla SDK'yi (C#, Java, Python, Go, PHP, Ruby, Node.js, Perl, Android, Swift) destekler."
weight: 20
---

Bu REST API, Excel çalışma sayfasına yeni bir satır ekler. Belirtilen sıfır tabanlı dizine boş bir satır ekler.

**Önkoşullar:**  
- Geçerli bir Aspose Cloud erişim belirteci (Bearer JWT) `Authorization` başlığında yer almalıdır.  
- Hedef çalışma kitabının Aspose Cloud depo alanınıza yüklenmiş olması gerekir; `folder` ve `storageName` parametreleri, dosyanın konumuna işaret etmelidir.

**Notlar:**  
- `rowIndex` sıfır tabanlıdır; dizin 0 olarak belirlenirse çalışma sayfasının en üstüne bir satır eklenir.  
- Excel çalışma sayfalarında maksimum 1.048.576 satır bulunabilir; bu sınırı aşarak ekleme yapmak

## PutInsertWorksheetRow API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### **İstek parametreleri**

| Parametre Adı | Tür     | Konum  | Açıklama                                                  |
| ------------- | ------- | ------ | --------------------------------------------------------- |
| name          | string  | path   | Çalışma kitabının dosya adı.                              |
| sheetName     | string  | path   | Çalışma sayfasının adı.                                   |
| rowIndex      | integer | path   | Yeni satırın ekleneceği sıfır tabanlı dizin.              |
| folder        | string  | query  | Çalışma kitabının bulunduğu depodaki klasör yolu.         |
| storageName   | string  | query  | Kullanılacak Aspose Cloud depo adı.                      |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Cells/PutInsertWorksheetRow), herkese açık bir programlama arayüzü tanımlar ve web tarayıcınızdan doğrudan REST etkileşimlerinde bulunmanızı sağlar.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'sine nasıl istek yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/10" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

> **Not:** Tüm Aspose.Cells Cloud uç noktaları HTTPS gerektirir. Üretim ortamında güvenli `https://` şemasını kullanın.

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**HTTP Durum Kodları**

| Kod | Anlamı                       | Açıklama                                             |
|-----|------------------------------|------------------------------------------------------|
| 200 | OK (Tamam)                   | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request (Hatalı İstek)   | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)      | Geçersiz veya eksik JWT belirteci.                   |
| 413 | Payload Too Large (Çok Büyük Yük) | Yüklenen dosya boyut sınırını aşıyor.             |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                     |

*Hata yanıtı örneği (örneğin, satır dizini çalışma sayfası sınırını aşarsa):*

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "Satır dizini aralık dışına çıktı. Maksimum izin verilen satır sayısı: 1048576."
}
```

## Bulut SDK Ailesi

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoludur. Bir SDK, düşük seviye detayları soyutlayarak projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposunu</a> inceleyin.

Aşağıdaki kod örnekleri, farklı SDK'ler kullanılarak Aspose.Cells web servislerine nasıl istek yapıldığını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutInsertWorksheetRow.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutInsertWorksheetRow.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutInsertWorksheetRow.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutInsertWorksheetRow.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutInsertWorksheetRow.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutInsertWorksheetRow.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutInsertWorksheetRow.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutInsertWorksheetRow.go" >}}

{{< /tab >}}

{{< /tabs >}}