---
title: "Hücre Özelliklerini Al"
type: docs
url: /tr/get-cells-properties/
weight: 130
keywords: "Aspose Cells Cloud, REST API, Excel, Çalışma Sayfası, Hücre Özellikleri, Hücre Özelliklerini Al"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasında belirli bir hücrenin veya önceden tanımlanmış hücre yöntemlerinin özelliklerini nasıl alacağınızı öğrenin."
---

Bu REST API, bir Excel dosyasında belirli bir hücreyi almayı gösterir.

## REST API

```bash
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}
```

## Güvenlik ve Kimlik Doğrulama

Aspose.Cells Cloud API’leri güvenlidir ve [JWT belirteci tabanlı kimlik doğrulamaya](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) ihtiyaç duyar.

### İstek Parametreleri


| Parametre Adı      | Tür     | Konum | Açıklama                                                                                                                                                                           |
| ------------------ | ------- | ----- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **name**           | string  | path  | Excel belgesinin adı.                                                                                                                                                              |
| **sheetName**      | string  | path  | Hücreyi içeren çalışma sayfasının adı.                                                                                                                                             |
| **cellOrMethodName** | string | path  | Hücre adı veya önceden tanımlanmış bir yöntem adı (örn. `firstcell`, `endcell`, `maxrow`, `maxdatarow`, `maxcolumn`, `maxdatacolumn`, `minrow`, `mindatarow`, `mincolumn`, `mindatacolumn`). |
| **folder**         | string  | query | Belgenin depolandığı klasör.                                                                                                                                                       |
| **storageName**    | string  | query | Depolama hizmetinin adı.                                                                                                                                                           |

## **Yanıt**

Hücre Yanıtı (CellResponse) döner.

- **Yanıt Alanları Genel Bakış**

| Alan            | Tür     | Açıklama                                            |
| --------------- | ------- | --------------------------------------------------- |
| `Name`          | string  | Hücrenin adresi (örn. `F341`).                       |
| `Row`           | integer | Sıfır tabanlı satır indeksi.                         |
| `Column`        | integer | Sıfır tabanlı sütun indeksi.                         |
| `Value`         | string  | Hücrenin gösterilen değeri.                          |
| `Type`          | string  | Hücrenin veri türü (örn. `IsString`).               |
| `Formula`       | string  | Hücre bir formül içeriyorsa formül metni.           |
| `IsFormula`     | bool    | Hücrenin formül içerip içermediğini belirtir.        |
| `IsMerged`      | bool    | Hücrenin birleştirilmiş bir aralık parçası olup olmadığını belirtir. |
| `IsArrayHeader` | bool    | Hücrenin bir dizi başlığı olup olmadığını belirtir.  |
| `IsInArray`     | bool    | Hücrenin bir dizinin içinde olup olmadığını belirtir. |
| `IsErrorValue`  | bool    | Hücrenin bir hata değeri içerip içermediğini belirtir. |
| `IsInTable`     | bool    | Hücrenin bir tablonun içinde olup olmadığını belirtir. |
| `IsStyleSet`    | bool    | Hücreye bir stil uygulanıp uygulanmadığını belirtir. |
| `HtmlString`    | string  | Hücre değerinin HTML ile kodlanmış gösterimi.        |
| `Style.link`    | object  | Stil kaynağına yönelik hiperbağlantı.                |


```json
{
  "Status":"OK",
  "Code":200,
  "Cell":{
    "Name":"A1",
    "Row": 0,
    "Column":0,
    "Value": "Hello Aspose.Cells",
    "Type":"String",
    "Formula" : "",
    ...
  }
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                           |
|-----|-----------------------------|----------------------------------------------------|
| 200 | OK                          | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Bad Request                 | Eksik veya geçersiz parametreler (örn. desteklenmeyen dosya türü). |
| 401 | Unauthorized                | Geçersiz veya eksik JWT belirteci.                 |
| 413 | Payload Too Large           | Yüklenen dosya boyut sınırını aşıyor.               |
| 500 | Internal Server Error       | Beklenmeyen sunucu hatası.                         |

## SDK’lar ile GetWorksheetCell API’sini Nasıl Kullanılır

### GetWorksheetCell API Spesifikasyonu

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize izin verir.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye nasıl istek yapıldığını göstermektedir.
{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X GET "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3?client_id=YOUR_CLIENT_ID&client_secret=YOUR_CLIENT_SECRET" \
     -H "Accept: application/json"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "A3",
    "Row": 2,
    "Column": 0,
    "Value": "Statistical",
    "Type": "IsString",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">Statistical</Font>",
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    },
    "link": {
      "Href": "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3",
      "Rel": "self"
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme sürecini hızlandırmak için en etkili yoldur. Bir SDK, düşük seviye detayları soyutlayarak projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, Aspose.Cells web servislerini çeşitli SDK’larla nasıl çağırdığınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCell.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCell.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCell.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCell.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCell.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCell.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCell.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCell.go" >}}

{{< /tab >}}

{{< /tabs >}}

### Belirli bir hücreyi nasıl alırız?

- [Çalışma Sayfasından Hücre Verisi Al](/tr/cells/get-cell-data-from-a-worksheet/)
- [Excel Çalışma Sayfasından İlk Hücreyi Al](/tr/cells/get-first-cell-from-excel-worksheet/)
- [Excel Çalışma Sayfasının Son Hücresi](/tr/cells/get-last-cell-of-excel-worksheet/)
- [Excel Çalışma Sayfasından MaxRow Al](/tr/cells/get-maxrow-from-excel-worksheet/)
- [Excel Çalışma Sayfasından MaxDataRow Al](/tr/cells/get-maxdatarow-from-excel-worksheet/)
- [Excel Çalışma Sayfasından MaxColumn Al](/tr/cells/get-maxcolumn-from-excel-worksheet/)
- [Excel Çalışma Sayfasından MaxDataColumn Al](/tr/cells/get-maxdatacolumn-from-excel-worksheet/)
- [Excel Çalışma Sayfasından MinRow Al](/tr/cells/get-minrow-from-excel-worksheet/)
- [Excel Çalışma Sayfasından MinDataRow Al](/tr/cells/get-mindatarow-from-excel-worksheet/)
- [Excel Çalışma Sayfasından MinColumn Al](/tr/cells/get-mincolumn-from-excel-worksheet/)
- [Excel Çalışma Sayfasından MinDataColumn Al](/tr/cells/get-mindatacolumn-from-excel-worksheet/)