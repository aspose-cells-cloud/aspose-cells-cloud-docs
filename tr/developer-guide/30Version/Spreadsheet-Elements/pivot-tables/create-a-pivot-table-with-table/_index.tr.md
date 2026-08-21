---
title: "Tabloyu Pivot Tabloya Dönüştür"
second_title: "Belge"
linktype: "Dönüştür"
type: docs
url: /tr/pivot-tables/convert-table-to-pivottable/
aliases:
  [
    "/tr/create-a-pivottable-with-table/",
    "/tr/create-new-pivot-table-with-list-object-as-source-data/",
  ]
keywords: "pivot tablo, liste nesnesi, Aspose.Cells Cloud, REST API, tabloyu pivot tabloya dönüştür"
description: "Aspose.Cells Cloud REST API ile bir liste nesnesinden pivot tablo nasıl oluşturulacağını öğrenin. İsteği tanımlayan ayrıntılar, cURL örneği ve SDK referanslarını içerir."
weight: 60
ArticleTitle: "Tabloyu Pivot Tabloya Dönüştür – Aspose.Cells Cloud Belgeleme"
---

Bu REST API, bir liste nesnesinden bir **pivot tablo** oluşturur.

Pivot tablo, bir liste nesnesinden gelen verileri özetleyerek büyük veri setlerini doğrudan defter içinde analiz etmenize ve raporlamanıza olanak tanır.

**Önkoşullar:**  
- Kimlik doğrulama için geçerli bir JWT bearer token.  
- Defterin belirtilen depolama konumunda bulunması.  
- Hedef çalışma sayfasında özetlemek istediğiniz liste nesnesinin bulunması.

## PostWorksheetListObjectSummarizeWithPivotTable API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listObjectIndex}/SummarizeWithPivotTable
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/tr/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT token tabanlı kimlik doğrulama</a> gerektirir.

### **İstek Parametreleri**

| Parametre Adı   | Tür      | Konum  | Açıklama                                    |
| ---------------- | -------- | ------ | ------------------------------------------- |
| name             | string   | path   | Defter dosyasının adı.                      |
| sheetName        | string   | path   | Liste nesnesini içeren çalışma sayfası.     |
| listObjectIndex  | integer  | path   | Çalışma sayfasındaki liste nesnesinin indeksi. |
| destsheetName    | string   | query  | Hedef çalışma sayfasının adı.               |
| request          | object   | body   | Pivot tabloyu tanımlayan JSON yükü.         |
| folder           | string   | query  | Defterin bulunduğu klasör yolu.             |
| storageName      | string   | query  | Depolama adı.                               |

İstek gövdesi aşağıdaki JSON şemasına uygun olmalıdır:

```json
{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "object",
  "properties": {
    "Name": { "type": "string", "description": "Yeni pivot tablonun adı." },
    "DestCellName": { "type": "string", "description": "Pivot tablonun sol üst hücresi (örneğin, \"C1\")." },
    "PivotFieldRows": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "Satırlara yerleştirilecek alanların sıfır tabanlı indeksleri."
    },
    "PivotFieldColumns": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "Sütunlara yerleştirilecek alanların sıfır tabanlı indeksleri."
    },
    "PivotFieldData": {
      "type": "array",
      "items": { "type": "integer" },
      "description": "Veri alanları olarak kullanılacak alanların sıfır tabanlı indeksleri."
    }
  },
  "required": ["Name", "DestCellName", "PivotFieldRows", "PivotFieldColumns", "PivotFieldData"]
}
```

<a href="https://apireference.aspose.cloud/cells/#/ListObjects/PostWorksheetListObjectSummarizeWithPivotTable" rel="noopener noreferrer">OpenAPI Specification</a>, herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web servislerine kolayca erişmek için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye istek nasıl yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/TestCase.xlsx/worksheets/Sheet2/listobjects/0/SummarizeWithPivotTable?folder=CellsTests&destsheetName=Sheet4" \
-X POST \
-d '{"Name":"TestPivot","DestCellName":"C1","PivotFieldRows":[0,1],"PivotFieldColumns":[2],"PivotFieldData":[3,4]}' \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

*Not: Canlı ortamlar için üretim uç noktasını (`api.aspose.cloud`) kullanın. QA uç noktası (`api-qa.aspose.cloud`) yalnızca test amaçlıdır. Tüm üretim çağrıları için HTTPS zorunludur.*

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

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                                  |
|-----|-----------------------------|-----------------------------------------------------------|
| 200 | OK (Tamam)                  | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT token. |
| 413 | Payload Too Large (Yük Çok Büyük) | Yüklenen dosya boyut limitini aşıyor. |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası. |

## Bulut SDK Ailesi

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. SDK, düşük seviye detayları yöneterek projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web servislerine istek nasıl yapılacağını göstermektedir: