---
title: "Boş bir Excel Çalışma Kitabı Oluşturun"
second_title: "Belge"
linktitle: "Boş Çalışma Kitabı"
type: docs
url: /create-an-empty-excel-file/
aliases:
  [
    /create-an-empty-excel-workbook/,
    /workbook/new/,
    /workbook/create/empty-workbook/,
  ]
keywords: "Aspose.Cells, Bulut, Excel, boş çalışma kitabı, REST API, SDK"
description: "Aspose.Cells Cloud REST API kullanarak nasıl boş bir Excel çalışma kitabı oluşturulacağını öğrenin. cURL ve SDK örneklerini içerir."
weight: 20
ArticleTitle: "Aspose.Cells Cloud API ile Boş bir Excel Çalışma Kitabı Oluşturun"
---

Bu REST API, **boş bir çalışma kitabını** oluşturur.

## PutWorkbookCreate API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### Sorgu Parametreleri

| Parametre Adı | Tür    | Açıklama                                                     |
| ------------- | ------ | ------------------------------------------------------------ |
| templateFile  | string | Temel olarak kullanılacak şablon çalışma kitabının yolu (isteğe bağlı). |
| dataFile      | string | Çalışma kitabını doldurmak için kullanılacak veri dosyasının yolu (isteğe bağlı). |
| isWriteOver   | boolean | `true` mevcut bir dosyanın üzerine yazmak için; aksi takdirde `false`. |
| folder        | string | Oluşturulan çalışma kitabının konumlandırılacağı klasör (isteğe bağlı). |
| storageName   | string | Kullanılacak depolama hizmetinin adı.                        |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür | Açıklama                                   |
| ------------- | --- | ------------------------------------------ |
| data          | file | Oluşturulacak çalışma kitabının ikili içeriği. |

### **Yanıt**

```json
{
    "Name": "ResponseFile",
    "DataType": {
        "Identifier": "File",
        "Reference": "Stream",
        "Name": "file"
    }
}
```

**HTTP Durum Kodları**

| Kod | Anlam                      | Ne Zaman Döndürülür                     |
|-----|----------------------------|-----------------------------------------|
| 200 OK | Çalışma kitabı başarıyla oluşturuldu | Normal akış                              |
| 201 Created | Çalışma kitabı oluşturuldu (alternatif yanıt) | API oluşturuldu durumunu döndürdüğünde |
| 400 Bad Request | Geçersiz parametreler | İstemci tarafı hatası                        |
| 401 Unauthorized | Eksik veya geçersiz belirteç | Kimlik doğrulama hatası                    |
| 409 Conflict | Dosya mevcut ve `isWriteOver=false` | Mevcut dosya ile çakışma            |

## PutWorkbookCreate API'yi SDK’larla Nasıl Kullanılır

### PutWorkbookCreate API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookCreate), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

**cURL** komut satırı aracını Aspose.Cells web hizmetlerine erişmek için kullanabilirsiniz. Geçerli bir OAuth2/JWT erişim belirteci ile `Authorization` başlığını ekleyin. Boş bir çalışma kitabı için istek gövdesi isteğe bağlıdır; bir dosya yüklemeniz gerekiyorsa, aşağıda gösterildiği gibi `--data-binary @empty.xlsx` ekleyin.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
# newworkbook.xlsx adında boş bir çalışma kitabı oluşturun
curl -X PUT "https://api.aspose.cloud/v3.0/cells/newworkbook.xlsx?isWriteOver=false" \
     -H "accept: application/json" \
     -H "Authorization: Bearer <access_token>" \
     --data-binary @empty.xlsx   # Gerçekten boş bir çalışma kitabı için bu satırı atlayın
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```
{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoldur. Bir SDK, düşük seviye detayları soyutlayarak projenizin görevlerine odaklanabilmenizi sağlar. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web hizmetlerini çağırma yöntemlerini göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookCreateEmpty.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookCreateEmpty.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookCreateEmpty.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookCreateEmpty.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookCreateEmpty.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookCreateEmpty.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookCreateEmpty.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookCreateEmpty.go" >}}

{{< /tab >}}

{{< /tabs >}}
---