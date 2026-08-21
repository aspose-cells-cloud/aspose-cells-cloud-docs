---
title: "Excel Çalışma Sayfasına Bir OLE Nesnesi Ekleyin"
second_title: "Belge"
linktitle: "OLE nesnesi ekle"
type: docs
url: /oleobjects/add/
aliases: [/add-oleobject-to-excel-worksheet/]
keywords: "OLE nesnesi ekle, Excel, Aspose.Cells Cloud, REST API, SDK"
description: "Aspose.Cells Cloud REST API’sini kullanarak Excel çalışma sayfalarına OLE nesneleri ekleyin. API, doğrudan veya C#, Java, PHP, Ruby, Node.js, Python, Perl ve Go için SDK’lar aracılığıyla çağrılabilir."
ArticleTitle: "Aspose.Cells Cloud API ile Excel Çalışma Sayfasına OLE Nesnesi Ekleme"
weight: 20
---

Aspose.Cells Cloud API, Excel çalışma kitaplıklarının programlı olarak manipulate edilmesini sağlar; bu, OLE nesnelerini (örneğin Word belgeleri, PDF’ler veya diğer ikili dosyalar) doğrudan bir çalışma sayfasına gömme yeteneğini de içerir.

Bu REST API, bir Excel çalışma sayfasına bir **OLE nesnesi** ekler.

**Önkoşullar** – Geçerli bir JWT kimlik doğrulama belirteciniz olmalıdır ve `oleFile` veya `imageFile` tarafından başvurulan kaynak dosyalar, uç noktayı çağırmadan önce belirtilen depolama konumuna yüklenmiş olmalıdır.

## PutWorksheetOleObject API

```http
PUT https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/oleobjects
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### İstek parametreleri

| Parametre Adı   | Tür      | Konum | Açıklama                                            |
| ---------------- | -------- | ----- | --------------------------------------------------- |
| name             | string   | path  | Çalışma kitabı dosya adı.                           |
| sheetName        | string   | path  | Çalışma sayfası adı.                                |
| oleObject        | object   | body  | OLE nesnesi tanımı.                                 |
| upperLeftRow     | integer  | query | Üst sol köşenin satır indeksi (varsayılan 0).       |
| upperLeftColumn  | integer  | query | Üst sol köşenin sütun indeksi (varsayılan 0).       |
| height           | integer  | query | OLE nesnesinin yüksekliği (varsayılan 0).           |
| width            | integer  | query | OLE nesnesinin genişliği (varsayılan 0).            |
| oleFile          | string   | query | OLE kaynak dosyasının adı.                          |
| imageFile        | string   | query | Önizleme resim dosyasının adı.                      |
| folder           | string   | query | Çalışma kitabını içeren klasör.                     |
| storageName      | string   | query | Kullanılacak depolama adı.                          |

**Notlar** – `upperLeftRow` ve `upperLeftColumn` sıfır tabanlı indeksleme kullanır. `oleFile` (ve isteğe bağlı olarak `imageFile`) hedef depolamada zaten mevcut olmalıdır; aksi takdirde istek bir hata döndürür.

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/OleObjects/PutWorksheetOleObject), herkese açık bir programlama arayüzü tanımlar ve web tarayıcınızdan doğrudan REST etkileşimlerinde bulunmanıza olanak tanır.

Aspose.Cells web servislerini çağırmak için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile bir OLE nesnesi eklemeyi nasıl yapacağınızı göstermektedir. **Tüm üretim çağrılarında HTTPS gereklidir.**

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/Sheet1/oleobjects" \
  -X PUT \
  -H "Content-Type: application/json" \
  -H "Accept: application/json" \
  -H "Authorization: Bearer <jwt token>" \
  -d '{"ImageSourceFullName":"aspose-logo.png", "IsAutoSize":true, "SourceFullName":"Sample_Book2.xls", "UpperLeftRow":15, "Top":10, "UpperLeftColumn":5, "Left":10, "Width":400, "Height":400}'
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

![Excel çalışma sayfasına gömülü bir OLE nesnesi gösteren ekran görüntüsü](/cells/images/ole-object-example.png)

**Olası HTTP durum kodları**

| Kod  | Açıklama                                             |
|------|------------------------------------------------------|
| 200  | OLE nesnesi başarıyla eklendi.                      |
| 400  | Geçersiz istek – eksik veya geçersiz parametreler.  |
| 401  | Yetkisiz – geçersiz veya eksik JWT belirteci.       |
| 404  | Bulunamadı – çalışma kitabı, çalışma sayfası veya kaynak dosya mevcut değil. |
| 500  | Sunucu iç hatası – beklenmedik bir hata oluştu.     |

Tipik bir başarılı yanıt aşağıdaki JSON yükünü döndürür:

```json
{
  "Code": 200,
  "Status": "OK",
  "Data": {
    "OleObjectId": "12345",
    "UpperLeftRow": 15,
    "UpperLeftColumn": 5,
    "Width": 400,
    "Height": 400,
    "SourceFullName": "Sample_Book2.xls",
    "ImageSourceFullName": "aspose-logo.png"
  }
}
```

## Bulut SDK Ailesi

SDK kullanmak geliştirme sürecini hızlandırır. Bir SDK, düşük seviye detayları soyutlayarak iş mantığınıza odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, Aspose.Cells web servislerini çeşitli SDK’lar kullanarak nasıl çağıracaklarınızı göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExamplePutWorksheetOleObject.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_PutWorksheetOleObject.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_PutWorksheetOleObject.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_PutWorksheetOleObject.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_PutWorksheetOleObject.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_PutWorksheetOleObject.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_PutWorksheetOleObject.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_PutWorksheetOleObject.go" >}}

{{< /tab >}}

{{< /tabs >}}