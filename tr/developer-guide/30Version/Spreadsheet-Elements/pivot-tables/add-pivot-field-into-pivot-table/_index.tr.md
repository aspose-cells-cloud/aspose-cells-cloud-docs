---
title: "Bir Pivot Tabloya Pivot Alanı Ekle"
second_title: "Belge"
linktitle: "Pivot Alanı Ekle"
type: docs
url: /tr/pivot-tables/add-pivot-field/
aliases: [/add-a-pivot-table-in-a-worksheet/]
keywords: "Aspose.Cells Cloud, Excel, pivot tablo, pivot alanı ekle, REST API, SDK"
description: "Aspose.Cells Cloud REST API kullanarak mevcut bir pivot tabloya bir pivot alanı ekleyin. İstek ayrıntılarını, cURL örneğini ve SDK kod parçacıklarını içerir."
weight: 40
ArticleTitle: "Bir Pivot Tabloya Pivot Alanı Ekle – Aspose.Cells Cloud Belgelendirmesi"
---

Bu REST API, **mevcut bir pivot tabloya bir pivot alanı ekler**.

> **Önkoşul:** Bu uç noktayı çağırmak için `Authorization` başlığına geçerli bir JWT kimlik doğrulama belirteci eklemeniz ve çalışma kitabının belirtilen klasörde veya varsayılan depolama alanına kayıtlı olduğundan emin olmanız gerekir.

## REST API

```bash
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField
```

### İstek parametreleri

| Parametre Adı   | Tür     | Konum | Açıklama                                                            |
| ---------------- | ------- | ----- | ------------------------------------------------------------------- |
| name             | string  | path  | Belge adı.                                                          |
| sheetName        | string  | path  | Çalışma sayfası adı.                                                |
| pivotTableIndex  | integer | path  | Pivot tablonun dizini.                                              |
| pivotFieldType   | string  | query | Alanlar alanı türü (örneğin, Row, Column).                         |
| request          | object  | body  | Eklemek için alan indekslerini içeren DTO.                         |
| needReCalculate  | boolean | query | İşlem sonrası pivot tabloyu yeniden hesaplamak için **true** olarak ayarlayın. |
| folder           | string  | query | Belgenin bulunduğu klasör.                                          |
| storageName      | string  | query | Depolama alanı adı.                                                 |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/PivotTables/PutPivotTableField), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerini çağırmak için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL kullanarak bir pivot alanı nasıl ekleyeceğinizi göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/PivotField?pivotFieldType=Row" \
  -X PUT \
  -d '{"Data":[1,2]}' \
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

Başarılı yanıt, `Code` ve `Status` alanlarını içeren bir JSON nesnesi döndürür. Örnek şema:

```json
{
  "Code": 0,        // HTTP durum kodunu gösteren tamsayı
  "Status": "OK"    // Dize mesajı
}
```

Olası hata yanıtları arasında eksik parametreler için **400 Bad Request**, geçersiz belirteç için **401 Unauthorized** ve sunucu tarafındaki sorunlar için **500 Internal Server Error** yer alır.

## Bulut SDK Ailesi

Bu işlevselliği entegre etmenin en hızlı yolu, bir SDK kullanmaktır. SDK’lar düşük seviye ayrıntıları yönetir, böylece iş mantığınıza odaklanabilirsiniz. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanarak Aspose.Cells web hizmetlerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="Ruby" tabName4="Python" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-AddPivotFieldInPivottable-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-AddPivotFieldInPivottable-add-pivot-field.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddPivotFieldInPivotTable.py" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-AddPivotFieldInPivottable-1.js" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-AddPivotFieldInPivottable-add-pivot-field.java" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-AddPivotFieldInPivottable-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "8f9b66d50f7cfa2b14c24fa7ddb396e7" >}}

{{< /tab >}}

{{< /tabs >}}

**Ayrıca bakınız:**  
- [Pivot Tablo Ekle](https://docs.aspose.cloud/cells/pivot-tables/add-pivot-table/)  
- [Pivot Alanı Sil](https://docs.aspose.cloud/cells/pivot-tables/delete-pivot-field/)