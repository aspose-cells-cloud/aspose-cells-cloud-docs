---
title: "Bir Excel Çalışma Kitabından Yazma Korumasını (Parola) Kaldırın"
second_title: "Belge"
linktype: "Excel Dosyalarının Parolasını Temizle"
type: docs
url: /clear-excel-files-password/
aliases:
  [
    /clear-modify-password-of-excel-workbooks/,
    /workbook/clear-modify-password/，/workbook/password/clear/,
  ]
keywords: "Aspose.Cells, Excel, parola kaldırma, yazma koruması, REST API, SDK örnekleri"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma kitabından yazma korumasını (parolayı) nasıl sileceğinizi öğrenin. cURL örneği, kimlik doğrulama adımları ve SDK kod örnekleri içerir."
weight: 110
ArticleTitle: "Bir Excel Çalışma Kitabından Yazma Korumasını (Parola) Kaldırın"
---

Bu REST API, bir Excel çalışma kitabından **yazma korumasını (parolayı)** kaldırır ve böylece Excel parola korumasını programlı olarak **kaldırmanızı** sağlar.

**Ön Koşullar:** Geçerli bir JWT jetonu edinin, çalışma kitabının desteklenen bir depolama konumunda bulunduğundan emin olun ve API sürümünü v3.0 olarak kullanın.

Koruma eklemek için [Excel'i Korumak](/cells/protect/) kılavuzuna bakın.

## DeleteDocumentUnprotectFromChanges API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/writeProtection
```

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvendir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT jeton tabanlı kimlik doğrulama</a> gerektirir.

### **İstek Parametreleri**

| Parametre Adı  | Tür     | Konum  | Açıklama                                             |
| -------------- | ------- | ------ | ---------------------------------------------------- |
| `name`         | string  | path   | Excel çalışma kitabının adı.                         |
| `folder`       | string  | query  | Çalışma kitabını içeren klasör (isteğe bağlı).      |
| `storageName`  | string  | query  | Depolama hizmetinin adı (isteğe bağlı).             |


### Yanıt

```json
{
  "Status":"OK",
  "Code":200
}
```

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                                  |
|-----|-----------------------------|-----------------------------------------------------------|
| 200 | Tamam                       | Filtre başarıyla uygulandı; yanıt işlem ayrıntılarını içerir. |
| 400 | Geçersiz İstek              | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Yetkisiz                    | Geçersiz veya eksik JWT jetonu.                            |
| 413 | Yük Çok Büyük               | Yüklü dosya boyut sınırını aşıyor.                         |
| 500 | Sunucu İç Hatası            | Beklenmeyen sunucu hatası.                                |

## DeleteDocumentUnprotectFromChanges API’yi SDK’larla Nasıl Kullanılır?

### DeleteDocumentUnprotectFromChanges API Belirtimi

[OpenAPI Belirtimi](https://apireference.aspose.cloud/cells/#/Workbook/DeleteDocumentUnprotectFromChanges), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile REST API’ye nasıl istek yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Test_Book.xlsx/writeProtection" \
  -X DELETE \
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


### Aspose.Cells Cloud SDK’larını Kullanma

SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. SDK, düşük seviye detayları kendisi yönetir, böylece siz projenizin görevlerine odaklanabilirsiniz. Aspose.Cells Cloud SDK’larının tam listesi için [GitHub deposuna](https://github.com/aspose-cells-cloud) bakın.

Aşağıdaki kod örnekleri, çeşitli SDK’lar kullanılarak Aspose.Cells web hizmetlerinin nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteDocumentUnprotectFromChanges.cs" >}}

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteDocumentUnprotectFromChanges.java" >}}

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteDocumentUnprotectFromChanges.php" >}}

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteDocumentUnprotectFromChanges.rb" >}}

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2b4189bc27ae92abf73c36b4df0" "Example_DeleteDocumentUnprotectFromChanges.ts" >}}

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteDocumentUnprotectFromChanges.py" >}}

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteDocumentUnprotectFromChanges.pl" >}}

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteDocumentUnprotectFromChanges.go" >}}

{{< /tab >}}

{{< /tabs >}}