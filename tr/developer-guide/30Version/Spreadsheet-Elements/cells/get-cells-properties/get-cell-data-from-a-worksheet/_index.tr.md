---
title: "Çalışma Sayfasından Hücre Verilerini Alın"
type: docs
url: /tr/get-cell-data-from-a-worksheet/
weight: 10
keywords: "Aspose.Cells Cloud, hücre verisi al, Excel API, REST API, hücre değeri, çalışma sayfası API, Aspose API örneği"
description: "Aspose.Cells Cloud REST API’sini (v3.0) kullanarak bir Excel çalışma sayfasından tek bir hücrenin değerini, türünü ve stilini alın. cURL ve SDK örnekleri, parametreler ve hata işleme içerir."
---

Bu REST API, **`cellOrMethodName`** parametresi bir hücre adını (örneğin `A3` gibi A1-stilinde bir adresi) belirttiğinde bir Excel çalışma sayfasından bir hücreyi getirir.

- **cURL Örneği**

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```shell
curl -X GET "https://api.aspose.com/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1/cells/A3" \
     -H "Authorization: Bearer <access_token>" \
     -H "Content-Type: application/json" \
     -H "Accept: application/json"
```

**Parametreler**

| Parametre          | Tür    | Açıklama                                                  | Gerekli |
|--------------------|--------|-----------------------------------------------------------|---------|
| `cellOrMethodName` | string | İlk hücreyi almak için `firstcell` olarak ayarlanmalıdır. | Evet    |
| `fileName`         | string | Çalışma kitapası dosyasının adı (örneğin `myWorkbook.xlsx`). | Evet    |
| `worksheet`        | string | Çalışma sayfasının adı (örneğin `Sheet1`).                | Evet    |
| `Authorization`    | header | Kimlik doğrulama için Bearer jetonu.                      | Evet    |

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Cell": {
    "Name": "A3",
    "Row": 2,
    "Column": 0,
    "Value": "Category",
    "Type": "IsString",
    "IsFormula": false,
    "IsMerged": false,
    "IsArrayHeader": false,
    "IsInArray": false,
    "IsErrorValue": false,
    "IsInTable": false,
    "IsStyleSet": false,
    "HtmlString": "<Font Style=\"FONT-FAMILY: Calibri;FONT-SIZE: 11pt;COLOR: #ffffff;\">Category</Font>",
    "Style": {
      "link": {
        "Href": "/style",
        "Rel": "self"
      }
    }
  },
  "Code": "200",
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

- **Aspose.Cells Cloud SDK’larını Kullanma**

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