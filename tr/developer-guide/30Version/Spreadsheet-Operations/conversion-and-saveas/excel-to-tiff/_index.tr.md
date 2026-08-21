---
title: "Excel'den TIFF'e"
second_title: "Belge"
linketitle: "Excel'den TIFF'e"
type: docs
url: /tr/convert-excel-file-to-tiff-file/
aliases: [  /tr/convert-excel-file-to-tiff-in-cloud/ , /tr/convert/excel-to-tiff/ ]
keywords: "Aspose.Cells Cloud, Excel'den TIFF'e dönüştürme, REST API, cURL, SDK, .NET, Java, Python, görüntü dışa aktarma"
description: "Aspose.Cells Cloud API ile Excel çalışma kitaplarını yüksek kaliteli TIFF görüntülerine nasıl dönüştüreceğinizi öğrenin. Detaylı cURL komutları, SDK örnekleri (C#, Java, Python, vb.), kimlik doğrulama adımları ve hata işleme."
weight: 90
---

**Aspose.Cells Cloud**’un **Dönüştür**, **Farklı Kaydet** ve **Dışa Aktar** uç noktaları, bir Excel çalışma kitabını TIFF görüntüsüne dönüştürmenizi sağlar.  
Bu uç noktaları doğrudan **cURL** ile veya desteklenen SDK’lardan biri aracılığıyla çağırabilirsiniz.

## REST API

| **API**                | **Yöntem** | **Amaç**                                                                                              | **Swagger Bağlantısı**                                                                      |
| ---------------------- | ---------- | ----------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| `/cells/convert`       | PUT        | İstek gövdesinde sağlanan çalışma kitabını belirtilen formata (TIFF) dönüştürür.                    | [PutConvertWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/PutConvertWorkBook) |
| `/cells/{name}`        | GET        | Adı belirtilen çalışma kitabını başka bir formata (TIFF) dışa aktarır ve sonucu yanıtta döndürür.    | [GetWorkBook](https://apireference.aspose.cloud/cells/#/Workbook/GetWorkBook)               |
| `/cells/{name}/saveAs` | POST       | Çalışma kitabını seçilen formata (TIFF) kaydeder ve sonucu bulut depolamada saklar.                 | [PostDocumentSaveAs](https://apireference.aspose.cloud/cells/#/SaveAs/PostDocumentSaveAs)   |

Bu uç noktalar herkese açıktır ve doğrudan bir web tarayıcısından veya herhangi bir HTTP istemcisinden çağrılabilir.

### cURL Örnekleri

{{< tabs tabTotal="3" tabID="11" tabName11="convert" tabName12="saveas" tabName13="export">}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/convert?format=tiff" \
     -X PUT \
     -d '{"File":{"Name":"book1.xlsx","Data":"<base64-içerik>"},"SaveFormat":"tiff"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt belirteci>"
```

{{< /tab >}}
{{< tab tabNum="12" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx/saveas?newfilename=book1.tiff" \
     -X POST \
     -d '{"SaveFormat":"tiff","ImageFormat":"tiff"}' \
     -H "Content-Type: application/json" \
     -H "Accept: application/json" \
     -H "Authorization: Bearer <jwt belirteci>"
```

{{< /tab >}}
{{< tab tabNum="13" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/book1.xlsx?format=tiff" \
     -X GET \
     -H "Authorization: Bearer <jwt belirteci>"
```

{{< /tab >}}
{{< /tabs >}}

> **Not:**
>
> - **Dönüştür** isteği gövdesi, dosyayı (veya depolanmış bir dosyaya bir referansı) ve istenen `SaveFormat` değerini içermelidir.
> - **Dışa Aktar** isteği için istek gövdesi gerekmez; format, sorgu dizgisinde (`format=tiff`) belirtilir.

## Hata İşleme

| **Durum Kodu** | **Anlamı**            | **Olası Neden**                             |
| --------------- | --------------------- | ------------------------------------------- |
| 200             | Başarılı              | TIFF görüntüsü döndürülür (ikili akış).    |
| 400             | Geçersiz İstek        | Eksik veya hatalı parametreler.             |
| 401             | Yetkisiz              | Geçersiz veya eksik JWT belirteci.          |
| 404             | Bulunamadı            | Belirtilen çalışma kitabı mevcut değil.    |
| 500             | Sunucu İç Hatası      | Beklenmeyen sunucu tarafı durumu.          |

Bir hata oluştuğunda API, `Code`, `Message` ve isteğe bağlı olarak `Description` alanlarını içeren bir JSON yükü döndürür.

## Bulut SDK Ailesi

SDK kullanmak, geliştirme yapmanın en hızlı yoludur. SDK, düşük seviye detayları yöneterek projenize odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposunu](https://github.com/aspose-cells-cloud) kontrol edin.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web hizmetlerini çağırma yöntemlerini göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutConvertWorkbookToTiff.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutConvertWorkbookToTiff.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutConvertWorkbookToTiff.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutConvertWorkbookToTiff.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutConvertWorkbookToTiff.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutConvertWorkbookToTiff.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutConvertWorkbookToTiff.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutConvertWorkbookToTiff.go" >}}

{{< /tab >}}

{{< /tabs >}}