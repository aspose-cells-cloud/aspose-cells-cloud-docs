---
title: "Adlandırılmış aralık temel alınarak hücre verilerini alın"
second_title: "Belge"
linktitle: "Değerler"
type: docs
url: /ranges/get/values/
aliases: [/get-cells-data-based-on-named-range/]
keywords: "Aspose.Cells, Bulut, REST API, Excel, adlandırılmış aralık, hücre değerleri, çalışma sayfası"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasındaki adlandırılmış bir aralıktan hücre değerlerini alın. Hizmet, birden fazla SDK (C#, Java, PHP, Ruby, Node.js, Python, Perl, Go) aracılığıyla mevcuttur ve geniş bir geliştirme platformu yelpazesinde çalışır."
weight: 20
ArticleTitle: "Adlandırılmış Aralık Temel alınarak Hücre Verilerini Alın – Aspose.Cells Cloud API"
---

**Ön Koşullar**

- Uygun kapsama alanına sahip geçerli bir JWT erişim belirteci.  
- Çalışma kitabının Aspose Cloud depolama alanına (veya belirtilen klasöre) yüklenmiş olması.  
- Varsayılan olmayan bir depo kullanıyorsanız hedef depo adının sağlandığından emin olun.

Bu REST API, bir adlandırılmış aralık veya satır-sütun indeksleri ile tanımlanan bir aralık içindeki hücrelerin listesini döndürür.

Bu işlem, geliştiricilerin bir Excel çalışma sayfasındaki belirli bir adlandırılmış aralığa ait hücre değerlerini programlı olarak almasını sağlar. `namedRange` tanımlayıcısı veya açık satır ve sütun indeksleri sağlanarak, API, hücre adresi, satır, sütun, değer, veri türü ve biçimlendirme bilgisi dahil olmak üzere detaylı bir hücre listesi döndürür. Yanıt, veri odaklı uygulamaları sürdürmek, raporlar oluşturmak veya sunucu tarafında daha fazla hesaplama yapmak için kullanılabilir. Aspose.Cells Cloud hizmeti, SDK’ları aracılığıyla birden fazla programlama dilini destekler, böylece geliştirme platformundan bağımsız olarak sorunsuz entegrasyon sağlar. HTTPS kullanımı, verilerin güvenli bir şekilde iletilmesini garanti eder ve API, REST prensiplerine uyar, başarı ve hata durumları için standart HTTP durum kodlarını döndürür.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/value
```

### **İstek parametreleri**

| Parametre Adı   | Tür      | Konum  | Açıklama                                                                                       |
| ---------------- | -------- | ------ | ---------------------------------------------------------------------------------------------- |
| name             | string   | path   | Çalışma kitabının dosya adı.                                                                   |
| sheetName        | string   | path   | Çalışma kitabındaki çalışma sayfasının adı.                                                    |
| namedRange       | string   | query  | Alınacak adlandırılmış aralık, örneğin `A1:B2` veya `range_name1`.                             |
| firstRow         | integer  | query  | Aralığın ilk satırının sıfır tabanlı indeksi (`namedRange` sağlanmadığında kullanılır).        |
| firstColumn      | integer  | query  | Aralığın ilk sütununun sıfır tabanlı indeksi (`namedRange` sağlanmadığında kullanılır).        |
| rowCount         | integer  | query  | Aralığa dahil edilecek satır sayısı.                                                           |
| columnCount      | integer  | query  | Aralığa dahil edilecek sütun sayısı.                                                           |
| folder           | string   | query  | Çalışma kitabını içeren klasör.                                                                |
| storageName      | string   | query  | Çalışma kitabının bulunduğu bulut depo adı.                                                    |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/Ranges/GetWorksheetCellsRangeValue), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından yapmanızı sağlar.

Aspose.Cells web hizmetlerini kolayca çağırmak için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, bir adlandırılmış aralıktan hücre değerlerini nasıl isteyeceğinizi göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/value?namerange=data" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "CellsList": [
    {
      "Name": "B10",
      "Row": 9,
      "Column": 1,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "C10",
      "Row": 9,
      "Column": 2,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "D10",
      "Row": 9,
      "Column": 3,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "E10",
      "Row": 9,
      "Column": 4,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "F10",
      "Row": 9,
      "Column": 5,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "G10",
      "Row": 9,
      "Column": 6,
      "Value": null,
      "Type": "IsNull",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\"></Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    },
    {
      "Name": "H10",
      "Row": 9,
      "Column": 7,
      "Value": "a8",
      "Type": "IsString",
      "Formula": null,
      "IsFormula": false,
      "IsMerged": false,
      "IsArrayHeader": false,
      "IsInArray": false,
      "IsErrorValue": false,
      "IsInTable": false,
      "IsStyleSet": false,
      "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #000000;\">a8</Font>",
      "Style": {
        "link": {
          "Href": "/style",
          "Rel": "self",
          "Title": null,
          "Type": null
        }
      },
      "Worksheet": null,
      "link": null
    }
  ],
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Güvenlik Notu:** API’yi çağırırken her zaman HTTPS kullanın. Hizmet düz HTTP’yi desteklemez; HTTPS kullanımı, isteğin şifrelendiğinden ve güvenlik en iyi uygulamalarına uygun olduğundan emin olunur.

**HTTP Durum Kodları**

| Kod  | Anlamı                      | Açıklama                                               |
|------|-----------------------------|--------------------------------------------------------|
| 200  | OK (Tamam)                  | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400  | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401  | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci. |
| 413  | Payload Too Large (Çok Büyük Yük) | Yüklenen dosya boyut sınırını aşıyor. |
| 500  | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası. |

**Örnek hata yanıtı (400 Bad Request)**

```json
{
  "Code": 400,
  "Status": "Bad Request",
  "Message": "'namedRange' parametresi eksik veya geçersiz."
}
```

> **İpucu:** API, `firstRow` ve `firstColumn` için sıfır tabanlı indeksler kullanır. Örneğin, çalışma sayfasının ilk satırı `0`dır.

## Bulut SDK Ailesi

SDK kullanmak, geliştirmeyi hızlandırmanın en verimli yoludur. Bir SDK, düşük seviyeli ayrıntıları soyutlar ve iş mantığına odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web hizmetlerini nasıl çağıracağınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetCellsRangeValue.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetCellsRangeValue.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetCellsRangeValue.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetCellsRangeValue.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetCellsRangeValue.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetCellsRangeValue.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetCellsRangeValue.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetCellsRangeValue.go" >}}

{{< /tab >}}

{{< /tabs >}}
---