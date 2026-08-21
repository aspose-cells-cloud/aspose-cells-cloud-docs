---
title: "Bir Excel çalışma kitabını birden fazla dosyaya bölme"
ArticleTitle: "Aspose.Cells Cloud API ile Bir Excel Çalışma Kitabını Birden Fazla Dosyaya Nasıl Bölersiniz?"
second_title: "Belge"
linktitle: "Bir Excel dosyasını bölme"
type: docs
url: /tr/split-multi-excel-files/
aliases: [  /tr/split/multi-files/ ]
keywords: "Excel, Aspose.Cells Cloud, REST API, çalışma kitabını bölme, birden fazla dosya, JPEG, PNG, PDF, CSV, JSON"
description: "Aspose.Cells Cloud REST API, bir Excel çalışma kitabını farklı formatlarda birden fazla dosyaya bölmenizi sağlar. Bu belgeler, C#, Java, PHP, Ruby, Node.js, Python, Perl ve Go gibi diller için istek parametrelerini, bir cURL örneğini ve SDK kod örneklerini içerir."
weight: 130
---

Bu REST API, bir Excel **çalışma kitabını** farklı formatlarda birden fazla dosyaya böler.

> **Önkoşullar** – Bu API’yi kullanmak için geçerli bir JWT jetonuna sahip olmanız, desteklenen bir SDK sürümünü kullandığınızdan emin olmanız ve çalışma kitabınızın desteklenen bir depolama konumunda saklandığından emin olmanız gerekir. API, aynı zamanda platform yönergelerinde belgelenen dosya boyutu sınırlarını da uygular.

## PostWorkbookSplit API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/split
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT jeton tabanlı kimlik doğrulamayı</a> gerektirir.

### İstek parametreleri

| Parametre Adı        | Tür     | Konum     | Açıklama                                                                                   | Gerekli |
| -------------------- | ------- | --------- | ------------------------------------------------------------------------------------------ | ------- |
| files[]              | dosya   | formData  | **Bölünecek** bir veya daha fazla Excel çalışma kitabını belirtir. İstekte `file1`, `file2`, … kullanın. | Evet    |
| format               | string  | Query     | Bölünen dosyalar için istenen çıktı formatı.                                              | Hayır   |
| from                 | integer | Query     | Başlangıç sayfa dizini.                                                                     | Hayır   |
| to                   | integer | Query     | Bitiş sayfa dizini.                                                                         | Hayır   |
| horizontalResolution | integer | Query     | Görüntü yatay çözünürlüğü.                                                                  | Hayır   |
| verticalResolution   | integer | Query     | Görüntü dikey çözünürlüğü.                                                                  | Hayır   |
| outFolder            | string  | Query     | Bölünen dosyaların çıktı klasörü.                                                           | Hayır   |
| splitNameRule        | string  | Query     | Bölünen dosyalara uygulanacak adlandırma kuralı.                                            | Hayır   |
| folder               | string  | Query     | Orijinal çalışma kitabının bulunduğu klasör.                                                | Hayır   |
| storageName          | string  | Query     | Kullanılacak depo adı.                                                                     | Hayır   |

### **Yanıt**

```json
{
    "Status":"OK",
    "Code":200,
    "Files": [
      {
        "Filename" : "[file1 name]",
        "Filesize" : [file size],
        "FileContent" : "[Base64String]"
      },
      {
        "Filename" : "[file2 name]",
        "Filesize" : [file size],
        "FileContent" : "[Base64String]"
      },
      {
        "Filename" : "[file3 name]",
        "Filesize" : [file size],
        "FileContent" : "[Base64String]"
      }
    ]
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                         |
|-----|-----------------------------|--------------------------------------------------|
| 200 | OK (Tamam)                  | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT jetonu. |
| 413 | Payload Too Large (Çok Büyük Yük) | Yüklenen dosya boyutu sınırını aşıyor. |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası. |

## SDK’lar ile PostWorkbookSplit API Nasıl Kullanılır?

### PostWorkbookSplit API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Workbook/PostWorkbookSplit), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web servislerine kolayca erişmek için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye istek nasıl yapılır gösterir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/test.xlsx/split?format=jpeg&from=1&to=1&horizontalResolution=0&verticalResolution=0" -H "accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Result": {
    "Documents": [
      {
        "Id": 1,
        "link": {
          "Href": "413e3375-c163-4d5c-8b84-8f95f63902f6.png",
          "Rel": null,
          "Title": null,
          "Type": null
        }
      }
    ]
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanma

Bir SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. Bir SDK, düşük seviye detayları yönetir böylece projenizin görevlerine odaklanabilirsiniz. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web servislerine nasıl istek yapıldığını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorkbookSplit.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorkbookSplit.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorkbookSplit.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorkbookSplit.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorkbookSplit.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorkbookSplit.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorkbookSplit.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorkbookSplit.go" >}}

{{< /tab >}}

{{< /tabs >}}