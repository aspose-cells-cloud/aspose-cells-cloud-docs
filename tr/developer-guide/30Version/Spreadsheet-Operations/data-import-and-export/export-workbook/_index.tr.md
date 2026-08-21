---
title: "Çalışma Kitabını Dışa Aktar"
second_title: "Belge"
linktitle: "Çalışma Kitabı"
type: docs
url: /export-excel-to-different-formats/
aliases: [/export/excel-to-different-formats/]
keywords: "Aspose.Cells Cloud, Excel dışa aktarma, çalışma kitaplığı dönüştürme, PDF, CSV, JSON, görüntü formatları, elektronik tablo API'si, XLSX, ODS, PNG"
description: "Aspose.Cells Cloud REST API ve SDK'larını kullanarak Excel çalışma kitaplarını PDF, CSV, JSON ve çeşitli görüntü türleri dahil olmak üzere birden fazla forma dışa aktarma adım adım kılavuzu."
weight: 20
---

Aşağıdaki formatlardan herhangi birine çalışma kitaplarını dışa aktarabilirsiniz: [XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/), [PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [DIF](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [NUMBERS](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

## REST API


```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.


### İstek Parametreleri

| Parametre Adı | Tür    | Yol/Sorgu Dizesi/HTTP Gövdesi | Gerekli | Açıklama                                                |
|----------------|---------|-----------------------------|-----------|------------------------------------------------------------|
| file           | dosya    | formData                    | Evet | Yüklenecek dosya                                             |
| objectType  | string | sorgu                       |   Evet | Dışa aktarılacak nesne türü. Çizelge dışa aktarması için `chart` kullanın. Diğer olası değerler `worksheet`, `picture` vb. |
| format  | string | sorgu                       |  Evet | İstenen çıktı formatı. Desteklenen değerler: `png`, `jpeg`, `gif`, `bmp`, `svg`, `tiff`, `emf`, `wmf`, `pdf`.
 |


### **Yanıt**

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx.tif",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx.tif",
      "FileSize": 348126,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```


**HTTP Durum Kodları**

| Kod | Anlamı               | Açıklama |
|------|-----------------------|-------------|
| 200  | Tamam (OK)                    | Şekiller başarıyla dışa aktarıldı; yanıt dosya listesini içerir. |
| 400  | Geçersiz İstek           | Eksik veya geçersiz parametreler. |
| 401  | Yetkisiz           | Geçersiz veya eksik erişim belirteci. |
| 413  | Yük Çok Büyük           | Yüklenecek dosya boyut limitini aşıyor. |
| 500  | Sunucu İç Hatası | Beklenmeyen sunucu hatası. |


## SDK'larla PostExport API Nasıl Kullanılır

### PostExport API Spesifikasyonu


[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/LightCells/PostExport), bir web tarayıcısından doğrudan REST etkileşimlerinde bulunmanıza olanak tanıyan herkese açık bir programlama arayüzü tanımlar.

Aspose.Cells web servislerine kolayca erişmek için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'yi nasıl çağıracağınızı göstermektedir.

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=workbook&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Aspose.Cells Cloud SDK'larını Kullanma

Bir SDK kullanmak, düşük seviye detayları ele aldığından geliştirme sürecini hızlandırır ve iş mantığına odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi [GitHub deposunda](https://github.com/aspose-cells-cloud) mevcuttur.

Aşağıdaki kod örnekleri, farklı SDK'larla Aspose.Cells web servisini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExport.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExport.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExport.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExport.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExport.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExport.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExport.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExport.go" >}}

{{< /tab >}}

{{< /tabs >}}