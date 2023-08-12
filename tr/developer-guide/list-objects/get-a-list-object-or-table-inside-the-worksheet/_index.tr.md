---
title: Excel çalışma sayfasında bir liste nesnesi alın
second_title: Aspose.Cells Cloud Documen
linktitle: Ge
type: docs
url: /tr/list-objects/get/
aliases: [/get-a-list-object-or-table-inside-the-worksheet/,/tables/get/]
keywords: Get a list object(table) into an Excel worksheet
description: Aspose.Cells Cloud REST API, bir Excel çalışma sayfasına bir liste nesnesi (tablo) almayı destekler. SDK, geliştirme dili türlerini destekler. Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve Swift'i içerir
weight: 9
---
Bu REST API, `get`'e bir liste nesnesi bilgisini dizine göre gösterir veya `list object`'i bir Excel çalışma sayfasındaki farklı biçim dosyasına dönüştürür.

## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/listobjects/{listobjectindex}
 
```
 İstek parametreleri şunlardır:
 
| Parametre adı| Tip| Yol/Sorgu Dizesi/HTTPBody|Tanım|
|:- |:- |:- |:- |
| isim| sicim| yol| Belge adı.|
| sayfaAdı| sicim| yol| Çalışma sayfası adı.|
| listobjectindex| tamsayı| yol| liste nesne dizini.|
| biçim| sicim| sorgu| dışa aktarma biçimi.|
| dosya| sicim| sorgu| Belgenin klasörü.|
| depolamaAdı| sicim| sorgu| depolama adı.|
 
 bu[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/ListObjects/GetWorksheetListObject) herkesin erişebileceği bir programlama arabirimi tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.
 
Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'e nasıl çağrı yapılacağını gösterir.
 
{{< tabs tabTotal="2" tabID="11" tabName11="Request" tabName12="Response" >}}
 
{{< tab tabNum="11" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/1" \
-X GET \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
 
```
 
{{< /tab >}}
 
{{< tab tabNum="12" >}}
 
```bash
{
	"ListObject": {
		"AutoFilter": {
			"FilterColumns": [],
			"Range": "B2:F11",
			"Sorter": {
				"CaseSensitive": false,
				"HasHeaders": false,
				"KeyList": [],
				"SortLeftToRight": false
			}
		},
		"DisplayName": "Table3",
		"StartColumn": 1,
		"StartRow": 1,
		"EndColumn": 5,
		"EndRow": 10,
		"ListColumns": [{
			"Name": "Column1",
			"Range": {
				"ColumnCount": 1,
				"ColumnWidth": 8.5,
				"FirstColumn": 1,
				"FirstRow": 1,
				"RefersTo": "=Sheet1!$B$2:$B$11",
				"RowCount": 10,
				"RowHeight": 13.5,
				"Worksheet": "Sheet1"
			},
			"TotalsCalculation": "None"
		}, {
			"Name": "Column2",
			"Range": {
				"ColumnCount": 1,
				"ColumnWidth": 8.5,
				"FirstColumn": 2,
				"FirstRow": 1,
				"RefersTo": "=Sheet1!$C$2:$C$11",
				"RowCount": 10,
				"RowHeight": 13.5,
				"Worksheet": "Sheet1"
			},
			"TotalsCalculation": "None"
		}, {
			"Name": "Column3",
			"Range": {
				"ColumnCount": 1,
				"ColumnWidth": 8.5,
				"FirstColumn": 3,
				"FirstRow": 1,
				"RefersTo": "=Sheet1!$D$2:$D$11",
				"RowCount": 10,
				"RowHeight": 13.5,
				"Worksheet": "Sheet1"
			},
			"TotalsCalculation": "None"
		}, {
			"Name": "Column4",
			"Range": {
				"ColumnCount": 1,
				"ColumnWidth": 8.5,
				"FirstColumn": 4,
				"FirstRow": 1,
				"RefersTo": "=Sheet1!$E$2:$E$11",
				"RowCount": 10,
				"RowHeight": 13.5,
				"Worksheet": "Sheet1"
			},
			"TotalsCalculation": "None"
		}, {
			"Name": "Column5",
			"Range": {
				"ColumnCount": 1,
				"ColumnWidth": 8.5,
				"FirstColumn": 5,
				"FirstRow": 1,
				"RefersTo": "=Sheet1!$F$2:$F$11",
				"RowCount": 10,
				"RowHeight": 13.5,
				"Worksheet": "Sheet1"
			},
			"TotalsCalculation": "None"
		}],
		"ShowHeaderRow": true,
		"ShowTableStyleColumnStripes": false,
		"ShowTableStyleFirstColumn": false,
		"ShowTableStyleLastColumn": false,
		"ShowTableStyleRowStripes": true,
		"ShowTotals": false,
		"TableStyleName": "None",
		"TableStyleType": "None",
		"link": {
			"Href": "api-qa.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/listobjects/0",
			"Rel": "self"
		}
	},
	"Code": 200,
	"Status": "OK"
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
## Bulut SDK Ailesi
 
 Bir SDK kullanmak, geliştirmeyi hızlandırmanın en iyi yoludur. Bir SDK, alt düzey ayrıntılarla ilgilenir ve proje görevlerinize odaklanmanızı sağlar. Lütfen kontrol edin[GitHub deposu](https://github.com/aspose-cells-cloud) Aspose.Cells Bulut SDK'larının tam listesi için.
 
Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanılarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını gösterir:
 
Bu REST API, farklı biçim dosyasına bir excel `listobject` nesnesi alır.


{{< tabs tabTotal="9" tabID="1" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Android" tabName7="Perl" tabName8="Go" tabName9="Python" >}}

{{< tab tabNum="1" >}}



{{< /tab >}}

{{< tab tabNum="2" >}}


{{< /tab >}}

{{< tab tabNum="3" >}}



{{< /tab >}}

{{< tab tabNum="4" >}}


{{< /tab >}}

{{< tab tabNum="5" >}}


{{< /tab >}}

{{< tab tabNum="6" >}}


{{< /tab >}}

{{< tab tabNum="7" >}}


{{< /tab >}}

{{< tab tabNum="8" >}}


{{< /tab >}}

{{< tab tabNum="9" >}}


{{< /tab >}}

{{< /tabs >}}
