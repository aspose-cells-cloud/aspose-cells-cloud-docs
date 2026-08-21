---
title: "Veriyi Excel Dosyalarına İçe Aktarın ve Excel Dosyalarından Veri Dışa Aktarın"
second_title: "Belge"
linktitle: "Veri İçe ve Dışa Aktarma"
type: docs
url: /tr/data-import-and-export/
keywords: "Aspose.Cells Cloud, veri içe aktarma, Excel dışa aktarma, API, CSV, JSON, resim, dizi"
description: "Aspose.Cells Cloud API (v3.0) kullanarak CSV, JSON, diziler ve resimlerden veriyi Excel dosyalarına nasıl içe aktarabileceğinizi ve çalışma kitaplarını, grafikleri ve şekilleri PDF, PNG ve diğer formatlara nasıl dışa aktarabileceğinizi öğrenin."
weight: 25
---

Aspose.Cells Cloud API, çeşitli kaynaklardan veri içe aktarmayı destekler ve Excel çalışma kitaplarını, grafiklerini ve diğer nesnelerini **XLSX**, **CSV**, **PDF**, **HTML**, **PNG** ve daha fazlası gibi farklı formatlara dışa aktarabilir. Bu, veri yönetimi ve paylaşımını basit ve verimli hale getirir.

**API sürümü:** **v3.0** – Son güncelleme: **2024‑03‑15**

### Hızlı Başlangıç Kılavuzu

1. **İstek gövdesini hazırlayın** – İçe veya dışa aktarma seçeneklerini tanımlayan bir JSON gövdesi oluşturun (örneğin, `ImportCSVDataOption`, `ExportOptions`).
2. **İsteği gönderin** – `curl`, Postman veya bir SDK kullanarak uygun uç noktayı (`POST /cells/import` veya `POST /cells/export`) çağırın.
3. **Yanıtı işleyin** – Başarılı olursa işlenmiş dosyayı (ikili veya Base64) alırsınız. Hata durumunda HTTP durum kodunu ve JSON gövdesinde döndürülen hata mesajını inceleyin.

#### Ön Gereksinimler

- Aktif bir Aspose Cloud hesabı ve geçerli bir JWT belirteci.
- Hedef çalışma kitabının belirtilen depolama konumunda mevcut olması (depoya dayalı API’ler için).
- Doğru `Content-Type` başlık değerleri (dosya yükleme için `multipart/form-data`, JSON gövdeleri için `application/json`).

## Çeşitli veri kaynaklarından veri nasıl içe aktarılır

Verinin bir Excel dosyasına içe aktarılması süreci sırasında dikkat edilmesi gereken birçok husus içerir. Aspose.Cells Cloud’un profesyonel kalitede birçok format ve veri türünü içe aktarma yeteneği, öne çıkan özelliklerinden biridir.

### Veri İçe Aktarma API Bilgileri

Aşağıdaki API’ler, bir veya birden fazla Excel dosyasına veri içe aktarmak için sağlanmıştır:

| API                                                                                                | Açıklama                                                  |
| :------------------------------------------------------------------------------------------------- | :-------------------------------------------------------- |
| [POST /cells/import](https://apireference.aspose.cloud/cells/#/LightCells/PostImport)              | Depolama kullanmadan veriyi Excel dosyalarına içe aktarır. |
| [POST /cells/{name}/importdata](https://apireference.aspose.cloud/cells/#/Workbook/PostImportData) | Bulutta depolanan bir Excel dosyasına veri içe aktarır.   |

### İstek Parametreleri

#### Depolama kullanmadan

| Parametre Adı | Tür           | Konum     | Açıklama                |
| :------------ | :------------ | :-------- | :---------------------- |
| file          | file          | formData  | Yüklenecek dosya        |
| ImportOption  | ImportOptions | body      | İçe aktarma formatını belirtir (IntArray, DoubleArray, StringArray, TwoDimensionIntArray, TwoDimensionDoubleArray, TwoDimensionStringArray, BatchData, csvData, Picture) |

#### Depolama kullanarak

| Parametre Adı | Tür           | Konum  | Açıklama                |
| :------------ | :------------ | :----- | :---------------------- |
| name          | string        | path   | Excel dosyasının adı    |
| folder        | string        | query  | Depolamadaki klasör yolu |
| storageName   | string        | query  | Depolama adı            |
| importData    | ImportOptions | body   | Veri içe aktarma gövdesi  |

#### Veri içe aktarma seçeneği parametreleri

**Önemli parametreler aşağıdaki tablolarda açıklanmıştır:**

{{< tabs tabTotal="11" tabID="1" tabName1="ImportBatchDataOption"  tabName2="ImportCSVDataOption"   tabName3="ImportPictureOption" tabName4="Import2DimensionIntArrayOption" tabName5="Import2DimensionDoubleArrayOption" tabName6="Import2DimensionStringArrayOption" tabName7="ImportIntegerArrayOption" tabName8="ImportDoubleArrayOption" tabName9="ImportStringArrayOption" tabName10="CellValue" tabName11="FileSource" >}}

{{< tab tabNum="1" >}}

<table class="table">
  <thead>
    <tr><th>Parametre</th><th>Tür</th><th>Açıklama</th></tr>
  </thead>
  <tbody>
    <tr><td>BatchData</td><td>List&lt;CellValue&gt;</td><td>İçe aktarılacak toplu veri</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Hedef çalışma sayfası adı</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Verinin eklenip eklenmeyeceği (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionStringBatchDataArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>BatchData null olduğunda veri dosyasının konumu</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="2" >}}

<table class="table">
  <thead>
    <tr><th>Parametre</th><th>Tür</th><th>Açıklama</th></tr>
  </thead>
  <tbody>
    <tr><td>ConvertNumericData</td><td>boolean</td><td>Sayısal verilerin dönüştürülüp dönüştürülmeyeceği (true/false)</td></tr>
    <tr><td>FirstRow</td><td>int</td><td>İlk satırın indeksi</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>İlk sütunun indeksi</td></tr>
    <tr><td>SeparatorString</td><td>string</td><td>Sütun ayırıcısı</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Hedef çalışma sayfası adı</td></tr>
    <tr><td>CustomParsers</td><td>List&lt;CustomParserConfig&gt;</td><td>Özel ayrıştırıcı yapılandırmaları</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>CSVData</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>BatchData null olduğunda veri dosyasının konumu</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="3" >}}

<table class="table">
  <thead>
    <tr><th>Parametre</th><th>Tür</th><th>Açıklama</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>İlk satırın indeksi</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>İlk sütunun indeksi</td></tr>
    <tr><td>IsVertical</td><td>boolean</td><td>Resmin dikey yerleştirilip yerleştirilmeyeceği (true/false)</td></tr>
    <tr><td>Data</td><td>string[]</td><td>Resim verisi (base‑64 dizeleri)</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Hedef çalışma sayfası adı</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Verinin eklenip eklenmeyeceği (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>Picture</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>BatchData null olduğunda veri dosyasının konumu</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="4" >}}

<table class="table">
  <thead>
    <tr><th>Parametre</th><th>Tür</th><th>Açıklama</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>İlk satırın indeksi</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>İlk sütunun indeksi</td></tr>
    <tr><td>Data</td><td>int[,] </td><td>İki boyutlu tamsayı dizisi</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Hedef çalışma sayfası adı</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Verinin eklenip eklenmeyeceği (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionIntArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>BatchData null olduğunda veri dosyasının konumu</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="5" >}}

<table class="table">
  <thead>
    <tr><th>Parametre</th><th>Tür</th><th>Açıklama</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>İlk satırın indeksi</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>İlk sütunun indeksi</td></tr>
    <tr><td>Data</td><td>double[,] </td><td>İki boyutlu çift noktalı sayı dizisi</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Hedef çalışma sayfası adı</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Verinin eklenip eklenmeyeceği (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionDoubleArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>BatchData null olduğunda veri dosyasının konumu</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="6" >}}

<table class="table">
  <thead>
    <tr><th>Parametre</th><th>Tür</th><th>Açıklama</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>İlk satırın indeksi</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>İlk sütunun indeksi</td></tr>
    <tr><td>Data</td><td>string[,] </td><td>İki boyutlu dize dizisi</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Hedef çalışma sayfası adı</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Verinin eklenip eklenmeyeceği (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>TwoDimensionStringArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>BatchData null olduğunda veri dosyasının konumu</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="7" >}}

<table class="table">
  <thead>
    <tr><th>Parametre</th><th>Tür</th><th>Açıklama</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>İlk satırın indeksi</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>İlk sütunun indeksi</td></tr>
    <tr><td>IsVertical</td><td>boolean</td><td>Dizinin dikey olup olmadığı (true/false)</td></tr>
    <tr><td>Data</td><td>int[] </td><td>Bir boyutlu tamsayı dizisi</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Hedef çalışma sayfası adı</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Verinin eklenip eklenmeyeceği (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>IntegerArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>BatchData null olduğunda veri dosyasının konumu</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="8" >}}

<table class="table">
  <thead>
    <tr><th>Parametre</th><th>Tür</th><th>Açıklama</th></tr>
  </thead>
  <tbody>
    <tr><td>FirstRow</td><td>int</td><td>İlk satırın indeksi</td></tr>
    <tr><td>FirstColumn</td><td>int</td><td>İlk sütunun indeksi</td></tr>
    <tr><td>IsVertical</td><td>boolean</td><td>Dizinin dikey olup olmadığı (true/false)</td></tr>
    <tr><td>Data</td><td>double[] </td><td>Bir boyutlu çift noktalı sayı dizisi</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Hedef çalışma sayfası adı</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Verinin eklenip eklenmeyeceği (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>DoubleArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>BatchData null olduğunda veri dosyasının konumu</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="9" >}}

<table class="table">
  <thead>
    <tr><th>Parametre</th><th>Tür</th><th>Açıklama</th></tr>
  </thead>
  <tbody>
    <tr><td>UpperLeftRow</td><td>int</td><td>Sol üst satır indeksi</td></tr>
    <tr><td>UpperLeftColumn</td><td>int</td><td>Sol üst sütun indeksi</td></tr>
    <tr><td>LowerRightRow</td><td>int</td><td> Sağ alt satır indeksi</td></tr>
    <tr><td>LowerRightColumn</td><td>int</td><td>Sağ alt sütun indeksi</td></tr>
    <tr><td>Filename</td><td>string</td><td>Kaynak dosyanın adı</td></tr>
    <tr><td>Data</td><td>string</td><td>İçe aktarılacak dize verisi</td></tr>
    <tr><td>DestinationWorksheet</td><td>string</td><td>Hedef çalışma sayfası adı</td></tr>
    <tr><td>IsInsert</td><td>boolean</td><td>Verinin eklenip eklenmeyeceği (true/false)</td></tr>
    <tr><td>ImportDataType</td><td>string</td><td>StringArray</td></tr>
    <tr><td>Source</td><td>FileSource</td><td>BatchData null olduğunda veri dosyasının konumu</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="10" >}}

<table class="table">
  <thead>
    <tr><th>Parametre</th><th>Tür</th><th>Açıklama</th></tr>
  </thead>
  <tbody>
    <tr><td>rowIndex</td><td>int</td><td>Hücrenin satır indeksi</td></tr>
    <tr><td>columnIndex</td><td>int</td><td>Hücrenin sütun indeksi</td></tr>
    <tr><td>type</td><td>string</td><td>Hücre değeri veri türü</td></tr>
    <tr><td>value</td><td>string</td><td>Hücre değeri</td></tr>
    <tr><td>style</td><td>Style (object)</td><td>Hücre stili tanımı</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< tab tabNum="11" >}}

<table class="table">
  <thead>
    <tr><th>Parametre</th><th>Tür</th><th>Açıklama</th></tr>
  </thead>
  <tbody>
    <tr><td>FileSourceType</td><td>string</td><td>InMemoryFiles, CloudFileSystem veya RequestFiles</td></tr>
    <tr><td>FilePath</td><td>string</td><td>Kaynak dosyanın yolu</td></tr>
  </tbody>
</table>

{{< /tab >}}
{{< /tabs >}}

## Excel nesneleri nasıl çeşitli dosya formatlarına dışa aktarılır

Orijinal olarak bir Excel dosyasını **XLS**, **XLSX**, **XLSB** veya **CSV** formatında oluşturduysanız, belirli özelliklerden yararlanmak amacıyla başka bir formata dönüştürmek isteyebilirsiniz. Örneğin, **PDF** formatına dışa aktarmak, içeriğin yetkisiz değişikliklere karşı korunmasını sağlarken okunmasını ve paylaşılmasını kolaylaştırır.

Excel nesnelerinin dışa aktarılması bazı hususları içerir. Aspose.Cells Cloud, çalışma kitaplarını, grafikleri, şekilleri ve resimleri geniş bir format yelpazesine yüksek kalitede dışa aktarır:

_Sadece dışa aktarma formatları_: PDF, OTS, XPS, DIF, PNG, JPEG, BMP, SVG, TIFF, EMF, NUMBERS, FODS.  
 Hem içe hem de dışa aktarma: XLS, XLSX, XLSB, CSV, TSV, XLSM, ODS, TXT.

İstek, [RFC 2046] ve [RFC 1341]’de tanımlanan multipart içeriği kullanır. İlk kısım veri dosyasını içerir; ikinci kısım kaydetme seçeneklerini içerir.

### Dışa Aktarma API Bilgileri

```bash
POST https://api.aspose.cloud/v3.0/cells/export
```

#### İstek parametreleri

| Parametre Adı | Tür    | Konum    | Açıklama                                                                                      |
| :------------ | :----- | :------- | :-------------------------------------------------------------------------------------------- |
| file          | file   | formData | Yüklenecek dosya                                                                              |
| objectType    | string | query    | Nesne türü (`workbook`, `worksheet`, `chart`, `shape`, `picture`, `listobject`, `oleobject`) |
| format        | string | query    | İstenen çıktı dosya formatı ([Desteklenen Dosya Formatları](/cells/supported-file-formats/) bakın) |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/LightCells/PostExport), web tarayıcınızdan doğrudan REST etkileşimleri gerçekleştirmenize olanak tanıyan herkese açık bir programlama arayüzü tanımlar.

API’yi çağırmak için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, bir isteği ve JSON yanıtını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/export" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -F 'file1=@example1.xlsx' \
  -F 'file2=@example2.xlsx'
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Files": [
    {
      "Filename": "example1.pdf",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    },
    {
      "Filename": "example2.pdf",
      "FileSize": 274022,
      "FileContent": "-----Base64String--------"
    }
  ]
}
```

{{< /tab >}}
{{< /tabs >}}

#### Yaygın HTTP durum kodları

| Durum | Anlam                                                          | Önerilen eylem                              |
| ----- | -------------------------------------------------------------- | ------------------------------------------- |
| 200   | Başarılı – dosya dışa aktarıldı                                | Döndürülen dosya(lar)ı işleyin              |
| 400   | Hatalı istek – eksik veya geçersiz parametreler                | İstek gövdesini ve sorgu dizelerini kontrol edin |
| 401   | Yetkisiz – geçersiz veya süresi geçmiş JWT belirteci          | Belirteci yenileyin ve tekrar deneyin       |
| 404   | Bulunamadı – belirtilen çalışma kitabı veya çalışma sayfası yok | Dosya adını ve depolama yolunu kontrol edin |
| 500   | İç sunucu hatası – sunucuda beklenmeyen durum                  | İstek kimliğiyle Aspose destek ekibine başvurun |

## İçe ve dışa aktarma API’leri nasıl çağrılır

Aşağıdaki makaleler her bir API’yi ayrıntılı olarak açıklar ve cURL ile SDK örnekleri içerir:

- [Depolama kullanmadan Excel dosyalarına veri nasıl içe aktarılır.](/cells/import/without-using-storage)
- [Depolama kullanarak Excel dosyalarına veri nasıl içe aktarılır.](/cells/import/with-using-storage)
- [Toplu Veri Nasıl Excel Çalışma Sayfasına İçe Aktarılır](/cells/import-batch-data-into-excel-worksheet/)
- [CSV Verisi Nasıl Excel Çalışma Sayfasına İçe Aktarılır](/cells/import-CSV-data-into-excel-worksheet/)
- [Resim Nasıl Excel Çalışma Sayfasına İçe Aktarılır](/cells/import-picture-into-excel-worksheet/)
- [Tamsayı Dizisi Nasıl Excel Çalışma Sayfasına İçe Aktarılır](/cells/import-integer-array-into-excel-worksheet/)
- [Çift Sayı Dizisi Nasıl Excel Çalışma Sayfasına İçe Aktarılır](/cells/import-double-array-into-excel-worksheet/)
- [Dize Dizisi Nasıl Excel Çalışma Sayfasına İçe Aktarılır](/cells/import-string-array-into-excel-worksheet/)
- [2 Boyutlu Tamsayı Dizisi Nasıl Excel Çalışma Sayfasına İçe Aktarılır](/cells/import-a-2D-integer-array-into-excel-worksheet/)
- [2 Boyutlu Çift Sayı Dizisi Nasıl Excel Çalışma Sayfasına İçe Aktarılır](/cells/import-a-2D-double-array-into-excel-worksheet/)
- [2 Boyutlu Dize Dizisi Nasıl Excel Çalışma Sayfasına İçe Aktarılır](/cells/import-a-2D-string-array-into-excel-worksheet/)
- [Excel Grafiği Nasıl Farklı Dosya Formatına Dışa Aktarılır](/cells/export-excel-chart-to-different-formats/)
- [Excel Liste Nesnesi Nasıl Farklı Dosya Formatına Dışa Aktarılır](/cells/export-excel-listobject-to-different-formats/)
- [Excel OLE Nesnesi Nasıl Farklı Dosya Formatına Dışa Aktarılır](/cells/export-excel-ole-object/)
- [Excel Resmi Nasıl Farklı Dosya Formatına Dışa Aktarılır](/cells/export-excel-picture-to-different-formats/)
- [Excel Şekli Nasıl Farklı Dosya Formatına Dışa Aktarılır](/cells/export-excel-shape-to-different-formats/)
- [Excel Çalışma Kitabı Nasıl Farklı Dosya Formatına Dışa Aktarılır](/cells/export-excel-to-different-formats/)
- [Excel Çalışma Sayfası Nasıl Farklı Dosya Formatına Dışa Aktarılır](/cells/export-excel-worksheet-to-different-formats/)