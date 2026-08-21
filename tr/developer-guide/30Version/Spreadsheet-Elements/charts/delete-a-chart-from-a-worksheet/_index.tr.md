---
title: "Bir Çalışma Sayfasından Bir Grafik Silme"
type: docs
url: /tr/charts/delete/
aliases: [  /tr/delete-a-chart-from-a-worksheet/ ]
weight: 40
keywords:
  - "Aspose.Cells"
  - "REST API"
  - "Grafik Silme"
  - "Çalışma Sayfası"
  - "Excel"
  - "Bulut SDK'sı"
  - "Grafik Silme"
  - "API Referansı"
description: "Aspose.Cells Cloud REST API kullanılarak bir çalışma sayfasından grafik, sıfır tabanlı indeksine göre silinir."
ArticleTitle: "Aspose.Cells Cloud REST API ile Bir Çalışma Sayfasından Bir Grafik Silme"
---

Bu REST API, bir grafik indeksine göre bir çalışma sayfası grafiğini siler.

İlgili işlemler için **[Grafik Ekle](#)** ve **[Grafiği Al](#)** sayfalarına bakın.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}
```

### Güvenlik ve Kimlik Doğrulama

Aspose.Cells Cloud API’leri güvenlidir ve [JWT belirteci tabanlı kimlik doğrulama](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür      | Konum  | Açıklama                                      |
| ------------- | -------- | ------ | --------------------------------------------- |
| name          | string   | path   | Çalışma kitabının adı.                        |
| sheetName     | string   | path   | Çalışma sayfasının adı.                       |
| chartIndex    | integer  | path   | Silinecek grafiğin sıfır tabanlı indeksi.    |
| folder        | string   | query  | Çalışma kitabının bulunduğu klasör.           |
| storageName   | string   | query  | Kullanılacak depo adı.                       |


### **Yanıt**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                              |
|-----|-----------------------------|-------------------------------------------------------|
| 200 | OK (Tamam)                  | Filtre başarıyla uygulandı; yanıt, işlem ayrıntılarını içerir. |
| 400 | Geçersiz İstek              | Eksik veya geçersiz parametreler (örn., desteklenmeyen dosya türü). |
| 401 | Yetkisiz                    | Geçersiz veya eksik JWT belirteci.                   |
| 413 | Yük Çok Büyük               | Yüklenecek dosya boyut sınırını aşıyor.              |
| 500 | Sunucu İç Hatası            | Beklenmeyen sunucu hatası.                           |

## PutWorksheetAddChart API'sini SDK’lar ile Nasıl Kullanılır

### PutWorksheetAddChart API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Charts/DeleteWorksheetDeleteChart), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’sine istek nasıl yapılır gösterir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet5/charts/0" \
-X DELETE \
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

API aşağıdaki durum kodlarını döndürür:

| Kod | Açıklama                              |
|-----|---------------------------------------|
| 200 | Grafik başarıyla silindi             |
| 400 | Geçersiz istek (örn., geçersiz indeks) |
| 401 | Yetkisiz (eksik veya geçersiz JWT)   |
| 404 | Çalışma kitabında, çalışma sayfasında veya grafik bulunamadı |
| 500 | Sunucu hatası                         |

**Hata yönetimi:** Ayrıntılı hata bilgisi için OpenAPI spesifikasyonundaki genel hata modeline bakın.

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme hızını artırmak için en iyi yoldur. SDK, düşük seviye detayları soyutlayarak projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetlerinin nasıl çağrılacağını gösterir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Charts-DeleteChart-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-chart-DeleteOneChart-delete-single-chart.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-DeleteWorksheetDeleteChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-delete_worksheet_chart_by_index-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteChartExcelWorksheet.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-DeleteChart-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-chart-DeleteOneChart-delete-single-chart.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-DeleteChart-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "b858c32efd7b745ebb75d61898ec50e0" >}}

{{< /tab >}}

{{< /tabs >}}