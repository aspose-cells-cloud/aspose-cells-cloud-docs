---
title: Cells Mülkiyetini Alın
type: docs
url: /tr/get-cells-properties/
weight: 130
---
Bu REST API, bir Excel dosyasında `get a specific cell`'in nasıl yapıldığını gösterir.

## RSET API
 
```bash
 
GET http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/cells/{cellOrMethodName}
 
```
 İstek parametreleri şunlardır:
 
| Parametre adı| Tip| Yol/Sorgu Dizesi/HTTPBody|Tanım|
|:- |:- |:- |:- |
| isim| sicim| yol| Belge adı.|
| sayfaAdı| sicim| yol| Çalışma sayfası adı.|
| hücreVeyaYöntemAdı| sicim| yol|Hücrenin veya yöntemin adı. (Metod adı değeri: firstcell, endcell, maxrow, maxdatarow, maxcolumn, maxdatacolumn, minrow, mindatarow, mincolumn, mindatacolumn ve cellName.)|
| dosya| sicim| sorgu| Belgenin klasörü.|
| depolamaAdı| sicim| sorgu| depolama adı.|
 
 bu[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Cells/GetWorksheetCell) herkesin erişebileceği bir programlama arabirimi tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.


- **Belirli bir hücre nasıl elde edilir**

   - [Bir Çalışma Sayfasından Hücre Verilerini Alma](/cells/tr/get-cell-data-from-a-worksheet/)
   - [Excel Çalışma Sayfasından İlk Hücreyi Alın](/cells/tr/get-first-cell-from-excel-worksheet/)
   - [Excel Çalışma Sayfasının Son Hücresini Alın](/cells/tr/get-last-cell-of-excel-worksheet/)
   - [Excel Çalışma Sayfasından MaxRow'u Alın](/cells/tr/get-maxrow-from-excel-worksheet/)
   - [Excel Çalışma Sayfasından MaxDataRow'u Alın](/cells/tr/get-maxdatarow-from-excel-worksheet/)
   - [Excel Çalışma Sayfasından MaxColumn'u Alın](/cells/tr/get-maxcolumn-from-excel-worksheet/)
   - [Excel Çalışma Sayfasından MaxDataColumn'u Alın](/cells/tr/get-maxdatacolumn-from-excel-worksheet/)
   - [Excel Çalışma Sayfasından MinRow'u Alın](/cells/tr/get-minrow-from-excel-worksheet/)
   - [Excel Çalışma Sayfasından MinDataRow'u Alın](/cells/tr/get-mindatarow-from-excel-worksheet/)
   - [Excel Çalışma Sayfasından MinColumn'u Alın](/cells/tr/get-mincolumn-from-excel-worksheet/)
   - [Excel Çalışma Sayfasından MinDataColumn'u Alın](/cells/tr/get-mindatacolumn-from-excel-worksheet/)
