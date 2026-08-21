---
title: "Bir Excel Çalışma Sayfasından Bir Pivot Tabloyu Silme"
second_title: "Belge"
linktype: "Delete"
type: docs
url: "/tr/pivot-tables/delete/"
aliases: [  /tr/delete-worksheet-pivot-table-by-index/ ]
keywords: "Aspose.Cells, pivot tablo, sil, Excel, REST API"
description: "Aspose.Cells Cloud REST API (v3.0) ile bir Excel çalışma sayfasından bir pivot tabloyu silin. İstek formatını, cURL örneğini, hata kodlarını ve C#, Java, Python, Node.js için SDK snippet’lerini içerir."
weight: 70
ArticleTitle: "Aspose.Cells Cloud ile Bir Excel Çalışma Sayfasından Pivot Tablo Nasıl Silinir?"
---

Bu REST API, bir çalışma sayfasından pivot tabloyu indeksine göre siler.

**Ön Koşullar** – Aspose.Cells Cloud için geçerli bir JWT erişim belirteciniz ve hedef Excel dosyanızın desteklenen bir depolama konumunda bulunması gerekir. API’yi çağırmadan önce dosya adının, çalışma sayfası adının ve depolama bilgilerinin doğru belirtildiğinden emin olun.

Pivot tablolar, bir **Excel çalışma sayfasında** verileri özetlemenin güçlü bir yoludur. Aspose.Cells Cloud kullanarak, tek bir HTTP DELETE isteğiyle istenmeyen bir pivot tabloyu programlı olarak kaldırabilirsiniz. Bu işlem, çalışma sayfalarını temizlemek, rapor oluşturma süreçlerini otomatikleştirmek veya Excel işlemeyi uygulamalarınıza entegre etmek istediğinizde idealdir.

## DeleteWorksheetPivotTable API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvendir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### **İstek Parametreleri**

| Parametre Adı   | Tür     | Konum | Açıklama                                               |
| ---------------- | ------- | ----- | ------------------------------------------------------ |
| name             | string  | path  | Excel belgesinin adı.                                  |
| sheetName        | string  | path  | Pivot tabloyu içeren çalışma sayfasının adı.           |
| pivotTableIndex  | integer | path  | Silinecek pivot tablonun sıfır tabanlı indeksi.        |
| folder           | string  | query | Belgenin bulunduğu klasörün yolu.                      |
| storageName      | string  | query | Depolama servisinin adı.                               |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PivotTables/DeleteWorksheetPivotTable), erişilebilir bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web hizmetlerine kolayca erişmek için **cURL komut satırı aracı** kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye istek yapmayı göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0" \
  -X DELETE \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

**Yanıt Örneği**

```json
{
  "Code": 200,
  "Status": "OK"
}
```

Yanıt, basit bir JSON şemasına uyar:

```json
{
  "Code": integer,   // İşlemin HTTP benzeri durum kodu
  "Status": string   // Metinsel açıklama, örn. "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Hata Yönetimi

Yaygın yanıt durum kodları aşağıda listelenmiştir:

| HTTP Durumu | Açıklama                                                           |
| ----------- | ------------------------------------------------------------------ |
| 400         | Geçersiz istek – eksik veya geçersiz parametreler.                |
| 401         | Yetkisiz erişim – geçersiz veya eksik JWT belirteci.              |
| 404         | Bulunamadı – dosya, çalışma sayfası veya pivot tablo mevcut değil. |
| 500         | Sunucu iç hatası – sunucuda beklenmedik bir koşul oluştu.         |

## Bulut SDK Ailesi

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoludur. SDK, düşük seviye detayları yönetir ve proje görevlerinize odaklanmanıza olanak tanır. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web hizmetlerine istek yapmayı göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-DeleteWorksheetPivotTableIndex-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-DeleteWorksheetPivotTableIndex-delete-worksheet-pivot-table-index.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "DeleteWorksheetPivotTablesByIndex.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-DeleteWorksheetPivotTableIndex-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-DeleteWorksheetPivotTableIndex-delete-worksheet-pivot-table-index.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-DeleteWorksheetPivotTableIndex-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "8798eca5f30bf41a4675b83583a72ec3" >}}

{{< /tab >}}

{{< /tabs >}}