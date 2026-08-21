---
title: "Bir Çalışma Sayfası Alanını PNG, PDF, CSV’ye Dışa Aktar – Aspose.Cells Cloud API"
second_title: "Belge"
linktitle: "Alan"
type: docs
url: /worksheets/area-to-different-formats/
aliases: [/get-worksheet-for-area/]
keywords: "Aspose.Cells, çalışma sayfası alanı dışa aktar, PNG, PDF, CSV, Excel dönüştürme, REST API, SDK"
description: "Aspose.Cells Cloud REST API veya SDK’ları (C#, Java, Python,…) kullanarak bir Excel çalışma sayfasından belirli bir hücre aralığını PNG, PDF, CSV ve 20'den fazla diğer formata nasıl dışa aktaracağınızı öğrenin."
weight: 230
ArticleTitle: "Aspose.Cells Cloud API ile Çalışma Sayfası Alanını PNG, PDF, CSV’ye Dışa Aktar – Tam Kılavuz"
---

[GET /cells/{name}/worksheets/{sheetName}](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet) API'si, bir çalışma sayfasının belirli bir alanını çeşitli dosya formatlarına dönüştürmenizi sağlar. Desteklenen formatlar: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [GIF](https://docs.fileformat.com/image/gif/), [BMP](https://docs.fileformat.com/image/bmp/), [WMF](https://docs.fileformat.com/image/wmf/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

Bu kılavuz, Aspose.Cells Cloud API’sini kullanarak bir Excel çalışma sayfasından **belirli bir hücre aralığını** PNG, PDF, CSV ve 20'den fazla ek formatına nasıl dışa aktaracağınızı gösterir. Tam bir çalışma sayfasını dışa aktarma veya bir çalışma kitabını dönüştürme gibi ilgili işlemler için **[Tüm Çalışma Sayfasını Dışa Aktar](https://docs.aspose.cloud/cells/worksheets/worksheet-to-different-formats/)** ve **[Çalışma Kitabını PDF’e Dönüştür](https://docs.aspose.cloud/cells/workbook/convert-to-pdf/)** sayfalarına bakın.

## REST API

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheetWithFormat), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

### İstek parametreleri

| Parametre             | Tür     | Gerekli | Açıklama                                      |
|-----------------------|---------|---------|-----------------------------------------------|
| `name`                | string  | Evet    | Çalışma kitabının dosya adı.                   |
| `sheetName`           | string  | Evet    | Hedef çalışma sayfasının adı.                   |
| `format`              | string  | Evet    | İstenen çıktı formatı (png, pdf, csv, vb.).    |
| `area`                | string  | Hayır   | Dışa aktarılacak hücre aralığı (örn. `B3:K8`). |
| `verticalResolution`  | int     | Hayır   | Raster formatlar için dikey DPI.               |
| `horizontalResolution`| int     | Hayır   | Raster formatlar için yatay DPI.               |
| `folder`              | string  | Hayır   | Dosyayı içeren bulut depolama klasörü.         |
| `storage`             | string  | Hayır   | Depolama hizmetinin adı.                       |

### Başarılı yanıt

* **200 OK** – İstenen dosyayı ikili formatta (PNG, PDF, CSV, vb.) döndürür.

### Hata yanıtları

| Durum Kodu | Açıklama                                      |
|------------|-----------------------------------------------|
| 400        | Hatalı istek – eksik veya geçersiz parametreler. |
| 401        | Yetkisiz – kimlik doğrulama belirteci eksik veya geçersiz. |
| 404        | Bulunamadı – belirtilen çalışma kitabını veya çalışma sayfası mevcut değil. |
| 500        | Sunucu iç hatası – sunucuda beklenmedik bir durum oluştu. |

**Örnek hata yükü**

```json
{
  "error": {
    "code": "InvalidParameter",
    "message": "'area' parametresi bozuk. Beklenen format: B3:K8."
  }
}
```

Aspose.Cells web hizmetlerine kolayca ulaşmak için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'sine nasıl istek yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1?format=png&verticalResolution=100&horizontalResolution=90&area=B3%3AK8&folder=DotnetFiles" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

Dönüştürülmüş resim (ikili PNG)

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Geliştirme Grubu

SDK kullanmak, geliştirme yapmanın en hızlı yoludur. SDK, düşük seviyeli detayları soyutlayarak proje mantığına odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerini çeşitli SDK’lar kullanarak nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellAreaWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellAreaWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellAreaWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellAreaWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellAreaWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellAreaWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellAreaWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellAreaWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}