---
title: "Aspose.Cells Cloud API ile Bir Çalışma Sayfası Dışa Aktarın – Formatlar, cURL ve SDK Örnekleri"
secondtitle: "Belge"
linktitle: "Çalışma Sayfası Dışa Aktarma"
type: docs
url: /worksheets/get-worksheet/
keywords: "Aspose.Cells Cloud Çalışma Sayfası Al, çalışma sayfası dışa aktarma, Excel API, REST, CSV, PDF, PNG, JPEG, GIF, BMP, TIFF, EMF, XPS, OTS, XLS, XLSX, XLSB, XLSM, ODS, FODS, Numbers, bulut API"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel dosyasından tek bir çalışma sayfasını nasıl dışa aktaracağınızı öğrenin. Uç nokta, parametreler, düzeltildi cURL örneği, kimlik doğrulama ayrıntıları, hata yönetimi ve C#, Java, Python ve diğerleri için SDK kod parçacıkları içerir."
weight: 10
ArticleTitle: "Aspose.Cells Cloud API ile Bir Çalışma Sayfası Dışa Aktarın – Formatlar, cURL ve SDK Örnekleri"
---

Bu REST API, bir Excel dosyasından **çalışma sayfasını** birçok farklı dosya formatına dışa aktarmanızı sağlar.

**Özet** – Tek bir çalışma sayfasını, seçtiğiniz formatta bir Çalışma Kitabı’ndan indirmek için **Çalışma Sayfası Al** uç noktasını kullanın.

Aşağıdaki formatlara dışa aktarabilirsiniz:

| Format  | Uzantı   | MIME Türü                                                         |
| ------- | -------- | ----------------------------------------------------------------- |
| XLS     | .xls     | application/vnd.ms-excel                                          |
| XLSX    | .xlsx    | application/vnd.openxmlformats-officedocument.spreadsheetml.sheet |
| XLSB    | .xlsb    | application/vnd.ms-excel.sheet.binary.macroEnabled.12             |
| CSV     | .csv     | text/csv                                                          |
| TSV     | .tsv     | text/tab-separated-values                                         |
| XLSM    | .xlsm    | application/vnd.ms-excel.sheet.macroEnabled.12                    |
| ODS     | .ods     | application/vnd.oasis.opendocument.spreadsheet                    |
| TXT     | .txt     | text/plain                                                        |
| PDF     | .pdf     | application/pdf                                                   |
| OTS     | .ots     | application/vnd.oasis.opendocument.spreadsheet-template           |
| XPS     | .xps     | application/vnd.ms-xpsdocument                                    |
| DIF     | .dif     | application/x-dif                                                 |
| PNG     | .png     | image/png                                                         |
| JPEG    | .jpeg    | image/jpeg                                                        |
| GIF     | .gif     | image/gif                                                         |
| BMP     | .bmp     | image/bmp                                                         |
| WMF     | .wmf     | image/wmf                                                         |
| TIFF    | .tiff    | image/tiff                                                        |
| EMF     | .emf     | image/emf                                                         |
| NUMBERS | .numbers | application/vnd.apple.numbers                                     |
| FODS    | .fods    | application/vnd.oasis.opendocument.spreadsheet-flat-xml           |

## Güvenlik ve Kimlik Doğrulama
Aspose.Cells Cloud API’leri güvenlidir ve [JWT belirteci tabanlı kimlik doğrulama](https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/) gerektirir.

## REST API

```bash
GET https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}
```

### **İstek Parametreleri**

| Parametre Adı            | Tür      | Konum  | Açıklama                                                               |
| ------------------------- | -------- | ------ | ---------------------------------------------------------------------- |
| **name**                  | string   | path   | **Gerekli.** Excel dosyasının adı.                                     |
| **sheetName**             | string   | path   | **Gerekli.** Dışa aktarılacak çalışma sayfasının adı.                 |
| **format**                | string   | query  | Dışa aktarılan çalışma sayfasının hedef dosya formatı (örn., `pdf`, `png`). |
| **verticalResolution**    | integer  | query  | Çözünürlüğü destekleyen formatlar (örn., PNG, JPEG) için görüntü DPI’si. |
| **horizontalResolution**  | integer  | query  | Çözünürlüğü destekleyen formatlar için görüntü DPI’si.                |
| **area**                  | string   | query  | Dışa aktarılacak hücre aralığı (örn., `A1:D10`).                      |
| **pageIndex**             | integer  | query  | Çalışma sayfası sayfalandırılmış olduğunda dışa aktarılacak sayfanın indeksi. |
| **folder**                | string   | query  | Kaynak dosyanın bulunduğu depolama dizin yolu.                         |
| **storageName**           | string   | query  | Aspose Cloud depolama adı.                                             |

<a href="https://apireference.aspose.cloud/cells/#/Worksheets/GetWorksheet" target="_blank" rel="noopener noreferrer">OpenAPI Specification</a>, herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından yapmanızı sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Bulut API’sini nasıl çağıracağınızı göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/myWorkbook.xlsx/worksheets/Sheet1?format=gif" \
  -X GET \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt_token>"
```

{{< /tab >}}

{{< tab tabNum="2" >}}

```http
HTTP/1.1 200 OK
Content-Type: image/gif
Content-Disposition: attachment; filename="Sheet1.gif"

<binary data>
```

{{< /tab >}}

{{< /tabs >}}

## Hata Yönetimi

API standart HTTP durum kodlarını döndürür. Yaygın yanıtlar şunlardır:

| Durum Kodu | Anlam                                                       | Örnek JSON Gövdesi                         |
| ---------- | ----------------------------------------------------------- | ------------------------------------------ |
| **200**    | Başarılı – çalışma sayfası akışı döndürülür.               | `{ "stream": "..." }`                      |
| **400**    | Hatalı istek – eksik veya geçersiz parametreler.           | `{ "error": "Geçersiz format parametresi." }` |
| **401**    | Yetkisiz – geçersiz veya eksik JWT belirteci.              | `{ "error": "Kimlik doğrulama başarısız." }`    |
| **404**    | Bulunamadı – belirtilen dosya veya çalışma sayfası yok.    | `{ "error": "Çalışma sayfası bulunamadı." }`      |
| **500**    | Sunucu iç hatası – sunucuda beklenmeyen durum.             | `{ "error": "Beklenmeyen hata." }`         |

İstemci kodunuzda bu yanıtları uygun şekilde işleyerek kullanıcıya uygun geri bildirim sağlayın.

## Bulut SDK Ailesi

SDK kullanmak, geliştirme hızını en hızlı şekilde artırmak için en iyi yoldur. Bir SDK, düşük seviye ayrıntıları kendisi yönetir ve size proje görevlerinize odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub deposuna</a> göz atın.

Aşağıdaki kod örnekleri, farklı SDK’ları kullanarak Aspose.Cells web hizmetlerine nasıl çağrı yapıldığını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleGetWorksheetWithFormat.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_GetWorksheetWithFormat.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_GetWorksheetWithFormat.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_GetWorksheetWithFormat.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_GetWorksheetWithFormat.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_GetWorksheetWithFormat.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_GetWorksheetWithFormat.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_GetWorksheetWithFormat.go" >}}

{{< /tab >}}

{{< /tabs >}}