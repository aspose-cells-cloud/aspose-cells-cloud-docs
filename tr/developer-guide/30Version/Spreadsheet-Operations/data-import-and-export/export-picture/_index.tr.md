---
title: "Resim Dışa Aktar"
second_title: "Belge"
linktitle: "Resim"
type: docs
url: /tr/export-excel-picture-to-different-formats/
aliases: [  /tr/export/excel-picture-to-different-formats/ ]
keywords: "Resim Dışa Aktar, Aspose.Cells Cloud, REST API, Excel, Görüntü Formatları, PNG, GIF, JPEG, BMP, SVG, TIFF, EMF, WMF"
description: "Aspose.Cells Cloud REST API kullanarak Excel resimlerini çeşitli görüntü formatlarına dışa aktarın. Hizmet, C#, Java, PHP, Ruby, Node.js, Python, Perl, Go ve Swift dahil olmak üzerebirden fazla programlama dili için SDK'ları destekler."
weight: 20
---

Aşağıdaki formatlara resim dışa aktarabilirsiniz: [PNG](https://docs.fileformat.com/Image/png/), [GIF](https://docs.fileformat.com/image/gif/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), ve [WMF](https://docs.fileformat.com/image/Wmf/).

## REST API


```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulamayı</a> gerektirir.


### İstek Parametreleri

| Parametre       | Konum       | Tür   | Gerekli | Açıklama                                                                              |
| --------------- | ----------- | ----- | ------- | ------------------------------------------------------------------------------------- |
| `file`          | Form verisi | dosya | Evet    | OLE nesnelerini içeren Excel çalışma kitabını (`.xlsx`, `.xls`, vb.) içerir.          |
| `outputFormat`  | Sorgu       | dize  | Evet    | Dışa aktarılan nesnelerin hedef formatı (`pdf`, `png`, `jpeg`, `docx`, `pptx`).       |
| `objectType`    | Sorgu       | dize  | Evet    | Sabit değer `oleobject`.                                                              |


### Yanıt

```json
{
  "Files": [
    {
      "Filename": "Book1_xlsx_Sheet6_Pictures_0.tif",
      "FileSize": 21680,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "Book1_xlsx_Sheet6_Pictures_1.tif",
      "FileSize": 21286,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet2_Pictures_0.tif",
      "FileSize": 130084,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "myDocument_xlsx_Sheet2_Pictures_1.tif",
      "FileSize": 120062,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                             |
|-----|-----------------------------|------------------------------------------------------|
| 200 | Tamam                       | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir. |
| 400 | Geçersiz İstek              | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Yetkisiz İstek              | Geçersiz veya eksik JWT belirteci. |
| 413 | Yük Çok Büyük               | Yüklenen dosya boyut sınırını aşıyor. |
| 500 | Sunucu İç Hatası            | Beklenmeyen sunucu hatası. |
## SDK'lar ile PostExport API Nasıl Kullanılır

### PostExport API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/LightCells/PostExport), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'ye nasıl istek yapıldığını göstermektedir.


```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=picture&format=tiff" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -H "x-aspose-client: Containerize.Swagger" \
     -d '{"File":{}}'
```

### Aspose.Cells Cloud SDK'larını Kullanma

Bir SDK kullanmak, geliştirmeyi hızlandırmanın en verimli yoludur. Bir SDK, düşük seviye detayları işler ve size proje mantığına odaklanma imkanı sunar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposunu](https://github.com/aspose-cells-cloud) kontrol edin.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerini çeşitli SDK'lar kullanarak nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportPicture.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportPicture.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportPicture.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportPicture.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportPicture.ts" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportPicture.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportPicture.pl" >}}
{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportPicture.go" >}}
{{< /tab >}}

{{< /tabs >}}