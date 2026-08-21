---
title: "Birden Fazla Hücre Stilini Güncelle – Aspose.Cells Cloud API Referansı (v3.0)"
type: docs
url: /tr/update-multiple-cells-style/
weight: 20
keywords: ["Aspose.Cells", "birden fazla hücre stilini güncelle", "Excel hücre stili API’si", "bulut SDK", "REST API", "cURL örneği", "JSON isteği", "JWT kimlik doğrulama"]
description: "Aspose.Cells Cloud REST API v3.0 kullanarak bir Excel çalışma kitabındaki hücre aralığının stilini nasıl güncelleyeceğinizi öğrenin. Endpoint, HTTP yöntemi, parametreler, cURL ve SDK örnekleri, kimlik doğrulama, hata işleme ve sürüm bilgilerini içerir."
ArticleTitle: "Birden Fazla Hücre Stilini Güncelle – Aspose.Cells Cloud API Referansı (v3.0)"
---

## REST API

Bu REST API, bir Excel çalışma kitabındaki hücre aralığının **stilini** ayarlar.

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/style
```

## Güvenlik ve Kimlik Doğrulama

Aspose.Cells Cloud API’leri güvenlidir ve [JWT belirteci tabanlı kimlik doğrulamaya](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) ihtiyaç duyar.


### İstek Parametreleri

| Parametre Adı | Tür   | Konum | Açıklama |
|---------------|-------|-------|----------|
| **name**      | string | path  | Çalışma kitabının adı. |
| **sheetName** | string | path  | Çalışma sayfasının adı. |
| **range**     | string | query | Hücre aralığı (örneğin, `A1:A10`). |
| **style**     | object | body  | Uygulanacak stili tanımlayan JSON nesnesi. |
| **folder**    | string | query | Çalışma kitabını içeren klasör. |
| **storageName**| string | query | Depo adı. |

#### Stil Nesnesi
`style` JSON nesnesi hücre biçimlendirmesini temsil eder. Aşağıdaki isteğe bağlı özelliklerden herhangi birini içerebilir:

- **Font** – Yazı tipi ayarları (`Name`, `Size`, `IsBold`, `IsItalic`, `Color`, vb.).  
- **BackgroundColor** – ARGB formatında arka plan rengi.  
- **ForegroundColor** – ARGB formatında ön plan rengi.  
- **Name**, **CultureCustom**, **Custom** – Ek stil meta verileri.

## **Yanıt**

CellCloudResponse döndürür.

- **Yanıt Alanları Genel Bakış**

| Alan              | Tür     | Açıklama                                           |
| ----------------- | ------- | -------------------------------------------------- |
| `Status`          | string  |                                                    |
| `Code`            | integer | 200,400,401,500,...                               |


```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP Durum Kodları**

| Kod | Anlamı                     | Açıklama                                        |
|-----|----------------------------|-------------------------------------------------|
| 200 | OK                         | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request                | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized               | Geçersiz veya eksik JWT belirteci. |
| 413 | Payload Too Large          | Yüklenen dosya boyut limitini aşıyor. |
| 500 | Internal Server Error      | Beklenmeyen sunucu hatası. |

## PostUpdateWorksheetRangeStyle API’sini SDK’larla Nasıl Kullanılır

### PostUpdateWorksheetRangeStyle API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Cells/PostUpdateWorksheetRangeStyle), tam şemayı sağlar.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, Cloud API’ye cURL ile nasıl istek gönderileceğini göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
cURL -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/style?range=a1%3Aa10" \
  -X POST \
  -d '{
        "Font": {
          "Color": { "A":255, "R":255, "G":255, "B":0 },
          "Size": 22,
          "IsBold": true,
          "IsItalic": true,
          "IsStrikeout": true,
          "IsSubscript": true,
          "IsSuperscript": true,
          "Name": "Arial"
        },
        "Name": "string",
        "CultureCustom": "string",
        "Custom": "string",
        "BackgroundColor": { "A":10, "R":10, "G":10, "B":10 },
        "ForegroundColor": { "A":255, "R":255, "G":255, "B":0 }
      }' \
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

SDK kullanmak, geliştirme sürecini hızlandırmak için en iyi yoldur. Bir SDK, düşük seviye detayları işler ve projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web servislerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeStyle.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeStyle.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeStyle.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeStyle.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeStyle.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeStyle.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeStyle.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeStyle.go" >}}

{{< /tab >}}

{{< /tabs >}}