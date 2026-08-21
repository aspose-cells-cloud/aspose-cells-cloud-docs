---
title: "Aspose.Cells Cloud API – CellsObjectOperate Görevi ile Çalışma (REST)"
second_title: "Belge"
type: docs
url: /tasks/cells-object-operate/
aliases: [/working-with-cellsobjectoperate-task/]
description: "Aspose.Cells Cloud API’de CellsObjectOperate görevini nasıl kullanacağınızı öğrenin; parametre referansları, istek/yanıt örnekleri ve çalışma kitapları, grafikler ve dönüştürme tabloları için en iyi uygulama ipuçları."
weight: 20
ArticleTitle: "Aspose.Cells Cloud API – CellsObjectOperate Görevi ile Çalışma (REST)"
keywords:
  - "Aspose CellsObjectOperate"
  - "CellsObjectOperate görevi"
  - "Aspose.Cells Cloud API"
  - "Excel REST API"
  - "grafik işlemi"
  - "dönüştürme tablosu API"
  - "sayfa sonu API"
---

**Genel Bakış**  
**CellsObjectOperate** görevi, tek bir REST çağrısı ile çalışma kitapları, çalışma sayfaları, grafikler, dönüştürme tabloları, şekiller, sayfa sonları ve daha fazlası gibi Excel nesneleri üzerinde oluşturma, okuma, güncelleme ve silme (CRUD) işlemlerini gerçekleştirmenizi sağlar. `OperateObjectType` ile nesne türünü belirtin ve karşılık gelen parametre bloğunu sağlayın (örneğin, grafikle ilgili işlemler için `ChartOperateParameter`).

---

**OperateObject**

| Parametre Adı         | Tür   | Açıklama |
| --------------------- | ----- | -------- |
| OperateObjectType     | string | İşlem yapılacak Excel nesnesinin türü. İzin verilen değerler: `Workbook`, `Worksheet`, `PageSetup`, `Cells`, `Chart`, `Shape`, `ListObject`, `PivotTable`, `WorkbookSettings`, `PageBreak`. |
| OperateObjectPosition | object | Hedef nesnenin konumunu belirleyen kapsayıcıdır (örneğin, çalışma kitabının adı, çalışma sayfasının adı, grafik dizini). Çoğu işlem için gerekli. |

**OperateObjectPosition**

| Parametre Adı      | Tür     | Açıklama |
| ------------------ | ------- | -------- |
| Workbook           | object  | Hedef nesneyi içeren çalışma kitabı. `FileName` (bulut depolama) veya `FileContent` (base‑64 kodlu) değerlerinden birini içermelidir. |
| SheetName          | string  | İşlemin uygulanacağı çalışma sayfasının adı. Çalışma sayfası düzeyindeki nesneler (grafikler, şekiller vb.) için gerekli. |
| ChartIndex         | integer | Çalışma sayfası içindeki grafiğin sıfır tabanlı dizini (`OperateObjectType` `Chart` olduğunda kullanılır). |
| ShapeIndex         | integer | Çalışma sayfası içindeki şeklin sıfır tabanlı dizini (`OperateObjectType` `Shape` olduğunda kullanılır). |
| CellName           | string  | A1 stili hücre başvurusu (örneğin, `A1`). Hücre düzeyindeki işlemler için kullanılır. |
| ListObjectIndex    | integer | Liste nesnesinin (tablo) sıfır tabanlı dizini (`OperateObjectType` `ListObject` olduğunda kullanılır). |

**ChartOperateParameter**

| Parametre Adı         | Tür    | Açıklama |
| --------------------- | ------ | -------- |
| ChartIndex            | integer | Düzenlenecek grafiğin dizini. Mevcut bir grafiği güncellerken gerekli. |
| ChartType             | string  | Oluşturulacak grafik türü (örneğin, `Bar`, `Line`, `Pie`). |
| UpperLeftRow          | integer | Grafiğin sol üst köşesinin satır numarası (sıfır tabanlı). |
| UpperLeftColumn       | integer | Grafiğin sol üst köşesinin sütun numarası (sıfır tabanlı). |
| LowerRightRow         | integer | Grafiğin sağ alt köşesinin satır numarası. |
| LowerRightColumn      | integer | Grafiğin sağ alt köşesinin sütun numarası. |
| Area                  | string  | Grafiğin veri aralığı (örneğin, `A1:B5`). |
| IsVertical            | string  | Grafiğin yönü dikeyse `true`; aksi halde `false`. |
| CategoryData          | string  | Kategori (X eksen) etiketlerini sağlayan aralık. |
| IsAutoGetSerialName   | string  | Seri adlarını otomatik oluşturmak için `true`; özel adları kullanmak için `false`. |
| Title                 | string  | Grafiğe görüntülenecek başlık metni. |

**ListObjectOperateParameter**

| Parametre Adı | Tür    | Açıklama |
| ------------- | ------ | -------- |
| ListObject    | object | Liste (tablo) işlemi için yapılandırma nesnesi. `ShowHeader`, `ShowTotal`, `Style` gibi özellikler içerir. |

**PageBreakOperateParameter**

| Parametre Adı | Tür     | Açıklama |
| ------------- | ------- | -------- |
| PageBreakType | string  | Sayfa sonu türü (`Horizontal` veya `Vertical`). |
| Index         | integer | Silinecek veya değiştirilecek sayfa sonunun sıfır tabanlı dizini. |
| Row           | integer | Yatay sayfa sonunun yerleştirileceği satır numarası. |
| Column        | integer | Dikey sayfa sonunun yerleştirileceği sütun numarası. |
| StartIndex    | integer | Aralıka dayalı sayfa sonu işlemi için başlangıç dizini. |
| EndIndex      | integer | Aralıka dayalı sayfa sonu işlemi için bitiş dizini. |

**PageSetupOperateParameter**

| Parametre Adı | Tür    | Açıklama |
| ------------- | ------ | -------- |
| PageSetup     | object | Sayfa düzeni ayarları (kenar boşlukları, yön, kağıt boyutu vb.). |

**PivotTableOperateParameter**

| Parametre Adı       | Tür         | Açıklama |
| ------------------- | ----------- | -------- |
| DestCellName        | string      | Dönüştürme tablosunun hedef aralığının sol üst hücresi (örneğin, `C5`). |
| SourceData          | string      | Dönüştürme tablosunun kaynak aralığı (örneğin, `A1:D100`). |
| TableName           | string      | Oluşturulan dönüştürme tablosuna atanan ad. |
| UseSameSource       | string      | Mevcut kaynak aralığını yeniden kullanmak için `true`; yeni bir tane oluşturmak için `false`. |
| PivotTableIndex     | integer     | Güncellenecek dönüştürme tablosunun dizini (değiştirme/silme işlemleri için gerekli). |
| PivotFieldRows      | integer[]   | Satırlar alanında görünecek alan dizinleri koleksiyonu. |
| PivotFieldColumns   | integer[]   | Sütunlar alanında görünecek alan dizinleri koleksiyonu. |
| PivotFieldData      | integer[]   | Veri alanında görünecek alan dizinleri koleksiyonu. |

**ShapeOperateParameter**

| Parametre Adı | Tür    | Açıklama |
| ------------- | ------ | -------- |
| Shape         | object | Şeklin tanımı (tür, konum, boyut, metin vb.). |

**WorkbookSettingsOperateParameter**

| Parametre Adı     | Tür    | Açıklama |
| ----------------- | ------ | -------- |
| WorkbookSettings  | object | Tüm çalışma kitabını etkileyen ayarlar (örneğin, hesaplama modu, hassasiyet). |

**WorksheetOperateParameter**

| Parametre Adı    | Tür    | Açıklama |
| ---------------- | ------ | -------- |
| Name             | string | İşlem yapılacak mevcut çalışma sayfasının adı. |
| SheetType        | string | Sayfa türü (`Worksheet`, `Chart` vb.). |
| NewName          | string | Yeniden adlandırma sırasında çalışma sayfasına verilecek yeni ad. |
| MovingRequest    | object | Çalışma sayfasını taşıma işlemi için parametreler (örneğin, `FromIndex`, `ToIndex`). |

## REST API

| API                    | Tür  | Açıklama | Kaynak Bağlantısı |
| ---------------------- | ---- | -------- | ----------------- |
| /cells/task/runtask    | POST | Görevi Çalıştır | [PostRunTask](https://apireference.aspose.cloud/cells/#/Task/PostRunTask) |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından yapmanızı sağlar.

### Ön Gereksinimler
- **Kimlik Doğrulama** – Geçerli bir `Authorization: Bearer <access_token>` üst bilgisini ekleyin.  
- **Depolama** – Kaynak çalışma kitabının Aspose Bulut Depolama’da saklanması veya istek gövdesinde base‑64 kodlu içerik olarak verilmesi gerekir.  
- **API Sürümü** – Bu belge, Aspose.Cells Cloud API’nin **v3.0** sürümünü hedef alır.

### Örnek İstek (cURL)

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/task/runtask" \
     -H "Authorization: Bearer {access_token}" \
     -H "Content-Type: application/json" \
     -d '{
           "OperateObject": {
               "OperateObjectType": "Chart",
               "OperateObjectPosition": {
                   "Workbook": { "FileName": "Sample.xlsx" },
                   "SheetName": "Sheet1"
               }
           },
           "ChartOperateParameter": {
               "ChartType": "Bar",
               "UpperLeftRow": 5,
               "UpperLeftColumn": 2,
               "LowerRightRow": 15,
               "LowerRightColumn": 8,
               "Area": "A1:B5",
               "Title": "Sales Chart",
               "IsVertical": "true"
           }
         }'
```

İstek gövdesi aşağıda tanımlanan **CellsObjectOperateRequest** şemasını takip eder:

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "title": "CellsObjectOperateRequest",
  "type": "object",
  "required": ["OperateObject"],
  "properties": {
    "OperateObject": {
      "type": "object",
      "required": ["OperateObjectType"],
      "properties": {
        "OperateObjectType": { "type": "string", "enum": ["Workbook","Worksheet","PageSetup","Cells","Chart","Shape","ListObject","PivotTable","WorkbookSettings","PageBreak"] },
        "OperateObjectPosition": { "$ref": "#/definitions/OperateObjectPosition" }
      }
    },
    "ChartOperateParameter": { "$ref": "#/definitions/ChartOperateParameter" },
    "ListObjectOperateParameter": { "$ref": "#/definitions/ListObjectOperateParameter" },
    "PageBreakOperateParameter": { "$ref": "#/definitions/PageBreakOperateParameter" },
    "PageSetupOperateParameter": { "$ref": "#/definitions/PageSetupOperateParameter" },
    "PivotTableOperateParameter": { "$ref": "#/definitions/PivotTableOperateParameter" },
    "ShapeOperateParameter": { "$ref": "#/definitions/ShapeOperateParameter" },
    "WorkbookSettingsOperateParameter": { "$ref": "#/definitions/WorkbookSettingsOperateParameter" },
    "WorksheetOperateParameter": { "$ref": "#/definitions/WorksheetOperateParameter" }
  },
  "definitions": {
    "OperateObjectPosition": {
      "type": "object",
      "properties": {
        "Workbook": { "type": "object" },
        "SheetName": { "type": "string" },
        "ChartIndex": { "type": "integer" },
        "ShapeIndex": { "type": "integer" },
        "CellName": { "type": "string" },
        "ListObjectIndex": { "type": "integer" }
      }
    },
    "ChartOperateParameter": {
      "type": "object",
      "properties": {
        "ChartIndex": { "type": "integer" },
        "ChartType": { "type": "string" },
        "UpperLeftRow": { "type": "integer" },
        "UpperLeftColumn": { "type": "integer" },
        "LowerRightRow": { "type": "integer" },
        "LowerRightColumn": { "type": "integer" },
        "Area": { "type": "string" },
        "IsVertical": { "type": "string", "enum": ["true","false"] },
        "CategoryData": { "type": "string" },
        "IsAutoGetSerialName": { "type": "string", "enum": ["true","false"] },
        "Title": { "type": "string" }
      }
    }
    /* Ek tanımlar, kısa tutmak için atlandı */
  }
}
```

### Örnek Yanıt (Başarılı – 200)

```json
{
  "Code": 200,
  "Status": "OK",
  "TaskId": "d9f2c4a1-5b6e-4a9c-8f2a-7e3b9c0e5f1a",
  "Result": {
    "ChartId": 0,
    "Message": "Chart created successfully."
  }
}
```

Yanıt aşağıdaki alanları içerir:

| Alan      | Tür    | Açıklama |
| --------- | ------ | -------- |
| Code      | integer| Görev motoru tarafından döndürülen HTTP benzeri durum kodu. |
| Status    | string | İnsan tarafından okunabilir durum (örneğin, `OK`). |
| TaskId    | string | Asenkron görevin tanımlayıcısı. |
| Result    | object | İşleme özel sonuçları içeren nesne. |
| Result.ChartId | integer | Oluşturulan veya değiştirilen grafiğin tanımlayıcısı. |
| Result.Message | string | Sonucu açıklayan kısa mesaj. |

### Hata İşleme

| HTTP Durumu | Hata Kodu      | Açıklama | Önerilen Çözüm |
| ----------- | -------------- | -------- | -------------- |
| 400         | InvalidParameter | Bir veya daha fazla istek parametresi eksik veya hatalı. | Gerekli alanları ve veri türlerini doğrulayın. |
| 401         | Unauthorized     | Geçersiz veya eksik kimlik doğrulama belirteci. | Erişim belirtecini yenileyin ve `Authorization` üst bilgisine ekleyin. |
| 404         | NotFound         | Belirtilen çalışma kitabı, çalışma sayfası veya nesne mevcut değil. | `FileName`, `SheetName` ve nesne dizinlerini kontrol edin. |
| 500         | ServerError      | Sunucuda beklenmeyen bir hata oluştu. | İsteği tekrar deneyin; sorun devam ederse destek ekibiyle iletişime geçin. |

### Yaygın Kullanım Senaryoları
- Bir çalışma sayfasına yeni bir grafik ekleyin.  
- Bir çalışma sayfasını yeniden adlandırın (`OperateObjectType = "Worksheet"` ve `WorksheetOperateParameter.NewName`).  
- Sayfa sonu ekleyin (`OperateObjectType = "PageBreak"` ve `PageBreakOperateParameter`).  
- Dönüştürme tablosunun kaynak verisini güncelleyin (`OperateObjectType = "PivotTable"` ve `PivotTableOperateParameter.SourceData`).  
- Hesaplama modu gibi çalışma kitabının genel ayarlarını değiştirin (`OperateObjectType = "WorkbookSettings"`).  

---  

*Tüm açıklamalar, resmi Aspose.Cells Cloud OpenAPI spesifikasyonundan türetilmiştir.*