---
title: "Pivot tablosu için stil güncelleme"
second_title: "Belge"
linktype: "Biçimlendirme"
type: docs
url: /tr/pivot-tables/format-all/
aliases: [  /tr/update-style-for-pivot-table/ ]
keywords: "pivot tablosu, stil güncelleme, Aspose.Cells Cloud, REST API, Excel, elektronik tablo, API, pivot tablo stili, tümünü biçimlendir"
description: "Aspose.Cells Cloud REST API kullanarak bir pivot tablosunun tamamının stilini nasıl güncelleyeceğinizi öğrenin. İsteği detaylandıran bilgiler, cURL örneği ve birden fazla programlama dili için SDK kod parçacıkları içerir."
weight: 100
ArticleTitle: "Pivot tablosu için stil güncelleme - Aspose.Cells Cloud API"
---

Bu REST API, bir pivot tablosunun stilini günceller.

## PostPivotTableStyle API

```http
POST https://api.aspose.cloud/v3.0/cells/{name}/worksheets/{sheetName}/pivottables/{pivotTableIndex}/FormatAll
```

**Önkoşullar / Kimlik Doğrulama**  
`Authorization` başlığındaki geçerli bir JWT erişim belirteci verilmelidir (örneğin, `Bearer <jwt token>`). Belirtecin belirtilen çalışma kitabına ve çalışma sayfasına erişim iznine sahip olduğundan emin olun.

### **Güvenlik ve Kimlik Doğrulama**

Aspose.Cells Cloud API'leri güvenlidir ve <a href="https://docs.aspose.cloud/total/getting-started/rest-api-overview/authenticating-api-requests/" rel="noopener noreferrer">JWT belirteci tabanlı kimlik doğrulama</a> gerektirir.

### **İstek parametreleri**

| Parametre Adı   | Tür      | Konum | Açıklama                                                                                      |
| ---------------- | -------- | ----- | ---------------------------------------------------------------------------------------------- |
| name             | string   | path  | Çalışma kitabı dosyasının adı.                                                                 |
| sheetName        | string   | path  | Pivot tabloyu içeren çalışma sayfası.                                                          |
| pivotTableIndex  | integer  | path  | Biçimlendirilecek pivot tablonun sıfır tabanlı indeksi.                                        |
| style            | object   | body  | Uygulanacak formatı tanımlayan bir stil DTO'su.                                               |
| needReCalculate  | boolean  | query | Biçimlendirmeden sonra pivot tabloyu yeniden hesaplamak için **true** olarak ayarlayın; varsayılan **false**'tur. |
| folder           | string   | query | Çalışma kitabının depolandığı klasör.                                                          |
| storageName      | string   | query | Depolama hizmetinin adı.                                                                       |

[OpenAPI Specification](https://apireference.aspose.cloud/cells/#/PivotTables/PostPivotTableStyle), erişilebilir bir programlama arayüzü tanımlar ve REST etkileşimlerini doğrudan bir web tarayıcısından gerçekleştirmenizi sağlar.

Aspose.Cells web hizmetlerine kolayca erişmek için cURL komut satırı aracını kullanabilirsiniz. Aşağıdaki örnek, cURL ile Cloud API'ye nasıl istek yapılacağını göstermektedir.

{{< tabs tabTotal="2" tabID="1" tabName1="İstek" tabName2="Yanıt" >}}

{{< tab tabNum="1" >}}

```bash
curl -v "https://api.aspose.cloud/v3.0/cells/Sample_Pivot_Table_Example.xls/worksheets/Sheet2/pivottables/0/FormatAll" \
  -X POST \
  -d '{"Font":{"Name":"Arial","Size":10}}' \
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

**HTTP Durum Kodları**

| Kod | Anlam                       | Açıklama                                          |
|-----|-----------------------------|---------------------------------------------------|
| 200 | OK (Tamam)                  | Filtre başarıyla uygulandı; yanıt işlem detaylarını içerir. |
| 400 | Bad Request (Hatalı İstek)  | Eksik veya geçersiz parametreler (örneğin, desteklenmeyen dosya türü). |
| 401 | Unauthorized (Yetkisiz)     | Geçersiz veya eksik JWT belirteci. |
| 413 | Payload Too Large (Çok Büyük Yük) | Yüklenecek dosya boyut sınırını aşıyor. |
| 500 | Internal Server Error (İç Sunucu Hatası) | Beklenmeyen sunucu hatası. |

{{< /tab >}}

{{< /tabs >}}

## Bulut SDK Kütüphanesi

SDK kullanmak, API’ye karşı en hızlı geliştirme yöntemidir. SDK, düşük seviye ayrıntıları soyutlayarak iş mantığınıza odaklanmanızı sağlar. Aspose.Cells Cloud SDK'larının tam listesi için <a href="https://github.com/aspose-cells-cloud" target="_blank" rel="noopener noreferrer">GitHub deposuna</a> bakın.

Aşağıdaki kod örneği, API’ye Go SDK kullanarak nasıl istekte bulunulacağını göstermektedir:

{{< tabs tabTotal="1" tabID="4" tabName1="Go" >}}

{{< tab tabNum="1" >}}

{{< gist "aspose-cells-cloud-gists" "0b2caae7acfa3e947b856c07b6e8633a" >}}

{{< /tab >}}

{{< /tabs >}}