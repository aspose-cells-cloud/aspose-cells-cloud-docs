---
title: "Bir Excel Çalışma Sayfasında bir OLE Nesnesini Güncelleme"
second_title: "Belge"
linktitle: "Güncelle"
type: docs
url: /oleobjects/update/
aliases: [/update-a-specific-oleobject-from-excel-worksheet/]
keywords: "OLE nesnesini güncelle, Excel, Aspose.Cells Cloud, REST API, SDK"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasında bir OLE nesnesini (resim, grafik vb.) nasıl güncelleyeceğinizi öğrenin. cURL, SDK örnekleri, kimlik doğrulama adımları ve hata işleme içerir."
weight: 30
author: "Aspose Cloud Dokümantasyon Ekibi"
lastmod: "2024-03-01"
ArticleTitle: "Bir Excel Çalışma Sayfasında bir OLE Nesnesini Güncelleme – Aspose.Cells Cloud API Kılavuzu"
---

Bu REST API, bir Excel çalışma sayfasındaki bir **OLE nesnesini** günceller.

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

## PostUpdateWorksheetOleObject API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects/{oleObjectIndex}
```

İstek parametreleri:

| Parametre Adı | Tür      | Parametre Konumu | Açıklama                                             |
| ------------- | -------- | ---------------- | ---------------------------------------------------- |
| name          | string   | path             | Çalışma kitabının adı.                               |
| sheetName     | string   | path             | Çalışma sayfasının adı.                              |
| oleObjectIndex| integer  | path             | Çalışma sayfası içindeki OLE nesnesinin indeksi.    |
| ole           | object   | body             | Güncellenecek OLE nesnesinin JSON gösterimi.         |
| folder        | string   | query            | Çalışma kitabını içeren klasör.                      |
| storageName   | string   | query            | Depolama hizmetinin adı.                             |

### İstek Gövdesi Alanları

| Alan                  | Tür      | Gerekli    | Açıklama                                                   |
| --------------------- | -------- | ---------- | ---------------------------------------------------------- |
| ImageSourceFullName   | string   | isteğe bağlı | OLE nesnesi için kullanılan resim dosyasının yolu.          |
| IsAutoSize            | boolean  | isteğe bağlı | OLE nesnesinin otomatik boyutlandırılıp olmayacağını belirtir. |
| SourceFullName        | string   | gerekli    | OLE nesnesinin kaynağı (örneğin bir resim veya grafik).     |
| UpperLeftRow          | integer  | gerekli    | Üst sol köşenin satır indeksi (sıfır tabanlı).             |
| UpperLeftColumn       | integer  | gerekli    | Üst sol köşenin sütun indeksi (sıfır tabanlı).             |
| Left                  | integer  | isteğe bağlı | Üst sol köşeden yatay ofset, nokta cinsinden.               |
| Top                   | integer  | isteğe bağlı | Üst sol köşeden dikey ofset, nokta cinsinden.               |
| Width                 | integer  | gerekli    | OLE nesnesinin genişliği, nokta cinsinden.                  |
| Height                | integer  | gerekli    | OLE nesnesinin yüksekliği, nokta cinsinden.                 |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/OleObjects/PostUpdateWorksheetOleObject), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'sini nasıl çağıracağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/" \
  -X POST \
  -d '{"ImageSourceFullName":"aspose-logo.png","IsAutoSize":true,"SourceFullName":"Sample_Book2.xls","UpperLeftRow":15,"Top":10,"UpperLeftColumn":5,"Left":10,"Width":400,"Height":400}' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK",
  "OLEObject": {
    "Index": 0,
    "ImageSourceFullName": "aspose-logo.png",
    "IsAutoSize": true,
    "SourceFullName": "Sample_Book2.xls",
    "UpperLeftRow": 15,
    "UpperLeftColumn": 5,
    "Left": 10,
    "Top": 10,
    "Width": 400,
    "Height": 400
  }
}
```

{{< /tab >}}

{{< /tabs >}}

## Hata Yanıtları

| HTTP Durumu | Kod  | Mesaj                                                          |
| ----------- | ---- | -------------------------------------------------------------- |
| 400         | 4000 | Geçersiz istek – eksik veya geçersiz parametreler.             |
| 401         | 4010 | Yetkisiz erişim – geçersiz veya eksik JWT belirteci.           |
| 404         | 4040 | Bulunamadı – çalışma kitabında, çalışma sayfasında veya OLE nesnesinde hata var. |
| 500         | 5000 | İç sunucu hatası – sunucu tarafında beklenmedik bir arıza.      |

API ayrıca yanıt gövdesinde HTTP durumuna karşılık gelen özel bir **Code** alanını da döndürür (örneğin, 200 → 2000, 400 → 4000 vb.).

## Bu API Ne Zaman Kullanılmalı?

Mevcut bir OLE nesnesini (gömülü resim, grafik veya belge gibi) tüm çalışma sayfasını yeniden yüklemeksizin değiştirmeniz gerektiğinde bu uç noktayı kullanın. Tipik senaryolar, resim kaynağını güncellemek, nesneyi yeniden boyutlandırmak veya çalışma kitabı oluşturulduktan sonra konumunu değiştirmek içerir. İlgili işlemler için bkz. [OLE Nesnesi Ekle](/oleobjects/add/) ve [OLE Nesnesi Sil](/oleobjects/delete/).

## Bulut SDK Ailesi

SDK kullanmak, geliştirme yapmanın en hızlı yoludur. SDK, alt seviye ayrıntıları soyutlar, böylece projenize odaklanabilirsiniz. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıda, Aspose.Cells Cloud SDK kullanarak bir OLE nesnesini güncelleyen kısa bir C# örneği verilmiştir:

```csharp
using Aspose.Cells.Cloud.SDK.Api;
using Aspose.Cells.Cloud.SDK.Model;

var config = new Configuration
{
    AppSid = "<your-app-sid>",
    AppKey = "<your-app-key>"
};
var oleApi = new OleObjectsApi(config);
var request = new OleObjectUpdateRequest
{
    ImageSourceFullName = "aspose-logo.png",
    IsAutoSize = true,
    SourceFullName = "Sample_Book2.xls",
    UpperLeftRow = 15,
    UpperLeftColumn = 5,
    Left = 10,
    Top = 10,
    Width = 400,
    Height = 400
};

var response = oleApi.UpdateWorksheetOleObject("SampleBook.xlsx", "Sheet1", 0, request, folder: "myFolder");
Console.WriteLine($"Durum: {response.Status}");
```

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerini çeşitli SDK'lar kullanarak nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUpdateWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUpdateWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUpdateWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUpdateWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUpdateWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUpdateWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUpdateWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUpdateWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}