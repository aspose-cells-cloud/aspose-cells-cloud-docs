---
title: Storag kullanarak Verileri İçe Aktar
second_title: Aspose.Cells Cloud Documen
linktitle: Storag ile verileri içe aktarın
type: docs
url: /tr/import/with-using-storage/
aliases: [/import-data-into-excel-worksheet/, /import-data-into-worksheet/ , /import-data-in-excel-worksheet/, /import-data/]
description: "Cells.Cloud API, Excel için çalıştır: Verileri Excel Çalışma Sayfasına Aktar"
weight: 10
---
Bu REST API, `import data`'i Excel dosyasına gösterir.
 
## RSET API
 
```bash
 
POST http://api.aspose.cloud/v3.0/cells/{name}/importdata
 
```
 İstek parametreleri şunlardır:
 
| Parametre adı| Tip| Yol/Sorgu Dizesi/HTTPBody|Tanım|
|:- |:- |:- |:- |
| isim| sicim| yol||
| dosya| sicim| sorgu||
| depolamaAdı| sicim| sorgu| depolama adı.|
| importData|| vücut||

**Verileri içe aktarma seçenekleri parametreleri**tarif edilir[referans bağlantısı](/cells/tr/import/#import-data-option-parameter).

 
 bu[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) herkesin erişebileceği bir programlama arabirimi tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.
 
Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'e nasıl çağrı yapılacağını gösterir.
 
{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}
 
{{< tab tabNum="1" >}}
 
```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/Book1.xlsx/importdata" \
-X POST \
-D "{\"Data\":[1,2,4],\"DestinationWorksheet\":\"Sheet1\",\"FirstRow\":1,\"FirstColumn\":2,\"IsVertical\":true,\"IsInsert\":true,\"importDataType\":\"IntArray\"}" \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"

```
 
{{< /tab >}}
 
{{< tab tabNum="2" >}}
 
```bash
{
"Code": 200,
"Status": "OK"
}
 
```
 
{{< /tab >}}
 
{{< /tabs >}}
 
 
Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanılarak Aspose.Cells web hizmetlerine nasıl çağrı yapılacağını gösterir:

