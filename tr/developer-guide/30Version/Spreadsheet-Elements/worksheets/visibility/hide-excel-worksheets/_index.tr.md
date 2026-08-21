---
title: "Bir Excel çalışma sayfasını gizle"
second_title: "Belge"
linktitle: "Gizle"
type: docs
url: /worksheets/hide/
aliases: [/hide-excel-worksheets/]
keywords: "Aspose.Cells Cloud, Excel, çalışma sayfası gizle, REST API, elektronik tablo"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma kitabında bir çalışma sayfasını gizlemek için adım adım kılavuz, istek detayları, bir cURL örneği ve birden fazla dil için SDK kod parçacıkları içerir."
weight: 50
---

Bu REST API, bir çalışma sayfasını gizler.

## REST API

```bash
PUT http://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/visible
```

### **İstek parametreleri**

| Parametre Adı   | Tür      | Konum  | Açıklama                                                       |
| ---------------- | -------- | ------ | -------------------------------------------------------------- |
| name             | string   | path   | Excel çalışma kitabı dosyasının adı.                            |
| sheetName        | string   | path   | Değiştirilecek çalışma sayfasının adı.                          |
| isVisible        | boolean  | query  | Görünürlük bayrağı (`true` görünür, `false` gizli için).        |
| folder           | string   | query  | Çalışma kitabının bulunduğu klasör yolu.                        |
| storageName      | string   | query  | Depolama hizmetinin adı.                                       |

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/Worksheets/PutChangeVisibilityWorksheet), herkese açık bir erişilebilir programlama arayüzü tanımlar ve web tarayıcınızdan doğrudan REST etkileşimlerinde bulunmanızı sağlar.

Aspose.Cells web servislerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'ye nasıl çağrı yapıldığını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "http://api.aspose.com/v3.0/cells/Sample_Test_Book.xls/worksheets/Sheet1/visible?isVisible=false" \
-X PUT \
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

## Bulut SDK Geliştirme Takımı

Bir SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. Bir SDK düşük seviye detayları kendisi yönetir ve sizin projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub deposuna](https://github.com/aspose-cells-cloud) göz atın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanarak Aspose.Cells web servislerine nasıl çağrı yapıldığını göstermektedir:

{{< tabs tabTotal="10" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Python" tabName6="Node.js" tabName7="Android" tabName8="Swift" tabName9="Perl" tabName10="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "Examples-DotNET-CSharp-Worksheet-HideWorksheet-1.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Examples-Java-worksheet-HideWorksheet-hide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Examples-PHP-Worksheet-PutChangeVisibilityWorksheet-.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Examples-Ruby-Worksheet-change_worksheet_visibility-.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "HideExcelWorkSheets.py" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Examples-Node.js-SDK-Worksheet-HideWorksheet-1.js" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "9d725d4678edaac53f95c5208e17783c" "Examples-Android-worksheet-HideWorksheet-hide-worksheets.java" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< /tab >}}

{{< tab tabNum="9" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Examples-Perl-Worksheet-HideWorksheet-1.pl" >}}

{{< /tab >}}

{{< tab tabNum="10" >}}

{{< gist "aspose-cells-cloud-gists" "cb5a1656cea2f870f0a5ef6d066525ef" >}}

{{< /tab >}}

{{< /tabs >}}