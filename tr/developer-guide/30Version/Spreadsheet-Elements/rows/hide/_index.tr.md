---
title: "Excel Çalışma Sayfasında Satırları Gizleme"
second_title: "Belge"
linktitle: "Gizle"
type: docs
url: /rows/hide/
aliases: [/hide-rows-in-excel-worksheet/]
keywords: "satırları gizle, Aspose.Cells Cloud, Excel API, REST, SDK"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasında bir veya birden fazla satırı nasıl gizleyeceğinizi öğrenin. cURL örneği, SDK kod parçacıkları, parametreler, kimlik doğrulama, yanıt detayları ve hata yönetimi içerir."
weight: 40
ArticleTitle: "Aspose.Cells Cloud API Kullanarak Excel Çalışma Sayfasında Satırları Gizleme"
---

Bu REST API, Excel çalışma sayfasında satırları gizler.

**Önkoşullar:** Aspose Cloud OAuth uç noktasından alınmış geçerli bir JWT Bearer belirteci, Aspose Cloud depolama alanına kaydedilmiş çalışma kitapçığı ve gizlenecek satırları içeren çalışma sayfasının adı. API, XLS, XLSX ve diğer desteklenen formatlardaki Excel dosyalarıyla çalışır.

## PostHideWorksheetRows API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows/hide
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre       | Tür     | Konum  | Açıklama                                                                 |
| ----------------- | ------- | ------ | ------------------------------------------------------------------------ |
| **name**        | string  | path   | Çalışma kitaplığı dosyasının adı.                                        |
| **sheetName**   | string  | path   | Gizlenecek satırları içeren çalışma sayfasının adı.                      |
| **startrow**    | integer | query  | Gizlenecek ilk satırın sıfır indeksli numarası.                          |
| **totalRows**   | integer | query  | **startrow**’dan itibaren ardışık olarak gizlenecek satır sayısı.        |
| **folder**      | string  | query  | Çalışma kitaplığının bulunduğu depodaki klasör.                          |
| **storageName** | string  | query  | Depolama hizmetinin adı.                                                 |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Cells/PostHideWorksheetRows), bir web tarayıcısından doğrudan REST etkileşimlerinde bulunmanıza olanak tanıyan herkese açık bir programlama arayüzü sağlar.

**cURL** komut satırı aracını Aspose.Cells web servislerini çağırmak için kullanabilirsiniz. API, Aspose Cloud OAuth uç noktasından alınan bir JWT Bearer belirteci gerektirir; bunu `Authorization` başlığında eklemeniz gerekir. Aşağıdaki örnek, cURL ile bir satırı gizlemeyi göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/cells/rows/hide?startrow=1&totalRows=1" \
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

**Yanıt durum kodları**

| Kod  | Açıklama                         |
|------|----------------------------------|
| 200  | Başarılı – satırlar gizlendi     |
| 400  | Geçersiz istek – hatalı parametreler |
| 401  | Yetkisiz – eksik veya geçersiz JWT |
| 404  | Bulunamadı – çalışma kitaplığı veya çalışma sayfası mevcut değil |
| 500  | Sunucu hatası – iç işlem başarısız |

Başarılı bir çağrı, `Code` ve `Status` alanlarını içeren bir JSON nesnesi döndürür. Hata durumunda yanıt, `Message` ve uygun HTTP durum kodları (örneğin 400, 401, 404, 500) gibi ek alanlar içerir.

**Notlar:** `startrow` değerinin çalışma sayfasının satır aralığı içinde olduğundan emin olun; aksi takdirde API 400 hatası döndürür. Satır indeksleri sıfır tabanlıdır, yani `startrow=0` birinci satıra karşılık gelir.

## Bulut SDK Ailesi

Bu işlevselliği uygulamanıza entegre etmenin en hızlı yolu bir SDK kullanmaktır. SDK’lar düşük seviye detayları yöneterek size iş mantığına odaklanma imkanı verir. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanılarak satırların nasıl gizleneceğini göstermektedir. (Örnek dosya adlarında “Unhide” ifadesinin geçmesinin neden eski isimlendirme kalıplarıdır; her gist içindeki kod aslında **Gizle** işlemini gerçekleştirmektedir.)

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostUnhideWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostUnhideWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostUnhideWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostUnhideWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostUnhideWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostUnhideWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostUnhideWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostUnhideWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}