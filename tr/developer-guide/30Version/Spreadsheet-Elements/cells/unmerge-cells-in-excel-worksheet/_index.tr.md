---
title: "Excel Çalışma Sayfasında Hücreleri Birleştirmeyi Kaldır"
type: docs
url: /tr/unmerge-cells-in-excel-worksheet/
weight: 120
keywords: "Aspose.Cells, Excel, Hücreleri Birleştirmeyi Kaldır, REST API, Bulut SDK"
description: "Aspose.Cells Cloud REST API kullanarak Excel çalışma sayfasındaki hücreleri birleştirmeyi nasıl kaldıracağınızı öğrenin. İstek örnekleri, yanıt biçimi ve birden fazla programlama dili için SDK kod örnekleriyle birlikte."
ArticleTitle: "Excel Çalışma Sayfasında Hücreleri Birleştirmeyi Kaldır"
---

Bu REST API, bir Excel dosyasındaki hücreleri birleştirmeyi kaldırır.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/unmerge
```

## Güvenlik ve Kimlik Doğrulama

Aspose.Cells Cloud API'leri güvenlidir ve [JWT belirteci tabanlı kimlik doğrulama](https://docs.aspose.cloud/tr/total/getting-started/rest-api-overview/authenticating-api-requests/) gerektirir.


**İstek Parametreleri**

| Parametre Adı  | Tür     | Konum   | Açıklama                                              |
|----------------|---------|----------|---------------------------------------------------------|
| name           | string  | path     | Çalışma kitaplığı dosyasının adı.                       |
| sheetName      | string  | path     | Çalışma sayfasının adı.                                 |
| startRow       | integer | query    | Birleştirmeyi kaldırma işlemine dahil edilecek ilk satırın sıfır tabanlı indeksi. |
| startColumn    | integer | query    | Birleştirmeyi kaldırma işlemine dahil edilecek ilk sütunun sıfır tabanlı indeksi. |
| totalRows      | integer | query    | Birleştirmeyi kaldırma işlemine dahil edilecek satır sayısı. |
| totalColumns   | integer | query    | Birleştirmeyi kaldırma işlemine dahil edilecek sütun sayısı. |
| folder         | string  | query    | Çalışma kitabının depolandığı klasör yolu.              |
| storageName    | string  | query    | Depolama hizmetinin adı.                               |

## **Yanıt**

CellCloudResponse döndürür.

- **Yanıt Alanları Genel Bakış**

| Alan            | Tür     | Açıklama                                              |
| --------------- | ------- | ----------------------------------------------------- |
| `Status`          | string  |                    |
| `Code`           | integer | 200,400,401,500,...                                 |


```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                           |
|------|-----------------------------|--------------------------------------------------|
| 200  | OK (Tamam)                  | Süzgeç başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400  | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401  | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci. |
| 413  | Payload Too Large (Çok Büyük Yük) | Yüklenen dosya boyut sınırını aşıyor. |
| 500  | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası. |

## PostWorksheetUnmerge API'sini SDK’larla Nasıl Kullanılır

### PostWorksheetUnmerge API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Cells/PostWorksheetUnmerge), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’sine nasıl istek yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/unmerge?startRow=10&startColumn=10&totalRows=10&totalColumns=10" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
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

### Aspose.Cells Cloud SDK’larını Kullanma

Bir SDK kullanmak, geliştirme sürecini hızlandırmak için en iyi yoldur. Bir SDK, düşük seviye ayrıntıları yönetir ve projenizdeki görevlere odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetlerine nasıl istek yapıldığını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetUnmerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetUnmerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetUnmerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetUnmerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetUnmerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetUnmerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetUnmerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetUnmerge.go" >}}

{{< /tab >}}

{{< /tabs >}}