---
title: "Aspose.Cells Cloud – Excel Aralığını HTML'e Dönüştür"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel dosyasının belirli bir aralığını (örneğin, A1:C10) HTML dosyasına dönüştürün. Kimlik doğrulama, istek örnekleri, yanıt işleme, SDK kod parçacıkları ve hata kodlarını içerir."
keywords: "Aspose.Cells, Excel'den HTML'e, aralık dönüştürme, bulut API, elektronik tablo"
slug: convert-range-to-html
date: 2026-07-30
type: docs
weight: 100
---

Yerel bir Excel çalışma kitabının seçili bir aralığını doğrudan Aspose.Cells Cloud aracılığıyla HTML dosyasına dönüştürün. Dönüştürme işlemi tamamen bulut sunucusunda gerçekleşir, bu nedenle çalışma kitabının tamamını yüklemenize veya yerel olarak Excel yüklü olması gerekmez.

## Excel Aralığını HTML'e Dönüştürme API'si

```http
PUT https://api.aspose.cloud/v4.0/cells/convert/range/html
```

İstek gövdesi, elektronik tablo dosyasını içeren `multipart/form-data` formatındadır. Diğer tüm seçenekler sorgu parametreleri olarak sağlanır.

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Adı                | Tür      | Konum      | Gerekli | Açıklama                                                                 |
| ------------------ | -------- | ---------- | ------- | ------------------------------------------------------------------------ |
| **Spreadsheet**    | Dosya    | FormData   | Evet    | Dönüştürülecek Excel çalışma kitabı.                                     |
| **worksheet**      | Dize     | Sorgu      | Evet    | Aralığın bulunduğu çalışma sayfasının adı.                               |
| **range**          | Dize     | Sorgu      | Evet    | Dönüştürülecek hücre alanı, örneğin `A1:C10`.                            |
| **outPath**        | Dize     | Sorgu      | Hayır   | Oluşan HTML dosyasının saklanacağı klasör yolu (varsayılan `null`).      |
| **outStorageName** | Dize     | Sorgu      | Hayır   | Çıktı dosyası için depolama hizmetinin adı.                              |
| **fontsLocation**  | Dize     | Sorgu      | Hayır   | Özel yazı tipi klasörünün yolu.                                           |
| **AutoRowsFit**    | Boole    | Sorgu      | Hayır   | Çalışma sayfasındaki tüm satırları otomatik olarak uygun hale getirir.   |
| **AutoColumnsFit** | Boole    | Sorgu      | Hayır   | Çalışma sayfasındaki tüm sütunları otomatik olarak uygun hale getirir.   |
| **region**         | Dize     | Sorgu      | Hayır   | Yerel tanımlayıcı (örneğin, `tr-TR`, `en-US`, `fr-FR`). Sayı/tarihBiçimini etkiler. |
| **password**       | Dize     | Sorgu      | Hayır   | Korumalı bir çalışma kitabını açmak için şifre.                          |
| **fontsLocation**  | Dize     | Sorgu      | Hayır   | Özel yazı tiplerinin konumu.                                              |
| **region**         | Dize     | Sorgu      | Hayır   | Elektronik tablo bölgesi/dil ayarı.                                      |
| **password**       | Dize     | Sorgu      | Hayır   | Elektronik tablo dosyasını açmak için şifre.                             |

## Yanıt

API, dönüştürülmüş HTML dosyasını **ikili akış** (`application/octet-stream`) olarak döndürür.

```json
[
  {
    "Name": "ResponseFile",
    "DataType": {
      "Identifier": "File",
      "Reference": "Stream"
    }
  }
]
```

### Örnek Başarılı Yanıt (HTTP)

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="rapor.html"
Content-Length: 8423

<table>
  <tr><th>Ürün</th><th>Fiyat</th></tr>
  <tr><td>Widget A</td><td>$10</td></tr>
  <tr><td>Widget B</td><td>$15</td></tr>
</table>
```

Tarayıcıda işlenmiş tabloyu görüntülemek için yanıt gövdesini bir dosyaya (örneğin, `rapor.html`) kaydedin.

---

**HTTP Durum Kodları**

| Kod | Anlamı                | Açıklama                                                           |
| --- | --------------------- | ------------------------------------------------------------------ |
| 200 | Tamam                 | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir.     |
| 400 | Geçersiz İstek        | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Yetkisiz              | Geçersiz veya eksik JWT belirteci.                                 |
| 413 | Yük Çok Büyük         | Yüklenen dosya boyut sınırını aşıyor.                              |
| 500 | Sunucu İç Hatası      | Beklenmeyen sunucu hatası.                                         |

## SDK'larla Excel Aralığını HTML'e Dönüştürme API'si Nasıl Kullanılır?

### OpenAPI Spesifikasyonu

[OpenAPI Spesifikasyonu](https://reference.aspose.cloud/cells/?urls.primaryName=API+v4#/Conversion/ConvertRangeToHTML), web tarayıcısından doğrudan REST etkileşimlerine izin veren herkese açık bir API'yi tanımlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'sine çağrı nasıl yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v4.0/cells/convert/range/html?worksheet=Sheet1&range=A1:C10&AutoRowsFit=true&AutoColumnsFit=true" \
     -H "Authorization: Bearer {access_token}" \
     -F "Spreadsheet=@Report.xlsx" \
     -F "outPath=output/report.html"

```

{{< /tab >}}

{{< tab tabNum="12" >}}

```
HTTP/1.1 200 OK
Content-Type: application/octet-stream
Content-Disposition: attachment; filename="rapor.html"
Content-Length: 8423

<table>
  <tr><th>Ürün</th><th>Fiyat</th></tr>
  <tr><td>Widget A</td><td>$10</td></tr>
  <tr><td>Widget B</td><td>$15</td></tr>
</table>
```

{{< /tab >}}

{{< /tabs >}}

## Aspose.Cells Cloud SDK'larını Kullanın

SDK kullanmak, düşük seviye detayları soyutlayarak bir veri aralığını minimum kodla HTML dosyasına dönüştürmenize izin vererek geliştirmenin en hızlı yoludur.  
Aspose.Cells Cloud SDK'larının tam listesini [GitHub deposunda](https://github.com/aspose-cells-cloud) inceleyebilirsiniz.

Aşağıdaki kod örnekleri, farklı SDK'lar kullanılarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını göstermektedir. Gist'ten yükleme engellenirse, örnekleri doğrudan depodan indirebilirsiniz.

{{<tabs tabTotal="8" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}
{{<tab tabNum="1" >}}
{{<gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Example40_ConvertRangeToHtml.cs" >}}
{{</tab>}}
{{<tab tabNum="2" >}}
{{<gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example40_ConvertRangeToHtml.java" >}}
{{</tab>}}
{{<tab tabNum="3" >}}
{{<gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example40_ConvertRangeToHtml.php" >}}
{{</tab>}}
{{<tab tabNum="4" >}}
{{<gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example40_ConvertRangeToHtml.rb" >}}
{{</tab>}}
{{<tab tabNum="5" >}}
{{<gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example40_ConvertRangeToHtml.ts" >}}
{{</tab>}}
{{<tab tabNum="6" >}}
{{<gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example40_ConvertRangeToHtml.py" >}}
{{</tab>}}
{{<tab tabNum="7" >}}
{{<gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example40_ConvertRangeToHtml.pl" >}}
{{</tab>}}
{{<tab tabNum="8" >}}
{{<gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example40_ConvertRangeToHtml.go" >}}
{{</tab>}}
{{< /tabs >}}