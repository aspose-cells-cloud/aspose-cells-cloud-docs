---
title: "Excel Çalışma Sayfasında Bir Aralık Verisini Sırala"
second_title: "Belge"
linktitle: "Sırala"
type: docs
url: /worksheets/sort-data/
aliases: [/sort-worksheet-data/]
keywords: "Aspose.Cells Cloud, Excel sıralama API'si, çalışma sayfası aralığı sıralama, REST API, dataSorter"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasında belirli bir aralığı sıralayın. Uç nokta, gerekli parametreler, kimlik doğrulama adımları, hata işleme ve SDK örnekleri içerir."
weight: 20
---

REST API, bir Excel çalışma sayfasında belirtilen bir aralık içindeki verileri sıralar.

## REST API

```shell
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/sort
```

### İstek parametreleri

| Parametre Adı | Tür     | Konum  | Gerekli | Açıklama                                                          |
| ------------- | ------- | ------ | ------- | ----------------------------------------------------------------- |
| name          | string  | path   | Evet    | Çalışma kitabının adı.                                             |
| sheetName     | string  | path   | Evet    | Çalışma sayfasının adı.                                            |
| cellArea      | string  | query  | Evet    | Sıralanacak hücre aralığı (örneğin, `A5:A10`).                    |
| dataSorter    | object  | body   | Evet    | Sıralama ayarlarını tanımlayan JSON nesnesi (aşağıdaki şemaya bakın). |
| folder        | string  | query  | Hayır   | Çalışma kitabının bulunduğu klasör.                               |
| storageName   | string  | query  | Hayır   | Çalışma kitabının bulunduğu depo adı.                             |

**`dataSorter` nesne şeması** – Gövde, aşağıdaki özelliklere sahip bir JSON nesnesi içermelidir:

- `CaseSensitive` _(boolean, gerekli)_ – Sıralamanın büyük/küçük harf duyarlı olup olmayacağını belirler.
- `HasHeaders` _(boolean, gerekli)_ – Aralığın bir başlık satırı içerip içermediğini belirtir.
- `KeyList` _(array, gerekli)_ – Sıralama anahtarlarının koleksiyonu. Her anahtar nesnesi şunları içerir:
  - `Key` _(integer)_ – Sıfırdan başlayarak sütun dizini.
  - `SortOrder` _(string)_ – `"ascending"` (artan) veya `"descending"` (azalan).
- `SortLeftToRight` _(boolean, gerekli)_ – `true` ise sıralama soldan sağa; aksi takdirde yukarıdan aşağıya yapılır.
- _(İsteğe bağlı)_ `CaseOrder`, `SortLeftToRight` gibi ek özellikler OpenAPI spesifikasyonuna göre sağlanabilir.

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Worksheets/PostWorksheetRangeSort), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'sine nasıl istek atılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```shell
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/sort?cellArea=A5:A10" \
  -X POST \
  -d '{"CaseSensitive":false,"HasHeaders":false,"KeyList":[{"Key":0,"SortOrder":"descending"}],"SortLeftToRight":false}' \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

**Hata işleme** – API standart HTTP hata kodlarını döndürebilir. Tipik yanıtlar şunları içerir:

| HTTP Durumu | Kod | Mesaj                                             |
| ----------- | --- | ------------------------------------------------- |
| 400         | 400 | Geçersiz istek – eksik veya geçersiz parametreler. |
| 401         | 401 | Yetkisiz erişim – geçersiz veya eksik JWT belirteci. |
| 404         | 404 | Bulunamadı – çalışma kitabı veya çalışma sayfası mevcut değil. |
| 500         | 500 | Sunucu iç hatası.                                  |

Hata durumlarında yanıt gövdesi `{ "Code": <durum>, "Message": "<açıklama>", "Status": "Error" }` şablonuna uyar.

## Bulut SDK Çevresi

SDK kullanmak, geliştirme yapmanın en hızlı yoludur. SDK, düşük seviye ayrıntıları işler ve projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub Deposu](https://github.com/aspose-cells-cloud) adresini kontrol edin.

Aşağıdaki kod örnekleri, farklı SDK'lar kullanılarak Aspose.Cells web hizmetlerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-.NET-CellsWorksheetsPostWorksheetRangeSort.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-SortWorksheetData-sort-worksheet-data.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PostWorksheetRangeSort-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-sort_worksheet_range-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "SortWorkSheetData.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-SortWorksheetData-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-SortWorksheetData-sort-worksheet-data.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-SortWorksheetData-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "48dd9dae5e2188a64e2284bb12b9201b" >}}

{{< /tab >}}

{{< /tabs >}}