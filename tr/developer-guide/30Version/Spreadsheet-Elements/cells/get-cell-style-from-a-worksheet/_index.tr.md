---
title: "Bir Çalışma Sayfasından Hücre Stilini Al – Aspose.Cells Cloud API"
type: docs
url: /tr/get-cell-style-from-a-worksheet/
weight: 10
keywords: "Aspose.Cells, Excel, REST API, hücre stili, elektronik tablo, bulut SDK, API dokümantasyonu"
description: "Aspose.Cells Cloud REST API v3 kullanarak bir Excel çalışma sayfasındaki belirli bir hücrenin stilini nasıl alacağınızı öğrenin. cURL örneği, yanıt şeması, durum kodları ve SDK snippet’leri içerir."
ArticleTitle: "Aspose.Cells Cloud API ile Bir Çalışma Sayfasından Hücre Stilini Al – Detaylı Kılavuz"
---

Bu REST API’yi, bir Excel çalışma sayfasındaki bir hücrenin **stilini** almak için kullanın.

## GetWorksheetCellStyle API

```http
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/style
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri


| Parametre Adı | Tür     | Konum  | Açıklama                                |
| ------------- | ------- | ------ | --------------------------------------- |
| name          | string  | path   | Excel belgesinin adı.                   |
| sheetName     | string  | path   | Çalışma sayfasının adı.                 |
| cellName      | string  | path   | Hücrenin adresi (örneğin, A1).          |
| folder        | string  | query  | Dosyayı içeren klasör.                  |
| storageName   | string  | query  | Kullanılacak depo adı.                 |


### **Yanıt**

```json
{
  "Style": {
    "Font": {
      "Color": { "A": 255, "R": 5, "G": 99, "B": 193 },
      "DoubleSize": 11,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Calibri",
      "Size": 11,
      "Underline": "Single"
    },
    "Name": null,
    "CultureCustom": "General",
    "Custom": "",
    "BackgroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "ForegroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "IsFormulaHidden": false,
    "IsDateTime": false,
    "IsTextWrapped": false,
    "IsGradient": false,
    "IsLocked": true,
    "IsPercent": false,
    "ShrinkToFit": false,
    "IndentLevel": 0,
    "Number": 0,
    "RotationAngle": 0,
    "Pattern": "None",
    "TextDirection": "Context",
    "VerticalAlignment": "Bottom",
    "HorizontalAlignment": "General",
    "BorderCollection": [
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "BottomBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalDown"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalUp"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Horizontal"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "LeftBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "RightBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "TopBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Vertical"
      }
    ],
    "BackgroundThemeColor": null,
    "ForegroundThemeColor": null,
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/cells/a1/style",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

**HTTP Durum Kodları**

| Kod  | Anlamı                      | Açıklama                                                   |
|------|-----------------------------|------------------------------------------------------------|
| 200  | OK (Tamam)                  | Filtre başarıyla uygulandı; yanıt, işlem ayrıntılarını içerir. |
| 400  | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401  | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci.                         |
| 413  | Payload Too Large (Çok Büyük Yük) | Yüklenen dosya boyut sınırlarını aşıyor.                 |
| 500  | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası.                             |

**Hata Yanıtları**  
Bu uç nokta için tipik hata yükleri, standart Aspose.Cells hata formatını izler. Örneğin, 400 Bad Request şu şekilde döner:

```json
{
  "Code": 400,
  "Message": "Invalid parameter 'cellName'.",
  "Description": "The cell name provided is not in a valid A1 format."
}
```

Benzer şekilde, 401 Unauthorized şu şekilde döner:

```json
{
  "Code": 401,
  "Message": "Authentication failed.",
  "Description": "The JWT token is missing or invalid."
}
```

## GetWorksheetCellStyle API'yi SDK’larla Nasıl Kullanırsınız?

### GetWorksheetCellStyle API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCellStyle), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’ye bir çağrı nasıl yapılacağını gösterir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/a1/style" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Style": {
    "Font": {
      "Color": { "A": 255, "R": 5, "G": 99, "B": 193 },
      "DoubleSize": 11,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Calibri",
      "Size": 11,
      "Underline": "Single"
    },
    "Name": null,
    "CultureCustom": "General",
    "Custom": "",
    "BackgroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "ForegroundColor": { "A": 0, "R": 0, "G": 0, "B": 0 },
    "IsFormulaHidden": false,
    "IsDateTime": false,
    "IsTextWrapped": false,
    "IsGradient": false,
    "IsLocked": true,
    "IsPercent": false,
    "ShrinkToFit": false,
    "IndentLevel": 0,
    "Number": 0,
    "RotationAngle": 0,
    "Pattern": "None",
    "TextDirection": "Context",
    "VerticalAlignment": "Bottom",
    "HorizontalAlignment": "General",
    "BorderCollection": [
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "BottomBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalDown"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "DiagonalUp"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Horizontal"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "LeftBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "RightBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "TopBorder"
      },
      {
        "LineStyle": "None",
        "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
        "BorderType": "Vertical"
      }
    ],
    "BackgroundThemeColor": null,
    "ForegroundThemeColor": null,
    "link": {
      "Href": "/test.xlsx/worksheets/Sheet1/cells/a1/style",
      "Rel": "self",
      "Title": null,
      "Type": null
    }
  },
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Yanıt Şeması

| Alan                     | Tür     | Açıklama                                                       |
| ------------------------ | ------- | -------------------------------------------------------------- |
| **Style**                | object  | Hücrenin tüm stil ile ilgili özelliklerini içeren kapsayıcı.  |
| Style.Font               | object  | Yazı tipi ayarları (ad, boyut, renk, stil bayrakları).         |
| Style.Font.Color         | object  | Yazı tipi için RGBA renk değerleri.                             |
| Style.Font.IsBold        | boolean | Yazı tipi kalın ise `true`.                                     |
| Style.Font.IsItalic      | boolean | Yazı tipi italik ise `true`.                                    |
| Style.Font.IsStrikeout   | boolean | Yazı tipinde üstü çizili varsa `true`.                          |
| Style.Font.IsSubscript   | boolean | Yazı tipi alt simge ise `true`.                                 |
| Style.Font.IsSuperscript | boolean | Yazı tipi üst simge ise `true`.                                 |
| Style.Font.Name          | string  | Yazı tipi ailesi adı (örneğin, **Calibri**).                   |
| Style.Font.Size          | number  | Yazı tipi boyutu (nokta cinsinden).                             |
| Style.Font.Underline     | string  | Alt çizgi stili (örneğin, **Single**).                         |
| Style.IsLocked           | boolean | Hücrenin düzenlemeye karşı korunup korunmadığını gösterir.       |
| Style.IsTextWrapped      | boolean | Metin kaydırma etkinse `true`.                                  |
| Style.IsGradient         | boolean | Gradyan dolgu uygulanmışsa `true`.                              |
| Style.Pattern            | string  | Doldurma deseni adı (örneğin, **None**).                        |
| Style.BorderCollection   | array   | Çizgi stili, renk ve kenarlık türünü tanımlayan kenarlık nesneleri listesi. |
| Style.BackgroundColor    | object  | Hücre arka planı için RGBA değerleri.                           |
| Style.ForegroundColor    | object  | Hücre ön planı için RGBA değerleri.                             |
| …                        | …       | _(Diğer alanlar, API referansında tanımlananla aynı deseni izler.)_ |

### Aspose.Cells Cloud SDK’larını Kullanın

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. SDK, düşük seviye detayları işler; böylece projenizin görevlerine odaklanabilirsiniz. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’ları kullanarak Aspose.Cells web servislerine nasıl çağrı yapılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellStyle.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellStyle.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellStyle.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellStyle.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellStyle.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellStyle.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellStyle.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellStyle.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Ayrıca Bakınız**  
- [Hücre Stilini Ayarla](https://apireference.aspose.cloud/cells/#/Cells/SetWorksheetCellStyle)  
- [Hücre Değerini Al](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell)
---