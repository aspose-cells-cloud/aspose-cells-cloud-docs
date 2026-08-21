---
title: "Aralık Stilini Ayarla – Aspose.Cells Cloud API"
second_title: "Dokümantasyon"
linktitle: "Aralık Stilini Ayarla"
type: docs
url: /ranges/update/style/
aliases: [/set-the-style-of-the-range/]
keywords: "Aspose.Cells, aralık stili, API, Excel, bulut"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasındaki bir hücre aralığının stilini nasıl ayarlayacağınızı öğrenin. Kimlik doğrulama adımlarını, istek biçimini, yanıt detaylarını ve .NET, Java, Python, Go ve diğerleri için SDK örneklerini içerir."
weight: 70
---

## **Giriş**
Bu örnek, Aspose.Cells Cloud API kullanarak bir aralığın stilini nasıl ayarlayacağınızı gösterir. API’yi .NET, Java, PHP, Ruby, Python, JavaScript (jQuery) ve diğer birçok programlama dilinden çağırabilirsiniz.

## **API Bilgileri**

| API                                                   | Tür | Açıklama                              | Kaynak Bağlantısı                                                                                                                             |
| ----------------------------------------------------- | --- | ------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| /cells/{name}/worksheets/{sheetName}/ranges/style     | POST | Adlandırılmış bir aralığın hücre stili | [PostWorksheetCellsRangeStyle](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeStyle) |

### **cURL Örneği**

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

**Ön Gereksinimler**  
1. OAuth2 istemci kimlik bilgileri akışı (`POST https://api.aspose.cloud/connect/token`) aracılığıyla bir erişim belirteci edinin.  
2. Her isteğe `Authorization: Bearer <access_token>` başlığını ekleyin.  

**İstek**  

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/style" \
     -H "accept: application/json" \
     -H "Content-Type: application/json" \
     -H "Authorization: Bearer <access_token>" \
     -d '{
           "Range": {
               "FirstRow": 1,
               "FirstColumn": 1,
               "RowCount": 2,
               "ColumnCount": 2,
               "Worksheet": "Sheet1"
           },
           "Style": {
               "Font": {
                   "IsBold": true,
                   "IsItalic": true,
                   "IsStrikeout": true,
                   "IsSubscript": true,
                   "IsSuperscript": true,
                   "DoubleSize": 1
               }
           }
         }'
```

*`Range` nesnesi, aralığın sol‑üst hücresini ve boyutunu belirtir. `Style` nesnesi, uygulanacak biçimlendirme seçeneklerini içerir.*  

{{< /tab >}}

{{< tab tabNum="2" >}}

**Yanıt**  

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Hata yönetimi** – Başarısız isteklerde API, uygun bir HTTP durum kodunu (örneğin, 400, 401, 500) ve `Error` ile `Message` alanlarını içeren bir JSON gövdesini döndürür. `Code` değerini inceleyin; 200’den farklı olan tüm sonuçlar hata yönetimi politikanıza göre kaydedilmeli ve işlenmelidir.  

{{< /tab >}}

{{< /tabs >}}

## **SDK Kaynak Kodu**  
Aspose.Cells Cloud SDK’ları aşağıdaki sayfadan indirilebilir: [Mevcut SDK’lar](/cells/available-sdks/)

### **SDK Örnekleri**  
{{< tabs tabTotal="4" tabID="4" tabName1="PHP" tabName2="Ruby" tabName3="Objective C" tabName4="Go" >}}

{{< tab tabNum="1" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "81d7e60eaf43ae7192df00993997afde" >}}

{{< /tab >}}

{{< /tabs >}}
---