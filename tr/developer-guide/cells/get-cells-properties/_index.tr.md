---
title: Cells Özelliğini Alın
type: docs
url: /tr/get-cells-properties/
weight: 130
kwords: Excel, Office Cloud, REST API, Elektronik Tablo, PDF, CSV, Json, Markdwon, Cells Özelliklerini Al
---
Bu REST API, Excel dosyasında `get a specific cell`'in nasıl yapılacağını gösterir.

## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}
 
```
 İstek parametreleri şunlardır:
 
| Parametre adı| Tip| Yol/Sorgu Dizesi/HTTPBody|Tanım|
|:- |:- |:- |:- |
| isim| sicim| yol| Belge adı.|
| sayfaAdı| sicim| yol| Çalışma sayfası adı.|
| hücreVeyaYöntemAdı| sicim| yol|Hücrenin veya yöntemin adı. (Yöntem adı değeri: ilk hücre, son hücre, maxrow, maxdatarow, maxcolumn, maxdatacolumn, minrow, mindatarow, mincolumn, mindatacolumn ve cellName.)|
| dosya| sicim| sorgu| Belgenin klasörü.|
| depolamaAdı| sicim| sorgu| depolama adı.|
 
[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell) herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.


- **Belirli bir hücre nasıl alınır**

   - [Çalışma Sayfasından Hücre Verilerini Alma](/cells/tr/get-cell-data-from-a-worksheet/)
   - [Excel Çalışma Sayfasından İlk Hücreyi Alın](/cells/tr/get-first-cell-from-excel-worksheet/)
   - [Excel Çalışma Sayfasının Son Hücresini Al](/cells/tr/get-last-cell-of-excel-worksheet/)
   - [MaxRow'u Excel Çalışma Sayfasından edinin](/cells/tr/get-maxrow-from-excel-worksheet/)
   - [Excel Çalışma Sayfasından MaxDataRow'u edinin](/cells/tr/get-maxdatarow-from-excel-worksheet/)
   - [Excel Çalışma Sayfasından MaxColumn'u edinin](/cells/tr/get-maxcolumn-from-excel-worksheet/)
   - [Excel Çalışma Sayfasından MaxDataColumn'u edinin](/cells/tr/get-maxdatacolumn-from-excel-worksheet/)
   - [Excel Çalışma Sayfasından MinRow'u edinin](/cells/tr/get-minrow-from-excel-worksheet/)
   - [MinDataRow'u Excel Çalışma Sayfasından alın](/cells/tr/get-mindatarow-from-excel-worksheet/)
   - [Excel Çalışma Sayfasından MinColumn'u edinin](/cells/tr/get-mincolumn-from-excel-worksheet/)
   - [MinDataColumn'u Excel Çalışma Sayfasından alın](/cells/tr/get-mindatacolumn-from-excel-worksheet/)
