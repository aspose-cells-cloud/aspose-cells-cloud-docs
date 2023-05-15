---
title: ithalat
second_title: Aspose.Cells Cloud Documen
type: docs
url: /tr/import/ 
aliases: [/import-data-in-excel-worksheet-without-using-storage/]
keywords: Import data into Excel files
description: Aspose.Cells Cloud REST API, Excel dosyalarına veri aktarımını destekler. SDK, geliştirme dili türlerini destekler. Android, C#, Go, Java, NodeJS, Perl, PHP, Python, Ruby ve Swift'i içerir
weight: 31
---
Verileri bir Excel dosyasına aktarmak karmaşık bir işlemdir. Birçok faktör karmaşıklığa katkıda bulunur ve bu nedenle ihracat sürecinde dikkate alınmalıdır. Biçimleri ve veri türlerini kesin bir profesyonel kalitede dosyaya aktarma yeteneği, Aspose.Cells Cloud'un en önemli özelliğidir.

## RSET API'leri

Bir Excel dosyasına veya birden fazla Excel dosyasına veri aktarmak için aşağıdaki API'ler sağlanmıştır:

|API|Tanım|
|:- |:- |
|[POST /hücreler/içe aktarma](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)|Depolamayı kullanmadan Excel dosyalarına veri aktarın.|
|[POST /cells/{name}/impportdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData)|Depolamayı kullanarak verileri Excel dosyasına aktarın.|

## İstek Parametreleri
 
### Depolama kullanmadan

| Parametre adı| Tip| Yol/Sorgu Dizesi/HTTPBody|Tanım|
|:- |:- |:- |:- |
| dosya| dosya| form verisi| Yüklenecek dosya|
| İçe Aktarma Seçeneği| İçe Aktarma Seçenekleri| HTTPBody| IntArray/DoubleArray/StringArray/TwoDimensionIntArray/TwoDimensionDoubleArray/TwoDimensionStringArray/BatchData/CSVData/Picture|

### Depolama kullanarak

| Parametre adı| Tip| Yol/Sorgu Dizesi/HTTPBody|Tanım|
|:- |:- |:- |:- |
| isim| sicim| yol||
| dosya| sicim| sorgu||
| depolamaAdı| sicim| sorgu| depolama adı.|
| importData|| vücut||


### Veri seçeneği parametresini içe aktar

**Önemli parametreler aşağıdaki tabloda açıklanmıştır.**:

{{< tabs tabTotal="11" tabID="1" tabName1="ImportBatchDataOption" tabName2="ImportCSVDataOption" tabName3="ImportPictureOption" tabName4="Import2DimensionIntArrayOption" tabName5="Import2DimensionDoubleArrayOption" tabName6="Import2DimensionStringArrayOption" tabName7="ImportIntegerArrayOption" tabName8="ImportDoubleArrayOption" tabName9="ImportStringArrayOption" tabName10="CellValue" tabName11="FileSource" >}}
{{< tab tabNum="1" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parametre</th><th scope="col">Tip</th> <th scope="col">Tanım</th></tr>
  </thead>
  <tbody>
    <tr> <td>Toplu Veri</td><td>Liste<CellValue></td> <td>toplu veri</td> </tr>
    <tr> <td>HedefÇalışma Sayfası</td><td> Sicim</td><td> Hedef çalışma sayfası adı.</td></tr>
    <tr><td>Eklemek</td><td>Sicim</td><td>doğru yanlış.</td></tr>
    <tr><td>ImportDataType</td><td> Sicim</td><td>TwoDimensionStringBatchDataArray</td></tr>
    <tr> <td>Kaynak</td><td> Dosya Kaynağı</td><td>BatchData parametresi boş olduğunda veri dosyası konumunu gösterir.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="2" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parametre</th><th scope="col">Tip</th> <th scope="col">Tanım</th></tr>
  </thead>
  <tbody>
    <tr> <td>Sayısal Verileri Dönüştür</td><td>Sicim</td> <td>doğru yanlış.</td> </tr>
    <tr> <td>İlk sıra</td><td>int</td> <td></td> </tr>
    <tr> <td>İlk sütun</td><td>int</td><td></td></tr>
    <tr><td>AyırıcıDize</td><td> Sicim</td> <td></td></tr>
    <tr> <td>HedefÇalışma Sayfası</td><td> Sicim</td><td> Hedef çalışma sayfası adı.</td></tr>
    <tr><td>Özel Ayrıştırıcılar</td><td>Liste<CustomParserConfig></td><td></td></tr>
    <tr><td>ImportDataType</td><td> Sicim</td><td>CSVVerileri</td></tr>
    <tr> <td>Kaynak</td><td> Dosya Kaynağı</td><td>BatchData parametresi boş olduğunda veri dosyası konumunu gösterir.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="3" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parametre</th><th scope="col">Tip</th> <th scope="col">Tanım</th></tr>
  </thead>
  <tbody>
    <tr> <td>İlk sıra</td><td>int</td> <td></td> </tr>
    <tr> <td>İlk sütun</td><td>int</td><td></td></tr>
    <tr><td>Dikey mi</td><td>Sicim</td><td>doğru yanlış.</td></tr>
    <tr><td>Veri</td><td> Sicim[]</td> <td></td></tr>
    <tr> <td>HedefÇalışma Sayfası</td><td> Sicim</td><td> Hedef çalışma sayfası adı.</td></tr>
    <tr><td>Eklemek</td><td>Sicim</td><td>doğru yanlış.</td></tr>
    <tr><td>ImportDataType</td><td> Sicim</td><td>Resim</td></tr>
    <tr> <td>Kaynak</td><td> Dosya Kaynağı</td><td>BatchData parametresi boş olduğunda veri dosyası konumunu gösterir.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="4" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parametre</th><th scope="col">Tip</th> <th scope="col">Tanım</th></tr>
  </thead>
  <tbody>
    <tr> <td>İlk sıra</td><td>int</td> <td></td> </tr>
    <tr> <td>İlk sütun</td><td>int</td><td></td></tr>
    <tr><td>Veri</td><td> tamsayı[,]</td> <td></td></tr>
    <tr> <td>HedefÇalışma Sayfası</td><td> Sicim</td><td> Hedef çalışma sayfası adı.</td></tr>
    <tr><td>Eklemek</td><td>Sicim</td><td>doğru yanlış.</td></tr>
    <tr><td>ImportDataType</td><td> Sicim</td><td>TwoDimensionIntArray</td></tr>
    <tr> <td>Kaynak</td><td> Dosya Kaynağı</td><td>BatchData parametresi boş olduğunda veri dosyası konumunu gösterir.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="5" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parametre</th><th scope="col">Tip</th> <th scope="col">Tanım</th></tr>
  </thead>
  <tbody>
    <tr> <td>İlk sıra</td><td>int</td> <td></td> </tr>
    <tr> <td>İlk sütun</td><td>int</td><td></td></tr>
    <tr><td>Veri</td><td> Çift[,]</td> <td></td></tr>
    <tr> <td>HedefÇalışma Sayfası</td><td> Sicim</td><td> Hedef çalışma sayfası adı.</td></tr>
    <tr><td>Eklemek</td><td>Sicim</td><td>doğru yanlış.</td></tr>
    <tr><td>ImportDataType</td><td> Sicim</td><td>TwoDimensionDoubleArray</td></tr>
    <tr> <td>Kaynak</td><td> Dosya Kaynağı</td><td>BatchData parametresi boş olduğunda veri dosyası konumunu gösterir.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="6" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parametre</th><th scope="col">Tip</th> <th scope="col">Tanım</th></tr>
  </thead>
  <tbody>
    <tr> <td>İlk sıra</td><td>int</td> <td></td> </tr>
    <tr> <td>İlk sütun</td><td>int</td><td></td></tr>
    <tr><td>Veri</td><td> Sicim[,]</td> <td></td></tr>
    <tr> <td>HedefÇalışma Sayfası</td><td> Sicim</td><td> Hedef çalışma sayfası adı.</td></tr>
    <tr><td>Eklemek</td><td>Sicim</td><td>doğru yanlış.</td></tr>
    <tr><td>ImportDataType</td><td> Sicim</td><td>TwoDimensionStringArray</td></tr>
    <tr> <td>Kaynak</td><td> Dosya Kaynağı</td><td>BatchData parametresi boş olduğunda veri dosyası konumunu gösterir.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="7" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parametre</th><th scope="col">Tip</th> <th scope="col">Tanım</th></tr>
  </thead>
  <tbody>
    <tr> <td>İlk sıra</td><td>int</td> <td></td> </tr>
    <tr> <td>İlk sütun</td><td>int</td><td></td></tr>
    <tr><td>Dikey mi</td><td>Sicim</td><td>doğru yanlış.</td></tr>
    <tr><td>Veri</td><td> tamsayı[]</td> <td></td></tr>
    <tr> <td>HedefÇalışma Sayfası</td><td> Sicim</td><td> Hedef çalışma sayfası adı.</td></tr>
    <tr><td>Eklemek</td><td>Sicim</td><td>doğru yanlış.</td></tr>
    <tr><td>ImportDataType</td><td> Sicim</td><td>Tamsayı Dizisi</td></tr>
    <tr> <td>Kaynak</td><td> Dosya Kaynağı</td><td>BatchData parametresi boş olduğunda veri dosyası konumunu gösterir.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="8" >}}

<table class="table">
  <thead>
    <tr><th scope="col">Parametre</th><th scope="col">Tip</th> <th scope="col">Tanım</th></tr>
  </thead>
  <tbody>
    <tr> <td>İlk sıra</td><td>int</td> <td></td> </tr>
    <tr> <td>İlk sütun</td><td>int</td><td></td></tr>
    <tr><td>Dikey mi</td><td>Sicim</td><td>doğru yanlış.</td></tr>
    <tr><td>Veri</td><td> Çift[]</td> <td></td></tr>
    <tr> <td>HedefÇalışma Sayfası</td><td> Sicim</td><td> Hedef çalışma sayfası adı.</td></tr>
    <tr><td>Eklemek</td><td>Sicim</td><td>doğru yanlış.</td></tr>
    <tr><td>ImportDataType</td><td> Sicim</td><td>çift dizi</td></tr>
    <tr> <td>Kaynak</td><td> Dosya Kaynağı</td><td>BatchData parametresi boş olduğunda veri dosyası konumunu gösterir.</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< tab tabNum="9" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parametre</th><th scope="col">Tip</th> <th scope="col">Tanım</th></tr>
  </thead>
  <tbody>
    <tr> <td>ÜstSolSatır</td><td>int</td> <td></td> </tr>
    <tr> <td>Sol Üst Sütun</td><td>int</td><td></td></tr>
    <tr> <td>AltSağSatır</td><td>int</td> <td></td> </tr>
    <tr> <td>AltSağSütun</td><td>int</td><td></td></tr>
    <tr><td>Dosya adı</td><td>Sicim</td><td></td></tr>
    <tr><td>Veri</td><td> Sicim</td> <td></td></tr>
    <tr> <td>HedefÇalışma Sayfası</td><td> Sicim</td><td> Hedef çalışma sayfası adı.</td></tr>
    <tr><td>Eklemek</td><td>Sicim</td><td>doğru yanlış.</td></tr>
    <tr><td>ImportDataType</td><td> Sicim</td><td>Dize Dizisi</td></tr>
    <tr> <td>Kaynak</td><td> Dosya Kaynağı</td><td>BatchData parametresi boş olduğunda veri dosyası konumunu gösterir.</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="10" >}}
<table class="table">
  <thead>
    <tr><th scope="col">Parametre</th><th scope="col">Tip</th> <th scope="col">Tanım</th></tr>
  </thead>
  <tbody>
    <tr><td>satır dizini</td><td>int</td> <td></td> </tr>
    <tr><td>sütun dizini</td><td>int</td><td></td></tr>
    <tr><td>tip</td><td>Sicim</td><td>veri tipi</td></tr>
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
    <tr><td>Dosya Kaynağı Türü</td><td>Sicim</td> <td>InMemoryFiles/CloudFileSystem/RequestFiles</td> </tr>
    <tr><td>Dosya yolu</td><td>Sicim</td><td> dosya konumu</td></tr>
  </tbody>
</table>
{{< /tab >}}
{{< /tabs >}}

## RSET API'leri nasıl çağrılır?

Aşağıdaki makaleler, her API'in nasıl çağrılacağını ayrıntılı olarak açıklar ve cURL'i ve her API'in SDK Örneklerini içerir:

- [Depolamayı kullanmadan Excel dosyalarına nasıl veri aktarılır.](/cells/tr/import/without-using-storage)
- [Depolama kullanılarak Excel dosyalarına nasıl veri aktarılır.](/cells/tr/import/with-using-storage)
- [Toplu Verileri Excel Çalışma Sayfasına nasıl içe aktarılır](/cells/tr/import/batch-data/)
- [CSV Verileri Excel Çalışma Sayfasına nasıl aktarılır](/cells/tr/import/csv-data/)
- [Excel Çalışma Sayfasına resim nasıl aktarılır](/cells/tr/import/picture/)
- [Tamsayı Dizisini Excel Çalışma Sayfasına nasıl içe aktarırım](/cells/tr/import/integer-array/)
- [Double Array Excel Çalışma Sayfasına nasıl aktarılır](/cells/tr/import/double-array/)
- [Dize Dizisini Excel Çalışma Sayfasına nasıl aktarabilirim?](/cells/tr/import/string-array/)
- [2 Boyutlu Tamsayı Dizisini Excel Çalışma Sayfasına içe aktarma](/cells/tr/import/2dimension-integer-array/)
- [2 Boyutlu Çift Diziyi Excel Çalışma Sayfasına içe aktarma](/cells/tr/import/2dimension-double-array/)
- [2 Boyutlu Dize Dizisini Excel Çalışma Sayfasına Aktarma](/cells/tr/import/2dimension-string-array/)
