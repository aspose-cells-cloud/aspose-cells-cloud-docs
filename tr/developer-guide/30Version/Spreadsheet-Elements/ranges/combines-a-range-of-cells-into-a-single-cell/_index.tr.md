---
title: "Aspose.Cells Cloud API – Hücre Aralığını Birleştir"
secondtitle: "Belge"
linktitle: "Birleştir"
type: docs
url: /ranges/merge/
aliases: [/combines-a-range-of-cells-into-a-single-cell/]
keywords: "Aspose.Cells, hücre birleştir, Excel API, REST, bulut SDK"
description: "Aspose.Cells Cloud REST API ile bir hücre aralığını tek bir hücrede birleştirin. C#, Java, Python ve diğerleri için istek formatı, parametreler ve SDK örnekleri öğrenin."
weight: 20
---

Bu REST API, bir Excel çalışma sayfasındaki bir hücre aralığını tek bir hücrede birleştirir.

**Genel Bakış** – Bir aralığı birleştirmek, seçilen hücreleri tek bir hücrede birleştirir, üst‑sol hücrenin değerini korurken diğerlerini atar. Birden fazla sütunu veya satırı kapsayan bir başlık oluşturmak gerektiğinde veya bir çalışma sayfasının düzenini basitleştirmek istediğinizde bu işlemi kullanın.

## REST API

```bash
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/ranges/merge
```

### **İstek Parametreleri**

| Parametre Adı   | Tür     | Konum  | Açıklama                                             |
| ---------------- | ------- | ------ | ---------------------------------------------------- |
| **name**         | string  | path   | Çalışma kitabının adı.                               |
| **sheetName**    | string  | path   | Çalışma sayfasının adı.                              |
| **range**        | object  | body   | Birleştirilecek hücreleri belirten aralık nesnesi.  |
| **folder**       | string  | query  | Çalışma kitabının bulunduğu klasör.                  |
| **storageName**  | string  | query  | Depo adı.                                            |

#### İstek Gövdesi Şeması

**Range** nesnesi aşağıdaki alanları içermelidir (diğerleri isteğe bağlıdır):

| Özellik         | Tür     | Zorunlu | Açıklama                                               |
| ---------------- | ------- | ------- | ------------------------------------------------------ |
| **FirstRow**     | integer | Evet    | Aralıktaki ilk satırın sıfır tabanlı indeksi.          |
| **FirstColumn**  | integer | Evet    | Aralıktaki ilk sütunun sıfır tabanlı indeksi.         |
| **RowCount**     | integer | Evet    | Aralığa dahil edilecek satır sayısı.                  |
| **ColumnCount**  | integer | Evet    | Aralığa dahil edilecek sütun sayısı.                  |
| **Name**         | string  | Hayır   | Aralığın isteğe bağlı adı.                            |
| **RefersTo**     | string  | Hayır   | Aralığın işaret ettiği bir formül.                     |
| **Worksheet**    | string  | Hayır   | Çalışma sayfası adı (yol parametresinden farklıysa). |
| **RowHeight**    | number  | Hayır   | Aralıktaki satırların yüksekliği (piksel).            |
| **ColumnWidth**  | number  | Hayır   | Aralıktaki sütunların genişliği (piksel).             |

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API'sine nasıl istek yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/test.xlsx/worksheets/Sheet1/ranges/merge" \
  -X POST \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{
        "FirstRow": 9,
        "FirstColumn": 0,
        "RowCount": 1,
        "ColumnCount": 7
      }'
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

#### Yanıt Ayrıntıları

| HTTP Durum Kodu               | Açıklama                                                | Örnek JSON                                             |
| ----------------------------- | ------------------------------------------------------- | ------------------------------------------------------ |
| **200 OK**                    | Aralık başarıyla birleştirildi.                         | `{ "Code": 200, "Status": "OK" }`                      |
| **400 Bad Request**           | Geçersiz aralık parametreleri (örn., sınırlar dışındaki indeksler). | `{ "Code": 400, "Message": "Invalid range." }`         |
| **401 Unauthorized**          | Eksik veya geçersiz JWT jetonu.                         | `{ "Code": 401, "Message": "Authentication failed." }` |
| **404 Not Found**             | Çalışma kitabı veya çalışma sayfası bulunamadı.         | `{ "Code": 404, "Message": "Resource not found." }`    |
| **500 Internal Server Error** | Beklenmeyen sunucu hatası.                              | `{ "Code": 500, "Message": "Internal server error." }` |

## Bulut SDK Ailesi

Bir SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. Bir SDK, düşük seviye ayrıntıları işler; böylece projenizin görevlerine odaklanabilirsiniz. Aspose.Cells Cloud SDK'larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, çeşitli SDK'lar kullanılarak Aspose.Cells web servislerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePostWorksheetCellsRangeMerge.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PostWorksheetCellsRangeMerge.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PostWorksheetCellsRangeMerge.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PostWorksheetCellsRangeMerge.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PostWorksheetCellsRangeMerge.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PostWorksheetCellsRangeMerge.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PostWorksheetCellsRangeMerge.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PostWorksheetCellsRangeMerge.go" >}}

{{< /tab >}}

{{< /tabs >}}