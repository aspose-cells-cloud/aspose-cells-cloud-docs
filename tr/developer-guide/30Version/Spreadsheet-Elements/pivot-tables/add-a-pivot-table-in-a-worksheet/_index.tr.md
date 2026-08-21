---
title: "Excel çalışma sayfasına bir pivot tablo ekleyin"
second_title: "Belge"
linktype: Ekle
type: docs
url: /pivot-tables/add/
aliases: [/add-a-pivot-table-in-a-worksheet/]
keywords: "pivot tablo ekle, Excel çalışma sayfası, Aspose.Cells Cloud, REST API, SDK, Excel pivot tablosu"
description: "Aspose.Cells Cloud REST API’sini kullanarak bir Excel çalışma sayfasına pivot tablo ekleyin. C#, Java, PHP, Python, Node.js, Android, Swift, Perl, Go SDK’ları aracılığıyla erişilebilir."
weight: 30
ArticleTitle: "Aspose.Cells Cloud ile bir Excel Çalışma Sayfasına Pivot Tablo Nasıl Eklenir?"
---

Bu REST API, bir çalışma sayfasına pivot tablo ekler.

**Önkoşullar:**  
- Geçerli bir JWT erişim belirteci ile bir Aspose.Cells Cloud hesabı.  
- Hedef çalışma kitabının desteklenen bir depolama konumunda (varsayılan depo veya kullanıcı tarafından belirlenmiş depo) saklanıyor olması.  
- `sheetName` ile belirtilen çalışma sayfasının çalışma kitabında mevcut olması.  

## PutWorksheetPivotTable API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### **İstek parametreleri**

| Parametre Adı | Tür      | Konum  | Açıklama                                                                                                                           |
|---------------|----------|--------|-------------------------------------------------------------------------------------------------------------------------------------|
| name          | string   | path   | Excel belgesinin adı.                                                                                                              |
| sheetName     | string   | path   | Pivot tablonun oluşturulacağı çalışma sayfasının adı.                                                                             |
| request       | object   | body   | Pivot tablo tanımını içeren `CreatePivotTableRequest` DTO’su.                                                                      |
| folder        | string   | query  | Belgenin bulunduğu klasör.                                                                                                         |
| storageName   | string   | query  | Belgenin bulunduğu depo adı.                                                                                                       |
| sourceData    | string   | query  | Yeni pivot tablo önbelleği için kaynak verilerin sağlandığı aralık (örneğin, `A5:E10`).                                            |
| destCellName  | string   | query  | Pivot tablo raporunun hedef aralığının sol üst hücresinin adresi.                                                                  |
| tableName     | string   | query  | Yeni pivot tabloya verilen isim.                                                                                                   |
| useSameSource | boolean  | query  | `true` ise, yeni pivot tablo daha önce bu kaynağı kullanan başka bir pivot tablonun kaynak verilerini yeniden kullanarak belleği tasarruflu kullanır. |

[Pivot Table API’si OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/PivotTables/PutWorksheetPivotTable), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

Aspose.Cells web hizmetlerine kolayca erişmek için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’yi nasıl çağıracağınızı göstermektedir.

**Güvenlik Notu:** API’yi çağırırken her zaman `https://` protokolünü kullanın ve JWT belirtecinizi gizli tutun; düz HTTP üzerinden iletmek, belirtecin ele geçirilmesine neden olabilir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/pivottables" \
-X PUT \
-d '{"Name":"MyPivot","SourceData":"A5:E10","DestCellName":"H20","UseSameSource":true,"PivotFieldRows":[1],"PivotFieldColumns":[1],"PivotFieldData":[1]}' \
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

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                           |
|-----|-----------------------------|----------------------------------------------------|
| 200 | Tamam                       | Sü 필터 başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Geçersiz İstek              | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Yetkisiz                    | Geçersiz veya eksik JWT belirteci. |
| 413 | Yük Çok Büyük               | Yüklenen dosya boyut sınırlarını aşıyor. |
| 500 | İç Sunucu Hatası            | Beklenmeyen sunucu hatası. |

## Bulut SDK Geliştirme Grubu

Bir SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoludur. Bir SDK, düşük seviye detayları ele alır ve size proje görevlerinize odaklanma imkânı sunar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerini çeşitli SDK’lar kullanarak nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-PivotTables-AddPivottableWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-pivottables-AddPivottableWorksheet-add-pivot-table-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "AddPivotTableInw" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-PivotTables-AddPivottableWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-pivottables-AddPivottableWorksheet-add-pivot-table-worksheet.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-PivotTables-AddPivottableWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "980246b631d7816f257f2ad4664788ea" >}}

{{< /tab >}}

{{< /tabs >}}

Daha fazla işlem için ilgili API sayfalarına bakın: **[Bir pivot tabloyu alın](https://docs.aspose.cloud/cells/pivot-tables/get/)**, **[Bir pivot tabloyu silin](https://docs.aspose.cloud/cells/pivot-tables/delete/)** ve **[Bir pivot tabloyu güncelleyin](https://docs.aspose.cloud/cells/pivot-tables/update/)**.