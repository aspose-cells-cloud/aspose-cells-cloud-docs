---
title: "OLE Nesnesini Dışa Aktar – Aspose.Cells Cloud API"
second_title: "Belge"
linktitle: "OLE Nesnesi"
type: docs
url: /export-excel-ole-object/
aliases: [/export/excel-ole-object/]
keywords: "Aspose.Cells, OLE nesnesi, dışa aktar, Excel, bulut API, PDF, PNG, DOCX, PPTX"
description: "Aspose.Cells Cloud API kullanarak bir Excel çalışma kitabından OLE nesnelerini dışa aktarın. İstek formatını, parametreleri, örnek cURL isteğini ve hata işleme yöntemlerini öğrenin."
weight: 20
ArticleTitle: "OLE Nesnesini Dışa Aktar – Aspose.Cells Cloud API"
---

## **REST API**

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.


### İstek Parametreleri

| Parametre       | Konum      | Tür   | Gerekli | Açıklama                                                                 |
| --------------- | ---------- | ----- | ------- | ------------------------------------------------------------------------ |
| `file`          | Form‑data  | dosya | Evet    | OLE nesnelerini içeren Excel çalışma kitabı (`.xlsx`, `.xls`, vb.).     |
| `outputFormat`  | Sorgu      | string | Evet    | Dışa aktarılan nesnelerin hedef formatı (`pdf`, `png`, `jpeg`, `docx`, `pptx`). |
| `objectType`    | Sorgu      | string | Evet    | Sabit değer: `oleobject`.                                                |


### Yanıt

Başarılı bir istek, dışa aktarılan dosyaları listeleyen bir JSON nesnesi döndürür:

```json
{
  "Files": [
    {
      "Filename": "OLESlide.ppt",
      "FileSize": 390,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "OLEDoc.docx",
      "FileSize": 382,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                                  |
|-----|-----------------------------|-----------------------------------------------------------|
| 200 | Tamam                       | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir. |
| 400 | Hatalı İstek                | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Yetkisiz                    | Geçersiz veya eksik JWT belirteci.                        |
| 413 | Yük Çok Büyük               | Yüklenen dosya boyut sınırını aşıyor.                     |
| 500 | İç Sunucu Hatası            | Beklenmeyen sunucu hatası.                                |
## SDK’lar ile PostExport API Nasıl Kullanılır

### PostExport API Spesifikasyonu


[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/LightCells/PostExport), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web servislerine kolayca erişmek için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl istek gönderileceğini göstermektedir.


```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/export?objectType=oleobject&format=pdf" \
  -H "Authorization: Bearer $ACCESS_TOKEN" \
  -F "file=@MyWorkbook.xlsx" \
  -F "outputFormat=pdf"
```

### OLE Nesnesi Nedir?

Bir **OLE (Object Linking and Embedding – Nesne Bağlama ve Gömme)** nesnesi, Word belgeleri, PowerPoint slaytları, resimler veya diğer dosyalar gibi harici içerikleri bir Excel çalışma kitabının içine gömer. Dışa aktarılırken, gömülü içerik çıkarılır ve istenen çıktı formatında kaydedilir.

### Endpoint Genel Bakış

`POST https://api.aspose.cloud/v3.0/cells/export?objectType=oleobject&format={outputFormat}`

- `objectType` – `oleobject` olarak ayarlanmalıdır.
- `format` – İstenen çıktı formatı (örneğin, `pdf`, `png`, `jpeg`, `docx`, `pptx`).

### Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanmak, geliştirme sürecini hızlandırmak için en iyi yoldur. SDK, düşük seviye detayları yöneterek projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web servislerine nasıl istek gönderileceğini göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostExportOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostExportOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostExportOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostExportOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostExportOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostExportOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostExportOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostExportOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}
---