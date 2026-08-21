---
title: "Bir Çalışma Sayfası Sayfasını Dışa Aktar – Aspose.Cells Cloud API Referansı"
ArticleTitle: "Bir Çalışma Sayfası Sayfasını Dışa Aktar – Aspose.Cells Cloud API Referansı"
second_title: "Belge"
linktitle: "Sayfa"
type: docs
url: /tr/worksheets/page-to-different-formats/
aliases: [  /tr/get-worksheet-for-page-index/ ]
keywords: "Aspose.Cells Cloud, çalışma sayfası sayfası dışa aktarma, PDF, PNG, CSV, REST API, JWT kimlik doğrulama, dosya formatları"
description: "Aspose.Cells Cloud REST API kullanarak belirli bir çalışma sayfası sayfasını PDF, PNG, CSV ve diğer formatlara nasıl dışa aktaracağınızı öğrenin. cURL isteği, parametre kılavuzu ve birden fazla dil için SDK örneklerini içerir."
weight: 240
---

Belirli bir çalışma sayfası sayfasını dışa aktarmak, tüm çalışma kitabını indirmek yerine bir raporun yazdırılabilir anlık görüntüsüne, bir grafik görüntüsüne veya bir veri çıkıntısına ihtiyaç duyduğunuzda faydalıdır. Bu uç nokta, tek bir sayfayı alt işlem akışınız için en uygun formatla almanızı sağlar.

[GET /cells/{name}/worksheets/{sheetName}](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) API’si, bir çalışma sayfasının belirli bir sayfasını çeşitli dosya formatlarına dönüştürmenizi sağlar. Desteklenen formatlar: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [GIF](https://docs.fileformat.com/image/gif/), [BMP](https://docs.fileformat.com/image/bmp/), [WMF](https://docs.fileformat.com/image/wmf/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

## REST API

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından yapmanızı sağlar.

> **Önkoşullar** – Geçerli bir JWT kimlik doğrulama jetonuna ve `folder` parametresiyle belirttiğiniz bulut klasöründe depolanmış bir çalışma kitabına sahip olmanız gerekir.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’sine nasıl istek yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1?format=png&verticalResolution=100&horizontalResolution=90&pageIndex=1&folder=DotnetFiles" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**Yanıt** – Hizmet, istenen sayfayı seçilen formatta döndürür. Görüntü formatları (png, jpeg, gif vb.) için gövde ikili görüntü verisi içerir; belge formatları (pdf, xls, csv vb.) için gövde dosya içeriğini içerir. Başarılı bir çağrı HTTP 200 döndürür.

*PNG yanıtı örneği (kesilmiş base64 parçası):*

```text
iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8/9hAAABG0lEQVR42mNkYGBg+M+ABbJw
...
```

{{< /tab >}}

{{< /tabs >}}

**Parametreler**

| Parametre              | Tür     | Açıklama                                                               | Varsayılan |
| ---------------------- | ------- | ------------------------------------------------------------------------ | ---------- |
| `format`               | string  | Çıktı dosyası formatı (örn. `pdf`, `png`, `csv`).                       | `pdf`      |
| `verticalResolution`   | integer | Oluşturulan görüntünün dikey DPI’si.                                   | `100`      |
| `horizontalResolution` | integer | Oluşturulan görüntünün yatay DPI’si.                                   | `100`      |
| `pageIndex`            | integer | Dışa aktarılacak çalışma sayfası sayfasının sıfır tabanlı indeksi (`0` = ilk sayfa). | `0`        |
| `folder`               | string  | Kaynak çalışma kitabının bulunduğu bulut depolama klasörü.             | —          |

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                                  |
|-----|-----------------------------|-----------------------------------------------------------|
| 200 | Tamam                       | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | İstek Hatası                | Eksik veya geçersiz parametreler (örn. desteklenmeyen dosya türü). |
| 401 | Yetkisiz                    | Geçersiz veya eksik JWT jetonu.                           |
| 413 | Yük Çok Büyük               | Yüklenen dosya boyut sınırını aşıyor.                     |
| 500 | İç Sunucu Hatası            | Beklenmeyen sunucu hatası.                                |

**Olası hatalar**

- **401 Yetkisiz** – Geçersiz veya eksik JWT jetonu.
- **404 Bulunamadı** – Belirtilen çalışma kitabının veya çalışma sayfasının bulunamaması.
- **400 İstek Hatası** – Geçersiz parametre değeri (örn. desteklenmeyen `format`).
- **500 İç Sunucu Hatası** – Beklenmeyen sunucu tarafı sorunu.

## Bulut SDK Ailesi

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. SDK, düşük seviye ayrıntıları kendisi işlediği için projenizin görevlerine odaklanabilirsiniz. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetlerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}