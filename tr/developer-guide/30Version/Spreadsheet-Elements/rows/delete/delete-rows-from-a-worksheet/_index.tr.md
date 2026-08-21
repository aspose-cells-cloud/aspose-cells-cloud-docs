---
title: "Bir Excel Çalışma Sayfasından Birden Fazla Satır Silme"
second_title: "Belge"
linktitle: "Satırlar"
type: docs
url: /tr/rows/delete/rows/
keywords: "Aspose.Cells Cloud, satırları sil, birden fazla satır sil, Excel çalışma sayfası, REST API, SDK"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasından bir veya daha fazla satırı nasıl sileceğinizi öğrenin. Uç nokta ayrıntılarını, parametreleri, cURL örneğini ve çeşitli programlama dilleri için SDK kod örneklerini içerir."
weight: 80
ArticleTitle: "Aspose.Cells Cloud API ile Bir Excel Çalışma Sayfasından Birden Fazla Satır Silme"
---

Bu REST API, bir Excel çalışma sayfasından **birden fazla satırı siler**.

**Gereksinimler:** Bu uç noktayı çağırmak için Aspose Cloud kimlik doğrulamasından alınan geçerli bir JWT erişim belirteci ve çalışma kitabına ilişkin uygun depolama izinlerine sahip olmanız gerekir.

## DeleteWorksheetRows API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/rows
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### **İstek Parametreleri**

| Parametre Adı    | Tür      | Yol / Sorgu Dizesi / HTTP Gövdesi | Açıklama                                                                |
| ---------------- | -------- | -------------------------------- | ----------------------------------------------------------------------- |
| name             | string   | path                             | Çalışma kitabı adı.                                                     |
| sheetName        | string   | path                             | Çalışma sayfası adı.                                                    |
| startrow         | integer  | query                            | Silinecek ilk satırın sıfır tabanlı dizini (örneğin, `0` = ilk satır). |
| totalRows        | integer  | query                            | Silinecek satır sayısı.                                                 |
| updateReference  | boolean  | query                            | Silme işleminden sonra referansların güncellenip güncellenmeyeceği (`true`/`false`). |
| folder           | string   | query                            | Belge klasörü.                                                          |
| storageName      | string   | query                            | Depolama adı.                                                           |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Cells/DeleteWorksheetRows), herkese açık bir programlama arayüzü tanımlar ve web tarayıcınızdan doğrudan REST etkileşimlerinde bulunmanızı sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye istekte bulunmayı göstermektedir. **Tüm uç noktalar HTTPS gerektirir; HTTP kullanımdan kaldırılmıştır.**

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

**Mümkün olan yanıt kodları**

| HTTP Durumu | Açıklama                                |
|-------------|-----------------------------------------|
| 200         | Satırlar başarıyla silindi.             |
| 400         | Geçersiz istek – geçersiz parametreler. |
| 401         | Yetkisiz erişim – eksik veya geçersiz JWT belirteci. |
| 404         | Bulunamadı – çalışma kitabı veya çalışma sayfası mevcut değil. |
| 500         | İç sunucu hatası – beklenmeyen durum.   |

## Bulut SDK Kod Ailesi

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoludur. Bir SDK, düşük seviye ayrıntıları yönetir ve projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web hizmetlerine istekte bulunmayı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteWorksheetRows.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteWorksheetRows.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteWorksheetRows.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteWorksheetRows.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteWorksheetRows.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteWorksheetRows.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteWorksheetRows.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteWorksheetRows.go" >}}

{{< /tab >}}

{{< /tabs >}}