---
title: "Yatay Sayfa Sonrası Sil"
ArticleTitle: "Aspose.Cells Cloud – Yatay Sayfa Sonrası Silme (REST API)"
second_title: "Belge"
linktitle: "Yatay sayfa sonrası sil"
type: docs
url: /tr/page-breaks/delete-horizontal-page-break/
aliases: [  /tr/delete-horizontal-page-break-inside-worksheet/ ]
keywords: "Aspose.Cells Cloud, Yatay sayfa sonrası sil, Excel çalışma sayfası, REST API, SDK"
description: "Aspose.Cells Cloud REST API kullanarak bir Excel çalışma sayfasından yatay bir sayfa sonrasını silin. C#, Java, PHP, Ruby, Node.js, Python, Perl, Go için SDK'lar mevcuttur."
weight: 50
---

Bu REST API, bir **yatay** sayfa sonrasını siler.

**Önkoşullar**: Bu uç noktayı çağırmak için geçerli bir Aspose Cloud JWT erişim jetonuna sahip olmalısınız. [Kimlik Doğrulama Kılavuzu’nu](https://docs.aspose.cloud/cells/authentication/) izleyerek bunu edinin.

## DeleteHorizontalPageBreak API

```http
DELETE https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/horizontalpagebreaks/{index}
```

*Tüm API çağrıları **HTTPS** üzerinden yapılmalıdır.*

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API’leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT jeton tabanlı kimlik doğrulama</a> gerektirir.

### İstek Parametreleri

| Parametre Adı  | Tür     | Konum | Açıklama                                                       |
|----------------|---------|-------|----------------------------------------------------------------|
| `name`         | string  | path  | Excel dosyasının (çalışma kitabının) adı.                       |
| `sheetName`    | string  | path  | Sayfa sonrasını içeren çalışma sayfasının adı.                  |
| `index`        | integer | path  | Silinecek yatay sayfa sonrasının sıfır tabanlı indeksi.         |
| `folder`       | string  | query | Dosyanın bulunduğu depolamadaki isteğe bağlı klasör yolu.       |
| `storageName`  | string  | query | İsteğe bağlı depolama hizmetinin adı.                           |

### Hata Yanıtları

| HTTP Kodu | Açıklama                                                                          |
|-----------|-----------------------------------------------------------------------------------|
| 401       | Yetkisiz – eksik veya geçersiz jeton.                                            |
| 404       | Bulunamadı – belirtilen dosya, çalışma sayfası veya sayfa sonu indeksi mevcut değil. |
| 400       | Hatalı İstek – bozuk istek söz dizimi veya geçersiz parametreler.                |
| 500       | Sunucu İç Hatası – beklenmeyen bir durumla karşılaşıldı.                         |

**Ayrıca bkz.:**  
- [Yatay Sayfa Sonrası Ekle](/page-breaks/add-horizontal-page-break/)  
- [Yatay Sayfa Sonrasını Al](/page-breaks/get-horizontal-page-breaks/)  
- [Dikey Sayfa Sonrası Sil](/page-breaks/delete-vertical-page-break/)

[OpenAPI Spesifikasyonu](https://apireference.aspose.cloud/cells/#/PageBreaks/DeleteHorizontalPageBreak), herkese açık bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için **cURL** komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile bu çağrının nasıl yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Book1.xlsx/worksheets/sheet1/horizontalpagebreaks/0" \
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

**Yanıt Şeması**

| Alan    | Tür     | Açıklama                                      |
|---------|---------|-----------------------------------------------|
| Code    | integer | HTTP durum kodu (örn., 200).                   |
| Status  | string  | Metinsel durum mesajı (örn., "OK").            |
| Message | string  | Hata durumlarında isteğe bağlı ek bilgi.      |

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Ailesi

Bir SDK kullanmak, geliştirme sürecini hızlandırmanın en iyi yoldur. Bir SDK, düşük seviye detayları yöneterek projenizin görevlerine odaklanmanızı sağlar. Aspose.Cells Cloud SDK’larının tam listesi için lütfen [GitHub Deposu](https://github.com/aspose-cells-cloud)’nu inceleyin.

Aşağıdaki kod örnekleri, Aspose.Cells web hizmetlerinin farklı SDK’lar kullanılarak nasıl çağrılacağını göstermektedir:

{{< tabs tabTotal="8" tabID="4" tabName1="C#" tabName2="Java" tabName3="PHP" tabName4="Ruby" tabName5="Node.js" tabName6="Python" tabName7="Perl" tabName8="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "8a5b324fdf3e574dbd747c1a1e24b05d" "ExampleDeleteHorizontalPageBreak.cs" >}}
*Örnek yüklenemiyorsa, [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/8a5b324fdf3e574dbd747c1a1e24b05d) üzerinde görüntüleyin.*

{{< /tab >}}

{{< tab tabNum="2" >}}

{{< gist "aspose-cells-cloud-gists" "c59aa5c02f735466a5e34751cee73f5f" "Example_DeleteHorizontalPageBreak.java" >}}
*Örnek yüklenemiyorsa, [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/c59aa5c02f735466a5e34751cee73f5f) üzerinde görüntüleyin.*

{{< /tab >}}

{{< tab tabNum="3" >}}

{{< gist "aspose-cells-cloud-gists" "84283c8ba766ed815f47e6dfb0891152" "Example_DeleteHorizontalPageBreak.php" >}}
*Örnek yüklenemiyorsa, [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/84283c8ba766ed815f47e6dfb0891152) üzerinde görüntüleyin.*

{{< /tab >}}

{{< tab tabNum="4" >}}

{{< gist "aspose-cells-cloud-gists" "36ed8b8727561b92692939513d365fca" "Example_DeleteHorizontalPageBreak.rb" >}}
*Örnek yüklenemiyorsa, [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/36ed8b8727561b92692939513d365fca) üzerinde görüntüleyin.*

{{< /tab >}}

{{< tab tabNum="5" >}}

{{< gist "aspose-cells-cloud-gists" "e82de2e4189bc27ae92abf73c36b4df0" "Example_DeleteHorizontalPageBreak.ts" >}}
*Örnek yüklenemiyorsa, [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/e82de2e4189bc27ae92abf73c36b4df0) üzerinde görüntüleyin.*

{{< /tab >}}

{{< tab tabNum="6" >}}

{{< gist "aspose-cells-cloud-gists" "61e922de11e6e7144db88adcad6501c1" "Example_DeleteHorizontalPageBreak.py" >}}
*Örnek yüklenemiyorsa, [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/61e922de11e6e7144db88adcad6501c1) üzerinde görüntüleyin.*

{{< /tab >}}

{{< tab tabNum="7" >}}

{{< gist "aspose-cells-cloud-gists" "f82a3a00251e34ff8766116282c8c9ca" "Example_DeleteHorizontalPageBreak.pl" >}}
*Örnek yüklenemiyorsa, [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/f82a3a00251e34ff8766116282c8c9ca) üzerinde görüntüleyin.*

{{< /tab >}}

{{< tab tabNum="8" >}}

{{< gist "aspose-cells-cloud-gists" "2b824d4e13644368d12682856aa49185" "Example_DeleteHorizontalPageBreak.go" >}}
*Örnek yüklenemiyorsa, [GitHub Gist](https://gist.github.com/aspose-cells-cloud-gists/2b824d4e13644368d12682856aa49185) üzerinde görüntüleyin.*

{{< /tab >}}

{{< /tabs >}}