---
title: "Hücre Formülünü Hesapla – Aspose.Cells Cloud API"
type: docs
url: /calculate-cells-formula/
weight: 90
keywords: "Aspose.Cells Cloud, hücre formülünü hesapla, Excel API, REST API, SDK"
description: "Aspose.Cells Cloud REST API’si (v3.0) ile bir Excel hücre formülünü hesaplayın. Uç nokta, parametreler, cURL örneği ve SDK kod snippet’lerini içerir."
ArticleTitle: "Hücre Formülünü Hesapla – Aspose.Cells Cloud API Belgeleri"
---

## REST API

Bu REST API, bir Excel çalışma kitabındaki **hücre formülünü** hesaplar.

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/calculate
```

## Güvenlik ve Kimlik Doğrulama

Aspose.Cells Cloud API’leri güvenlidir ve [JWT belirteci tabanlı kimlik doğrulamaya](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) ihtiyaç duyar.

### İstek Parametreleri

| Parametre Adı | Tür   | Parametre Konumu (path/query/body) | Açıklama                                                                 |
|---------------|-------|------------------------------------|--------------------------------------------------------------------------|
| name          | string | path                               | Excel dosyasının adı (örneğin, `Book1.xlsx`).                            |
| sheetName     | string | path                               | Hücreyi içeren çalışma sayfasının adı.                                   |
| cellName      | string | path                               | Hesaplanacak hücrenin adresi (örneğin, `A1`).                           |
| options       | object | body                               | Hesaplama seçeneklerini içeren JSON nesnesi (bkz. **Options nesnesi** tablosu). |
| folder        | string | query                              | Dosyanın bulunduğu depolama klasörü.                                     |
| storageName   | string | query                              | Aspose Cloud deposunun adı.                                              |

#### Options nesnesi

| Alan             | Tür     | Açıklama                                                                        | Varsayılan |
|------------------|---------|---------------------------------------------------------------------------------|------------|
| CalcStackSize    | string  | Maksimum hesaplama yığını boyutu.                                               | `"1"`      |
| IgnoreError      | boolean | `true` ise hesaplama hataları yoksayılır ve hücre değeri `#N/A` olarak ayarlanır. | `false`    |
| Recursive        | boolean | Bağımlı hücrelerin özyinelemeli hesaplanmasını sağlar.                           | `false`    |
| Precision        | string  | Sayısal sonuçlar için ondalık basamak sayısı.                                  | `"15"`     |
| UseThreading     | boolean | Çoklu iş parçacıklı hesaplamayı sağlar.                                         | `false`    |


### **Yanıt**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                                       |
|-----|-----------------------------|----------------------------------------------------------------|
| 200 | OK                          | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir.  |
| 400 | Bad Request                 | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized                | Geçersiz veya eksik JWT belirteci.                             |
| 413 | Payload Too Large           | Yüklenen dosya boyut sınırını aşıyor.                          |
| 500 | Internal Server Error       | Beklenmeyen sunucu hatası.                                     |

## PostCellCalculate API’yi SDK’larla Nasıl Kullanılır

### PostCellCalculate API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Cells/PostCellCalculate), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’yi nasıl çağıracağınızı göstermektedir. **Önce `/connect/token` uç noktasına kimlik doğrulayarak bir JWT belirteci edinin** ve `<jwt token>` ifadesini belirteç değeriyle değiştirin.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/cells/A1/calculate" \
  -d '{"CalcStackSize":"1"}' \
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

### Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoludur. Bir SDK, düşük seviyeli ayrıntıları soyutlayarak projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub deposunu</a> kontrol edin.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetlerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostCellCalculate.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostCellCalculate.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostCellCalculate.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostCellCalculate.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostCellCalculate.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostCellCalculate.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostCellCalculate.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostCellCalculate.go" >}}

{{< /tab >}}

{{< /tabs >}}