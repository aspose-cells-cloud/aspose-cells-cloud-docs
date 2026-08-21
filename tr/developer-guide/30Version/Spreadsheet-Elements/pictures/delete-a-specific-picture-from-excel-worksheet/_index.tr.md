---
title: "Bir Excel Çalışma Sayfasından Görsel Sil – Aspose.Cells Cloud API"
second_title: "Belge"
linktitle: "Sil"
type: docs
url: /pictures/delete/
aliases: [/delete-a-specific-picture-from-excel-worksheet/]
keywords: "Aspose.Cells, Bulut API, görsel sil, Excel çalışma sayfası, REST"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasından bir görseli silin. DELETE uç noktasını, gerekli parametreleri, kimlik doğrulamayı, hata kodlarını ve örnek kodu öğrenin."
weight: 50
ArticleTitle: "Bir Excel Çalışma Sayfasından Görsel Sil – Aspose.Cells Cloud API"
---

Bu REST API, bir Excel çalışma sayfasından bir görseli siler.

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulamayı</a> gerektirir.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/{pictureIndex}
```

### İstek Parametreleri

| Parametre Adı  | Tür      | Konum  | Gerekli | Açıklama                                               |
|----------------|----------|--------|---------|--------------------------------------------------------|
| name           | string   | path   | Evet    | Çalışma kitabının dosya adı.                            |
| sheetName      | string   | path   | Evet    | Görselin bulunduğu çalışma sayfasının adı.              |
| pictureIndex   | integer  | path   | Evet    | Silinecek görselin sıfır tabanlı indeksi.               |
| folder         | string   | query  | Hayır   | Çalışma kitabının bulunduğu klasör.                     |
| storageName    | string   | query  | Hayır   | Depolama hizmetinin adı (isteğe bağlı).                 |

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile bu çağrının nasıl yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet2/pictures/0" \
  -X DELETE \
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

**Örnek Yanıt Başlıkları**

| Başlık         | Değer                         |
|----------------|-------------------------------|
| Content-Type   | application/json              |
| Content-Length | (değişir)                     |
| Date           | (sunucu tarihi)               |

{{< /tab >}}

{{< /tabs >}}

### Hata Yönetimi

| HTTP Kodu | Anlam                                                       | Örnek Hata Yükü                                                   |
|-----------|-------------------------------------------------------------|-------------------------------------------------------------------|
| 200       | Görsel başarıyla silindi.                                   | `{ "Code": 200, "Status": "OK" }`                                 |
| 400       | Geçersiz istek – geçersiz parametreler.                     | `{ "Code": 400, "Message": "Geçersiz pictureIndex." }`           |
| 401       | Yetkisiz erişim – eksik/geçersiz belirteç.                  | `{ "Code": 401, "Message": "Erişim belirteci eksik veya geçersiz." }` |
| 404       | Bulunamadı – çalışma kitabısı, çalışma sayfası veya görsel mevcut değil. | `{ "Code": 404, "Message": "Kaynak bulunamadı." }`         |
| 500       | İç sunucu hatası.                                           | `{ "Code": 500, "Message": "Beklenmeyen sunucu hatası." }`       |

## Bulut SDK Ailesi

SDK kullanmak, geliştirme yapmanın en hızlı yoludur. Bir SDK, düşük seviye detayları yöneterek projenize odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web servislerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}