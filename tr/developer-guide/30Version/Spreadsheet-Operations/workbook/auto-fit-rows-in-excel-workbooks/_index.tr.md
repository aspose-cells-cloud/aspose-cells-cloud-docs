---
title: "Excel Çalışma Kitabında Satırları Otomatik Uygun Hale Getirme"
second_title: "Belge"
linktitle: "Satırlar"
type: docs
url: /autofit-rows-on-an-excel-file/
aliases: [/auto-fit-rows-in-excel-workbooks/, /workbook/autofit/rows/]
keywords: "satırları otomatik uygun hale getirme, Excel çalışma kitabı, Aspose.Cells Cloud, REST API, otomatik uygunluk seçenekleri"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma kitabında satır yüksekliklerini otomatik olarak ayarlamayı öğrenin. Endpoint, parametreler, cURL örneği ve C#, Java, Python ve diğerleri için SDK snippet'leri içerir."
weight: 90
ArticleTitle: "Excel Çalışma Kitabında Satırları Otomatik Uygun Hale Getirme – Aspose.Cells Cloud API"
---

**Ön Gereksinimler**  
API’yi çağırmadan önce Aspose kimlik doğrulama hizmetinden geçerli bir Bearer JWT belirteci edinin ve hedef çalışma kitabının desteklenen bir depolama konumunda (varsayılan depo veya yapılandırdığınız özel bir depo) olduğunu doğrulayın.

Bu REST API, bir Excel çalışma kitabında **satırları otomatik olarak uygun hale getirmenizi** sağlar; yani veri eklendiğinde veya değiştirildiğinde satır yüksekliğini otomatik olarak ayarlar.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/autofitrows
```

İstek parametreleri şunlardır:

| Parametre Adı     | Tür               | Konum   | Açıklama                                                                              |
| ----------------- | ----------------- | ------- | ------------------------------------------------------------------------------------- |
| name              | string            | path    | Çalışma kitabının dosya adı.                                                          |
| autoFitterOptions | AutoFitterOptions | body    | Otomatik uygunluk davranışını kontrol eden seçenekler.                               |
| startRow          | integer           | query   | Otomatik uygun hale getirilecek ilk satırın indeksi.                                |
| endRow            | integer           | query   | Otomatik uygun hale getirilecek son satırın indeksi.                                |
| firstColumn       | integer           | query   | Otomatik uygunluk için dikkate alınacak ilk sütunun indeksi.                         |
| lastColumn        | integer           | query   | Otomatik uygunluk için dikkate alınacak son sütunun indeksi.                         |
| onlyAuto          | boolean           | query   | **true** ise, yalnızca Otomatik Uygunluk bayrağı olan satırlar işlenir (varsayılan **false**). |
| folder            | string            | query   | Çalışma kitabının depolandığı klasör yolu.                                           |
| storageName       | string            | query   | Depolama hizmetinin adı.                                                              |

**AutoFitterOptions**, otomatik uygunluk işleminin nasıl davranacağını belirleyen bir nesnedir (örneğin `AutoFitMergedCells`, `IgnoreHidden`).

**HTTP Durum Kodları**

| Kod  | Anlam                       | Açıklama                                         |
|------|-----------------------------|--------------------------------------------------|
| 200  | Başarılı (OK)               | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400  | Geçersiz İstek (Bad Request)| Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401  | Yetkisiz (Unauthorized)     | Geçersiz veya eksik JWT belirteci.               |
| 413  | Yük Çok Büyük (Payload Too Large) | Yüklenen dosya boyut sınırlarını aşıyor. |
| 500  | Sunucu İç Hatası (Internal Server Error) | Beklenmeyen sunucu hatası. |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Workbook/PostAutofitWorkbookRows), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web hizmetlerini çağırmak için cURL komut satırı aracını kullanabilirsiniz. `<jwt token>` ifadesini Aspose kimlik doğrulama hizmetinden edindiğiniz geçerli bir Bearer JWT belirteci ile değiştirin.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/autofitrows" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"AutoFitMergedCells":true, "IgnoreHidden":true}'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*Örnek hata yanıtı (örneğin, çalışma kitabı eksikse):*

```json
{
  "Code": 404,
  "Status": "Bulunamadı",
  "Message": "Belirtilen 'myWorkbook.xlsx' çalışma kitabı mevcut değil."
}
```

{{< /tab >}}

{{< /tabs >}}

**Notlar**  
- `AutoFitMergedCells` **true** olarak ayarlandığında, birleştirilmiş hücreler otomatik uygunluk işlemi sırasında tek bir varlık olarak dikkate alınır.  
- `IgnoreHidden` değerini **true** yapmak, gizli satır ve sütunları atlayarak mevcut boyutlarını korur.

## Bulut SDK Kütüphanesi

SDK kullanmak, geliştirme yapmanın en hızlı yoludur. SDK, düşük seviye detayları soyutlayarak projenize odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerini çeşitli SDK’lar kullanarak nasıl çağıracağınızı gösterir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostAutofitWorkbookRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostAutofitWorkbookRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostAutofitWorkbookRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostAutofitWorkbookRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostAutofitWorkbookRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostAutofitWorkbookRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostAutofitWorkbookRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostAutofitWorkbookRows.go" >}}

{{< /tab >}}

{{< /tabs >}}