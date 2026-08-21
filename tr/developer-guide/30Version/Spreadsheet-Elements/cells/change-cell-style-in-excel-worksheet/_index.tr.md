---
title: "Excel Çalışma Sayfasında Hücre Stilini Değiştirme"
type: docs
url: /change-cell-style-in-excel-worksheet/
weight: 30
keywords:
  - Aspose.Cells
  - Aspose.Cells Cloud
  - Excel
  - Hücre Stili
  - REST API
  - Bulut SDK'sı
  - cURL
  - hücre stili güncelleme
  - Excel API
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasındaki belirli bir hücrenin stilini nasıl güncelleyeceğinizi öğrenin; örnek istekleri, yanıtları ve SDK kod parçacıklarını içerir."
ArticleTitle: "Excel Çalışma Sayfasında Hücre Stilini Değiştirme – Aspose.Cells Cloud API Kılavuzu"
---

Bu REST API, bir Excel dosyasının **hücre stili**ni günceller.

## PostUpdateWorksheetCellStyle API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellName}/style
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı | Tür   | Konum | Açıklama                                           |
|---------------|-------|-------|----------------------------------------------------|
| name          | string | path  | Çalışma kitabının dosya adı.                       |
| sheetName     | string | path  | Çalışma sayfasının adı.                            |
| cellName      | string | path  | Hedef hücre (örneğin **A1**).                      |
| style         | object | body  | Hücreye uygulanacak stil ayarlarını tanımlayan JSON nesnesi. |
| folder        | string | query | Çalışma kitabını içeren klasör.                    |
| storageName   | string | query | Çalışma kitabının saklandığı depo adı.             |

### **Yanıt**

```json
{
    "Status":"OK",
    "Code":200
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                           |
|-----|-----------------------------|----------------------------------------------------|
| 200 | Tamam (OK)                  | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Geçersiz İstek (Bad Request) | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Yetkisiz (Unauthorized)     | Geçersiz veya eksik JWT belirteci.                 |
| 413 | İçerik Çok Büyük (Payload Too Large) | Yüklenecek dosya boyut sınırını aşıyor.            |
| 500 | İç Sunucu Hatası (Internal Server Error) | Beklenmeyen sunucu hatası.                        |

## PostUpdateWorksheetCellStyle API'sini SDK'larla Nasıl Kullanılır

### PostUpdateWorksheetCellStyle API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Cells/PostUpdateWorksheetCellStyle), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için **cURL** komut satırı aracını kullanabilirsiniz. `<jwt token>` ifadesini, Aspose Cloud kimlik doğrulama uç noktasından elde edilen geçerli bir OAuth 2.0 erişim belirteciyle değiştirin.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test_cells.xlsx/worksheets/Sheet3/cells/A1/style" \
-d '{ "BackgroundThemeColor": { "ColorType": "Text2", "Tint": 1 } }' \
-X POST \
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
      "Color": { "A": 255, "R": 0, "G": 0, "B": 0 },
      "DoubleSize": 11,
      "IsBold": false,
      "IsItalic": false,
      "IsStrikeout": false,
      "IsSubscript": false,
      "IsSuperscript": false,
      "Name": "Calibri",
      "Size": 11,
      "Underline": "None"
    },
    "Name": null,
    "CultureCustom": null,
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
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "BottomBorder" },
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "DiagonalDown" },
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "DiagonalUp" },
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "Horizontal" },
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "LeftBorder" },
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "RightBorder" },
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "TopBorder" },
      { "LineStyle": "None", "Color": { "A": 255, "R": 0, "G": 0, "B": 0 }, "BorderType": "Vertical" }
    ],
    "BackgroundThemeColor": null,
    "ForegroundThemeColor": null,
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/test_cells.xlsx/worksheets/Sheet3/cells/A1/style",
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

### Aspose.Cells Cloud SDK'larını Kullanma

SDK kullanmak, API'ye karşı hızlıca geliştirme yapmanın en hızlı yoludur. SDK, düşük seviye detayları soyutlayarak iş mantığınıza odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, farklı SDK'lar kullanılarak Aspose.Cells web hizmetlerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUpdateWorksheetCellStyle.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUpdateWorksheetCellStyle.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUpdateWorksheetCellStyle.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUpdateWorksheetCellStyle.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUpdateWorksheetCellStyle.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUpdateWorksheetCellStyle.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUpdateWorksheetCellStyle.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUpdateWorksheetCellStyle.go" >}}

{{< /tab >}}

{{< /tabs >}}

**Ayrıca bakınız:**  
- [Hücre Stilini Al](https://docs.aspose.cloud/cells/get-cell-style/) – Bir hücrenin mevcut stilini alın.  
- [Birden Fazla Hücre Stilini Güncelle](https://docs.aspose.cloud/cells/update-multiple-cells-style/) – Tek bir istekte bir hücre aralığına stil uygulayın.  
---