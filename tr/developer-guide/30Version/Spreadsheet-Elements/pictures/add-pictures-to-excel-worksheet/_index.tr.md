---
title: "Excel Dosyasına Resim Ekleyin"
second_title: "Belge"
linktitle: "Ekle"
type: docs
url: /tr/pictures/add/
aliases: [  /tr/add-pictures-to-excel-worksheet/ ]
keywords: "Aspose.Cells, Excel, resim ekle, REST API"
description: "Aspose.Cells Cloud REST API’sini kullanarak bir Excel çalışma sayfasına resim ekleyin. Android, C#, Go, Java, Node.js, Perl, PHP, Python, Ruby ve Swift için SDK’lar, platformlar arası entegrasyonu kolaylaştırır."
weight: 20
ArticleTitle: "Excel Çalışma Sayfasına Resim Ekleyin – Aspose.Cells Cloud API"
---

Bu REST API, bir Excel çalışma sayfasına yeni bir resim ekler.  
**Önkoşullar:** Geçerli bir Aspose Cloud kimlik doğrulama belirteci, desteklenen bir depolama ortamında bulunan mevcut bir hesap kitabınız ve çalışma sayfasını değiştirme yetkiniz olmalıdır.

## PutWorksheetAddPicture API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı    | Tür     | Konum | Açıklama                                                                                     |
| ---------------- | ------- | ----- | -------------------------------------------------------------------------------------------- |
| name             | string  | path  | Hesap kitabı adı.                                                                            |
| sheetName        | string  | path  | Çalışma sayfası adı.                                                                         |
| picture          | object  | body  | Resim nesnesi (ikili veri).                                                                  |
| upperLeftRow     | integer | query | Resmin yerleştirileceği sol üst köşe satırının sıfır tabanlı indeksi.                        |
| upperLeftColumn  | integer | query | Resmin yerleştirileceği sol üst köşe sütununun sıfır tabanlı indeksi.                        |
| lowerRightRow    | integer | query | Resim alanının sağ alt köşe satırının sıfır tabanlı indeksi.                                 |
| lowerRightColumn | integer | query | Resim alanının sağ alt köşe sütununun sıfır tabanlı indeksi.                                 |
| picturePath      | string  | query | Resim dosyasının yolu; atlanırsa, resim verisi istek gövdesinde sağlanmalıdır.               |
| folder           | string  | query | Hesap kitabının bulunduğu klasör.                                                            |
| storageName      | string  | query | Depolama hizmetinin adı.                                                                     |

**İstek Gövdesi Notu:** `picturePath` atlandığında, ikili resim verisini `multipart/form-data` kullanarak istek gövdesinde gönderin.

**HTTP Durum Kodları**

| Kod  | Anlam                       | Açıklama                                          |
|------|-----------------------------|--------------------------------------------------|
| 200  | Tamam                       | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir. |
| 400  | Hatalı İstek                | Eksik veya geçersiz parametreler (örn., desteklenmeyen dosya türü). |
| 401  | Yetkisiz                    | Geçersiz veya eksik JWT belirteci.               |
| 413  | Yük Çok Büyük               | Yüklenen dosya boyut sınırlarını aşıyor.         |
| 500  | Sunucu İç Hatası            | Beklenmeyen sunucu hatası.                       |

**Örnek 200 Yanıt Şeması**

```json
{
  "Code": 200,
  "Status": "OK",
  "PictureUrl": "https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pictures/1"
}
```

**Not:** Maksimum resim boyutu 10 MB’dır; daha büyük dosyalar `400 Bad Request` (Hatalı İstek) yanıtıyla reddedilir.

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Pictures/PutWorksheetAddPicture), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından yapmanızı sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye istek yapmayı göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.com/v1.1/cells/Sample_Test_Book.xls/worksheets/Sheet6/pictures?picturePath=aspose-cloud.png" \
  -X PUT \
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

## Bulut SDK’sı Ailesi

SDK kullanmak, geliştirme hızını en çok artıracak en iyi yoldur. SDK, düşük seviye ayrıntıları yöneterek size proje görevlerinize odaklanma imkanı sunar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web hizmetlerine istek yapmayı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetAddPicture.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetAddPicture.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetAddPicture.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetAddPicture.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82deb4189bc27ae92abf73c36b4df0" "Example_PutWorksheetAddPicture.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetAddPicture.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetAddPicture.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetAddPicture.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Not:** Desteklenen resim formatları şunlardır: PNG, JPEG, BMP ve GIF. Maksimum resim boyutu 10 MB’dır; daha büyük dosyalar `400 Bad Request` (Hatalı İstek) yanıtıyla reddedilir.