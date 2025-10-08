---
title: Excel dosyalarına veri aktarın ve Excel dosyalarına veri aktarın
second_title: Documen
linktitle: İthalat ve İhracat Verileri
type: docs
url: /tr/data-import-and-export/
keywords: Excel data import vs. Direct database access; Batch data import vs. Row-by-row data writing; Automated data export vs. Manual data extraction
description: Grafikler, tablolar ve diğer veri görselleştirme öğelerini içerebilen yeni belgeler veya raporlar oluşturun
weight: 25
kwords: Excel Veri içe aktarımı ve doğrudan veritabanı erişimi; Toplu veri içe aktarımı ve satır satır veri yazma; Otomatik veri dışa aktarımı ve manuel veri çıkarma.
---
Aspose.Cells Bulut API, çeşitli veri kaynaklarından veri içe aktarmayı destekler ve Excel'den verileri, grafikleri ve çizelgeleri Excel, CSV, PDF, HTML, PNG vb. dahil olmak üzere farklı biçimlerde dışa aktarabilir. Bu, veri yönetimini ve paylaşımını basit ve verimli hale getirir.

## Çeşitli veri kaynaklarından veri nasıl içe aktarılır?

Excel dosyasına veri aktarmak karmaşık bir işlemdir. Karmaşıklığa katkıda bulunan birçok faktör vardır ve bu nedenle dışa aktarma işlemi sırasında dikkate alınmalıdır. Çeşitli format ve veri türlerini dosyaya hassas ve profesyonel bir kalitede aktarabilme özelliği, Aspose.Cells Cloud'un en önemli özelliklerinden biridir.

### Veri API'leri Bilgilerini İçe Aktar

Excel dosyasına veya birden fazla Excel dosyasına veri aktarmak için aşağıdaki API'ler sağlanır:

|API|Tanım|
|:- |:- |
|[POST /hücreler/içe aktarma](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)|Depolama alanı kullanmadan Excel dosyalarına veri aktarın.|
|[POST /hücreler/{ad}/impportdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData)|Depolamayı kullanarak Excel dosyasına veri aktarın.|

### İstek Parametreleri

#### Depolama alanı kullanmadan

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi|Tanım|
|:- |:- |:- |:- |
| dosya| dosya| formData| Yüklenecek dosya|
| İçe Aktarma Seçeneği| İçe Aktarma Seçenekleri| HTTPGövdesi| IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData/Picture|

#### Depolama kullanımıyla

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi|Tanım|
|:- |:- |:- |:- |
| isim| sicim| yol||
| dosya| sicim| sorgu||
| depolamaAdı| sicim| sorgu| depolama adı.|
| importData|| vücut||

#### Veri içe aktarma seçeneği parametresi

**Önemli parametreler aşağıdaki tabloda açıklanmıştır**:

{{< tabs tabTotal="11" tabID="1" tabName1="ImportBatchDataOption" tabName2="ImportCSVDataOption" tabName3="ImportPictureOption" tabName4="Import2DimensionIntArrayOption" tabName5="Import2DimensionDoubleArrayOption" tabName6="Import2DimensionStringArrayOption" tabName7="ImportIntegerArrayOption" tabName8="ImportDoubleArrayOption" tabName9="ImportStringArrayOption" tabName10="CellValue" tabName11="FileSource" >}}
{{< tab tabNum="1" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parametre</th><th scope="col">Tip</th> <th scope="col">Tanım</th></tr>
  </thead>
  <tbody>
    <tr> <td>Toplu Veri</td><td>Liste<CellValue></td> <td>toplu veri</td> </tr>
    <tr> <td>Hedef Çalışma Sayfası</td><td> Sicim</td><td> Hedef çalışma kağıdının adı.</td></tr>
    <tr><td>IsInsert</td><td>Sicim</td><td>doğru/yanlış.</td></tr>
    <tr><td>Veri Türünü İçe Aktar</td><td> Sicim</td><td>İki BoyutluDizeTopluVeriDizisi</td></tr>
    <tr> <td>Kaynak</td><td> Dosya Kaynağı</td><td>BatchData parametresi boş olduğunda veri dosyasının konumunu gösterir.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="2" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parametre</th><th scope="col">Tip</th> <th scope="col">Tanım</th></tr>
  </thead>
  <tbody>
    <tr> <td>Sayısal Verileri Dönüştür</td><td>Sicim</td> <td>doğru/yanlış.</td> </tr>
    <tr> <td>İlk Sıra</td><td>int</td> <td></td> </tr>
    <tr> <td>İlkSütun</td><td>int</td><td></td></tr>
    <tr><td>AyırıcıDize</td><td> Sicim</td> <td></td></tr>
    <tr> <td>Hedef Çalışma Sayfası</td><td> Sicim</td><td> Hedef çalışma kağıdının adı.</td></tr>
    <tr><td>ÖzelAyrıştırıcılar</td><td>Liste<CustomParserConfig></td><td></td></tr>
    <tr><td>Veri Türünü İçe Aktar</td><td> Sicim</td><td>CSVVerileri</td></tr>
    <tr> <td>Kaynak</td><td> Dosya Kaynağı</td><td>BatchData parametresi boş olduğunda veri dosyasının konumunu gösterir.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="3" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parametre</th><th scope="col">Tip</th> <th scope="col">Tanım</th></tr>
  </thead>
  <tbody>
    <tr> <td>İlk Sıra</td><td>int</td> <td></td> </tr>
    <tr> <td>İlkSütun</td><td>int</td><td></td></tr>
    <tr><td>Dikey</td><td>Sicim</td><td>doğru/yanlış.</td></tr>
    <tr><td>Veri</td><td> Sicim[]</td> <td></td></tr>
    <tr> <td>Hedef Çalışma Sayfası</td><td> Sicim</td><td> Hedef çalışma kağıdının adı.</td></tr>
    <tr><td>IsInsert</td><td>Sicim</td><td>doğru/yanlış.</td></tr>
    <tr><td>Veri Türünü İçe Aktar</td><td> Sicim</td><td>Resim</td></tr>
    <tr> <td>Kaynak</td><td> Dosya Kaynağı</td><td>BatchData parametresi boş olduğunda veri dosyasının konumunu gösterir.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="4" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parametre</th><th scope="col">Tip</th> <th scope="col">Tanım</th></tr>
  </thead>
  <tbody>
    <tr> <td>İlk Sıra</td><td>int</td> <td></td> </tr>
    <tr> <td>İlkSütun</td><td>int</td><td></td></tr>
    <tr><td>Veri</td><td> Tam sayı[,]</td> <td></td></tr>
    <tr> <td>Hedef Çalışma Sayfası</td><td> Sicim</td><td> Hedef çalışma kağıdının adı.</td></tr>
    <tr><td>IsInsert</td><td>Sicim</td><td>doğru/yanlış.</td></tr>
    <tr><td>Veri Türünü İçe Aktar</td><td> Sicim</td><td>İki Boyutlu Tam Dizi</td></tr>
    <tr> <td>Kaynak</td><td> Dosya Kaynağı</td><td>BatchData parametresi boş olduğunda veri dosyasının konumunu gösterir.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="5" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parametre</th><th scope="col">Tip</th> <th scope="col">Tanım</th></tr>
  </thead>
  <tbody>
    <tr> <td>İlk Sıra</td><td>int</td> <td></td> </tr>
    <tr> <td>İlkSütun</td><td>int</td><td></td></tr>
    <tr><td>Veri</td><td> Çift[,]</td> <td></td></tr>
    <tr> <td>Hedef Çalışma Sayfası</td><td> Sicim</td><td> Hedef çalışma kağıdının adı.</td></tr>
    <tr><td>IsInsert</td><td>Sicim</td><td>doğru/yanlış.</td></tr>
    <tr><td>Veri Türünü İçe Aktar</td><td> Sicim</td><td>İki Boyutlu Çift Dizi</td></tr>
    <tr> <td>Kaynak</td><td> Dosya Kaynağı</td><td>BatchData parametresi boş olduğunda veri dosyasının konumunu gösterir.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="6" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parametre</th><th scope="col">Tip</th> <th scope="col">Tanım</th></tr>
  </thead>
  <tbody>
    <tr> <td>İlk Sıra</td><td>int</td> <td></td> </tr>
    <tr> <td>İlkSütun</td><td>int</td><td></td></tr>
    <tr><td>Veri</td><td> Sicim[,]</td> <td></td></tr>
    <tr> <td>Hedef Çalışma Sayfası</td><td> Sicim</td><td> Hedef çalışma kağıdının adı.</td></tr>
    <tr><td>IsInsert</td><td>Sicim</td><td>doğru/yanlış.</td></tr>
    <tr><td>Veri Türünü İçe Aktar</td><td> Sicim</td><td>İki BoyutluDizeDizisi</td></tr>
    <tr> <td>Kaynak</td><td> Dosya Kaynağı</td><td>BatchData parametresi boş olduğunda veri dosyasının konumunu gösterir.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="7" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parametre</th><th scope="col">Tip</th> <th scope="col">Tanım</th></tr>
  </thead>
  <tbody>
    <tr> <td>İlk Sıra</td><td>int</td> <td></td> </tr>
    <tr> <td>İlkSütun</td><td>int</td><td></td></tr>
    <tr><td>Dikey</td><td>Sicim</td><td>doğru/yanlış.</td></tr>
    <tr><td>Veri</td><td> Tam sayı[]</td> <td></td></tr>
    <tr> <td>Hedef Çalışma Sayfası</td><td> Sicim</td><td> Hedef çalışma kağıdının adı.</td></tr>
    <tr><td>IsInsert</td><td>Sicim</td><td>doğru/yanlış.</td></tr>
    <tr><td>Veri Türünü İçe Aktar</td><td> Sicim</td><td>TamsayıDizisi</td></tr>
    <tr> <td>Kaynak</td><td> Dosya Kaynağı</td><td>BatchData parametresi boş olduğunda veri dosyasının konumunu gösterir.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="8" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parametre</th><th scope="col">Tip</th> <th scope="col">Tanım</th></tr>
  </thead>
  <tbody>
    <tr> <td>İlk Sıra</td><td>int</td> <td></td> </tr>
    <tr> <td>İlkSütun</td><td>int</td><td></td></tr>
    <tr><td>Dikey</td><td>Sicim</td><td>doğru/yanlış.</td></tr>
    <tr><td>Veri</td><td> Çift[]</td> <td></td></tr>
    <tr> <td>Hedef Çalışma Sayfası</td><td> Sicim</td><td> Hedef çalışma kağıdının adı.</td></tr>
    <tr><td>IsInsert</td><td>Sicim</td><td>doğru/yanlış.</td></tr>
    <tr><td>Veri Türünü İçe Aktar</td><td> Sicim</td><td>ÇiftDizi</td></tr>
    <tr> <td>Kaynak</td><td> Dosya Kaynağı</td><td>BatchData parametresi boş olduğunda veri dosyasının konumunu gösterir.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="9" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parametre</th><th scope="col">Tip</th> <th scope="col">Tanım</th></tr>
  </thead>
  <tbody>
    <tr> <td>Sol Üst Satır</td><td>int</td> <td></td> </tr>
    <tr> <td>Sol Üst Sütun</td><td>int</td><td></td></tr>
    <tr> <td>AltSağSatır</td><td>int</td> <td></td> </tr>
    <tr> <td>AltSağSütun</td><td>int</td><td></td></tr>
    <tr><td>Dosya adı</td><td>Sicim</td><td></td></tr>
    <tr><td>Veri</td><td> Sicim</td> <td></td></tr>
    <tr> <td>Hedef Çalışma Sayfası</td><td> Sicim</td><td> Hedef çalışma kağıdının adı.</td></tr>
    <tr><td>IsInsert</td><td>Sicim</td><td>doğru/yanlış.</td></tr>
    <tr><td>Veri Türünü İçe Aktar</td><td> Sicim</td><td>Dize Dizisi</td></tr>
    <tr> <td>Kaynak</td><td> Dosya Kaynağı</td><td>BatchData parametresi boş olduğunda veri dosyasının konumunu gösterir.</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="10" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parametre</th><th scope="col">Tip</th> <th scope="col">Tanım</th></tr>
  </thead>
  <tbody>
    <tr><td>satırIndeksi</td><td>int</td> <td></td> </tr>
    <tr><td>sütunIndeksi</td><td>int</td><td></td></tr>
    <tr><td>tip</td><td>Sicim</td><td>veri türü</td></tr>
    <tr><td>değer</td><td> Sicim</td> <td></td></tr>
    <tr><td>stil</td><td> Stil(nesne)</td><td></td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="11" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parametre</th><th scope="col">Tip</th> <th scope="col">Tanım</th></tr>
  </thead>
  <tbody>
    <tr><td>DosyaKaynakTürü</td><td>Sicim</td> <td>BellekDosyaları/BulutDosyaSistemi/İstekDosyaları</td> </tr>
    <tr><td>DosyaYolu</td><td>Sicim</td><td> dosya konumu</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< /tabs >}}

## Excel nesneleri çeşitli dosya biçimlerine nasıl aktarılır

Başlangıçta belirli bir biçimde Excel dosyasını oluşturduysanız, örneğin:[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/) , Ve[CSV](https://docs.fileformat.com/spreadsheet/csv/)Bazen Excel dosyasını başka bir biçime dönüştürüp, sunduğu özel özelliklerden yararlanmayı faydalı bulabilirsiniz. Örneğin, bir Excel dosyasını şuraya aktarmak isteyebilirsiniz:[PDF](https://docs.fileformat.com/pdf/) İçeriklerinizi yetkisiz değişikliklerden korumak ve aynı anda okunmasını ve paylaşılmasını kolaylaştırmak için.

Excel nesnesinin dışa aktarımı karmaşık bir süreçtir. Karmaşıklığa katkıda bulunan birçok faktör vardır ve bu nedenle dışa aktarma işlemi sırasında dikkate alınmalıdır. Excel nesnesini tek bir format dosyasına hassas ve profesyonel bir kalitede aktarabilme özelliği, Aspose.Cells Cloud'un en önemli özelliklerinden biridir.

 Excel dosyasından dışa aktarılan çalışma kitabı, grafik, şekil ve resimler için mükemmel bir şekilde çalışır. Şu formatlarda dışa aktarabilirsiniz:[XLS](https://docs.fileformat.com/spreadsheet/xls/), [XLSX](https://docs.fileformat.com/spreadsheet/xlsx/), [XLSB](https://docs.fileformat.com/spreadsheet/xlsb/), [CSV](https://docs.fileformat.com/spreadsheet/csv/), [TSV](https://docs.fileformat.com/spreadsheet/tsv/), [XLSM](https://docs.fileformat.com/spreadsheet/xlsm/), [ODS](https://docs.fileformat.com/spreadsheet/ods/), [TXT](https://docs.fileformat.com/word-processing/txt/) Yalnızca dışa aktarılabilen biçimler:[PDF](https://docs.fileformat.com/pdf/), [OTS](https://docs.fileformat.com/spreadsheet/ots/), [XPS](https://docs.fileformat.com/page-description-language/xps/), [FARKLILIK](https://docs.fileformat.com/spreadsheet/dif/), [PNG](https://docs.fileformat.com/Image/png/), [JPEG](https://docs.fileformat.com/image/jpeg/), [BMP](https://docs.fileformat.com/image/bmp/), [SVG](https://docs.fileformat.com/page-description-language/svg/), [TIFF](https://docs.fileformat.com/image/tiff/), [EMF](https://docs.fileformat.com/image/emf/), [SAYILAR](https://docs.fileformat.com/spreadsheet/numbers/), [FODS](https://docs.fileformat.com/spreadsheet/fods/).

İstek, çok parçalı içeriğe sahip bir HTTP isteğidir (bkz.[RFC 2046](http://tools.ietf.org/html/rfc2046#page-17)veya[RFC 1341](http://www.w3.org/Protocols/rfc1341/7_2_Multipart.html)). Çok parçalı içeriğin ilk kısmı veri dosyasını, ikinci kısmı ise kaydetme seçeneklerini içerir.

REST API `export` çalışma kitabı ve dahili nesneler farklı format dosyasına.

### İhracat API Bilgi

```bash

POST https://api.aspose.cloud/v3.0/cells/export

```

İstek parametreleri şunlardır:

| Parametre Adı| Tip| Yol/Sorgu Dizesi/HTTPGövdesi|Tanım|
|:- |:- |:- |:- |
| dosya| dosya| formData| Yüklenecek dosya|
| nesne türü| sicim| sorgu| nesne türü (çalışma kitabı/çalışma sayfası/grafik/şekil/resim/liste nesnesi/ole nesnesi)|
| biçim| sicim| sorgu|[Dosya Biçimi](/cells/tr/supported-file-formats/)  |

 The[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/LightCells/PostExport) herkesin erişebileceği bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenize olanak tanır.

cURL komut satırı aracını kullanarak Aspose.Cells web servislerine kolayca erişebilirsiniz. Aşağıdaki örnek, cURL ile API Cloud'a nasıl çağrı yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="Request" tabName2="Response" >}}

{{< tab tabNum="1" >}}

```bash
 
curl -v "http://api.aspose.cloud/v3.0/cells/export" \
-X POST \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>" \
-F 'xxxxx1=@xxxx1.xlsx' \
-F 'xxxxx2=@xxxx2.xlsx' 
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```bash
{
    "Files":
    [
        { 
            "Filename":"xxxxx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        },
        { 
            "Filename":"xxxxx",
            "FileSize":274022,
            "FileContent":"-----Base64String--------"
        }
    ]
}
 
```

{{< /tab >}}

{{< /tabs >}}

## İçe ve dışa aktarma API'leri nasıl çağrılır?

Aşağıdaki makaleler her API'in nasıl aranacağını ayrıntılı olarak açıklamakta ve cURL'i ve her API'in SDK Örneklerini içermektedir:

- [Depolama alanı kullanmadan Excel dosyalarına veri nasıl aktarılır.](/cells/tr/import/without-using-storage)
- [Depolamayı kullanarak Excel dosyalarına veri nasıl aktarılır.](/cells/tr/import/with-using-storage)
- [Toplu Veriler Excel Çalışma Sayfasına Nasıl Aktarılır](/cells/tr/import-batch-data-into-excel-worksheet/)
- [CSV Verileri Excel Çalışma Sayfasına Nasıl Aktarılır](/cells/tr/import-csv-data-into-excel-worksheet/)
- [Excel Çalışma Sayfasına resim nasıl aktarılır](/cells/tr/import-picture-into-excel-worksheet/)
- [Tamsayı Dizisi Excel Çalışma Sayfasına Nasıl Aktarılır](/cells/tr/import-integer-array-into-excel-worksheet/)
- [Double Dizisi Excel Çalışma Sayfasına Nasıl Aktarılır](/cells/tr/import-double-array-into-excel-worksheet/)
- [Excel Çalışma Sayfasına Dize Dizisi Nasıl Aktarılır](/cells/tr/import-string-array-into-excel-worksheet/)
- [2 Boyutlu Tamsayı Dizisi Excel Çalışma Sayfasına Nasıl Aktarılır](/cells/tr/import-a-2D-integer-array-into-excel-worksheet/)
- [2 Boyutlu Çift Dizi Excel Çalışma Sayfasına Nasıl Aktarılır](/cells/tr/import-a-2D-double-array-into-excel-worksheet/)
- [2 Boyutlu Dize Dizisi Excel Çalışma Sayfasına Nasıl Aktarılır](/cells/tr/import-a-2D-string-array-into-excel-worksheet/)
- [Excel grafiğini farklı dosya biçimine aktarın](/cells/tr/export-excel-chart-to-different-formats/)
- [Excel liste nesnesini farklı bir dosya biçimine aktarın](/cells/tr/export-excel-listobject-to-different-formats/)
- [Excel ole nesnesini farklı bir dosya biçimine aktarın](/cells/tr/export-excel-ole-object/)
- [Excel resmini farklı dosya biçimine aktar](/cells/tr/export-excel-picture-to-different-formats/)
- [Excel şeklini farklı dosya biçimine aktar](/cells/tr/export-excel-shape-to-different-formats/)
- [Excel çalışma kitabını farklı bir dosya biçimine aktarın](/cells/tr/export-excel-to-different-formats/)
- [Excel çalışma sayfasını farklı bir dosya biçimine aktarın](/cells/tr/export-excel-worksheet-to-different-formats//)
