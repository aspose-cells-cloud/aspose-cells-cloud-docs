---
title: "Excel Çalışma Sayfasından Bir Satır Silme"
second_title: "Belge"
linktitle: "Satır"
type: docs
url: /tr/rows/delete/row/
aliases: [  /tr/delete-row-from-a-worksheet/ ]
description: "Aspose.Cells Cloud REST API aracılığıyla bir Excel çalışma sayfasından belirli bir satırı silmek için DELETE /worksheets/{sheetName}/cells/rows/{rowIndex} uç noktasını kullanın. cURL komutunu, SDK örneklerini ve tüm parametre referansını içerir."
keywords: "Aspose.Cells, satır sil, Excel, API, REST, Bulut, SDK"
weight: 80
ArticleTitle: "Excel Çalışma Sayfasından Bir Satır Silme – Aspose.Cells Cloud API Kılavuzu"
---

Bu REST API, bir Excel çalışma sayfasından bir satırı siler.

**Ön Gereksinimler**  
- Geçerli bir JWT **Yetkilendirme** belirteci.  
- Çalışma kitabının desteklenen Aspose Bulut depolama alanına (varsayılan veya özel) kaydedilmiş olması gerekir.  
- Hedef klasör (belirtilmişse) seçilen depolama alanında mevcut olmalıdır.

## REST API

```bash
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/{rowIndex}
```

### **İstek Parametreleri**

| Parametre Adı     | Tür      | Yol / Sorgu | Gerekli | Açıklama                                                                                        |
| ----------------- | -------- | ----------- | ------- | ----------------------------------------------------------------------------------------------- |
| **name**          | string   | path        | Evet    | Çalışma kitabı adı.                                                                             |
| **sheetName**     | string   | path        | Evet    | Çalışma sayfası adı.                                                                            |
| **rowIndex**      | integer  | path        | Evet    | Silinecek satırın sıfır tabanlı indeksi.                                                        |
| **startrow**      | integer  | query       | Hayır   | Silinecek ilk satırın indeksi (genellikle `rowIndex` ile aynı).                                 |
| **totalRows**     | integer  | query       | Hayır   | Silinecek ardışık satır sayısı.                                                                 |
| **updateReference** | boolean | query      | Hayır   | `true` (varsayılan) olarak ayarlandığında, silme işleminden sonra formüller, adlandırılmış aralıklar ve diğer referanslar güncellenir. |
| **folder**        | string   | query       | Hayır   | Çalışma kitabının bulunduğu klasör.                                                             |
| **storageName**   | string   | query       | Hayır   | Depolama hizmetinin adı.                                                                        |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetRow), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, tam olarak çalıştırılabilir bir çağrı göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
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

{{< /tab >}}

{{< /tabs >}}

**Olası HTTP Yanıt Kodları**

| Kod | Anlamı                               | Açıklama                                                                     |
|-----|--------------------------------------|------------------------------------------------------------------------------|
| 200 | OK (Tamam)                           | Satır başarıyla silindi.                                                    |
| 400 | Bad Request (Hatalı İstek)           | Eksik veya geçersiz parametreler (örneğin, sayısal olmayan `rowIndex`).     |
| 401 | Unauthorized (Yetkisiz)              | Geçersiz veya eksik JWT belirteci.                                           |
| 404 | Not Found (Bulunamadı)               | Belirtilen çalışma kitabı, çalışma sayfası veya satır mevcut değil.         |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası; ayrıntılar için hata yanıtına bakın.           |

**Hata Yanıt Örneği**

```json
{
  "Code": 400,
  "Message": "Geçersiz satır indeksi sağlandı."
}
```

## Bulut SDK Ailesi

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. Bir SDK, düşük seviyeli detayları soyutlayarak projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub Deposu](https://github.com/aspose-cells-cloud)’na göz atın.

Aşağıdaki kod örnekleri, Aspose.Cells web servislerine yönelik çağrıların farklı SDK’larla nasıl yapılacağını göstermektedir:

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -X DELETE "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows?startrow=1&totalRows=1&updateReference=true" \
  -H "accept: application/json" \
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

**İlgili İşlemler**  
- [Satır Ekle](/cells/rows/add/row/)  
- [Birden Fazla Satır Sil](/cells/rows/delete/rows/)  
- [Satır Detaylarını Al](/cells/rows/get/row/)  
---