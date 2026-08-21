---
title: "Aralık İçinde Sütun Genişliklerini Değiştirme"
ArticleTitle: "Aralık İçinde Sütun Genişliklerini Değiştirme – Aspose.Cells Cloud API"
second_title: "Belge"
linktitle: "Sütun genişliği"
type: docs
url: /ranges/update/column-width/
aliases: [/change-widths-of-columns-inside-the-range/]
keywords: "Aspose.Cells, sütun genişliği, REST API, Excel, SDK, aralık, bulut"
description: "Aspose.Cells Cloud REST API veya SDK’ları (C#, Java, Python vb.) kullanarak bir aralık içinde sütun genişliklerini nasıl değiştireceğinizi öğrenin. cURL, istek/yanıt ayrıntıları ve kimlik doğrulama adımları içerir."
weight: 74
---

Bu REST API, bir aralığın sütun genişliğini ayarlar.

## Güvenlik ve Kimlik Doğrulama
Aspose.Cells Cloud API’leri güvenlidir ve [JWT token tabanlı kimlik doğrulama](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) gerektirir.

## REST API

```bash
POST http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/columnWidth
```

**Önkoşullar** – Uç noktayı çağırmadan önce şunları yapmanız gerekir:

1. Bir Aspose Cloud hesabı oluşturun ve bir *istemci ID* ile *istemci gizli anahtarı* edinin.  
2. OAuth uç noktasını (`/connect/token`) çağırarak bir JWT token isteyin. Token, `access_token` alanında döndürülür.  
3. Hedef çalışma kitabını Aspose Cloud depo alanınıza yükleyin (veya zaten belirtilen klasörde mevcut olduğundan emin olun).  

İstek parametreleri aşağıdaki gibidir:

| Parametre Adı  | Tür     | Konum   | Açıklama                                      |
|----------------|---------|---------|-----------------------------------------------|
| name           | string  | path    | Çalışma kitabı dosyasının adı                  |
| sheetName      | string  | path    | Çalışma sayfasının adı                         |
| value          | number  | query   | İstenen sütun genişliği değeri                 |
| range          | object  | body    | Hedef hücreleri tanımlayan aralık nesnesi      |
| folder         | string  | query   | Çalışma kitabının depolandığı klasör yolu      |
| storageName    | string  | query   | Depolama hizmetinin adı                        |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeColumnWidth), herkese açık erişilebilir bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’ye nasıl istek yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

<h3 id="request">İstek</h3>

```bash
# *test.xlsx* adlı çalışma kitabının,
# *Sheet1* adlı çalışma sayfasının seçili sütunlarının genişliğini 20 punto olarak ayarlamak için sütun genişliği uç noktasını çağırın.
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/columnWidth?value=20" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "ColumnCount": 7,
        "ColumnWidth": 19,
        "FirstColumn": 0,
        "FirstRow": 9,
        "Name": "string",
        "RefersTo": "string",
        "RowCount": 1,
        "RowHeight": 15,
        "Worksheet": "Sheet1"
      }'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

<h3 id="response">Yanıt</h3>

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*Olası hata yanıtları*  

| HTTP Kodu | Açıklama                                  |
|-----------|-------------------------------------------|
| 400       | Hatalı İstek – geçersiz JSON veya parametreler |
| 401       | Yetkisiz – eksik veya geçersiz token      |
| 404       | Bulunamadı – çalışma kitabı veya çalışma sayfası eksik |

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Ailesi
Bir SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. Bir SDK, düşük seviye detayları yöneterek size proje görevlerinize odaklanma imkanı sunar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerini çeşitli SDK’lar kullanarak nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeColumnWidth.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeColumnWidth.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeColumnWidth.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeColumnWidth.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeColumnWidth.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeColumnWidth.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeColumnWidth.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeColumnWidth.go" >}}

{{< /tab >}}

{{< /tabs >}}

## SSS

**S:** *Bir Excel çalışma kitabında bir aralığın sütun genişliğini ayarlamak için hangi uç noktayı çağırırım?*  
**C:** `POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/columnWidth` (burada `{name}` çalışma kitabı dosya adıdır ve `{sheetName}` hedef çalışma sayfasıdır).

**S:** *Sütun genişliği API’sini kullanırken isteği nasıl kimlik doğrularım?*  
**C:** `Authorization: Bearer <jwt token>` başlığını ekleyin. JWT token’ı, istemci ID ve istemci gizli anahtarınızla Aspose Cloud OAuth akışı (`/connect/token`) aracılığıyla edinin.

**S:** *Sütun A’dan C’ye kadar olan genişliği 25 punto yapmak için hangi JSON gövdesini göndermeliyim?*  
**C:**  

```json
{
  "FirstColumn": 0,
  "ColumnCount": 3,
  "FirstRow": 0,
  "RowCount": 1
}
```

İsteğe URL’ye `value=25` sorgu parametresini ekleyin.