---
title: "Liste Nesnesini Dışa Aktar"
second_title: "Belge"
linktitle: "Liste Nesnesi"
type: docs
url: /tr/export-excel-listobject-to-different-formats/
aliases: [  /tr/export/excel-listobject-to-different-formats/ ]
keywords: "ListeNesnesi Dışa Aktar, Excel ListeNesnesi, Aspose.Cells Cloud, REST API, PDF, CSV, JSON, XLSX, ODS, PNG, TIFF, SDK'lar"
description: "Aspose.Cells Cloud REST API, Excel ListeNesnelerini çeşitli dosya formatlarına dışa aktarmayı sağlar. C#, Java, Python, Node.js, Go, PHP, Ruby, Perl ve Swift dahil birçok programlama dili için SDK’lar mevcuttur."
weight: 20
---

Aşağıdaki formatlara dışa aktarabilirsiniz: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.


### İstek Parametreleri

| Parametre Adı | Tür    | Yol/Sorgu Dizisi/HTTP Gövdesi | Gerekli |Açıklama                                                |
|----------------|---------|-----------------------------|-----------|------------------------------------------------------------|
| file           | dosya   | formData                    | Evet | Yüklenecek dosya                                             |
| objectType  | string | sorgu                       |   Evet | Dışa aktarılacak nesne türü. Grafik dışa aktarmak için `chart` kullanın. Diğer olası değerler: `worksheet`, `picture` vb. |
| format  | string | sorgu                       |  Evet | İstenen çıktı formatı. Desteklenen değerler: `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf`.
 |

### Yanıt

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet1_ListObjects_0.tif",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet2_ListObjects_0.tif",
      "FileSize": 10040,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet1_ListObjects_0.tif",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```


**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                      |
|------|-----------------------------|--------------------------------------------------|
| 200  | Tamam (OK)                  | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir. |
| 400  | Geçersiz İstek (Bad Request)| Eksik veya geçersiz parametreler (örn., desteklenmeyen dosya türü). |
| 401  | Yetkisiz (Unauthorized)      | Geçersiz veya eksik JWT belirteci. |
| 413  | Yük Çok Büyük (Payload Too Large) | Yüklenecek dosya boyut sınırını aşıyor. |
| 500  | Sunucu İç Hatası (Internal Server Error) | Beklenmeyen sunucu hatası. |
## SDK’larla PostExport API Nasıl Kullanılır?

### PostExport API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/LightCells/PostExport), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye istekte bulunmayı göstermektedir.

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=listobject&format=tiff" \
-H "accept: multipart/form-data" \
-H "Content-Type: multipart/form-data" \
-H "x-aspose-client: Containerize.Swagger" \
-d '{"File":{}}'
```

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. SDK, düşük seviye detayları yöneterek size proje görevlerinize odaklanma imkanı verir. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web hizmetlerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportListObject.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportListObject.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportListObject.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportListObject.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportListObject.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportListObject.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportListObject.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportListObject.go" >}}
{{< /tab >}}

{{< /tabs >}}