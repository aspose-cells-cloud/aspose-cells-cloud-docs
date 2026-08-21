---
title: "Grafik Özniteliklerini Güncelle"
type: docs
url: /charts/properties/update/
aliases: [/update-chart-properties/]
weight: 160
keywords: "Aspose.Cells, grafik, güncelle, Excel, REST API, SDK"
description: "Aspose.Cells Cloud REST API (v3.0) kullanarak bir Excel çalışma kitabında grafik özniteliklerini (türü, başlığı, efsane vb.) nasıl güncelleyeceğinizi öğrenin. Endpoint, parametreler, cURL örneği ve C#, Java, PHP, Ruby, Node.js, Perl ve Go için SDK kod parçacıklarını içerir."
ArticleTitle: "Grafik Özniteliklerini Güncelle – Aspose.Cells Cloud REST API"
---

Bu REST API, grafik özniteliklerini günceller.

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

## PostWorksheetChart API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/charts/{chartIndex}
```

### İstek Parametreleri

| Parametre Adı | Tür     | Yol/Sorgu Dizesi/HTTPBody | Açıklama                                                      |
| ------------- | ------- | ------------------------- | ------------------------------------------------------------- |
| name          | string  | path                      | Excel dosyasının adı.                                         |
| sheetName     | string  | path                      | Grafiğin bulunduğu çalışma sayfasının adı.                    |
| chartIndex    | integer | path                      | Güncellenecek grafiğin sıfır tabanlı dizini.                  |
| chart         | object  | body                      | Değiştirilecek grafik özniteliklerini tanımlayan JSON nesnesi. |
| folder        | string  | query                     | Dosyanın bulunduğu depolama klasörü.                          |
| storageName   | string  | query                     | Depolama hizmetinin adı.                                      |

### İstek Gövdesi Şeması

**`chart`** nesnesi, değiştirebileceğiniz öznitelikleri içerir. Aşağıda, yaygın olarak kullanılan birkaç alanı içeren temsilci bir JSON örneği verilmiştir:

```json
{
  "Title": {
    "Text": "Çeyreklik Satışlar"
  },
  "ShowLegend": true,
  "Type": "Line",
  "DataLabels": {
    "ShowValue": true,
    "ShowPercentage": false
  },
  "ChartArea": {
    "BorderColor": "Blue",
    "FillColor": "White"
  }
}
```

> **Not:** Yalnızca değiştirmek istediğiniz alanları sağlamanız gerekir. Atlanan öznitelikler mevcut değerlerini korur.

<a href="https://apireference.aspose.cloud/cells/#/Charts/PostWorksheetChart" target="_blank" rel="noopener noreferrer">OpenAPI Spesifikasyonu</a>, herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API’ye istekte bulunmayı göstermektedir.

{{< tabs tabTotal="2" tabID="11" tabName11="İstek" tabName12="Yanıt" >}}

{{< tab tabNum="11" >}}

```bash
curl -X POST "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet4/charts/1" \
-d '{"Type": "line"}' \
-H "Content-Type: application/json" \
-H "Accept: application/json" \
-H "Authorization: Bearer <jwt token>"
```

{{< /tab >}}

{{< tab tabNum="12" >}}

```json
{
  "Code": 200,
  "Status": "OK"
}
```

{{< /tab >}}

{{< /tabs >}}

## Yanıt

API, işlemin sonucunu gösteren bir JSON nesnesi döndürür. Başarılı bir güncelleme şu şekilde olur:

```json
{
  "Code": 200,
  "Status": "OK"
}
```

**Başarılı durum kodları**

| HTTP Durumu | Açıklama                                      |
| ----------- | --------------------------------------------- |
| 200         | OK – Grafik öznitelikleri başarıyla güncellendi. |

**Yanıt üstbilgileri**

| Üstbilgi       | Açıklama                                                   |
| -------------- | ---------------------------------------------------------- |
| `Content-Type` | `application/json` – Yanıt gövdesinin JSON formatında olduğunu belirtir. |
| `X-RequestId`  | İstek için benzersiz tanımlayıcı (sorun giderme için kullanışlıdır). |

Olası hata yanıtları şunlardır:

| HTTP Durumu | Açıklama                                      |
| ----------- | --------------------------------------------- |
| 400         | Bad Request – geçersiz parametreler veya gövde |
| 401         | Unauthorized – eksik veya geçersiz belirteç    |
| 404         | Not Found – dosya, çalışma sayfası veya grafik bulunamadı |
| 500         | Internal Server Error                         |

Diğer grafikle ilgili işlemler için, ilgili konulara bakın, örneğin [Grafik Başlığını Güncelle](/charts/title/update/) ve [Grafik Efsanesini Güncelle](/charts/legend/update/).

## Bulut SDK Geliştirme Takımı

SDK kullanmak, geliştirme hızını artırmak için en iyi yoldur. Bir SDK, düşük seviye detayları yönetir ve projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub deposuna</a> bakın.

Aşağıdaki kod örnekleri, farklı SDK’lar kullanarak Aspose.Cells web hizmetlerine istek yapmayı göstermektedir:

{{< tabs tabTotal="6" tabID="4" tabName1="C#" tabName2="PHP" tabName3="Ruby" tabName4="Node.js" tabName5="Perl" tabName6="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNet-CSharp-Charts-UpdateChartProperties-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Charts-CellsChartsPostWorksheetChart-.php" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Charts-cells_charts_post_worksheet_chart-.rb" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Charts-UpdateChartProperties-1.js" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Charts-UpdateChartProperties-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "d554e51920e174943a60f4343a97e203" >}}

{{< /tab >}}

{{< /tabs >}}