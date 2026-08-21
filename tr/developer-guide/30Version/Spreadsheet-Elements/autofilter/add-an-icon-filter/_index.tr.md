---
title: "Excel Çalışma Sayfasına İkon Filtresi Ekleyin"
second_title: "Belge"
linktitle: "İkon filtresi ekle"
type: docs
url: /tr/autofilter/add-icon-filter/
aliases: [/tr/add-an-icon-filter/,/tr/autofilter/add-an-icon-filter/]
keywords: "Aspose.Cells Cloud, Excel, İkon Filtresi, Otomatik Filtre, REST API"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasına nasıl ikon filtresi eklendiğini, istek detayları, cURL örneği, SDK kod örnekleri ve hata yönetimi ile öğrenin."
weight: 65
ArticleTitle: "Excel Çalışma Sayfasına İkon Filtresi Ekleyin – Aspose.Cells Cloud Belgesi"
---

## REST API

Bu REST API, **Aspose.Cells Cloud REST API** kullanarak bir Excel çalışma sayfasına bir **ikon filtresi** ekler.

**Arka Plan:** İkon filtresi, hücrelerin değerlerine göre görsel bir ikon seti uygular ve veri eğilimlerinin hızlı görsel analizine olanak tanır. Yaygın kullanım durumları arasında performans metriklerini vurgulama, durum göstergelerini gösterme veya trafiğin kırmızı-kırmızı-yeşil ikonları ile değerleri doğrudan Excel çalışma sayfalarında kategorize etme yer alır.


```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/autoFilter/iconFilter
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.


### İstek Parametreleri:

| Parametre Adı | Tür      | Konum   | Açıklama |
|---------------|----------|---------|----------|
| name          | string   | Yol     | Çalışma kitabının adı. |
| sheetName     | string   | Yol     | Çalışma sayfasının adı. |
| range         | string   | Sorgu   | Filtrenin uygulanacağı hücre aralığı (örn. `A1:B1`). |
| fieldIndex    | integer  | Sorgu   | Filtrenin uygulanacağı sütunun sıfır tabanlı indeksi. |
| iconSetType   | string   | Sorgu   | Kullanılacak ikon seti. İzin verilen değerler: `Arrows3`, `ArrowsGray3`, `Flags3`, `Signs3`, `Symbols3`, `Symbols32`, `TrafficLights31`, `TrafficLights32`, `Arrows4`, `ArrowsGray4`, `Rating4`, `RedToBlack4`, `TrafficLights4`, `Arrows5`, `ArrowsGray5`, `Quarters5`, `Rating5`, `Stars3`, `Boxes5`, `Triangles3`, `None`, `CustomSet`, `Smilies3`, `ColorSmilies3`. |
| iconId        | integer  | Sorgu   | Seçilen ikon seti içindeki belirli ikonun tanımlayıcısı. |
| matchBlanks   | boolean  | Sorgu   | Boş hücrelerin dahil edilip edilmeyeceğini belirler (`true` veya `false`). |
| refresh       | boolean  | Sorgu   | Uygulamadan sonra filtrenin yeniden hesaplanıp hesaplanmayacağını belirtir (`true` veya `false`). |
| folder        | string   | Sorgu   | Orijinal çalışma kitabının bulunduğu klasör. |
| storageName   | string   | Sorgu   | Çalışma kitabının bulunduğu depo adı. |

### **Yanıt**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                        |
|-----|-----------------------------|-------------------------------------------------|
| 200 | Tamam                       | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir. |
| 400 | Geçersiz İstek              | Eksik veya geçersiz parametreler (örn. desteklenmeyen dosya türü). |
| 401 | Yetkisiz                    | Geçersiz veya eksik JWT belirteci. |
| 413 | Yük Çok Büyük               | Yüklenecek dosya boyut sınırını aşıyor. |
| 500 | Sunucu İç Hatası            | Beklenmeyen sunucu hatası. |
## SDK’lar ile PutWorksheetIconFilter API Nasıl Kullanılır?

### PutWorksheetIconFilter API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/AutoFilter/PutWorksheetIconFilter), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından yapmanıza olanak tanır.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl istek yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/autoFilter/iconFilter?range=A1:B1&fieldindex=0&iconsettype=ArrowsGray3&iconid=1" \
  -X PUT \
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

Olası yanıt durum kodları:

| Kod | Açıklama |
|-----|----------|
| 200 | Filtre başarıyla uygulandı. |
| 400 | Geçersiz istek – eksik veya geçersiz parametreler. |
| 401 | Yetkisiz – geçersiz veya eksik kimlik doğrulama belirteci. |
| 404 | Çalışma kitabı, çalışma sayfası veya belirtilen aralık bulunamadı. |
| 500 | Sunucu iç hatası. |
{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanın

Bir SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. SDK, düşük seviye detayları yöneterek sizin projenizin işlerine odaklanmanıza olanak tanır. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web servislerine nasıl istek yapıldığını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetIconFilter.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetIconFilter.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetIconFilter.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetIconFilter.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetIconFilter.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetIconFilter.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetIconFilter.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetIconFilter.go" >}}

{{< /tab >}}

{{< /tabs >}}

Diğer Otomatik Filtre (AutoFilter) yetenekleri için lütfen **[Renk Filtresi Ekleme](/tr/autofilter/add-color-filter/)**, **[Tarih Filtresi Ekleme](/tr/autofilter/add-date-filter/)** ve **[Otomatik Filtreyi Temizleme](/tr/autofilter/clear-autofilter/)** belgelerine bakın.