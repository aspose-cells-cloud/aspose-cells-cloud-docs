---
title: "Bir Excel Çalışma Sayfasında Bağlantıyı Güncelle – Aspose.Cells Cloud API Kılavuzu"
description: "Aspose.Cells Cloud REST API'sini (v3.0) kullanarak bir Excel çalışma sayfasındaki bir bağlantıyı nasıl güncelleyeceğinizi öğrenin. Uç nokta, parametreler, istek gövdesi şeması, cURL örneği, SDK kod parçacıkları, hata işleme, hız sınırlama ve ön koşullar içerir."
keywords:
  - "Aspose.Cells"
  - "bağlantı güncelleme"
  - "Excel API"
  - "REST API"
  - "bulut çalışma tablosu"
  - "v3.0"
weight: 30
aliases:
  - /hyperlinks/update/
  - /update-hyperlinks-in-excel-worksheet/
---

# Bir Excel Çalışma Sayfasında Bağlantıyı Güncelle  

**API sürümü:** v3.0  

**PostWorksheetHyperlink** işlemi, sıfır tabanlı diziniyle belirtilen bir çalışma sayfasındaki mevcut bir bağlantıyı günceller.

---

## İçindekiler
1. [Ön Koşullar](#ön-koşullar)  
2. [Hız Sınırlama](#hız-sınırlama)  
3. [Uç Nokta](#uç-nokta)  
4. [Parametreler](#parametreler)  
   - [Yol parametreleri](#yol-parametreleri)  
   - [Sorgu parametreleri](#sorgu-parametreleri)  
   - [İstek gövdesi şeması](#istek-gövdesi-şeması)  
5. [Yanıtlar](#yanıtlar)  
   - [Başarılı](#başarılı-yanıt)  
   - [Hata yanıtları](#hata-yanıtları)  
6. [cURL Örneği](#curl-örneği)  
7. [SDK Kod Parçacıkları](#sdk-kod-parçacıkları)  
8. [Ayrıca Bkz.](#ayrıca-bkz.)  

---

## Ön Koşullar <a name="ön-koşullar"></a>

| Gereksinim | Açıklama |
|------------|----------|
| **Kimlik Doğrulama** | JWT belirteci tabanlı kimlik doğrulama. Belirteci almak için [Kimlik Doğrulama Kılavuzu](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) sayfasını inceleyin. |
| **Depolama** | Çalışma kitabının desteklenen bir Aspose Cloud deposunda saklanmalıdır (varsayılan: **Default**). |
| **İzinler** | JWT belirtecinin hedef çalışma kitabını okuma ve yazma iznine sahip olması gerekir. |
| **Üst Bilgiler** | Tüm istekler için `Content-Type: application/json` ve `Accept: application/json` üst bilgileri gereklidir. |

---

## Hız Sınırlama <a name="hız-sınırlama"></a>

Aspose.Cells Cloud, **her erişim belirteci başına maksimum 60 istek/dakika** sınırını uygular. Bu sınıra aşılması durumunda HTTP **429 Too Many Requests** (Çok Fazla İstek) hatası döndürülür. Sıkıştırma durumunda üstel geri dönüş stratejisi uygulayın veya `Retry-After` üstbilgisine uyun.

---

## Uç Nokta <a name="uç-nokta"></a>

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/hyperlinks/{hyperlinkIndex}
```

*`name` dosyasının `sheetName` çalışma sayfasındaki `hyperlinkIndex` dizinli bağlantıyı günceller.*

---

## Parametreler <a name="parametreler"></a>

### Yol parametreleri <a name="yol-parametreleri"></a>

| Ad              | Tür    | Gerekli | Açıklama |
|-----------------|--------|---------|----------|
| `name`          | string | ✅ | Excel dosyasının adı (uzantısı dahil). |
| `sheetName`     | string | ✅ | Bağlantının bulunduğu çalışma sayfasının adı. |
| `hyperlinkIndex`| integer| ✅ | Güncellenecek bağlantının sıfır tabanlı dizini. |

### Sorgu parametreleri <a name="sorgu-parametreleri"></a>

| Ad             | Tür    | Gerekli | Açıklama |
|----------------|--------|---------|----------|
| `folder`       | string | ❌ | Çalışma kitabının bulunduğu deponun klasör yolu. |
| `storageName`  | string | ❌ | Depolama hizmetinin adı (örneğin, `Default`). |

### İstek gövdesi şeması <a name="istek-gövdesi-şeması"></a>

İstek gövdesi bir **`hyperlink`** nesnesi içermelidir. Değiştirmek istediğiniz alanları sağlamanız yeterlidir; atlanan isteğe bağlı alanlar mevcut değerlerini korur.

| Alan          | Tür    | Gerekli | Açıklama |
|---------------|--------|---------|----------|
| `Address`     | string | ✅ | Bağlantının hedef URL'si. |
| `Area`        | object | ✅ | Bağlantının yerleştirildiği hücre aralığı. `StartRow`, `StartColumn`, `EndRow`, `EndColumn` (tümü tamsayı, sıfır tabanlı) içermelidir. |
| `ScreenTip`   | string | ❌ | Fare imleci üzerine getirildiğinde gösterilen araç ipucu metni. |
| `TextToDisplay`| string| ❌ | Hücre içinde gösterilen metin. |
| `link`        | object| ❌ | Hiperlink bağlantıları (`Href`, `Rel`, `Title`, `Type`). Genellikle istek yüklerinde atlanır. |

**`Area` nesne tanımı**

| Alt Alan      | Tür    | Gerekli | Açıklama |
|---------------|--------|---------|----------|
| `StartRow`    | integer| ✅ | Sıfır tabanlı başlangıç satır dizini. |
| `StartColumn` | integer| ✅ | Sıfır tabanlı başlangıç sütun dizini. |
| `EndRow`      | integer| ✅ | Sıfır tabanlı bitiş satır dizini. |
| `EndColumn`   | integer| ✅ | Sıfır tabanlı bitiş sütun dizini. |

---

## Yanıtlar <a name="yanıtlar"></a>

### Başarılı yanıt <a name="başarılı-yanıt"></a>

| Alan    | Tür    | Açıklama |
|---------|--------|----------|
| `Code`  | integer| HTTP durum kodu (başarı için 200). |
| `Status`| string | Metinsel durum (`OK`). |
| `Hyperlink`| object (isteğe bağlı) | `link` alt nesnesi istendiğinde döndürülen güncellenmiş bağlantı nesnesi. |

**Örnek JSON**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

### Hata yanıtları <a name="hata-yanıtları"></a>

| HTTP Kodu | Neden | Örnek Gövde |
|-----------|-------|-------------|
| **400** | Hatalı İstek – eksik veya geçersiz parametreler. | `{ "Code":"400", "Message":"Geçersiz parametre değeri." }` |
| **401** | Yetkisiz – eksik veya geçersiz JWT belirteci. | `{ "Code":"401", "Message":"Erişim belirteci eksik veya geçersiz." }` |
| **404** | Bulunamadı – çalışma kitabısı, çalışma sayfası veya bağlantı mevcut değil. | `{ "Code":"404", "Message":"Dosya bulunamadı." }` |
| **429** | Çok Fazla İstek – hız sınırı aşıldı. | `{ "Code":"429", "Message":"İstek sınırı aşıldı. Daha sonra tekrar deneyin." }` |
| **500** | İç Sunucu Hatası – beklenmeyen sunucu hatası. | `{ "Code":"500", "Message":"Beklenmeyen bir hata oluştu." }` |

---

## cURL Örneği <a name="curl-örneği"></a>

```bash
curl -L -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/hyperlinks/1" \
  -H "Authorization: Bearer <YOUR_JWT_TOKEN>" \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -d '{
        "hyperlink": {
          "Address": "https://www.msnbc.com/",
          "Area": {
            "StartRow": 1,
            "StartColumn": 6,
            "EndRow": 1,
            "EndColumn": 6
          },
          "ScreenTip": "MSNBC ana sayfa",
          "TextToDisplay": "MSNBC"
        },
        "folder": "samples",
        "storageName": "Default"
      }'
```

**Yanıt**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

*İpucu:* JSON yükünü bir dosyaya (örneğin `payload.json`) kaydedip temiz kopyalama/yapıştırma için `--data @payload.json` kullanın.

---

## SDK Kod Parçacıkları <a name="sdk-kod-parçacıkları"></a>

Aşağıdaki kod parçacıkları, resmi Aspose.Cells Cloud SDK’larını kullanarak **PostWorksheetHyperlink** işlemini nasıl çağıracağınızı göstermektedir. Yer tutucu değerleri (`<YOUR_JWT_TOKEN>`, `<FILE_NAME>` vb.) gerçek verilerle değiştirin.

| Dil | Örnek |
|-----|-------|
| **C#** | ```csharp\nvar api = new CellsApi("<client_id>", "<client_secret>");\nvar hyperlink = new Hyperlink {\n    Address = \"https://www.msnbc.com/\",\n    Area = new LinkArea { StartRow = 1, StartColumn = 6, EndRow = 1, EndColumn = 6 },\n    ScreenTip = \"MSNBC ana sayfa\",\n    TextToDisplay = \"MSNBC\"\n};\nvar response = api.PostWorksheetHyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, folder: \"samples\");\n``` |
| **Java** | ```java\nCellsApi api = new CellsApi(clientId, clientSecret);\nHyperlink hyperlink = new Hyperlink();\nhyperlink.setAddress(\"https://www.msnbc.com/\");\nLinkArea area = new LinkArea();\narea.setStartRow(1);\narea.setStartColumn(6);\narea.setEndRow(1);\narea.setEndColumn(6);\nhyperlink.setArea(area);\nhyperlink.setScreenTip(\"MSNBC ana sayfa\");\nhyperlink.setTextToDisplay(\"MSNBC\");\nCellsCloudResponse resp = api.postWorksheetHyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, \"samples\", null);\n``` |
| **Python** | ```python\nimport asposecellscloud\nfrom asposecellscloud.apis.cells_api import CellsApi\napi = CellsApi(client_id, client_secret)\nhyperlink = asposecellscloud.models.Hyperlink(\n    address=\"https://www.msnbc.com/\",\n    area=asposecellscloud.models.LinkArea(start_row=1, start_column=6, end_row=1, end_column=6),\n    screen_tip=\"MSNBC ana sayfa\",\n    text_to_display=\"MSNBC\"\n)\nresponse = api.post_worksheet_hyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, folder=\"samples\")\n``` |
| **Node.js** | ```javascript\nconst { CellsApi, Hyperlink, LinkArea } = require('asposecellscloud');\nconst api = new CellsApi(clientId, clientSecret);\nlet hyperlink = new Hyperlink({\n  address: 'https://www.msnbc.com/',\n  area: new LinkArea({ startRow: 1, startColumn: 6, endRow: 1, endColumn: 6 }),\n  screenTip: 'MSNBC ana sayfa',\n  textToDisplay: 'MSNBC'\n});\napi.postWorksheetHyperlink('test.xlsx', 'Sheet1', 1, hyperlink, { folder: 'samples' })\n  .then(resp => console.log(resp));\n``` |
| **Go** | ```go\nimport (\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3\"\n    \"github.com/asposecellscloud/aspose-cells-cloud-go/v3/api\"\n)\nclient := api.NewCellsApiClient(clientId, clientSecret)\narea := asposecellscloud.LinkArea{StartRow: 1, StartColumn: 6, EndRow: 1, EndColumn: 6}\nhyperlink := asposecellscloud.Hyperlink{Address: \"https://www.msnbc.com/\", Area: &area, ScreenTip: \"MSNBC ana sayfa\", TextToDisplay: \"MSNBC\"}\nresp, _ := client.PostWorksheetHyperlink(\"test.xlsx\", \"Sheet1\", 1, hyperlink, \"samples\", \"\")\nfmt.Println(resp)\n``` |
| **PHP** | ```php\n<?php\nrequire_once('vendor/autoload.php');\nuse Aspose\Cells\CellsApi;\n$api = new CellsApi($clientId, $clientSecret);\n$hyperlink = new \\Aspose\\Cells\\Model\\Hyperlink();\n$hyperlink->setAddress('https://www.msnbc.com/');\n$area = new \\Aspose\\Cells\\Model\\LinkArea();\n$area->setStartRow(1);\n$area->setStartColumn(6);\n$area->setEndRow(1);\n$area->setEndColumn(6);\n$hyperlink->setArea($area);\n$hyperlink->setScreenTip('MSNBC ana sayfa');\n$hyperlink->setTextToDisplay('MSNBC');\n$response = $api->postWorksheetHyperlink('test.xlsx', 'Sheet1', 1, $hyperlink, 'samples');\nprint_r($response);\n?>\n``` |
| **Ruby** | ```ruby\nrequire 'aspose_cells_cloud'\napi = AsposeCellsCloud::CellsApi.new(client_id: CLIENT_ID, client_secret: CLIENT_SECRET)\nhyperlink = AsposeCellsCloud::Hyperlink.new(\n  address: 'https://www.msnbc.com/',\n  area: AsposeCellsCloud::LinkArea.new(start_row: 1, start_column: 6, end_row: 1, end_column: 6),\n  screen_tip: 'MSNBC ana sayfa',\n  text_to_display: 'MSNBC'\n)\nresult = api.post_worksheet_hyperlink('test.xlsx', 'Sheet1', 1, hyperlink, folder: 'samples')\nputs result\n``` |
| **Perl** | ```perl\nuse AsposeCellsCloud::CellsApi;\nmy $api = AsposeCellsCloud::CellsApi->new(client_id => $client_id, client_secret => $client_secret);\nmy $area = AsposeCellsCloud::LinkArea->new(startRow => 1, startColumn => 6, endRow => 1, endColumn => 6);\nmy $hyperlink = AsposeCellsCloud::Hyperlink->new(address => 'https://www.msnbc.com/', area => $area, screenTip => 'MSNBC ana sayfa', textToDisplay => 'MSNBC');\nmy $resp = $api->post_worksheet_hyperlink(name=>'test.xlsx', sheetName=>'Sheet1', hyperlinkIndex=>1, hyperlink=>$hyperlink, folder=>'samples');\nprint $resp->{Code}, \" \", $resp->{Status}, \"\\n\";\n``` |

*Tüm SDK’lar açık kaynaklıdır ve [Aspose.Cells Cloud GitHub deposunda](https://github.com/aspose-cells-cloud) bulunabilir.*

---

## Ayrıca Bkz. <a name="ayrıca-bkz."></a>

- **Kimlik Doğrulama** – [JWT belirteçleri ile başlangıç](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/)  
- **Depolama işlemleri** – [Bir dosya yükleme](https://apireference.aspose.cloud/cells/#/Storage/UploadFile)  
- **Diğer bağlantı işlemleri** – [Bağlantı ekleme](https://apireference.aspose.cloud/cells/#/Hyperlinks/PostWorksheetHyperlink) | [Bağlantı silme](https://apireference.aspose.cloud/cells/#/Hyperlinks/DeleteWorksheetHyperlink)  
- **OpenAPI Spesifikasyonu** – Uç noktanın tam tanımı: <https://apireference.aspose.cloud/cells/#/Hyperlinks/PostWorksheetHyperlink>  

--- 

*Belge son güncelleme tarihi: 2026‑07‑30*