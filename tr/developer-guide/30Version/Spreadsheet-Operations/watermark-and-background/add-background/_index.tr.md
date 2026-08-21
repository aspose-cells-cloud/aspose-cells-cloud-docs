---
title: "Çalışma Kitabına Arka Plan Resmi Ekle"
second_title: "Belge"
linktype: "Ekle"
type: docs
url: /tr/add-background-in-excel-file/
aliases:
  - /add-background-in-workbook/
  - /workbook/add-background/
  - /workbook/background/add/
keywords: "Aspose.Cells, arka plan resmi ekle, Excel API, REST, bulut SDK, cURL, çalışma kitabı arka planı"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma kitabına arka plan resmi nasıl ekleneceğini öğrenin. Gerekli parametreler, kimlik doğrulama ayrıntıları, tam bir cURL örneği ve hata işleme bilgilerini içerir."
weight: 160
---

## REST API

Bu REST API, bir Excel çalışma kitabına bir **arka plan resmi** ekler.

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/background
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.


### Sorgu Parametreleri

| Parametre Adı | Tür   | Açıklama                                                   |
| ------------- | ----- | ---------------------------------------------------------- |
| `picPath`     | string | Arka plan olarak kullanılacak resim dosyasının yolu.      |
| `folder`      | string | Orijinal çalışma kitabının bulunduğu klasör.               |
| `storageName` | string | Dosyanın bulunduğu depo adı.                               |

### İstek Gövdesi Parametresi

| Parametre Adı | Tür  | Açıklama                                                |
| ------------- | ---- | ------------------------------------------------------- |
| `datafile`    | file | Arka planın uygulanacağı çalışma kitabının dosyası.     |

**Yol Parametresi** – URL'deki `{name}`, **çalışma kitabının dosya adını** temsil eder (örneğin, `Book1.xlsx`).


### **Yanıt**

```json
{
    "Status" : "OK",
    "Code" : 200
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                                    |
|-----|-----------------------------|-------------------------------------------------------------|
| 200 | Tamam                       | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Yanlış İstek                | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Yetkisiz                    | Geçersiz veya eksik JWT belirteci.                           |
| 413 | Yük Çok Büyük               | Yüklenen dosya boyut sınırını aşıyor.                        |
| 500 | İç Sunucu Hatası            | Beklenmeyen sunucu hatası.                                   |

## PutWorkbookBackground API’sini SDK’larla Nasıl Kullanılır?

### PutWorkbookBackground API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Workbook/PutWorkbookBackground), web tarayıcınızdan doğrudan REST etkileşimlerini gerçekleştirmenizi sağlayan herkese açık bir programlama arayüzü tanımlar.

Aspose.Cells web hizmetlerine kolayca erişmek için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, multipart dosya yükleme bayrağı ve gerekli kimlik doğrulama başlığıyla birlikte tam bir isteği göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -X PUT "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/background?picPath=DotnetFiles%2FWaterMark.png&folder=DotnetFiles" \
     -H "Authorization: Bearer <access_token>" \
     -H "accept: multipart/form-data" \
     -H "Content-Type: multipart/form-data" \
     -F "datafile=@/path/to/Book1.xlsx"
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


### Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanmak, geliştirme yapmanın en hızlı yoludur. Bir SDK, düşük seviyeli ayrıntıları soyutlayarak iş mantığınıza odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web hizmetlerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorkbookBackground.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorkbookBackground.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorkbookBackground.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorkbookBackground.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorkbookBackground.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorkbookBackground.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorkbookBackground.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorkbookBackground.go" >}}

{{< /tab >}}

{{< /tabs >}}