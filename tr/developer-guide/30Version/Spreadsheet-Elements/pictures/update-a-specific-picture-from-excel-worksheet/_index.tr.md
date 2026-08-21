---
title: "Excel dosyasında resim güncelleme"
second_title: "Belge"
linktitle: "Güncelle"
type: docs
url: /pictures/update/
aliases: [/update-a-specific-picture-from-excel-workshee/]
keywords: "Aspose.Cells Cloud, Excel, Resim güncelle, REST API, SDK"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasında resim nasıl güncellenir öğrenin. İstek detaylarını, cURL örneğini ve birden fazla dil için SDK snippet'lerini içerir."
ArticleTitle: "Aspose.Cells Cloud REST API kullanarak Excel dosyasında resim güncelleme"
weight: 70
---

Bu REST API, bir Excel çalışma sayfasındaki belirli bir resmi, dizin numarası ile tanımlanarak günceller.

**Önkoşullar:** Geçerli bir Aspose Cloud JWT jetonuna, hedef Excel dosyasının Aspose Cloud depolama alanınızda bulunmasına ve API sürümü 3.0 veya üstüne sahip olmanız gerekir.

## PostWorksheetPicture API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT jeton tabanlı kimlik doğrulama</a> gerektirir.

### **İstek parametreleri**

| Parametre Adı | Tür      | Konum  | Açıklama                                                      |
| ------------- | -------- | ------ | ------------------------------------------------------------- |
| name          | string   | path   | Excel belgesinin adı.                                         |
| sheetName     | string   | path   | Resmin bulunduğu çalışma sayfasının adı.                      |
| pictureIndex  | integer  | path   | Güncellenecek resmin sıfır tabanlı dizini.                    |
| picture       | object   | body   | Güncellenecek resim özelliklerini tanımlayan JSON nesnesi.    |
| folder        | string   | query  | Belgenin bulunduğu klasör.                                    |
| storageName   | string   | query  | Depolama hizmetinin adı.                                      |

**Not:** Resim dizini sıfır tabanlıdır. Desteklenen resim formatları JPEG, PNG, BMP ve GIF'tir. Maksimum resim boyutu 10 MB'dir.

### Hata Yanıtları

| HTTP Kodu | Açıklama                                               |
| --------- | ------------------------------------------------------ |
| 401       | Yetkisiz – eksik veya geçersiz jeton.                  |
| 404       | Bulunamadı – belirtilen dosya, çalışma sayfası veya resim dizini mevcut değil. |
| 400       | Geçersiz İstek – hatalı istek söz dizimi veya geçersiz parametreler. |
| 500       | Sunucu içi hatası – beklenmeyen bir durumla karşılaşıldı. |

<a href="https://apireference.aspose.cloud/cells/#/Pictures/PostWorksheetPicture" rel="noopener noreferrer">OpenAPI Spesifikasyonu</a>, herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından yapmanızı sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'ye istek nasıl atlanacağını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/1" \
-X POST \
-d "{ \"UpperLeftRow\": 10, \"Top\": 0, \"UpperLeftColumn\": 1, \"Left\": 0, \"LowerRightRow\": 0, \"Bottom\": 0, \"LowerRightColumn\": 3, \"ImageFormat\": \"jpg\", \"SourceFullName\": \"download.jpg\"}" \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
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

## Bulut SDK Ailesi

SDK kullanmak, geliştirmenin en hızlı yoludur. SDK, düşük seviye detayları yöneterek size proje görevlerinize odaklanma imkanı verir. Aspose.Cells Cloud SDK'larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" rel="noopener noreferrer">GitHub deposunu</a> kontrol edin.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerini çeşitli SDK’lar kullanarak nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}

*İlgili konular:* Resim ekleme, Resim silme, Resim alma, Resimleri temizleme – Aspose.Cells Cloud API'deki diğer resimle ilgili işlemler.