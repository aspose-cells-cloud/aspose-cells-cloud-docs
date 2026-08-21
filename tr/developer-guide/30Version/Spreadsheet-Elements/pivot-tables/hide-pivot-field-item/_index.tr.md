---
title: "Pivot tabloda pivot alanı öğesini gizle"
second_title: "Document"
linktitle: Gizle
type: docs
url: /tr/pivot-tables/hide-pivot-field-item/
aliases: [  /tr/hide-pivot-field-item/ ]
keywords: "Aspose.Cells, pivot alanı öğesini gizle, PivotTable API, REST API, bulut SDK"
description: "Aspose.Cells Cloud REST API kullanarak bir pivot tabloda pivot alanı öğesini nasıl gizleyeceğinizi öğrenin. İstek ayrıntılarını, cURL örneğini ve birden fazla dil için SDK kod parçacıklarını içerir."
weight: 110
ArticleTitle: "Pivot Tabloda Pivot Alan Öğesini Gizle – Aspose.Cells Cloud API Kılavuzu"
---

API'yi çağırmadan önce şunlardan emin olun:

* Geçerli bir **JWT erişim belirteci** (Aspose Cloud kimlik doğrulama akışı aracılığıyla elde edilebilir).  
* Hedef çalışma kitabının Aspose Cloud depolarınızda yüklenmiş olması.  
* Çalışma sayfasının ve pivot tablonun zaten oluşturulmuş olması.

Bu ön koşullar, kimlik doğrulama hatalarını ve "kaynak bulunamadı" yanıtlarını önler. Aşağıdaki adımlar, API'yi çağırmadan önce gereken kurulumu özetlemektedir.

Bu REST API, bir pivot tablodaki bir pivot alanı öğesini gizler.

## PostPivotTableFieldHideItem API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/PivotField/Hide
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### **İstek parametreleri**

| Parametre Adı   | Tür      | Konum   | Açıklama                                                                                      |
| ---------------- | -------- | ------- | ---------------------------------------------------------------------------------------------- |
| name             | string   | path    | Excel dosyasının adı.                                                                          |
| sheetName        | string   | path    | Pivot tabloyu içeren çalışma sayfası.                                                          |
| pivotTableIndex  | integer  | path    | Çalışma sayfasındaki pivot tablonun indeksi.                                                   |
| pivotFieldType   | string   | query   | Pivot alanın türü (Satır, Sütun, Sayfa, Veri vb.).                                            |
| fieldIndex       | integer  | query   | Düzenlenecek pivot alanın sıfır tabanlı indeksi.                                               |
| itemIndex        | integer  | query   | Gizlenecek alan içindeki belirli öğenin indeksi.                                               |
| isHide           | boolean  | query   | Öğeyi gizlemek için **true**, göstermek için **false** olarak ayarlayın.                       |
| needReCalculate  | boolean  | query   | Değişiklikten sonra pivot tablonun yeniden hesaplanıp hesaplanmayacağını belirtir. Varsayılan **false**. |
| folder           | string   | query   | Çalışma kitabının bulunduğu klasör yolu.                                                        |
| storageName      | string   | query   | Depolama hizmetinin adı.                                                                        |

**Gerekli sorgu parametrelerinin hızlı başvurusu**

- **pivotFieldType** – alanın türü (örneğin, `Row`).  
- **fieldIndex** – düzenlenecek alanın sıfır tabanlı indeksi.  
- **itemIndex** – gizleyeceğiniz/göstereceğiniz öğenin sıfır tabanlı indeksi.  
- **isHide** – gizlemek için `true`, göstermek için `false`.  
- **needReCalculate** – isteğe bağlı, varsayılan olarak `false`.

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableFieldHideItem), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile API'yi nasıl çağıracağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/pivottables/0/PivotField/Hide?pivotFieldType=Row&fieldIndex=0&itemIndex=1&isHide=true&needReCalculate=true" \
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

**Yanıt ayrıntıları**

| Durum Kodu | Açıklama                                                           |
| ---------- | ------------------------------------------------------------------ |
| 200        | Öğe başarıyla gizlendi.                                           |
| 400        | Geçersiz istek – eksik veya geçersiz parametreler.                |
| 401        | Yetkisiz – geçersiz veya eksik JWT belirteci.                      |
| 500        | Sunucu hatası – işlem tamamlanamadı.                              |

**Not:** Sağlanan `fieldIndex` veya `itemIndex` aralık dışındaysa, API **400 Bad Request** (Geçersiz İstek) yanıtı döndürür.

## Bulut SDK Ailesi

API ile hızlı geliştirme yapmanın en hızlı yolu SDK kullanmaktır. SDK'lar, alt seviye ayrıntıları ele alır, böylece iş mantığınıza odaklanabilirsiniz. Aspose.Cells Cloud SDK'larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK'lar kullanarak pivot alanı öğesini nasıl gizleyeceğinizi göstermektedir.

{{< tabs tabTotal="2" tabID="4" tabName1="C#" tabName2="Go" >}}

{{< tab tabNum="1" >}}

```csharp
public void Run_PivotTable_NeedReCalculate()
{
    // Çalışma kitabını ve çalışma sayfasını hazırlayın
    url = @"https://api.aspose.cloud/v3.0/storage/file/Temp/V17.02.00_01.xlsx";
    using (HttpWebResponse response = _helper.CallDelete(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Çalışma kitabını yükleyin
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Pivot tabloyu içerecek ikinci çalışma sayfası oluşturun
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Örnek verileri içeren ikinci bir çalışma sayfası oluşturun
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/Sheet2?folder=Temp";
    using (HttpWebResponse response = _helper.CallPut(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Örnek verileri Sheet2'ye içe aktarın
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/importdata?folder=Temp";
    data = "{ \"BatchData\":[{...}] }"; // Kısa tutmak için kısaltıldı
    using (HttpWebResponse response = _helper.CallPost(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // PivotSheet'e bir pivot tablo ekleyin
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables?folder=Temp";
    data = "{\"Name\":\"TestPivot\",\"SourceData\":\"=Sheet2!A1:E8\",\"DestCellName\":\"C1\",\"UseSameSource\":true,\"PivotFieldRows\":[0,1],\"PivotFieldColumns\":[2],\"PivotFieldData\":[3,4]}";
    using (HttpWebResponse response = _helper.CallPut(url, data, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }

    // Belirli bir satır alan öğesini gizleyin
    url = @"https://api.aspose.cloud/v3.0/cells/V17.02.00_01.xlsx/worksheets/PivotSheet/pivottables/0/PivotField/Hide?pivotFieldType=Row&fieldIndex=0&itemIndex=1&isHide=true&needReCalculate=true&folder=Temp";
    using (HttpWebResponse response = _helper.CallPost(url, string.Empty, contentType))
    {
        Assert.AreEqual(response.StatusCode, HttpStatusCode.OK);
    }
}
```

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "a0bec26a8274b9f7cb514015843a214e" >}}

{{< /tab >}}

{{< /tabs >}}

**Not:** SDK örnekleri, kimlik doğrulamanın (JWT belirteci) zaten yapılandırıldığını ve çalışma kitabının belirtilen depolama klasöründe bulunduğunu varsayar. Ortamınıza göre `folder` ve `storageName` parametrelerini gerektiği gibi ayarlayın.
---