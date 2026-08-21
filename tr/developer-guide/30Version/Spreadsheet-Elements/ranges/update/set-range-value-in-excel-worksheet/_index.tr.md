---
title: "Excel Çalışma Sayfasında Aralık Değeri Ayarlama"
second_title: "Belge"
linktype: "Değerleri ayarla"
type: docs
url: /tr/ranges/update/values/
aliases: [  /tr/set-range-value-in-excel-worksheet/ ]
keywords: "Aspose.Cells, Excel API, aralık değeri ayarlama, REST API, bulut SDK, çalışma sayfası güncelleme"
description: "Aspose.Cells Cloud REST API (v3.0) kullanarak bir Excel defterinde bir hücre veya aralığın değerini nasıl ayarlayacağınızı öğrenin. Uç nokta, parametreler, cURL örneği, SDK kod örnekleri ve hata işleme içerir."
weight: 72
ArticleTitle: "Excel Çalışma Sayfasında Aralık Değeri Ayarlama – Aspose.Cells Cloud API"
---

Bu REST API’yi belirtilen aralıkta bir değer ayarlamak için kullanın. Uygun durumlarda, değer başka bir veri türüne dönüştürülür ve hücrenin sayı formatı sıfırlanır.

**Önkoşullar**  
- Geçerli bir Aspose Cloud hesabı.  
- `Cells.ReadWrite` kapsamını içeren bir JWT belirteci.  
- Defterin hedef depolama konumuna önceden yüklenmiş olması gerekir.

## PostWorksheetCellsRangeValue API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/value
```

İstek parametreleri:

| Parametre Adı | Tür      | Konum  | Açıklama                                         |
|---------------|----------|--------|--------------------------------------------------|
| name          | string   | path   | Defter adı                                       |
| sheetName     | string   | path   | Çalışma sayfası adı                              |
| value         | string   | query  | Giriş değeri                                     |
| range         | object   | body   | Çalışma sayfasındaki aralık nesnesi             |
| isConverted   | boolean  | query  | Giriş değerinin dönüştürülüp dönüştürülmeyeceğini belirtir |
| setStyle      | boolean  | query  | Hedef hücrelere stil uygulanıp uygulanmayacağını belirtir |
| folder        | string   | query  | Defter klasörü                                   |
| storageName   | string   | query  | Depolama adı                                     |

**İstek gövdesine gönderilebilecek `range` nesnesi örneği:**

```json
{
  "range": {
    "FirstRow": 0,
    "FirstColumn": 0,
    "RowCount": 1,
    "ColumnCount": 1
  }
}
```

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Ranges/PostWorksheetCellsRangeValue), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize izin verir.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’ye nasıl istek gönderileceğini göstermektedir. **`Authorization` başlığına geçerli bir JWT belirteci ekleyin.**

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/value?value=25&isConverted=false&setStyle=false" \
  -X POST \
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

**Yanıt Şeması**

| Alan    | Tür     | Açıklama                                                |
|---------|---------|---------------------------------------------------------|
| Code    | integer | İşlemin HTTP durum kodu.                               |
| Status  | string  | Sonucun kısa açıklaması (örneğin, "OK").               |
| Message | string  | İstek başarısız olduğunda detaylı hata mesajı (isteğe bağlı). |
| Result  | object  | Başarılı çağrılar için döndürülen ek veriler (isteğe bağlı). |

**Olası HTTP Durum Kodları**

- **200 OK** – Aralık değeri başarıyla ayarlandı.  
- **400 Bad Request** – Geçersiz parametreler veya bozuk istek gövdesi.  
- **401 Unauthorized** – Eksik veya geçersiz JWT belirteci.  
- **403 Forbidden** – İstenen işlem için yetersiz yetkiler.  
- **404 Not Found** – Belirtilen defter, çalışma sayfası veya aralık mevcut değil.  
- **500 Internal Server Error** – Beklenmeyen sunucu hatası.

*400 Bad Request için örnek hata yanıtı:*

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "'range' nesnesinde gerekli alanlar eksik."
}
```

## Bulut SDK Ailesi

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoludur. SDK, düşük seviye detayları yöneterek projenizdeki görevlere odaklanmanıza olanak tanır. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposunu](https://github.com/aspose-cells-cloud) inceleyin.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak Aspose.Cells web hizmetlerine nasıl istek gönderileceğini göstermektedir:

{{< tabs tabTotal="9" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Swift" tabName8="Perl" tabName9="Go" >}}

{{< tab tabNum="1" >}}
{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Cells-SetRangeValueWorksheet-1.cs" >}}
{{< /tab >}}

{{< tab tabNum="2" >}}
{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-cells-SetRangeValueWorksheet-1.java" >}}
{{< /tab >}}

{{< tab tabNum="3" >}}
{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Cells-PostSetCellRangeValue-.php" >}}
{{< /tab >}}

{{< tab tabNum="4" >}}
{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Cells-set_cell_range_value-.rb" >}}
{{< /tab >}}

{{< tab tabNum="5" >}}
{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Cells-SetRangeValueWorksheet-1.js" >}}
{{< /tab >}}

{{< tab tabNum="6" >}}
{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SetRangeValueInExcelWorksheet.py" >}}
{{< /tab >}}

{{< tab tabNum="7" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}
{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Cells-SetRangeValueWorksheet-1.pl" >}}
{{< /tab >}}

{{< tab tabNum="9" >}}
{{< gist "aspose-cells-cloud-gists" "7dc9243752ac8a0e5d9c0f211a029cd9" >}}
{{< /tab >}}

{{< /tabs >}}